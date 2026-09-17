# Registro de Riesgos: FamiGest

| ID | Descripción del Riesgo | Impacto | Probabilidad | Estrategia de Mitigación |
| :--- | :--- | :---: | :---: | :--- |
| **RSK-01** | **Fallas en la detección por iluminación o fondo:** Variaciones en el entorno del usuario pueden afectar la extracción de landmarks de MediaPipe. | Alto | Media | Implementar validaciones visuales en pantalla indicando al usuario ajustar la posición de la mano e iluminación. |
| **RSK-02** | **Latencia en inferencia on-device:** Incompatibilidad o lentitud al procesar cuadros de cámara en dispositivos de gama baja. | Alto | Baja | Normalizar coordenadas $x,y$ y utilizar un clasificador de señas estáticas ligero optimizado para el dispositivo. |
| **RSK-03** | **Retraso en la integración Expo/Cámara:** Incompatibilidad entre versiones de la librería de cámara y la extracción de cuadros en tiempo real. | Medio | Media | Utilizar módulos estándar de Expo Camera y realizar pruebas continuas de integración desde las primeras fases del Sprint 2. |
