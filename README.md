# Triple-Threat: Proyecto Orlando 🤖

---

## 🚀 Categoría: Futuros Ingenieros WRO 2025

![Logo del Equipo Triple Threat](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Logo%20del%20Equipo/Logo%20del%20Equipo.jpg)

---

## 🚀 Presentación del Equipo

Desde que tenemos memoria, la robótica ha sido nuestra pasión. Somos Triple Threat, hermanos trillizos: Carlos, nuestro experto en programación; Valeria, la encargada del diario de ingeniería; y Valentina, la ingeniera mecánica detrás de cada diseño.

Hace dos años, nuestra aventura en la WRO comenzó en la categoría de Deportes Robóticos. No fue cualquier partido, era un tenis doble con una particularidad que lo hacía desafiante: cuatro pelotas en cada lado, una pared en contra y una rampa que agregaba una capa extra de complejidad al campo de juego. Fue un reto estratégico donde aprendimos la importancia de cada detalle, la precisión en el movimiento y la presión del tiempo. El año pasado, la emoción se multiplicó cuando, con mucho esfuerzo y dedicación, logramos clasificar para la etapa internacional en Turquía. Esa experiencia fue inolvidable: conocer a equipos de todo el mundo, sumergirnos en diferentes culturas y, sobre todo, poner a prueba nuestras habilidades en un escenario global.

Ahora, después de esas dos increíbles experiencias, queríamos un nuevo desafío, algo que nos llevara al límite. Queríamos medir hasta dónde hemos crecido, no solo individualmente, sino como equipo. Por eso, decidimos inscribirnos en la categoría de Futuros Ingenieros. Este no es solo otro concurso para nosotros; es la oportunidad perfecta para aplicar todo lo que hemos aprendido, para innovar, para enfrentarnos a problemas complejos y demostrar que nuestra pasión y nuestro trabajo en equipo son más fuertes que nunca. Queremos ver de qué somos capaces cuando la creatividad, la lógica y la camaradería se unen en un robot que redefine los límites.

---

## 📖 Diario de Ingeniería / Documentación Técnica

[![Imagen de Portada del Proyecto Orlando](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Logo%20del%20Equipo/Imagen%20de%20Portada.jpg)](https://github.com/TripleThreat19/Triple-Threat-AI)

Este repositorio centraliza toda la **documentación técnica** del proyecto **Orlando**, una iniciativa desarrollada por el equipo **Triple Threat** para la categoría **Futuros Ingenieros** de la **WRO 2025**. Aquí, desglosamos meticulosamente cada aspecto de nuestro robot: desde el **diseño detallado del vehículo** y la **programación del sistema de control**, hasta la **selección estratégica de componentes** y la **estructura de cableado** implementada para su óptimo funcionamiento.

Cada sección es un reflejo de nuestro **esfuerzo, dedicación y compromiso** como equipo frente a este emocionante desafío. El proyecto Orlando no es solo una solución técnica a un problema propuesto; es el culmen de incontables horas de **trabajo en equipo, investigación profunda, pruebas constantes y mejora continua**, todo impulsado por nuestra **pasión por la robótica y el aprendizaje colaborativo**.

Con este trabajo, nuestro objetivo es doble: no solo buscamos destacar en la competencia, sino también **inspirar a otros jóvenes** a sumergirse en el fascinante mundo de la ingeniería con creatividad, disciplina y un entusiasmo inquebrantable. ¡Esperamos que este diario sea una fuente de aprendizaje y motivación!

---

---

# Problema Identificado: Vehículo Autónomo para Competición "Time Attack" (WRO Futuros Ingenieros)

## Desafío del Reto

El desafío de la **World Robot Olympiad (WRO)** en la categoría de **Futuros Ingenieros** para esta temporada se enfoca en **vehículos autónomos para carreras tipo "Time Attack"**. El objetivo es diseñar, construir y programar un robot capaz de navegar una pista, superar obstáculos específicos y realizar un estacionamiento en paralelo, todo ello buscando el mejor tiempo posible.

## Problemas Clave a Resolver

Hemos identificado los siguientes desafíos técnicos principales que nuestro vehículo debe superar:

### 1. Navegación y Control de Alta Velocidad
* **Seguimiento de Pista Preciso:** El robot necesita un sistema robusto para mantenerse dentro de la pista y seguir la línea con gran exactitud durante múltiples vueltas, optimizando la trayectoria para la velocidad.
* **Control Dinámico de Velocidad:** Mantener la máxima velocidad posible sin perder el control en curvas o secciones complejas es crucial para el "Time Attack".

### 2. Adaptación a Obstáculos Variables

#### Desafío de Muros Interiores Aleatorios:
* **Detección de Muros en Tiempo Real:** El robot debe identificar la posición cambiante de los muros en la pista sin depender de un mapa predefinido.
* **Evasión Eficiente:** Desarrollar algoritmos que permitan al robot rodear los muros rápidamente y sin colisionar, recalculando su ruta sobre la marcha.

#### Desafío de Señales de Tráfico (Pilares Verdes/Rojos):
* **Reconocimiento Visual de Señales:** Implementar un sistema fiable para detectar y diferenciar los pilares verdes (girar a la izquierda) y rojos (girar a la derecha).
* **Decisión y Maniobra Basada en Señal:** El robot debe ajustar su posición en el carril según la señal detectada, ejecutando la maniobra con precisión para no desplazar los pilares.

### 3. Maniobra de Estacionamiento en Paralelo
* **Detección de Zona de Aparcamiento:** El robot necesita identificar el espacio de estacionamiento designado al finalizar las vueltas.
* **Ejecución Precisa del Paralelo:** Realizar una secuencia compleja de movimientos coordinados para estacionar el vehículo correctamente en un espacio reducido.

---

## 🎯  Nuestro Enfoque

Nuestro proyecto busca desarrollar un vehículo autónomo que integre **percepción avanzada del entorno, toma de decisiones dinámica y control de movimiento de alta precisión**. Para lograr esto, utilizaremos una **cámara Raspberry Pi AI** para el procesamiento visual y la detección de elementos clave en la pista, conectada a una **Raspberry Pi** que actuará como el cerebro principal para la lógica de control, la planificación de trayectoria y la ejecución de maniobras. Esta combinación nos permitirá abordar eficazmente los desafíos de navegación, adaptación a obstáculos variables y la maniobra final de estacionamiento, con el objetivo de lograr los mejores tiempos en la competición.

---

## 🛠️ Factor de Ingeniería / Diseño del Prototipo

---

El prototipo es un **robot móvil** con un diseño basado en un **modelo 3D**. Su principal característica es su sistema de **movilidad tipo automóvil**, utilizando **ruedas delanteras directrices** para una **dirección precisa** y ruedas traseras para la propulsión.

Electrónicamente, es controlado por una **Raspberry Pi 5** con una **cámara AI** para la visión. Los movimientos son ejecutados por un **servomotor** para la dirección y **motores Makeblock 180** para el avance, gestionados por un **Puente H** y alimentados por **baterías** y un **regulador de voltaje**. Este conjunto busca ofrecer un **control exacto** y una **navegabilidad eficiente** para diversas tareas.

---

### 💡 Componentes Clave del Vehículo

Hemos seleccionado cuidadosamente cada componente para asegurar el máximo rendimiento y fiabilidad de nuestro robot. A continuación, detallamos los elementos esenciales que dan vida a nuestro proyecto.

#### 🧠 Raspberry Pi 5

La **Raspberry Pi 5** es el cerebro de nuestro sistema, definida por la misma Raspberry Pi Foundation como una **PC de bajo coste del tamaño de una tarjeta de crédito**. Permite explorar el mundo de la informática y aprender lenguajes de programación como Scratch y Python, siendo una herramienta increíblemente versátil.

La **Raspberry Pi 5** es ideal para nuestro robot por su **gran potencia de procesamiento para IA y visión**, lo que nos permite implementar algoritmos complejos. Su **amplia RAM** asegura una multitarea eficiente y su **conectividad avanzada** facilita la comunicación. Además, el **almacenamiento SSD ultrarrápido** y los **conectores MIPI duales para cámaras** son fundamentales para la percepción y toma de decisiones en tiempo real, garantizando un robot de **alto rendimiento y gran fiabilidad**.


#### 📸 Raspberry Pi AI Camera

La **Raspberry Pi AI Camera** está específicamente diseñada para aprovechar el **procesamiento avanzado de inteligencia artificial (IA)** en dispositivos Raspberry Pi, especialmente cuando se combina con hardware de aceleración como el Hailo AI Module.

La **Raspberry Pi AI Camera** es fundamental para nuestro robot porque permite la **IA en el borde**, procesando visión directamente en el chip. Esto libera recursos de la Pi 5, reduce la latencia y la necesidad de ancho de banda. Su **alta resolución** y la capacidad de enviar **metadatos de IA pre-procesados** simplifican el desarrollo. Además, es **energéticamente eficiente**, clave para la autonomía del robot. En definitiva, convierte a nuestro robot en un agente **inteligente y reactivo** capaz de percibir e interpretar su entorno de forma autónoma.


---

## ⚡ Gestión de la Potencia y los Sensores

Nuestro robot gestiona su energía mediante baterías de litio que, a través de un regulador de voltaje, alimentan de forma estable la Raspberry Pi 5 y la Raspberry Pi AI Camera. Un simple switch enciende y apaga el sistema. Para el control del movimiento, la Raspberry Pi 5 se comunica con los motores Makeblock 180 (que tienen codificadores ópticos para precisión) a través de un Puente H, y dirige las ruedas delanteras directrices con un servomotor. La Raspberry Pi AI Camera actúa como el sensor visual principal, permitiendo a la Pi procesar el entorno con visión por computadora e inteligencia artificial, todo orquestado por software basado en Python para una navegación y operación autónoma.

---

## 🚗 Gestión de Movilidad

Este robot, diseñado en 3D, se mueve como un coche: sus ruedas traseras lo impulsan y las ruedas delanteras directrices lo guían. Su diseño mecánico, detallado en el modelo 3D, busca ser robusto y ligero, con espacio para todos los componentes.

La dirección es clave: un servomotor mueve las ruedas delanteras, controlando los giros mediante un mecanismo de dirección (tipo Ackerman). Un controlador coordina estos movimientos para lograr una maniobrabilidad precisa. En resumen, es un vehículo ágil, diseñado para el control exacto de su trayectoria..

---

## 🧠 Estrategias Planteadas para Resolver los Retos

En esta sección, compartimos las metodologías y enfoques innovadores que hemos diseñado para superar los desafíos propuestos en la competencia WRO 2025.

---
