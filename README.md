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

## 1. Mecánica del Robot

El diseño mecánico se enfoca en una estructura **robusta y ligera**, optimizada para la distribución del peso y la integración de todos los componentes electrónicos y motrices.

### 1.1. Componentes Clave

* **Chasis**: Es la base del robot. Su diseño está pensado para soportar todos los componentes y asegurar la **rigidez estructural**. La forma y el material (generalmente polímeros resistentes o aleaciones ligeras, según el **modelo 3D**) se seleccionan según la aplicación específica del robot.

* **Tren de Rodaje**: Se compone de un mínimo de cuatro ruedas. Las **ruedas delanteras** son las encargadas de la **dirección**, mientras que las **ruedas traseras** actúan como propulsoras, brindando el empuje necesario para el movimiento. 

---

## 2. Sistema de Dirección

El sistema de dirección es fundamental para la **maniobrabilidad** del robot, imitando el principio de un automóvil. Se basa en el movimiento angular de las **ruedas delanteras**.

### 2.1. Componentes Principales

* **Ruedas Delanteras Direccionales**: Estas ruedas giran alrededor de un eje vertical (similar al pivote de dirección de un coche) para modificar la trayectoria del robot. Ambas **ruedas delanteras direccionales** están interconectadas y se mueven en un ángulo coordinado gracias a un **mecanismo de dirección**.

* **Mecanismo de Dirección**: Este sistema, detallado en el **modelo 3D**, es una simple barra de acoplamiento que conecta ambas ruedas delanteras
  
* **Servomotor**: Un servomotor de alta precisión, es el responsable de ejecutar el movimiento angular de las **ruedas delanteras direccionales**. Este motor recibe las señales de control de la tarjeta controladora (Rasberry PI) y las traduce en el ángulo de giro deseado. La correcta ubicación y el acoplamiento de este servomotor con el mecanismo de dirección son aspectos críticos en el diseño **3D** para garantizar un movimiento fluido y sin holguras.

* **Rasberry PI 5**: La tarjeta controladora del robot Rasberry PI 5 es la encargada de enviar las señales al servomotor para ajustar el ángulo de las **ruedas delanteras direccionales**. Este controlador puede recibir entradas de la Camara Rasberry PI AI para determinar la dirección que se desea tomar.

---

## 3. Funcionamiento General

Para que el robot pueda moverse y girar eficientemente, el sistema opera de la siguiente manera:

* **Propulsión**: Los motores acoplados a las **ruedas traseras** (o un motor diferencial para ambas) giran para impulsar el robot hacia adelante o hacia atrás. La velocidad se regula mediante la potencia suministrada a estos motores.

* **Dirección**: Para iniciar un giro, la Rasberry PI 5 envía una señal al **servomotor**. El servomotor, a su vez, activa el mecanismo de dirección, lo que provoca el cambio en el ángulo de las **ruedas delanteras direccionales**. El grado de giro de estas ruedas determina directamente el radio de giro del robot.

* **Coordinación**: La clave para un movimiento óptimo reside en la **coordinación** entre la velocidad de las ruedas propulsoras y el ángulo de las **ruedas delanteras direccionales**. Para ejecutar giros cerrados, las ruedas delanteras se angulan más, y la velocidad de las ruedas traseras puede ajustarse para facilitar la maniobra y asegurar un giro suave y controlado.

---

Este diseño, meticulosamente modelado en **3D**, permite una visualización detallada y una optimización exhaustiva de la ergonomía, la resistencia y la funcionalidad del robot antes de proceder con su construcción física. Esto asegura un rendimiento óptimo en todos los aspectos de su mecánica y dirección.


---

## Debate Técnico sobre la Gestión de la Movilidad

### 1. Selección e Implementación de Motores

Para la propulsión del robot utilicé un motor DC con encoder, ya que me permite medir la velocidad angular y la posición de cada rueda, lo cual es clave para controlar con precisión la trayectoria. Este motor se seleccionó por su buen equilibrio entre par (torque) y velocidad para una plataforma de tamaño medio (~1.5 a 2 kg de peso total).

El encoder facilita técnicas de control como PID, permitiendo mantener una velocidad constante incluso con cambios en el terreno o peso del robot.

Para el sistema de dirección utilicé un servomotor de rotación limitada (180°). Este tipo de actuador me permite posicionar con precisión las ruedas delanteras en distintos ángulos, lo que se traduce en giros más suaves y exactos. Elegí un servo de alto torque (más de 10 kg·cm), suficiente para girar ambas ruedas mediante la barra de acoplamiento sin generar vibraciones o juego mecánico.

### 2. Principios de Ingeniería Aplicados

- Velocidad:Se estimó una velocidad objetivo de 0.5 a 1 m/s, adecuada para pruebas y recorridos controlados en escenarios de competencia.
- Par (torque): Los motores deben superar la inercia del robot y el rozamiento del suelo. Para eso, se eligió un motor con un torque mínimo de 2 kg·cm en las ruedas traseras.
- Potencia: La potencia eléctrica se dimensionó en función del consumo del motor DC (~6W por motor) y el servomotor (~2-3W en carga), permitiendo alimentar el sistema con una batería Li-ion de 7.4V.

### 3. Diseño y Selección del Chasis

El chasis fue diseñado en CAD 3D para ser liviano, resistente y fácil de imprimir en una impresora 3D FDM. Utilicé PLA reforzado como material principal por su buena relación rigidez/peso. La forma del chasis favorece la distribución de peso centrada, con espacio suficiente para el servo, motores, controlador y batería.

### 4. Montaje de Componentes

- El chasis impreso contiene ranuras específicas para montar los motores DC y sus reductoras usando tornillos M3.
- El servo de dirección se acopla con dos tornillos a un soporte elevado en el centro del eje delantero.
- Las ruedas delanteras están conectadas por una barra rígida impresa en 3D que transmite el movimiento angular del servo.
- La Raspberry Pi 5, el controlador motor y la batería se fijan al chasis mediante bridas plásticas o tornillos autorroscantes en zonas ya previstas en el diseño.

---


### Control del Movimiento (Actuadores):

Motores Modificadores Ópticos Makeblock 180: Estos motores son los encargados de la propulsión del robot, conectados a las ruedas traseras. Incluyen codificadores ópticos que nos dan retroalimentación precisa sobre la velocidad y la distancia recorrida, información vital para la odometría y un control de movimiento exacto.

Puente H: Funciona como la interfaz de potencia entre la Raspberry Pi 5 y los motores Makeblock 180. Permite a la Pi controlar la dirección y la velocidad de los motores (mediante PWM) con señales de bajo voltaje.

Servomotor (Dirección): Este servomotor es crucial para el control preciso del ángulo de las ruedas delanteras directrices. La Raspberry Pi 5 le envía señales PWM para posicionar las ruedas con exactitud, permitiendo giros controlados y suaves.

Percepción del Entorno (Sensores):

Raspberry Pi AI Camera: Este es el principal sensor visual del robot. Conectada a la Raspberry Pi 5, nos permite implementar visión por computadora y algoritmos de Inteligencia Artificial. La cámara procesa el entorno para:

Detección y Reconocimiento de Objetos: Identifica obstáculos, marcas o elementos clave en el entorno.

Seguimiento de Trayectorias: Percibe líneas o caminos a seguir.

Análisis Espacial: Comprende la profundidad y la disposición de los elementos.
La potente Raspberry Pi 5 puede procesar estos datos de imagen en tiempo real, permitiendo al robot tomar decisiones informadas sobre su navegación y acciones.

Software de Control: Todo el sistema lo gestiona el software que se ejecuta en la Raspberry Pi 5, desarrollado principalmente en Python. Este software integra las lecturas de los codificadores y la cámara, procesa la información y genera las señales de control para el Puente H y el servomotor, coordinando así todos los aspectos del movimiento y la interacción del robot con su entorno.

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

![Motor Codificador Optico Makeblock 180](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Models/Elemento%2010.jpg)

* **Motor:** Se ubica y fija en la parte trasera del chasis. Esta posición estratégica ayuda a concentrar el peso, optimizando la tracción y el balance general del robot.

* **Baterías (Pilas):** Se colocan centralmente en el chasis y se aseguran mediante tornillos. Esta disposición es crucial para lograr una distribución equilibrada del peso, lo que mejora significativamente la estabilidad y la maniobrabilidad del vehículo.

* **Regulador de Voltaje (Regulador):** Aunque no es visible en la disposición general, se situará típicamente cerca de las baterías. Su función es regular el voltaje de entrada para alimentar de forma estable y segura el resto de la electrónica de control del robot.

* **Puente H:** Este componente clave se colocará lo más próximo al motor posible. Esta cercanía minimiza la longitud del cableado, lo que reduce las pérdidas de energía y optimiza el control de dirección y velocidad del motor.

* **Servomotor: Este componente se ubicará en la parte delantera del chasis. Su función principal es controlar el mecanismo de dirección de las ruedas delanteras, permitiendo al robot cambiar de trayectoria con precisión
---


🤖 Ensamblaje del Robot: Distribución de Componentes en el Chasis ⚙️
Nuestro chasis ha sido meticulosamente diseñado para una distribución estratégica de componentes, buscando optimizar el centro de gravedad, la funcionalidad y la facilidad de montaje. A continuación, detallamos la ubicación pensada para los elementos clave:

---

Disposición de Componentes de Percepción y Procesamiento (Segundo Piso):

Estos componentes vitales para la inteligencia y operación del robot se alojarán en una placa superior o "segundo piso", que se montará sobre el chasis principal, aprovechando estructuras como las mostradas en "Elemento 11.jpg".

---

![Motor Codificador Optico Makeblock 180](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Models/Elemento%2011.jpg))


Soporte Frontal Vertical (Cámara y Módulo): Esta estructura, parte del segundo piso o conectada a él, está diseñada específicamente para montar la cámara y su módulo adicional en la parte frontal elevada. Su posición estratégica garantiza un campo de visión despejado y alto, crucial para tareas como la detección de obstáculos, navegación y mapeo ambiental.

Espacio Inferior del Segundo Piso (Raspberry Pi y Puente H): En la zona inferior de este segundo nivel (o sobre la superficie de esta placa superior) se destinará el espacio para el Powerbank y la Raspberry Pi. Esta ubicación es fundamental para mantener el "cerebro" del robot (Raspberry Pi) y su fuente de energía suplementaria (Powerbank) accesibles, a la vez que se optimiza el cableado y se minimiza la altura total, contribuyendo al centro de gravedad general del conjunto.

---

# Electrónica

---

Nuestro sistema electrónico, que impulsa y controla cada movimiento de nuestro robot, está cuidadosamente ensamblado con los siguientes elementos clave:
-	Raspberry Pi 5
-	Raspberry Pi AI Camera
-	Servomotor
-	Motor Modificador Óptico Makeblock 180
-	Puente H
- Regulador de Voltaje
-	Baterías
-	Switch
-	Power Bank 

  
A continuación, se presentará el Diagrama de Cableado que ilustra cómo estos componentes se interconectan para funcionar en armonía.

![Motor Codificador Optico Makeblock 180](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Schemes/Diagrama%20de%20Cableado%20II.jpg)

Explicación del Diagrama Expuesto

Raspberry Pi: Es la computadora principal del sistema. Recibe información de algunos componentes y envía órdenes a otros.

Power Bank: Este es la fuente de energía exclusiva para la Raspberry Pi. Le suministra la electricidad necesaria para funcionar.

Baterías: Estas baterías son la fuente de energía exclusiva para los motores. Suministran electricidad al Módulo Regulador de Voltaje y al Módulo de Driver de Motor.

Módulo de Driver de Motor: Este módulo se conecta a la Raspberry Pi (para recibir órdenes) y a las baterías (para obtener energía). Se usa específicamente para controlar el motor DC con encoder.

Servo Motor: Este motor puede moverse a posiciones específicas y se controla a través del drive.

Motor DC con Encoder: Este es un motor que gira continuamente, y el "encoder" le permite a la Raspberry Pi saber exactamente qué tan rápido está girando o qué posición tiene. También se controla a través del driver del motor.

Módulo Regulador de Voltaje: Este módulo toma la energía de las baterías (las rojas) y la ajusta a un voltaje específico que necesita el servomotor, asegurando que reciba la cantidad correcta de energía de manera estable. 

Cámara: Esta cámara se conecta directamente a la Raspberry Pi. Permite a la Raspberry Pi "ver" y capturar imágenes o video.

****
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

(AC) convencionales por su capacidad de **controlar con precisión su posición angular, velocidad y, en algunos casos, su aceleración**. Piensa en él como un motor que no solo gira, sino que sabe exactamente dónde está y puede ir a una posición específica y mantenerla, incluso si hay una fuerza externa que intenta moverlo.

---

Servomotor
Un servomotor es un tipo de motor especial que se diferencia de los motores de corriente continua (DC) o alterna (AC) convencionales por su capacidad de controlar con precisión su posición angular, velocidad y, en algunos casos, su aceleración. Piensa en él como un motor que no solo gira, sino que sabe exactamente dónde está y puede ir a una posición específica y mantenerla, incluso si hay una fuerza externa que intenta moverlo.

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


![Regulador de Voltaje](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/Schemes/Regulador%20de%20voltaje%201.jpg)


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



---

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

# Gestión de Potencia y Control de Sentido del Vehiculo

---

Este documento detalla la estrategia de gestión de potencia y el sistema de control de sentido implementados en nuestro robot, utilizando una Raspberry Pi 5 y la Raspberry Pi AI Camera.

---

## Gestión de Energía y Sensores

Esta sección aborda cómo el vehículo gestiona su energía y sensores para navegar con precisión y eficiencia en los desafíos del entorno. Se detalla la fuente de alimentación, los sensores utilizados, su justificación técnica y el impacto de estos en el comportamiento del robot, así como un resumen del consumo energético.

## 1. Fuente de Energía
El robot utiliza dos fuentes de energía diferenciadas:

- Power Bank USB de 5V 3A: Alimenta exclusivamente a la Raspberry Pi 5, garantizando una alimentación estable y continua. Esta opción es práctica, segura y evita la necesidad de reguladores externos para la Raspberry.

- Batería Li-ion de 7.4V (mínimo 2000 mAh): Alimenta directamente el motor DC con encoder (propulsión) y el servomotor SG90 (dirección). Esta batería está conectada a través de un módulo de control de motor (usando GPIO y PWM desde la Raspberry Pi).

Este enfoque separa las cargas de procesamiento y movimiento, evitando caídas de tensión en la Raspberry Pi debido a picos de corriente de los motores.

Regulador de Voltaje (Buck Converter): Como la Raspberry Pi 5 y la Raspberry Pi AI Camera operan a 5V, y nuestras baterías de litio tienen un voltaje nominal más alto, un regulador de voltaje DC-DC (buck converter) es indispensable. Este componente reduce y estabiliza el voltaje de las baterías a los 5V requeridos, protegiendo la electrónica sensible de sobretensiones y fluctuaciones.

Switch Principal: Un interruptor físico nos permite encender y apagar el robot de forma segura, controlando el flujo general de energía desde las baterías.

## 2. Sensores
El sistema utiliza múltiples sensores y módulos para recopilar información del entorno:

- Cámara Picamera2: Captura video en tiempo real, analiza el entorno mediante visión artificial y detecta colores (negro, azul y naranja) en formato HSV para identificar líneas de guía, obstáculos y realizar conteo de vueltas.

- Encoder en motor DC: Permite medir la rotación del motor, ayudando al conteo de vueltas.
El sistema tiene un pin asignado para un encoder, pero la funcionalidad de conteo de vueltas actual se basa puramente en la visión por computadora.

- Servomotor SG90: Aunque es un actuador, responde constantemente a los comandos del sistema basados en los datos provenientes de los sensores para ejecutar giros precisos.

  ## 3. Consumo de Energía
Se estima el siguiente consumo energético:

- Raspberry Pi 5 (desde Power Bank): ~2.5 A @ 5V
- Motor DC: ~0.8 A @ 7.4V
- Servomotor SG90: ~150 mA @ 5V
- Cámara Picamera2: ~250 mA @ 5V (alimentada por la Raspberry)

El sistema completo requiere una batería con una capacidad mínima de 15 Wh para operar durante una sesión completa.

## 4. Justificación de Selección de Componentes
Los componentes fueron seleccionados por su eficiencia y compatibilidad:

- El motor DC con encoder permite una propulsión controlada y precisa, útil para detectar vueltas sin sensores adicionales.
- El servomotor SG90 proporciona dirección precisa y rápida con bajo consumo energético.
- La cámara permite reducir la cantidad de sensores al detectar colores y obstáculos simultáneamente mediante visión artificial.

El código de control implementado en Python gestiona la interpretación de los datos de los sensores y actúa en consecuencia, ajustando la dirección, velocidad y decisiones del robot según las condiciones del entorno.


---

## 🚗 Gestión de Movilidad

Este robot, diseñado en 3D, se mueve como un coche: sus ruedas traseras lo impulsan y las ruedas delanteras directrices lo guían. Su diseño mecánico, detallado en el modelo 3D, busca ser robusto y ligero, con espacio para todos los componentes.

La dirección es clave: un servomotor mueve las ruedas delanteras, controlando los giros mediante un mecanismo de dirección (tipo Ackerman). Un controlador coordina estos movimientos para lograr una maniobrabilidad precisa. En resumen, es un vehículo ágil, diseñado para el control exacto de su trayectoria..

---

## 🧠 Estrategias Planteadas para Resolver los Retos

En esta sección, compartimos las metodologías y enfoques innovadores que hemos diseñado para superar los desafíos propuestos en la competencia WRO 2025.

---
