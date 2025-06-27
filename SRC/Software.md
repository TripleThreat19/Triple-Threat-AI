Detección de Objetos y Límites de Pista 🤖

----
![Motor Codificador Optico Makeblock 180](https://github.com/TripleThreat19/Triple-Threat-AI/blob/main/SRC/Python.png)

Para capacitar a nuestro robot con la habilidad de "ver" su entorno, integramos un conjunto de sensores clave. Si bien los sensores de proximidad (como los ultrasónicos o infrarrojos) son cruciales para detectar obstáculos cercanos y medir distancias, el componente central de nuestra visión es la Cámara Raspberry Pi AI.

La Cámara Raspberry Pi AI, en combinación con algoritmos de visión por computadora desarrollados en Python, aprovecha librerías potentes como OpenCV para el procesamiento avanzado de imágenes. Esta sinergia nos permite no solo identificar la presencia de obstáculos, sino también clasificarlos eficazmente, ya sean conos u otros elementos estáticos presentes en el entorno de la pista. La información obtenida de esta detección es indispensable para que el robot tome decisiones de navegación precisas, como la desaceleración o la evasión.

Paralelamente, para asegurar que el robot se mantenga dentro de su trayectoria, utilizamos la Cámara Raspberry Pi AI para el reconocimiento de los bordes de la pista. A través del procesamiento de imágenes en Python, el sistema analiza las características visuales de la pista, incluyendo líneas y paredes, permitiendo al robot ajustar su dirección de forma continua para permanecer dentro de los límites predefinidos.


