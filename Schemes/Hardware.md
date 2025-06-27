---

# 🤖 Sistema de Rueda y Eje para Nuestro Robot ⚙️

¡Bienvenidos a la sección de hardware de nuestro proyecto! Aquí explicaremos cómo se ensamblan las piezas clave para el movimiento de nuestro robot. La imagen de arriba muestra un "despiece" de los componentes esenciales que conforman una de las unidades de rueda.

---

### Visión General del Ensamblaje

Este sistema está diseñado para proporcionar una rotación fluida y robusta, fundamental para la locomoción de nuestro robot. Cada componente juega un papel crucial en la durabilidad y eficiencia del movimiento.

Es importante destacar que este diseño en particular está pensado para las ruedas delanteras de nuestro robot, actuando como las ruedas directrices. Esto significa que estas unidades serán responsables de la dirección del vehículo. Las ruedas traseras, por su parte, serán las que vayan impulsadas directamente por un motor, complementando este sistema para mejorar significativamente la movilidad y la capacidad de maniobra de nuestro vehículo.

---

### Desglose del Proceso de Montaje

![Motor Codificador Optico Makeblock 180](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Armado%20del%20Vehiculo/imagen%202.png)

El montaje de este subsistema se concibe en una secuencia lógica que asegura la correcta funcionalidad y alineación de las partes:

1.  **Eje y Rodamiento:**
    El punto de partida es el **eje**, un elemento central sobre el cual se montará el **rodamiento**. Este rodamiento es una pieza ingenieril clave, cuya función principal es minimizar la fricción, permitiendo que el eje (y, por ende, la rueda) gire con la mayor suavidad posible y con un mínimo desgaste.

2.  **Soporte del Rodamiento:**
    Una vez que el rodamiento está posicionado en el eje, ambos se alojan dentro del **soporte de rodamiento**. Este soporte se compone de dos mitades que se unen, encapsulando y asegurando el rodamiento en su lugar. La unión de estas dos secciones se logra mediante el uso de **tornillos y tuercas más pequeños**, garantizando que el rodamiento quede firmemente contenido, pero con libertad para girar sobre el eje.

3.  **Fijación de la Rueda:**
    Con el eje y el conjunto de rodamiento/soporte listos, la **rueda** se desliza sobre el extremo libre del eje. Para asegurar que la rueda no se desplace ni se suelte durante el funcionamiento de nuestro robot, se utiliza una **tuerca adicional** que se rosca firmemente en el extremo del eje, fijando la rueda en su posición adecuada.

4.  **Integración en el Chasis del Robot:**
    Finalmente, este ensamblaje completo (compuesto por la rueda, el eje, el rodamiento y su soporte) se integra directamente en la estructura principal de nuestro robot. El diseño del **soporte de rodamiento** incluye puntos de montaje que permiten su fijación segura al chasis o a los brazos de suspensión, si los tuviera. Esta integración no solo proporciona el anclaje físico, sino que también establece el punto de pivote exacto para la rotación de la rueda, siendo esencial para la dinámica de movimiento de nuestro robot.

---

# 🤖 Distribución de Componentes en el Chasis del Robot ⚙️

Nuestro chasis ha sido meticulosamente diseñado para una distribución específica de componentes, buscando optimizar el centro de gravedad y facilitar el proceso de montaje. A continuación, detallamos la ubicación estratégica de los elementos principales:

---

### Colocación de Componentes Clave en la Primera Placa:

![Motor Codificador Optico Makeblock 180](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Armado%20del%20Vehiculo/imagen%202.png)

* **Motor (con reductor):** Se ubica y fija en la parte trasera del chasis. Esta posición estratégica ayuda a concentrar el peso, optimizando la tracción y el balance general del robot.

* **Baterías (Pilas):** Se colocan centralmente en el chasis y se aseguran mediante tornillos. Esta disposición es crucial para lograr una distribución equilibrada del peso, lo que mejora significativamente la estabilidad y la maniobrabilidad del vehículo.

* **Regulador de Voltaje (Regulador):** Aunque no es visible en la disposición general, se situará típicamente cerca de las baterías. Su función es regular el voltaje de entrada para alimentar de forma estable y segura el resto de la electrónica de control del robot.

* **Puente H:** Este componente clave se colocará lo más próximo al motor posible. Esta cercanía minimiza la longitud del cableado, lo que reduce las pérdidas de energía y optimiza el control de dirección y velocidad del motor.

---

### 💡 Componentes del Vehículo

Hemos seleccionado cuidadosamente cada componente para asegurar el máximo rendimiento y fiabilidad de nuestro robot. A continuación, detallamos los elementos esenciales que dan vida a nuestro proyecto.

#### 🧠 Raspberry Pi 5

La **Raspberry Pi 5** es el cerebro de nuestro sistema, definida por la misma Raspberry Pi Foundation como una **PC de bajo coste del tamaño de una tarjeta de crédito**. Permite explorar el mundo de la informática y aprender lenguajes de programación como Scratch y Python, siendo una herramienta increíblemente versátil.

---
**_Características Destacadas:_**

* **CPU de alto rendimiento:** Procesador Broadcom BCM2712 Quad-core Arm Cortex-A76 a 2.4 GHz, ofreciendo un gran poder de procesamiento.
* **GPU avanzada:** GPU VideoCore VII para capacidades gráficas y de procesamiento de visión mejoradas.
* **Memoria RAM generosa:** Disponible con hasta 8GB de RAM LPDDR4X-4267, ideal para multitarea y aplicaciones exigentes.
* **Conectividad versátil:** Incluye Wi-Fi 5 de doble banda, Bluetooth 5.0 y Gigabit Ethernet para una comunicación robusta.
* **Almacenamiento de alta velocidad:** Soporte para tarjetas microSD de alta velocidad y una interfaz PCIe 2.0 x1 para SSDs M.2 externos (vía adaptador).
* **Salida de video dual:** Dos puertos micro HDMI que soportan hasta 4K a 60Hz.
* **Puertos USB 3.0:** Dos puertos USB 3.0 para conectar periféricos de alta velocidad.
* **Conectores MIPI duales:** Dos transceptores MIPI de 4 carriles para hasta dos cámaras o pantallas.
* **Control de ventilador:** Conector dedicado para un ventilador PWM, asegurando un rendimiento óptimo bajo cargas intensas.

---

La **Raspberry Pi 5** es ideal para nuestro robot por su **gran potencia de procesamiento para IA y visión**, lo que nos permite implementar algoritmos complejos. Su **amplia RAM** asegura una multitarea eficiente y su **conectividad avanzada** facilita la comunicación. Además, el **almacenamiento SSD ultrarrápido** y los **conectores MIPI duales para cámaras** son fundamentales para la percepción y toma de decisiones en tiempo real, garantizando un robot de **alto rendimiento y gran fiabilidad**.

![Raspberry Pi 5](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Schemes/raspberry-pi-5.jpg)

#### 🔌 Puente H

Un **Puente H** es un circuito electrónico crucial que nos permite **invertir la polaridad de la tensión** aplicada a una carga, comúnmente un motor de corriente continua. Esto se logra mediante la disposición de cuatro interruptores (transistores o relés) que permiten el flujo de corriente en dos direcciones opuestas, controlando así el sentido de giro del motor.

---
**_Características Esenciales:_**

* **Control del sentido de giro:** Permite invertir la polaridad del voltaje aplicado a un motor codificador Óptico, facilitando su rotación hacia adelante o hacia atrás.
* **Control de velocidad:** Al integrar una señal de Modulación por Ancho de Pulso (PWM), puede variar la velocidad del motor de manera eficiente.
* **Capacidad de corriente y voltaje:** Cada Puente H está diseñado para manejar un rango específico, crucial para que coincida con los requisitos del motor y evitar daños.
* **Protecciones integradas:** Muchos puentes H comerciales incluyen protecciones contra sobrecorriente, cortocircuitos y sobrecalentamiento, aumentando la seguridad y durabilidad.
* **Compatibilidad con microcontroladores:** Son fácilmente controlables por microcontroladores como la Raspberry Pi o Arduino, simplificando la lógica de control del motor.
* **Aislamiento y protección del microcontrolador:** Actúa como una interfaz de potencia, protegiendo los componentes de control sensibles de las altas corrientes y ruidos generados por el motor.

---

El **Puente H** es fundamental para nuestro robot porque permite el **control total del motor**: puede cambiar el sentido de giro (adelante/atrás) y, con PWM, controlar la velocidad con precisión. Además, actúa como un **escudo protector para el motor**, aislando los componentes sensibles y garantizando la fiabilidad y seguridad del sistema.

![Puente H](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Schemes/Purnte%20H.jpg)

#### 📸 Raspberry Pi AI Camera

La **Raspberry Pi AI Camera** está específicamente diseñada para aprovechar el **procesamiento avanzado de inteligencia artificial (IA)** en dispositivos Raspberry Pi, especialmente cuando se combina con hardware de aceleración como el Hailo AI Module.

---
**_Características Sobresalientes:_**

* **Procesamiento de IA en el chip (Edge AI):** Realiza la inferencia de redes neuronales directamente en el sensor Sony IMX500, liberando la Raspberry Pi principal de esta carga computacional. Esto permite IA en tiempo real con baja latencia.
* **Sensor de alta resolución:** Cuenta con un sensor de 12.3 megapíxeles (4056 x 3040 píxeles), capturando imágenes detalladas.
* **Salida de metadatos de tensor:** Además de la imagen, la cámara puede enviar directamente los resultados del procesamiento de IA, simplificando la integración con otras aplicaciones.
* **Compatibilidad y enfoque manual:** Se conecta vía CSI estándar con todas las Raspberry Pi compatibles y permite ajustar manualmente el enfoque para diversas aplicaciones.
* **Reducción de latencia y ancho de banda:** Los datos procesados de IA (como la detección de objetos) se generan directamente en la cámara, minimizando la latencia y reduciendo significativamente el ancho de banda necesario en el bus de datos CSI.

---

La **Raspberry Pi AI Camera** es fundamental para nuestro robot porque permite la **IA en el borde**, procesando visión directamente en el chip. Esto libera recursos de la Pi 5, reduce la latencia y la necesidad de ancho de banda. Su **alta resolución** y la capacidad de enviar **metadatos de IA pre-procesados** simplifican el desarrollo. Además, es **energéticamente eficiente**, clave para la autonomía del robot. En definitiva, convierte a nuestro robot en un agente **inteligente y reactivo** capaz de percibir e interpretar su entorno de forma autónoma.

![La Raspberry Pi AI Camera](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Schemes/Camara%20Rasberry%20PI%205.jpg)

#### 🔋 Power Bank PB-607

El **Power Bank PB-607** es un cargador portátil o batería externa, fabricado por la marca Harvic. Está diseñado para recargar dispositivos electrónicos como teléfonos inteligentes, tabletas y otros gadgets cuando no tienes acceso a una toma de corriente.

---
**_Características Clave:_**

* **Capacidad:** 10,000mAh (miliamperios-hora). Esta es una capacidad común que permite varias cargas completas.
* **Tipo de batería:** Polímero de Litio. Este tipo de batería es ligero, tiene un buen rendimiento y es más seguro que las antiguas baterías de iones de litio en algunos aspectos.
* **Salida (Output):** 5V-2.1A. Esto indica la velocidad de carga para tus dispositivos. Un output de 2.1A es considerado una carga rápida para muchos dispositivos móviles.
* **Puertos de salida:** Un puerto USB estándar (tipo A) y un puerto Tipo-C con capacidad de carga rápida.
* **Cables incorporados:** Algunos modelos del PB-607 incluyen cables integrados, típicamente uno para dispositivos iPhone (Lightning) y otro Tipo-C, lo que es muy conveniente ya que no necesitas llevar cables adicionales.

---

El **Power Bank PB-607** es vital para nuestro robot porque le otorga **autonomía de operación** al ser una fuente de energía portátil y duradera de 10,000 mAh. Esta capacidad permite alimentar la Raspberry Pi 5, asegurando que el robot se mueva y funcione libremente sin necesidad de estar enchufado, lo cual es esencial para su movilidad y continuidad. Además, sus puertos USB y Tipo-C le permiten recargar otros componentes, manteniendo todo el sistema operativo y fiable.

![Power Bank PB-607](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Schemes/PowerBank%20.jpg)
#### ⚙️ Servomotor

Un **servomotor** es un tipo de motor especial que se diferencia de los motores de corriente continua (DC) o alterna (AC) convencionales por su capacidad de **controlar con precisión su posición angular, velocidad y, en algunos casos, su aceleración**. Piensa en él como un motor que no solo gira, sino que sabe exactamente dónde está y puede ir a una posición específica y mantenerla, incluso si hay una fuerza externa que intenta moverlo.

---
**_Características Principales:_**

* **Control de Posición Preciso:** Esta es su característica principal. A diferencia de un motor DC que gira libremente cuando se le aplica voltaje, un servomotor puede ser instruido para moverse a un ángulo específico (por ejemplo, 45 grados, 90 grados, etc.) y mantenerse allí.
* **Sistema de Lazo Cerrado:** Un servomotor siempre forma parte de un sistema de "lazo cerrado". Esto significa que tiene un mecanismo de retroalimentación (generalmente un potenciómetro o un encoder) que constantemente informa al controlador sobre la posición actual del eje del motor. El controlador compara esta posición con la posición deseada y ajusta la energía al motor para corregir cualquier desviación.
* **Componentes Internos:**
    * **Motor DC o AC:** El motor eléctrico real que genera el movimiento.
    * **Engranajes reductores:** Un sistema de engranajes que reduce la velocidad del motor pero aumenta su torque (fuerza de giro), permitiendo movimientos más controlados y con mayor fuerza.
    * **Sensor de Posición (Potenciómetro/Encoder):** Mide la posición actual del eje del motor y envía esta información al controlador.
* **Tipos de Señal de Control:** Generalmente se controlan mediante señales de Modulación por Ancho de Pulso (PWM). La duración del pulso determina la posición a la que debe moverse el servomotor.

---

El **servomotor** es crucial para nuestro robot porque permite un **control de posición angular preciso**, a diferencia de los motores DC simples. Esto es fundamental para que el robot realice **movimientos exactos y articulados**, como orientar cámaras o manipular objetos. Su sistema de lazo cerrado y el control por PWM simplifican la programación de movimientos complejos, asegurando que el robot interactúe con su entorno de forma controlada y efectiva.

![Servomotor](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Schemes/servomotor.jpg)

#### ⚡ Regulador de Voltaje

Un **regulador de voltaje electrónico** en robótica es un componente crucial diseñado para **mantener una tensión eléctrica de salida constante y estable** para los distintos sistemas del robot, sin importar las variaciones en la fuente de alimentación (como una batería que se descarga) o los cambios en la demanda de energía de los componentes del robot.

---
**_Características Esenciales:_**

* **Estabilización de la Tensión de Suministro:** Su función principal es vital para un robot. Asegura que la Raspberry Pi, los servomotores y los sensores reciban el voltaje exacto que necesitan (por ejemplo, 5V para la Pi), incluso si la batería del robot comienza a descargarse y su voltaje total disminuye. Esto es crucial para la estabilidad y fiabilidad del sistema.
* **Manejo de Diferentes Niveles de Voltaje:** Un robot suele tener varios componentes que operan a diferentes voltajes (ej. 5V para la lógica, 12V para los motores). Los reguladores permiten crear "rieles" de voltaje específicos a partir de una única fuente de alimentación, simplificando el diseño del sistema de energía.
* **Eficiencia Energética (para Robots Autónomos):** En robótica, la eficiencia es fundamental para la autonomía. Los reguladores conmutados (switching) son preferidos en robots. Son mucho más eficientes que los lineales, ya que minimizan la energía que se pierde como calor. Esto significa que la batería del robot durará más tiempo, aumentando su autonomía operativa.
* **Versatilidad:** Pueden ser reductores (buck) para bajar el voltaje de la batería (ej. de 12V a 5V para la Pi) o incluso elevadores (boost) si un componente necesita un voltaje mayor que el de la batería.

---

El **Regulador de Voltaje Electrónico** es indispensable para el robot porque asegura una **alimentación eléctrica constante y estable** específicamente para el/los servomotor(es). Es vital para:

* **Proteger los servomotores:** Garantiza que reciban siempre el voltaje óptimo, previniendo daños por fluctuaciones de la batería o picos de carga.
* **Asegurar su rendimiento preciso:** Un voltaje estable es clave para el funcionamiento fiable y la precisión de movimiento del/de los servomotor(es).
* **Maximizar la autonomía:** Al usar reguladores conmutados eficientes, minimiza la pérdida de energía en la alimentación del/de los servomotor(es), prolongando la duración de la batería del robot.

En esencia, el regulador es fundamental para la **fiabilidad y la prolongación de la vida útil** de los componentes eléctricos del robot.

![Regulador de Voltaje](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Schemes/Regulador%20de%20Voltaje.jpg)

#### ⚙️ Motor Codificador Óptico Makeblock 180

El **Motor Codificador Óptico Makeblock 180** es un tipo de motor DC (corriente continua) que incorpora un **codificador óptico** en su diseño. Esto lo convierte en un componente clave para aplicaciones de robótica y automatización donde se requiere un **control de movimiento preciso y con retroalimentación**.

---
**_Características Destacadas:_**

* **Motor DC con Engranajes:** Esencialmente, es un motor de corriente continua con una caja reductora de engranajes (con una relación de reducción de 39.6). Esto significa que el motor, aunque gira a altas RPM internamente (hasta 14,000 RPM sin carga), su eje de salida gira a una velocidad mucho menor (350 RPM sin carga), pero con un **par (torque) significativamente mayor** (800 g·cm nominal, 5 kg·cm de arranque). Este alto torque es fundamental para mover ruedas o cargar estructuras en un robot.
* **Codificador Óptico Integrado:** Esta es la característica más importante y lo que lo diferencia de un motor DC estándar. Un codificador óptico utiliza un disco ranurado y un sensor de luz para detectar el movimiento rotatorio del eje del motor. A medida que el disco gira, interrumpe un haz de luz, generando pulsos eléctricos.
* **Precisión de Detección:** El codificador óptico del Makeblock 180 tiene una **precisión de detección de 1°**, lo que permite un control muy fino.
* **Retroalimentación:** Al contar estos pulsos, un microcontrolador (como la Raspberry Pi) puede saber con precisión la **posición angular exacta del eje del motor, la velocidad de rotación y la distancia recorrida** (si está conectado a una rueda).
* **Construcción Robusta y Reducción de Ruido:** Makeblock ha diseñado este motor con materiales personalizados que ayudan a reducir el ruido durante su funcionamiento. Además, cuenta con un eje de salida de acero para una mayor durabilidad y una caja de engranajes de materiales POM (polioximetileno) que son antiabrasivos.

---

El **Motor Codificador Óptico Makeblock 180** es fundamental para nuestro robot porque ofrece un **control de movimiento preciso y con retroalimentación**. Su codificador óptico permite a la Raspberry Pi 5 conocer exactamente la posición, velocidad y distancia recorrida, lo cual es indispensable para una **navegación autónoma exacta, control de movimiento fino** (giros y paradas precisas), detección de bloqueos y una **mayor fiabilidad y repetibilidad** en sus desplazamientos. Transforma al robot en un sistema de **navegación inteligente y confiable**.

![Motor Codificador Optico Makeblock 180](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Schemes/motor%20codificador%20optico%20Makeblock%20180.jpg)


