# Triple-Threat
Categoría Futuros Ingenieros 

# DIARIO DE INGIENERIA/DOCUMENTO

Este Repositorio reúne toda la documentación técnica del proyecto Orlando, desarrollado por el equipo **_Triple Threat_** para la categoría Futuros Ingenieros de la WRO 2025. Aquí se detallan el diseño del vehículo,la programación del sistema de control, la selección de componentes y sensores, así como la estructura del cableado empleada para su funcionamiento.Cada sección refleja el esfuerzo, la dedicación y el compromiso que hemos puesto como equipo en este desafío. Este proyecto no solo representa una solución técnica a un problema propuesto, sino también el resultado de muchas horas de trabajo en equipo, investigación, pruebas constantes y mejora continua, motivados por nuestra pasión por la robótica y el aprendizaje colaborativo.A través de este trabajo, buscamos no solo destacar en la competencia, sino también inspirar a otros jóvenes a explorar el mundo de la ingeniería con creatividad, disciplina y entusiasmo.

# FACTOR DE INGENIERIA/DISEÑO DEL PROTOTIPO

# COMPONENTES DEL VEHICULO

# Triple-Threat
Categoría Futuros Ingenieros 

# DIARIO DE INGIENERIA/DOCUMENTO

Este Repositorio reúne toda la documentación técnica del proyecto Orlando, desarrollado por el equipo **_Triple Threat_** para la categoría Futuros Ingenieros de la WRO 2025. Aquí se detallan el diseño del vehículo,la programación del sistema de control, la selección de componentes y sensores, así como la estructura del cableado empleada para su funcionamiento.Cada sección refleja el esfuerzo, la dedicación y el compromiso que hemos puesto como equipo en este desafío. Este proyecto no solo representa una solución técnica a un problema propuesto, sino también el resultado de muchas horas de trabajo en equipo, investigación, pruebas constantes y mejora continua, motivados por nuestra pasión por la robótica y el aprendizaje colaborativo.A través de este trabajo, buscamos no solo destacar en la competencia, sino también inspirar a otros jóvenes a explorar el mundo de la ingeniería con creatividad, disciplina y entusiasmo.

# FACTOR DE INGENIERIA/DISEÑO DEL PROTOTIPO

# COMPONENTES DEL VEHICULO

**Rasberry Pi 5**

 La misma Raspberry Pi Foundation la define como una PC de bajo coste con el tamaño de una tarjeta de crédito que se conecta a un monitor o TV, utilizándose con un teclado y ratón. Dando igual la edad, permite explorar el mundo de la informática y aprender lenguajes de programación Scratch y Python.

  **_Características_**

- CPU de alto rendimiento: Procesador Broadcom BCM2712 Quad-core Arm Cortex-A76 a 2.4 GHz, ofreciendo un gran poder de procesamiento.
- GPU avanzada: GPU VideoCore VII para capacidades gráficas y de procesamiento de visión mejoradas.
- Memoria RAM generosa: Disponible con hasta 8GB de RAM LPDDR4X-4267, ideal para multitarea y aplicaciones exigentes.
- Conectividad versátil: Incluye Wi-Fi 5 de doble banda, Bluetooth 5.0 y Gigabit Ethernet para una comunicación robusta
- Almacenamiento de alta velocidad: Soporte para tarjetas microSD de alta velocidad y una interfaz PCIe 2.0 x1 para SSDs M.2 externos (vía adaptador)
- Salida de video dual: Dos puertos micro HDMI que soportan hasta 4K a 60Hz.
- Puertos USB 3.0: Dos puertos USB 3.0 para conectar periféricos de alta velocidad.
- Conectores MIPI duales: Dos transceptores MIPI de 4 carriles para hasta dos cámaras o pantallas.
- Control de ventilador: Conector dedicado para un ventilador PWM, asegurando un rendimiento óptimo bajo cargas intensas.

  La Raspberry Pi 5 es ideal para nuestro robot por su gran potencia de procesamiento para IA y visión, que permite algoritmos complejos. Su amplia RAM asegura una multitarea eficiente y su conectividad avanzada facilita la comunicación. Además, el almacenamiento SSD ultrarrápido y los conectores MIPI duales para cámaras son fundamentales para la percepción y toma de decisiones en tiempo real, garantizando un robot de alto rendimiento y gran fiabilidad.



 ![Rasberry Pi 5](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Componentes%20Electronicos/raspberry-pi-5.jpg)


  **Puente H**

 Un puente H, en electrónica, es un circuito que permite invertir la polaridad de la tensión aplicada a una carga, generalmente un motor de corriente continua. Esto se logra mediante la disposición de cuatro interruptores (generalmente transistores o relés) que permiten que la corriente fluya en dos direcciones opuestas a través de la carga, lo que a su vez controla el sentido de giro del motor. 

 **_Características_**

- Control del sentido de giro: Permite invertir la polaridad del voltaje aplicado a un motor DC, lo que le permite girar hacia adelante o hacia atrás. Es su función esencial.
- Control de velocidad: Al integrar una señal de Modulación por Ancho de Pulso (PWM), puede variar la velocidad del motor de manera eficiente.
- Capacidad de corriente y voltaje: Cada puente H está diseñado para manejar un rango específico de corriente y voltaje, crucial para que coincida con los requisitos del motor y evitar daños.
- Protecciones integradas: Muchos puentes H comerciales (en circuitos integrados) incluyen protecciones contra sobrecorriente, cortocircuitos y sobrecalentamiento, aumentando la seguridad y durabilidad.
- Compatibilidad con microcontroladores: Son fácilmente controlables por microcontroladores como la Raspberry Pi o Arduino, simplificando la lógica de control del motor.
- Aislamiento y protección del microcontrolador: El puente H actúa como una interfaz de potencia entre el microcontrolador (que opera con bajos voltajes y corrientes) y el motor (que consume mucha más potencia). Esto protege los componentes de control sensibles de las altas corrientes, voltajes y ruidos generados por el motor.

El Puente H es fundamental para nuestro robot porque permite el control total de los motores: puede cambiar el sentido de giro (adelante/atrás) y, con PWM, controlar la velocidad con precisión. Además, actúa como un escudo protector para nuestra Raspberry Pi, aislando los componentes sensibles del motor y garantizando la fiabilidad y seguridad del sistema.

 ![Puente H](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Componentes%20Electronicos/Purnte%20H.jpg)

 **La Raspberry Pi AI Camera**

 La Cámara Raspberry Pi AI es una cámara diseñada para aprovechar el procesamiento avanzado de inteligencia artificial (IA) en dispositivos Raspberry Pi, especialmente cuando se combina con hardware de aceleración como el Hailo AI Module.

  **_Características_**

- Procesamiento de IA en el chip (Edge AI): Realiza la inferencia de redes neuronales directamente en el sensor Sony IMX500, liberando la Raspberry Pi principal de esta carga computacional. Esto permite IA en tiempo real con baja latencia.
- Sensor de alta resolución: Cuenta con un sensor de 12.3 megapíxeles (4056 x 3040 píxeles), capturando imágenes detalladas.
- Salida de metadatos de tensor: Además de la imagen, la cámara puede enviar directamente los resultados del procesamiento de IA, simplificando la integración con otras aplicaciones.
- Compatibilidad y enfoque manual: Se conecta vía CSI estándar con todas las Raspberry Pi compatibles y permite ajustar manualmente el enfoque para diversas aplicaciones.
- Reducción de latencia y ancho de banda: Como los datos procesados de IA (como la detección de objetos) se generan directamente en la cámara, solo los resultados o metadatos relevantes necesitan ser transmitidos a la Raspberry Pi. Esto minimiza la latencia en aplicaciones de visión en tiempo real y reduce significativamente el ancho de banda necesario en el bus de datos CSI.

La Raspberry Pi AI Camera es fundamental para nuestro robot porque permite la IA en el borde, procesando visión directamente en el chip. Esto libera recursos de la Pi 5, reduce la latencia y la necesidad de ancho de banda. Su alta resolución y la capacidad de enviar metadatos de IA pre-procesados simplifican el desarrollo. Además, es energéticamente eficiente, clave para la autonomía del robot. En definitiva, convierte a nuestro robot en un agente inteligente y reactivo capaz de percibir e interpretar su entorno de forma autónoma.

 ![La Raspberry Pi AI Camera](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Componentes%20Electronicos/Camara%20Rasberry%20PI%205.jpg)


 

# GESTIÓN DE LA POTENCIA Y LOS SENTIDOS 

# GESTION DE MOVILIDAD 

# ESTRATEGIAS PLANTEADAS PARA RESOLVER LOS RETOS 






















