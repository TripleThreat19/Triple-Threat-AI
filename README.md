# Triple-Threat: Proyecto Orlando 🤖

---

## 🚀 Categoría: Futuros Ingenieros WRO 2025

![Logo del Equipo Triple Threat](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Logo%20del%20Equipo/Logo%20del%20Equipo.jpg)](https://github.com/TripleThreat19/Triple-Threat-AI)

---

## 📖 Diario de Ingeniería / Documentación Técnica

[![Imagen de Portada del Proyecto Orlando](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Logo%20del%20Equipo/Imagen%20de%20Portada.jpg)](https://github.com/TripleThreat19/Triple-Threat-AI)

Este repositorio centraliza toda la **documentación técnica** del proyecto **Orlando**, una iniciativa desarrollada por el equipo **Triple Threat** para la categoría **Futuros Ingenieros** de la **WRO 2025**. Aquí, desglosamos meticulosamente cada aspecto de nuestro robot: desde el **diseño detallado del vehículo** y la **programación del sistema de control**, hasta la **selección estratégica de componentes** y la **estructura de cableado** implementada para su óptimo funcionamiento.

Cada sección es un reflejo de nuestro **esfuerzo, dedicación y compromiso** como equipo frente a este emocionante desafío. El proyecto Orlando no es solo una solución técnica a un problema propuesto; es el culmen de incontables horas de **trabajo en equipo, investigación profunda, pruebas constantes y mejora continua**, todo impulsado por nuestra **pasión por la robótica y el aprendizaje colaborativo**.

Con este trabajo, nuestro objetivo es doble: no solo buscamos destacar en la competencia, sino también **inspirar a otros jóvenes** a sumergirse en el fascinante mundo de la ingeniería con creatividad, disciplina y un entusiasmo inquebrantable. ¡Esperamos que este diario sea una fuente de aprendizaje y motivación!

---

## 🛠️ Factor de Ingeniería / Diseño del Prototipo

En esta sección, profundizamos en la conceptualización y materialización de nuestro prototipo, detallando las decisiones de diseño que lo hacen robusto y eficiente para los retos de la WRO 2025.

---

### 💡 Componentes Clave del Vehículo

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

![Raspberry Pi 5](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Componentes%20Electronicos/raspberry-pi-5.jpg)

#### 🔌 Puente H

Un **Puente H** es un circuito electrónico crucial que nos permite **invertir la polaridad de la tensión** aplicada a una carga, comúnmente un motor de corriente continua. Esto se logra mediante la disposición de cuatro interruptores (transistores o relés) que permiten el flujo de corriente en dos direcciones opuestas, controlando así el sentido de giro del motor.

---
**_Características Esenciales:_**

* **Control del sentido de giro:** Permite invertir la polaridad del voltaje aplicado a un motor DC, facilitando su rotación hacia adelante o hacia atrás.
* **Control de velocidad:** Al integrar una señal de Modulación por Ancho de Pulso (PWM), puede variar la velocidad del motor de manera eficiente.
* **Capacidad de corriente y voltaje:** Cada Puente H está diseñado para manejar un rango específico, crucial para que coincida con los requisitos del motor y evitar daños.
* **Protecciones integradas:** Muchos puentes H comerciales incluyen protecciones contra sobrecorriente, cortocircuitos y sobrecalentamiento, aumentando la seguridad y durabilidad.
* **Compatibilidad con microcontroladores:** Son fácilmente controlables por microcontroladores como la Raspberry Pi o Arduino, simplificando la lógica de control del motor.
* **Aislamiento y protección del microcontrolador:** Actúa como una interfaz de potencia, protegiendo los componentes de control sensibles de las altas corrientes y ruidos generados por el motor.

---

El **Puente H** es fundamental para nuestro robot porque permite el **control total de los motores**: puede cambiar el sentido de giro (adelante/atrás) y, con PWM, controlar la velocidad con precisión. Además, actúa como un **escudo protector para nuestra Raspberry Pi**, aislando los componentes sensibles del motor y garantizando la fiabilidad y seguridad del sistema.

![Puente H](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Componentes%20Electronicos/Purnte%20H.jpg)

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

![La Raspberry Pi AI Camera](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Componentes%20Electronicos/Camara%20Rasberry%20PI%205.jpg)

---

## ⚡ Gestión de la Potencia y los Sensores

Aquí se detalla cómo nuestro robot maneja la energía y utiliza sus diversos sensores para interactuar con el entorno y tomar decisiones informadas.

---

## 🚗 Gestión de Movilidad

Exploramos los sistemas y mecanismos que permiten a nuestro robot desplazarse de manera eficiente y precisa en el campo de juego.

---

## 🧠 Estrategias Planteadas para Resolver los Retos

En esta sección, compartimos las metodologías y enfoques innovadores que hemos diseñado para superar los desafíos propuestos en la competencia WRO 2025.

---
