# 🧪 Reporte de Pruebas de Usabilidad y Resultados

## 📋 Pruebas Informales (Diseño y Protocolo)

**Diseño Experimental:**  
Se realizaron 5 iteraciones de prueba de usabilidad con usuarios primarios (estudiantes universitarios), utilizando un prototipo de fidelidad media. El objetivo fue evaluar la facilidad de uso, la encontrabilidad de funciones y la comprensión de los flujos principales.

**Protocolo de Prueba (Task-Based Testing):**  
Se siguió un guion estandarizado dividiendo la prueba en 5 tareas críticas:

1. **Configuración:** Navegación hacia ajustes y personalización.  
2. **Autenticación:** Flujos de registro e inicio de sesión.  
3. **Modo Enfoque:** Activación y configuración de temporizadores (Pomodoro, Personalizado).  
4. **Calendario:** Asignación de tareas y selección de fechas.  
5. **Bienestar:** Registro de hábitos y visualización de gráficos.

**Indicadores Recolectados:**
* **Encontrabilidad:** Capacidad del usuario para ubicar el acceso a funciones (ej. icono de configuración, inicio de sesión).
* **Comprensión:** Nivel de entendimiento sobre la diferencia entre modos de estudio y categorías.
* **Satisfacción (CSAT):** Cuestionario post-prueba para medir la percepción visual y funcional (Promedio obtenido: 4.5/5).

---

## 📊 Resultados y Análisis de Mejoras

**Análisis de Hallazgos:**
* **Validación General:** El prototipo obtuvo una calificación promedio de **4.5 sobre 5**, indicando una alta aceptación de la interfaz visual.
* **Modo Enfoque (Iteración 01):** El usuario logró activar el modo Pomodoro eficazmente. Sin embargo, se identificó un problema de usabilidad crítico: el icono de configuración ("tuerca") no fue intuitivo para cambiar los rangos de tiempo. Además, se detectó la ausencia de un botón explícito de "Pausa".
* **Limitaciones Técnicas:** En las tareas de Calendario y Bienestar (Tests 4 y 5), la falta de interactividad del prototipo (botones no funcionales) generó fricción momentánea, aunque los usuarios identificaron correctamente las zonas de clic.
* **Autenticación:** Se reportó dificultad visual al ingresar texto debido a una limitación de la herramienta de diseño (Figma), donde no se previsualizaba lo escrito.

---

## 🛠️ Plan de Mejoras Específicas (Acciones Correctivas)

| Área | Hallazgo / Incidente | Mejora a Implementar | Clasificación |
| :--- | :--- | :--- | :--- |
| **Interfaz (UI)** | El icono de "tuerca" no se asocia con cambiar tiempos del temporizador. | **Rediseñar icono:** Cambiar por un indicador de tiempo más explícito o mejorar la etiqueta del botón. | Bug (Usabilidad) |
| **Funcionalidad** | El usuario no encontró cómo detener el tiempo momentáneamente. | **Agregar Botón de Pausa:** Incluir control de *Play/Pause* visible en la pantalla del temporizador. | Feature Required |
| **Interacción** | Confusión en campos de texto (Login). | **Feedback Visual:** Implementar estados activos en los inputs para confirmar la escritura. | Mejora de UX |
| **Navegación** | Instrucciones del guion no comprendidas en la búsqueda de modos. | **Simplificar Acceso:** Hacer el menú de "Modos de Estudio" más prominente en el Home. | Mejora de UX |
