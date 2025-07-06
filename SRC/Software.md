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



