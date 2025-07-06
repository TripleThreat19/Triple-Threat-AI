# *Lenguaje de Programación*

---

# Detección de Objetos y Límites de Pista 🤖
![Motor Codificador Optico Makeblock 180](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/SRC/Python.png)

Para capacitar a nuestro robot con la habilidad de "ver" su entorno, integramos un conjunto de sensores clave. Si bien los sensores de proximidad (como los ultrasónicos o infrarrojos) son cruciales para detectar obstáculos cercanos y medir distancias, el componente central de nuestra visión es la Cámara Raspberry Pi AI.

La Cámara Raspberry Pi AI, en combinación con algoritmos de visión por computadora desarrollados en Python, aprovecha librerías potentes como OpenCV para el procesamiento avanzado de imágenes. Esta sinergia nos permite no solo identificar la presencia de obstáculos, sino también clasificarlos eficazmente, ya sean conos u otros elementos estáticos presentes en el entorno de la pista. La información obtenida de esta detección es indispensable para que el robot tome decisiones de navegación precisas, como la desaceleración o la evasión.

Paralelamente, para asegurar que el robot se mantenga dentro de su trayectoria, utilizamos la Cámara Raspberry Pi AI para el reconocimiento de los bordes de la pista. A través del procesamiento de imágenes en Python, el sistema analiza las características visuales de la pista, incluyendo líneas y paredes, permitiendo al robot ajustar su dirección de forma continua para permanecer dentro de los límites predefinidos.

# DIAGRAMAS DE LOS CODIGOS 


----

Este documento presenta los diagramas de código de nuestro prototipo de robot, donde este esquivara las paredes tanto internas como externas de la pista. El objetivo es ofrecer una comprensión clara y estructurada de la arquitectura de software y la lógica de control que permiten al robot navegar de forma autónoma en entornos con obstáculos.

Los diagramas visualizan el flujo de procesamiento de información, desde la percepción del entorno mediante los sensores hasta la toma de decisiones para evitar colisiones y la ejecución de movimientos por parte de los actuadores. Se detallará la interacción entre los módulos de detección de obstáculos, los algoritmos de navegación y la manipulación de los sistemas de propulsión y dirección.

Esta representación gráfica facilitará el entendimiento de la secuencia lógica y las interdependencias entre los componentes de software, proporcionando una visión integral del funcionamiento autónomo del robot.


![Motor Codificador Optico Makeblock 180](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Other/Diagrama%20de%20Flujo%20del%20Codigo%201%20Desafio%20Abierto%20.png)

---
# Codigo del Robot/Solución de problemas


```python
# Nombre de archivo: robot_headless.py

# --- Dependencias del Proyecto ---
# time: Para manejar pausas y timeouts en la lógica de decisión.
# lgpio: Biblioteca para el control de bajo nivel de los pines GPIO en la Raspberry Pi.
# cv2 (OpenCV): El núcleo del sistema de visión por computador para procesamiento de imágenes.
# numpy: Para la manipulación eficiente de arrays, fundamental en el procesamiento de imágenes con OpenCV.
# picamera2: La biblioteca oficial para interactuar con el módulo de cámara de la Raspberry Pi.
# libcamera.controls: Para acceder a los controles específicos del framework de la cámara.
import time
import lgpio
import cv2
import numpy as np
from picamera2 import Picamera2
from libcamera import controls

# ===================================================================================
# CLASE DEL CONTROLADOR DEL ROBOT
# ===================================================================================
# Esta clase abstrae toda la interacción con el hardware (motor DC y servomotor).
# Su propósito es ofrecer una API de alto nivel (ej: avanzar, girar) al resto del
# programa, ocultando la complejidad del manejo de señales PWM y GPIO.
class ControladorRobot:
    def _init_(self):
        # --- Configuración de Hardware ---
        # Mapeo de pines GPIO a funciones del hardware (Puente H para motor y servo).
        self.IN1_PIN, self.IN2_PIN, self.ENA_PIN = 2, 3, 18
        self.SERVO_PIN = 14
        # Calibración del servo: Rango del ciclo de trabajo (duty cycle) para los 0-180 grados.
        self.SERVO_MIN_DUTY, self.SERVO_MAX_DUTY = 2.5, 12.5
        # Frecuencia del PWM para el motor DC. Una frecuencia alta (>100Hz) evita el zumbido audible.
        self.MOTOR_PWM_FREQ = 500
        # Handle para la conexión con el chip GPIO, se inicializa en None.
        self.h_gpio = None
        
        # --- Variables de Estado del Robot ---
        # Estos atributos mantienen el contexto del robot entre iteraciones del bucle principal.
        self.modo_pista = "indefinido"  # 'horario' o 'antihorario'
        self.contador_vueltas = 0
        self.vueltas_objetivo = 20
        # Flag para el detector de flanco ascendente (detectar la línea una sola vez por pasada).
        self.linea_detectada_anteriormente = False
        
        # --- Máquina de Estados para la Maniobra de Desempate ---
        # Gestiona la secuencia de evasión cuando ambos sensores detectan un obstáculo.
        self.estado_giro_desempate = None  # e.g., 'retrocediendo', 'buscando', 'recuperando'
        self.tiempo_inicio_estado = 0
        self.direccion_futuro_giro = None

    def inicializar(self):
        """Abre la conexión con el chip GPIO, reclama los pines como salida y resetea el estado del robot."""
        self.h_gpio = lgpio.gpiochip_open(0)
        # Reclamar pines asegura que este proceso tiene control exclusivo sobre ellos.
        lgpio.gpio_claim_output(self.h_gpio, self.IN1_PIN); lgpio.gpio_claim_output(self.h_gpio, self.IN2_PIN); lgpio.gpio_claim_output(self.h_gpio, self.ENA_PIN); lgpio.gpio_claim_output(self.h_gpio, self.SERVO_PIN)
        # Establece un estado inicial conocido y seguro: robot detenido y ruedas centradas.
        self.detener(); self.centrar_direccion()
        print("[Controlador] Inicializado.")

    def set_modo_pista(self, modo):
        """Fija el modo de la pista (horario/antihorario) una única vez al detectar la primera línea de color."""
        if self.modo_pista == "indefinido": self.modo_pista = modo; print(f"### MODO DE PISTA FIJADO: {self.modo_pista.upper()} ###")

    def detener(self):
        """Corta la energía del motor estableciendo el PWM a 0."""
        if self.h_gpio: lgpio.gpio_write(self.h_gpio, self.IN1_PIN, 0); lgpio.gpio_write(self.h_gpio, self.IN2_PIN, 0); lgpio.tx_pwm(self.h_gpio, self.ENA_PIN, self.MOTOR_PWM_FREQ, 0)

    def mover(self, direccion, velocidad=100):
        """Controla el motor DC. Modifica la dirección (Puente H) y la velocidad (PWM)."""
        if self.h_gpio:
            velocidad = max(0, min(100, velocidad))  # Sanitiza la entrada de velocidad al rango [0, 100].
            # Lógica del Puente-H: IN1 y IN2 en estados opuestos para girar.
            if direccion == 1: lgpio.gpio_write(self.h_gpio, self.IN1_PIN, 0); lgpio.gpio_write(self.h_gpio, self.IN2_PIN, 1)  # Adelante
            elif direccion == -1: lgpio.gpio_write(self.h_gpio, self.IN1_PIN, 1); lgpio.gpio_write(self.h_gpio, self.IN2_PIN, 0) # Atrás
            # La velocidad se controla mediante el ciclo de trabajo del PWM en el pin ENA.
            lgpio.tx_pwm(self.h_gpio, self.ENA_PIN, self.MOTOR_PWM_FREQ, velocidad)
    
    def _establecer_angulo_servo(self, duty_cycle):
        """Función interna para enviar el comando PWM de bajo nivel al servomotor."""
        if self.h_gpio: lgpio.tx_pwm(self.h_gpio, self.SERVO_PIN, 50, duty_cycle) # Frecuencia estándar para servos es 50Hz.

    def girar_direccion(self, angulo):
        """Convierte un ángulo en grados (0-180) a su correspondiente ciclo de trabajo PWM."""
        if not (0 <= angulo <= 180): return
        # Mapeo lineal del rango de ángulos al rango de duty cycle del servo.
        duty = self.SERVO_MIN_DUTY + (angulo / 180.0) * (self.SERVO_MAX_DUTY - self.SERVO_MIN_DUTY)
        self._establecer_angulo_servo(duty)

    # --- Métodos de Abstracción de Alto Nivel ---
    def centrar_direccion(self): self.girar_direccion(85)
    def avanzar(self, velocidad): self.centrar_direccion(); self.mover(1, velocidad)
    def retroceder(self, velocidad): self.centrar_direccion(); self.mover(-1, velocidad)

    def girar(self, lado, velocidad_giro, angulo_giro=45):
        """Combina un giro de dirección y un movimiento hacia adelante para realizar un giro."""
        if lado == "izquierda": self.girar_direccion(min(90 + angulo_giro, 180))
        elif lado == "derecha": self.girar_direccion(max(90 - angulo_giro, 0))
        self.mover(1, velocidad_giro)

    def liberar(self):
        """Detiene el robot y libera los recursos GPIO. Crucial para un apagado limpio."""
        if self.h_gpio: self.detener(); self._establecer_angulo_servo(0); lgpio.gpiochip_close(self.h_gpio); print("[Controlador] GPIO limpio y robot detenido.")

# ===================================================================================
# FUNCIÓN DE DETECCIÓN DE COLOR
# ===================================================================================
def detectar_colores(frame_bgr):
    """Realiza la segmentación de colores en el espacio HSV para aislar los elementos de interés."""
    # Conversión a HSV (Hue, Saturation, Value) porque es más robusto a cambios de iluminación que BGR.
    hsv = cv2.cvtColor(frame_bgr, cv2.COLOR_BGR2HSV)
    # Definición de los rangos de color para crear máscaras booleanas.
    lower_black = np.array([0, 0, 0]); upper_black = np.array([180, 255, 85])
    lower_orange_hsv = np.array([5, 120, 150]); upper_orange_hsv = np.array([20, 255, 255])
    lower_blue_hsv = np.array([100, 120, 100]); upper_blue_hsv = np.array([120, 255, 255])
    # Creación de máscaras binarias donde los píxeles blancos representan el color detectado.
    mask_black = cv2.inRange(hsv, lower_black, upper_black)
    mask_orange = cv2.inRange(hsv, lower_orange_hsv, upper_orange_hsv)
    mask_blue = cv2.inRange(hsv, lower_blue_hsv, upper_blue_hsv)
    # Aplicación de una operación morfológica de apertura para eliminar ruido (pequeños puntos de color aislados).
    kernel = np.ones((5, 5), np.uint8)
    mask_orange = cv2.morphologyEx(mask_orange, cv2.MORPH_OPEN, kernel)
    mask_blue = cv2.morphologyEx(mask_blue, cv2.MORPH_OPEN, kernel)
    return mask_black, mask_orange, mask_blue

# ===================================================================================
# FUNCIÓN DE ANÁLISIS DE FRAME
# ===================================================================================
# Esta es la función principal de lógica. Recibe un frame y el objeto robot (su estado)
# y devuelve una única decisión de alto nivel (ej: "avanzar").
def analizar_frame(frame, robot):
    height, width, _ = frame.shape

    # Condición de terminación del programa.
    if robot.contador_vueltas >= robot.vueltas_objetivo:
        return "detener"

    # --- Definición de Regiones de Interés (ROI) ---
    # Se enfocan en áreas específicas del frame para optimizar y simplificar el análisis.
    ROI_OBSTACULOS_Y_START = int(height * 0.60)
    ROI_OBSTACULOS_Y_END = height
    ROI_LINEA_Y_START = int(height * 0.85)
    
    # --- Lógica de Conteo de Vueltas (usando la ROI inferior) ---
    roi_linea = frame[ROI_LINEA_Y_START:height, :]
    _, mask_orange, mask_blue = detectar_colores(roi_linea)
    # Se considera una línea detectada si el número de píxeles no-cero supera un umbral.
    linea_naranja_detectada = cv2.countNonZero(mask_orange) > 500
    linea_azul_detectada = cv2.countNonZero(mask_blue) > 500
    
    # Fija el modo de la pista basado en la primera línea de color que detecta.
    if robot.modo_pista == "indefinido":
        if linea_naranja_detectada: robot.set_modo_pista("horario")
        elif linea_azul_detectada: robot.set_modo_pista("antihorario")
    
    # Comprueba si la línea del modo actual está visible.
    linea_del_modo_detectada = (robot.modo_pista == "horario" and linea_naranja_detectada) or \
                                 (robot.modo_pista == "antihorario" and linea_azul_detectada)
        
    # Implementa un detector de flanco: cuenta la vuelta solo en la transición de no ver a ver la línea.
    if linea_del_modo_detectada and not robot.linea_detectada_anteriormente:
        robot.contador_vueltas += 1
        print(f"¡VUELTA {robot.contador_vueltas} / {robot.vueltas_objetivo} REGISTRADA!")
    robot.linea_detectada_anteriormente = linea_del_modo_detectada
    
    # --- Lógica de Detección de Obstáculos (usando la ROI central/inferior) ---
    roi_obstaculos = frame[ROI_OBSTACULOS_Y_START:ROI_OBSTACULOS_Y_END, :]
    mask_black, _, _ = detectar_colores(roi_obstaculos)
    
    # Divide la ROI de obstáculos en dos mitades para detectar de qué lado está el obstáculo.
    PUNTO_DIVISION = roi_obstaculos.shape[1] // 2
    area_total_lado = (PUNTO_DIVISION * roi_obstaculos.shape[0])
    # Calcula la densidad de píxeles negros en cada lado.
    porcentaje_izquierdo = (cv2.countNonZero(mask_black[:, :PUNTO_DIVISION]) / area_total_lado) * 100
    porcentaje_derecho = (cv2.countNonZero(mask_black[:, PUNTO_DIVISION:]) / area_total_lado) * 100
    
    hay_obstaculo_izq = porcentaje_izquierdo > 13
    hay_obstaculo_der = porcentaje_derecho > 13

    # --- Lógica de Decisión Jerárquica ---
    decision = "avanzar"  # Decisión por defecto.
    
    # 1. Se prioriza la máquina de estados de desempate si está activa.
    if robot.estado_giro_desempate is not None:
        # Lógica secuencial basada en tiempo para la maniobra de evasión.
        if robot.estado_giro_desempate == "retrocediendo_para_desempate":
            if time.time() - robot.tiempo_inicio_estado > TIMEOUT_RETROCESO_SEGS:
                robot.estado_giro_desempate = "buscando"
                robot.tiempo_inicio_estado = time.time()
            else:
                decision = "retroceder_desempate"
        elif robot.estado_giro_desempate == "buscando":
            if time.time() - robot.tiempo_inicio_estado > TIMEOUT_GIRO_DESEMPATE_SEGS:
                robot.estado_giro_desempate = "recuperando"
                robot.tiempo_inicio_estado = time.time()
            else:
                decision = "girando_desempate_derecha" if robot.direccion_futuro_giro == "derecha" else "girando_desempate_izquierda"
        elif robot.estado_giro_desempate == "recuperando":
            if time.time() - robot.tiempo_inicio_estado > TIMEOUT_RECUPERACION_SEGS:
                robot.estado_giro_desempate = None # Fin de la maniobra
                decision = "avanzar"
            else:
                decision = "giro_recuperacion_izquierda" if robot.direccion_futuro_giro == "derecha" else "giro_recuperacion_derecha"
    # 2. Si no hay desempate, se evalúa la condición de obstáculo frontal.
    elif hay_obstaculo_izq and hay_obstaculo_der:
        # Activa la máquina de estados de desempate.
        robot.estado_giro_desempate = "retrocediendo_para_desempate"
        robot.direccion_futuro_giro = "derecha" if robot.modo_pista == "horario" else "izquierda"
        robot.tiempo_inicio_estado = time.time()
        decision = "retroceder_desempate"
    # 3. Se evalúan los obstáculos laterales.
    elif hay_obstaculo_izq:
        decision = "giro_normal_derecha"
    elif hay_obstaculo_der:
        decision = "giro_normal_izquierda"

    return decision

# ===================================================================================
# CÓDIGO PRINCIPAL - MODO HEADLESS
# ===================================================================================
# Punto de entrada del programa.
robot = ControladorRobot()

# --- Hiperparámetros de Comportamiento ---
# Externalizar estos valores facilita el ajuste y la calibración del robot sin tocar la lógica principal.
VELOCIDAD_AVANCE = 50
VELOCIDAD_GIRO = 40
VELOCIDAD_RETROCESO = 50
ANGULO_GIRO_NORMAL = 45
ANGULO_GIRO_DESEMPATE = 50
ANGULO_GIRO_RECUPERACION = 50
TIMEOUT_RETROCESO_SEGS = 0.8
TIMEOUT_GIRO_DESEMPATE_SEGS = 2.4
TIMEOUT_RECUPERACION_SEGS = 0

ultima_decision = None

try:
    # --- Fase de Inicialización ---
    robot.inicializar()
    picam2 = Picamera2()
    # Configuración de la cámara: es crucial para obtener imágenes consistentes.
    # Se deshabilitan controles automáticos (foco, exposición, balance de blancos) para
    # asegurar que las condiciones de imagen no varíen y afecten la detección de color.
    config = picam2.create_video_configuration(main={"size": (640, 480)}, controls={"AfMode": controls.AfModeEnum.Manual, "LensPosition": 1.5, "AeEnable": True, "AwbEnable": True, "Brightness": 0.05, "Contrast": 1.2, "FrameRate": 30})
    picam2.configure(config)
    picam2.start()
    print("Programa iniciado en modo headless. Presiona Ctrl+C para salir.")

    # --- Bucle Principal de Control ---
    # Este es el corazón del programa: un ciclo infinito de percibir-planificar-actuar.
    while True:
        # 1. Percibir: Captura un frame de la cámara.
        frame_bgr = cv2.cvtColor(picam2.capture_array(), cv2.COLOR_RGB2BGR)
        
        # 2. Planificar: Llama a la función de análisis para obtener una decisión.
        decision = analizar_frame(frame_bgr, robot)

        # Imprime la acción solo cuando cambia para no saturar la consola.
        if decision != ultima_decision:
            print(f"Acción: {decision}")
            ultima_decision = decision
        
        # 3. Actuar: Ejecuta la acción decidida a través de la API del controlador del robot.
        # Este bloque 'if/elif' actúa como un despachador que mapea la decisión (string) a un método del objeto robot.
        if decision == "avanzar":
            robot.avanzar(VELOCIDAD_AVANCE)
        elif decision == "giro_normal_derecha":
            robot.girar("derecha", VELOCIDAD_GIRO, angulo_giro=ANGULO_GIRO_NORMAL)
        elif decision == "giro_normal_izquierda":
            robot.girar("izquierda", VELOCIDAD_GIRO, angulo_giro=ANGULO_GIRO_NORMAL)
        elif decision == "retroceder_desempate":
            robot.retroceder(VELOCIDAD_RETROCESO)
        elif decision == "girando_desempate_derecha":
            robot.girar("derecha", VELOCIDAD_GIRO, angulo_giro=ANGULO_GIRO_DESEMPATE)
        elif decision == "girando_desempate_izquierda":
            robot.girar("izquierda", VELOCIDAD_GIRO, angulo_giro=ANGULO_GIRO_DESEMPATE)
        elif decision == "giro_recuperacion_izquierda":
            robot.girar("izquierda", VELOCIDAD_GIRO, angulo_giro=ANGULO_GIRO_RECUPERACION)
        elif decision == "giro_recuperacion_derecha":
            robot.girar("derecha", VELOCIDAD_GIRO, angulo_giro=ANGULO_GIRO_RECUPERACION)
        elif decision == "detener":
            robot.detener()
            print("Objetivo de vueltas alcanzado. Deteniendo el robot.")
            break # Rompe el bucle while y termina el programa.

# Manejo de la interrupción por teclado para un cierre controlado.
except KeyboardInterrupt:
    print("\nPrograma interrumpido por el usuario (Ctrl+C).")
# El bloque 'finally' se ejecuta siempre, sin importar si hubo un error o no.
# Es el lugar ideal para la limpieza de recursos.
finally:
    print("Iniciando secuencia de apagado...")
    robot.liberar() # Libera los pines GPIO.
    if 'picam2' in locals() and picam2.started:
        picam2.stop() # Detiene la cámara.
    print("Recursos de cámara y GPIO liberados. Programa terminado.")


