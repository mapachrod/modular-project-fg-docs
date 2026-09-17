# Project Charter: FamiGest

**Fecha:** Septiembre 2026  
**Estado del documento:** Borrador | En revisión | Aprobado  

---

## Resumen Ejecutivo
FamiGest es una aplicación móvil gamificada orientada a ayudar a familiares oyentes a aprender Lengua de Señas Mexicana (LSM) para mejorar la comunicación con personas sordas en el entorno familiar. El sistema utiliza la cámara frontal del dispositivo para detectar de manera local y en tiempo real la postura de la mano mediante procesamiento de visión por computadora y aprendizaje automático, brindando retroalimentación inmediata sobre la correcta ejecución de las señas estáticas.

---

## Meta del Proyecto (SMART)
Desarrollar, validar y entregar, antes del cierre del ciclo académico, un prototipo funcional de la aplicación móvil FamiGest capaz de ofrecer al menos 3 lecciones interactivas de LSM con detección de mano por cámara, extracción de landmarks y clasificación de señas estáticas en tiempo real (con retroalimentación Correcto/Incorrecto en menos de 2 segundos), validado mediante pruebas piloto documentadas con 2 usuarios finales.

---

## Entregables Principales
- **Aplicación Móvil Prototipo (APK / Build funcional):** Navegación completa con lista de lecciones, pantalla de práctica con cámara y panel de resultados.
- **Módulo de Visión por Computadora e Inferencia:** Integración on-device de MediaPipe Hand Landmarker y clasificador estático para 3 señas de LSM.
- **Módulo de Persistencia Local:** Almacenamiento en dispositivo (AsyncStorage / SQLite) del progreso, intentos y porcentaje de aciertos.
- **Documentación de Gestión e Ingenieril:** Documentación de arquitectura, paquete de entrega de construcción (*Construction Handover Package*) y reporte de pruebas piloto.

---

## Justificación / Antecedentes
Las familias con integrantes sordos frecuentemente enfrentan barreras de comunicación debido a la falta de herramientas accesibles e interactivas para el aprendizaje de LSM. FamiGest aborda esta problemática combinando ludificación e inteligencia artificial en el dispositivo, ofreciendo una experiencia práctica de aprendizaje sin depender de conectividad constante a servidores externos para el procesamiento de imagen.

---

## Beneficios y Costos

### Beneficios
- Facilita el aprendizaje autónomo de LSM en entornos familiares.
- Retroalimentación interactiva e inmediata sin latencia de red gracias al procesamiento local (*on-device*).
- Prototipo de bajo costo, escalable y respetuoso con la privacidad visual del usuario al no transmitir video a la nube.

### Costos Estimados y Recursos
- Herramientas y entornos de desarrollo de código abierto (React Native, Expo, MediaPipe, TensorFlow Lite / JS).
- Dispositivos de prueba móviles (Android / iOS con cámara frontal).
- Horas hombre de diseño de interfaz, desarrollo de software, entrenamiento de clasificador y pruebas.

---

## Alcance y Exclusiones

### Dentro del Alcance (In-Scope)
- Interfaz de usuario y flujo de navegación para 3 lecciones estáticas de LSM.
- Captura de video frontal e integración con MediaPipe Hand Landmarker (21 puntos clave).
- Normalización de coordenadas ($x, y$) y clasificación local de postura.
- Almacenamiento local de progreso del usuario.
- Pruebas de usabilidad y precisión con un piloto de 2 usuarios.

### Fuera del Alcance (Out-of-Scope)
- Reconocimiento de señas dinámicas (movimiento complejo en el tiempo).
- Backend en la nube para autenticación de usuarios o almacenamiento centralizado.
- Diccionario completo de LSM (limitado únicamente al alcance del prototipo de 3 lecciones).
- Videollamadas o traducción bidireccional en tiempo real.

---

## Equipo del Proyecto
- **Patrocinador del Proyecto:** Evaluación Académica / Coordinación del Curso
- **Líder del Proyecto / Desarrollador Principal:** Maria Fernanda (Mafer)
- **Equipo de Soporte / Consultores:** Desarrollador UX/UI, Integrador de ML/CV

---

## Medición del Éxito
1. **Precisión y Autonomía:** El sistema clasifica correctamente las 3 señas estáticas de las lecciones con un tiempo de respuesta de retroalimentación en pantalla menor a 2 segundos.
2. **Evaluación Piloto:** El 100% de los usuarios de la prueba piloto (2 personas) logran completar las 3 lecciones y registrar su progreso localmente de forma satisfactoria.
3. **Cumplimiento de Entregables:** Entrega completa de la documentación de arquitectura, repositorio organizado y etiquetas de versión en Git (`construction-handover-v1.0`).
