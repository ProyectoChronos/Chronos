# Reporte de Descubrimiento - Sprint 2 (User Research)

**Objetivo del Sprint:** Validar las necesidades de nuestros usuarios, probar la viabilidad del prototipo inicial y definir los perfiles de usuario para guiar el desarrollo de Chronos.

**Responsable de Consolidación:** Edrick

---

## 1. User Personas (Definido por Edrick)

Basado en las historias de usuario y los datos iniciales, definimos dos perfiles clave que representan a nuestro público objetivo.

### User Persona 1: "Esteban el Estudiante"
* **(Foto de stock de un estudiante universitario)**
* **Nombre:** Esteban "El Abrumado"
* **Datos:** 20 años, Estudiante universitario.
* **Bio:** Esteban es un estudiante que se distrae fácilmente. Siempre tiene "muchas tareas", proyectos y exámenes, y le cuesta trabajo organizarse, lo que le genera estrés.
* **Frustraciones (Dolores):**
    * Se distrae mucho al tratar de estudiar.
    * Tiene tantos pendientes que no sabe por dónde empezar.
    * Siente estrés por la desorganización.
    * Usa post-its o notas físicas que son fáciles de olvidar o perder (Hallazgo de Entrevistas).
* **Necesita de Chronos:**
    * Poder agregar y clasificar sus tareas por fecha límite y prioridad.
    * Recibir **recomendaciones inteligentes** que le digan con qué tarea empezar.
    * Un **"Modo Enfoque"** que incluya diferentes técnicas de estudio como Pomodoro.
    * Recordatorios automáticos que le avisen de sus tareas.

### User Persona 2: "Mónica la Multitareas"
* **(Foto de stock de una persona trabajando en casa)**
* **Nombre:** Mónica "La Ocupada"
* **Datos:** 29 años, Empleada / Persona con múltiples compromisos.
* **Bio:** Mónica es una persona que balancea "múltiples compromisos", incluyendo tareas académicas, laborales y personales. Su día está lleno de reuniones y objetivos diarios.
* **Frustraciones (Dolores):**
    * Su información está regada (usa Google Calendar y libretas físicas); no puede "visualizar todo en un solo lugar".
    * Siente que el calendario es para "eventos", no para "tareas", y se le mezclan (Hallazgo de Entrevistas).
    * Le cuesta mantener un equilibrio en su vida.
* **Necesita de Chronos:**
    * Un **calendario integrado** para ver todas sus tareas.
    * Que el calendario tenga vistas diaria, semanal y mensual.
    * Poder diferenciar sus tareas (laborales vs. personales) con colores o etiquetas.

---

## 2. Hallazgos de Encuestas (Datos de Azul)

Se realizó una encuesta a 7 usuarios. Los hallazgos confirman nuestras hipótesis:

* **Uso de Herramientas:** La mayoría (5 de 7) ya usa una herramienta.
* **Herramienta Dominante:** "Google" (probablemente Calendar/Tasks) es la más mencionada.
* **Motivación Principal:** La principal motivación para cambiar sería "Que sea fácil y rápida de usar".
* **Características Más Deseadas:** 1) Recordatorios automáticos, 2) Clasificación por categorías, y 3) Modo de enfoque.

---

## 3. Hallazgos de Entrevistas (Datos de Ana)

Se realizaron 5 entrevistas semi-estructuradas. Los hallazgos clave son:

* **Frustración Universal:** La información está dispersa. Los usuarios usan una combinación de libretas físicas, Google Calendar, post-its y notas del celular. La necesidad de un "todo en uno" es el punto de dolor más grande.
* **Validación de Módulos:** Hubo un interés voluntario y recurrente en el **Modo Enfoque** (tipo Pomodoro) y en la **Gamificación** (recompensas, logros) como un gran motivador.
* **Calendario vs. Tareas:** Un hallazgo importante es que los usuarios mentalmente separan "Eventos" (reuniones, clases) de "Tareas" (pendientes, entregas).

---

## 4. Análisis de Competencia (Datos de Carlos)

Se realizó un análisis comparativo con las principales apps del mercado (TickTick, Todoist, Google Calendar).

* **Posición de Chronos:** Nuestra app busca ser un "todo en uno", combinando la organización de tareas (como Todoist), el seguimiento de hábitos y el modo enfoque.
* **Diferenciador Clave:** Mientras la competencia se enfoca solo en una cosa (Organización o Hábitos), nuestro valor agregado es la **integración total** de estas funciones en un solo lugar.

---

## 5. Hallazgos de Pruebas de Usabilidad (Datos de Guillermo)

Se ejecutaron las 5 pruebas de usabilidad planeadas con el prototipo del Sprint 1. Los resultados son claros:

* **Hallazgo 1 (Login - ÉXITO):** 5 de 5 usuarios completaron el flujo de login y registro sin ningún problema.
* **Hallazgo 2 (Home - FRACASO):** 4 de 5 usuarios **no encontraron la opción para hacer una tarea "recurrente"**. El botón estaba muy oculto y no era intuitivo.
* **Hallazgo 3 (Modo Enfoque - FRACASO):** 3 de 5 usuarios **no encontraron el "Modo Enfoque"**. Mencionaron que el ícono en la barra de navegación no era claro y lo buscaron primero en el menú de "Configuración".
* **Hallazgo 4 (Feedback General):** 2 de 5 usuarios mencionaron que la paleta de colores del prototipo era "muy brillante" y "cansaba la vista".

---

## 6. Conclusión Final y Próximos Pasos (Definido por Edrick)

Este sprint de descubrimiento fue exitoso. Hemos validado que existe una necesidad real para una app "todo en uno" y, lo más importante, hemos encontrado fallas críticas en nuestro primer prototipo antes de construirlo.

**Conclusiones Clave:**
1.  **El problema es real:** Los usuarios están frustrados por tener sus tareas y eventos en múltiples plataformas (libretas, apps, calendario).
2.  **Validamos los Módulos:** Las encuestas y entrevistas muestran un fuerte deseo por el "Modo Enfoque" y la "Gamificación".
3.  **El Prototipo Falló (¡Y eso es bueno!):** Las pruebas de usabilidad demuestran que, aunque la idea es buena, nuestro diseño actual para "Tareas Recurrentes" y el acceso al "Modo Enfoque" **no funciona** y debe ser rediseñado por completo.

**Próximos Pasos (Sugerencias para Sprint 3):**
1.  **Rediseño CRÍTICO (Home):** Rediseñar el flujo para "Agregar Tarea", haciendo que la opción "recurrente" sea obvia y fácil de encontrar.
2.  **Rediseño CRÍTICO (Navegación):** Mover o rediseñar el ícono del "Modo Enfoque" para que sea accesible e intuitivo (quizás moverlo al menú principal).
3.  **Ajuste de UI:** Revisar la paleta de colores para reducir el brillo y mejorar la accesibilidad.