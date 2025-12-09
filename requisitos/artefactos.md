# 📋 Artefactos del Proyecto

## Definición de Artefactos

Los artefactos son documentos, modelos, diagramas y entregables que se producen durante el desarrollo del proyecto CHRONOS. Estos artefactos documentan decisiones, diseños, procesos y resultados del proyecto.

---

# Historias de Usuarios

## A) Gestión General de Tareas
**Como:** Un usuario de la aplicación CHRONOS  
**Quiero:** Poder agregar y clasificar mis tareas  
**Para que:** Pueda organizar mejor mis pendientes y reducir mi estrés

**Criterios de aceptación:**
1. Debo poder crear tareas y asignarles categorías y subcategorías.
2. La aplicación debe permitirme establecer fechas límites y niveles de prioridad para cada tarea.
3. Debe haber recordatorios automáticos que me avisen sobre mis tareas pendientes.
4. Quiero ver un indicador visual de mi progreso, mostrando tareas completadas y pendientes.

> **Notas de diseño:** La interfaz debe ser intuitiva y fácil de usar.

---

## B) Recomendaciones Inteligentes (Estudiante)
**Como:** Estudiante con muchas tareas  
**Quiero:** Recibir recomendaciones inteligentes que me sugieran el orden de ejecución según urgencia y carga  
**Para que:** Pueda administrar mejor mi tiempo y priorizar lo más importante

**Criterios de aceptación:**
1. El sistema debe analizar las tareas según fecha límite, prioridad y carga acumulada.
2. Debe sugerirme un orden de ejecución visible.
3. Debo poder aceptar o ignorar las recomendaciones.
4. Las recomendaciones deben actualizarse automáticamente al cambiar fechas o prioridades.
5. El sistema debe justificar brevemente por qué recomienda ese orden (ej. "Fecha límite más próxima").

> **Notas:**  
> * Las recomendaciones deben mostrarse de manera clara y no invasiva.  
> * El algoritmo debe ser eficiente y no afectar el rendimiento de la app.

---

## C) Modos de Estudio y Enfoque
**Como:** Estudiante que se distrae fácilmente  
**Quiero:** Activar un modo enfoque o seleccionar entre diferentes modos de estudio  
**Para que:** Pueda concentrarme en mis actividades y elegir la técnica que mejor se adapte a mi forma de trabajar

**Criterios de aceptación:**
1. Debo poder elegir entre distintos modos de estudio antes de iniciar (ej. Modo Enfoque simple, Pomodoro, Sesión libre, Descanso programado).
2. Cada modo debe tener una breve descripción para que el usuario entienda cómo funciona antes de seleccionarlo.
3. Debo poder personalizar la duración de los intervalos de cada modo (ej. Pomodoro de 50/10 en lugar de 25/5).
4. El sistema debe mostrar un temporizador con el tiempo restante en cada ciclo o sesión.
5. El sistema debe guardar un historial de las sesiones realizadas (ej. cuántos pomodoros completados en un día).
6. Si el usuario selecciona Pomodoro u otro modo cíclico, el sistema debe notificar claramente cuándo es momento de descansar o volver a trabajar.

> **Notas:**  
> * Diseño minimalista con colores/sonidos para cambios de estado.  
> * Integración con sistema de recompensas (ej. medallas).  
> * Configuración de modo favorito para inicio rápido.  
> * Futuras versiones: Time Blocking o Deep Work.

---

## D) Calendario Integrado (Múltiples Compromisos)
**Como:** Persona con múltiples compromisos  
**Quiero:** Un calendario integrado que sincronice mis tareas académicas, laborales y personales  
**Para que:** Pueda visualizar todo en un solo lugar y mantener equilibrio en mi vida

**Criterios de aceptación:**
1. Debo poder ver todas mis tareas organizadas en un calendario integrado.
2. El calendario debe permitir vistas diaria, semanal y mensual.
3. Cada categoría de tarea debe diferenciarse con un color o etiqueta.
4. Debo poder crear, editar y eliminar eventos directamente en el calendario.
5. El sistema debe mostrar notificaciones de los eventos agendados.

> **Notas:**  
> * El calendario debe ser responsivo (móviles y pantallas grandes).  
> * Se recomienda ofrecer exportación a PDF/ICS para compartir la agenda.


## Clasificación de Artefactos

### 📚 Artefactos de Gestión

#### AGE-001: Charter del Proyecto
**Descripción:** Documento que autoriza formalmente el inicio del proyecto  
**Responsable:** Equipo completo  
**Estado:** ✅ Completado  
**Ubicación:** `README.md`

#### AGE-002: Plan de Trabajo
**Descripción:** Cronograma detallado de actividades y entregables  
**Responsable:** Scrum Master (rotativo)  
**Estado:** 🔄 En progreso  
**Ubicación:** `proceso/gestion.md`

#### AGE-003: Matriz de Responsabilidades (RACI)
**Descripción:** Definición de roles y responsabilidades por actividad  
**Responsable:** Equipo completo  
**Estado:** ✅ Completado  
**Ubicación:** `proceso/organizacion.md`

#### AGE-004: Registro de Riesgos
**Descripción:** Identificación y plan de mitigación de riesgos  
**Responsable:** Líder de proyecto (rotativo)  
**Estado:** 🔄 En progreso  
**Ubicación:** `proceso/gestion.md`

### 📖 Artefactos de Requisitos

#### ARQ-001: Documento de Requisitos Funcionales
**Descripción:** Especificación detallada de funcionalidades del sistema  
**Responsable:** Analista de requisitos (rotativo)  
**Estado:** ✅ Completado  
**Ubicación:** `requisitos/funcionales.md`

#### ARQ-002: Documento de Requisitos No Funcionales
**Descripción:** Especificación de calidad, rendimiento y restricciones  
**Responsable:** Arquitecto de software (rotativo)  
**Estado:** ✅ Completado  
**Ubicación:** `requisitos/no-funcionales.md`

#### ARQ-003: Matriz de Priorización
**Descripción:** Análisis y priorización de todos los requisitos  
**Responsable:** Product Owner (rotativo)  
**Estado:** ✅ Completado  
**Ubicación:** `requisitos/priorizacion.md`

#### ARQ-004: Casos de Uso
**Descripción:** Escenarios detallados de interacción usuario-sistema  
**Responsable:** Analista de requisitos (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `requisitos/casos-uso.md` (futuro)

#### ARQ-005: Historias de Usuario
**Descripción:** Requisitos desde perspectiva del usuario final  
**Responsable:** Product Owner (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `requisitos/historias-usuario.md` (futuro)

### 🎨 Artefactos de Diseño

#### ADI-001: Wireframes de Baja Fidelidad
**Descripción:** Bocetos básicos de interfaces de usuario  
**Responsable:** UX/UI Designer (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `diseno/wireframes/` (futuro)

#### ADI-002: Mockups de Alta Fidelidad
**Descripción:** Diseños visuales detallados de la aplicación  
**Responsable:** UX/UI Designer (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `diseno/mockups/` (futuro)

#### ADI-003: Prototipo Interactivo
**Descripción:** Prototipo navegable para validación de UX  
**Responsable:** UX/UI Designer (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `diseno/prototipo/` (futuro)

#### ADI-004: Guía de Estilo Visual
**Descripción:** Colores, tipografías, iconografía y elementos visuales  
**Responsable:** UX/UI Designer (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `diseno/guia-estilo.md` (futuro)

#### ADI-005: Sistema de Diseño (Design System)
**Descripción:** Componentes reutilizables y patrones de diseño  
**Responsable:** UX/UI Designer (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `diseno/design-system/` (futuro)

### 🏗️ Artefactos de Arquitectura

#### AAR-001: Documento de Arquitectura de Software
**Descripción:** Estructura técnica de alto nivel del sistema  
**Responsable:** Arquitecto de software (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `arquitectura/documento-arquitectura.md` (futuro)

#### AAR-002: Diagrama de Arquitectura del Sistema
**Descripción:** Representación visual de componentes y sus relaciones  
**Responsable:** Arquitecto de software (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `arquitectura/diagramas/` (futuro)

#### AAR-003: Modelo de Base de Datos
**Descripción:** Diseño conceptual y físico de la base de datos  
**Responsable:** Database Designer (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `arquitectura/base-datos/` (futuro)

#### AAR-004: Especificación de API
**Descripción:** Documentación detallada de endpoints y contratos  
**Responsable:** Backend Developer (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `arquitectura/api-spec.md` (futuro)

#### AAR-005: Diagrama de Componentes
**Descripción:** Estructura interna de módulos y componentes  
**Responsable:** Arquitecto de software (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `arquitectura/componentes.md` (futuro)

### 💻 Artefactos de Implementación

#### AIM-001: Código Fuente
**Descripción:** Implementación del sistema en tecnologías seleccionadas  
**Responsable:** Equipo de desarrollo  
**Estado:** 📅 Pendiente  
**Ubicación:** `src/` (futuro)

#### AIM-002: Scripts de Base de Datos
**Descripción:** Scripts de creación, migración y semillas de datos  
**Responsable:** Database Developer (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `database/` (futuro)

#### AIM-003: Configuración de Ambiente
**Descripción:** Archivos de configuración para diferentes ambientes  
**Responsable:** DevOps Engineer (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `config/` (futuro)

#### AIM-004: Documentación de Código
**Descripción:** Comentarios y documentación técnica inline  
**Responsable:** Cada desarrollador  
**Estado:** 📅 Pendiente  
**Ubicación:** Dentro del código fuente

### 🧪 Artefactos de Pruebas

#### APR-001: Plan de Pruebas
**Descripción:** Estrategia y enfoque de testing del sistema  
**Responsable:** QA Engineer (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `testing/plan-pruebas.md` (futuro)

#### APR-002: Casos de Prueba
**Descripción:** Escenarios específicos para validar funcionalidades  
**Responsable:** QA Engineer (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `testing/casos-prueba/` (futuro)

#### APR-003: Scripts de Pruebas Automatizadas
**Descripción:** Tests unitarios, integración y end-to-end  
**Responsable:** Equipo de desarrollo  
**Estado:** 📅 Pendiente  
**Ubicación:** `tests/` (futuro)

#### APR-004: Reportes de Pruebas
**Descripción:** Resultados y métricas de ejecución de pruebas  
**Responsable:** QA Engineer (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `testing/reportes/` (futuro)

#### APR-005: Pruebas de Usabilidad
**Descripción:** Tests con usuarios reales para validar UX  
**Responsable:** UX Researcher (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `testing/usabilidad/` (futuro)

### 📊 Artefactos de Seguimiento

#### ASE-001: Reportes de Avance
**Descripción:** Status semanal del progreso del proyecto  
**Responsable:** Scrum Master (rotativo)  
**Estado:** 🔄 En progreso  
**Ubicación:** `reportes/avance/` (futuro)

#### ASE-002: Métricas del Proyecto
**Descripción:** KPIs de desarrollo, calidad y rendimiento del equipo  
**Responsable:** Analista de métricas (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `metricas/` (futuro)

#### ASE-003: Lecciones Aprendidas
**Descripción:** Retrospectivas y mejoras identificadas  
**Responsable:** Equipo completo  
**Estado:** 🔄 En progreso  
**Ubicación:** `retrospectivas/` (futuro)

#### ASE-004: Log de Decisiones Técnicas
**Descripción:** Registro de decisiones importantes y su justificación  
**Responsable:** Arquitecto de software (rotativo)  
**Estado:** 📅 Pendiente  
**Ubicación:** `decisiones/` (futuro)

---

## Calendario de Entregables

### 📅 Sprint 0 (Semana 1-2) - Planificación
- [x] Charter del Proyecto (AGE-001)
- [x] Documento de Requisitos Funcionales (ARQ-001)
- [x] Documento de Requisitos No Funcionales (ARQ-002)
- [x] Matriz de Priorización (ARQ-003)
- [ ] Plan de Trabajo (AGE-002)
- [ ] Matriz RACI (AGE-003)

### 📅 Sprint 1 (Semana 3-4) - Diseño
- [ ] Casos de Uso (ARQ-004)
- [ ] Historias de Usuario (ARQ-005)
- [ ] Wireframes de Baja Fidelidad (ADI-001)
- [ ] Documento de Arquitectura (AAR-001)
- [ ] Plan de Pruebas (APR-001)

### 📅 Sprint 2 (Semana 5-6) - Arquitectura Detallada
- [ ] Mockups de Alta Fidelidad (ADI-002)
- [ ] Diagrama de Arquitectura (AAR-002)
- [ ] Modelo de Base de Datos (AAR-003)
- [ ] Especificación de API (AAR-004)
- [ ] Configuración de Ambiente (AIM-003)

### 📅 Sprint 3-8 (Semana 7-16) - Desarrollo MVP
- [ ] Código Fuente - Fase 1 (AIM-001)
- [ ] Scripts de Base de Datos (AIM-002)
- [ ] Tests Unitarios (APR-003)
- [ ] Casos de Prueba (APR-002)
- [ ] Reportes de Avance semanales (ASE-001)

### 📅 Sprint 9-12 (Semana 17-24) - Características Avanzadas
- [ ] Código Fuente - Fase 2 (AIM-001)
- [ ] Prototipo Interactivo (ADI-003)
- [ ] Guía de Estilo Visual (ADI-004)
- [ ] Pruebas de Usabilidad (APR-005)
- [ ] Métricas del Proyecto (ASE-002)

---

## Estándares de Documentación

### 📝 Formato de Documentos
- **Markdown** para toda la documentación textual
- **Mermaid** para diagramas técnicos
- **Figma** para diseños visuales y prototipos
- **JSON/YAML** para configuraciones

### 📂 Estructura de Archivos
```
chronos/
├── README.md                    # Charter del proyecto
├── producto/                    # Definición del producto
├── requisitos/                  # Documentación de requisitos
├── diseno/                      # Artefactos de diseño (futuro)
├── arquitectura/                # Documentos técnicos (futuro)
├── src/                         # Código fuente (futuro)
├── tests/                       # Pruebas automatizadas (futuro)
├── docs/                        # Documentación adicional (futuro)
└── reportes/                    # Seguimiento del proyecto (futuro)
```

### ✅ Criterios de Calidad
Todos los artefactos deben cumplir:
- **Completitud:** Información suficiente para su propósito
- **Consistencia:** Coherencia con otros artefactos
- **Claridad:** Lenguaje claro y comprensible
- **Actualización:** Mantenido al día con cambios
- **Trazabilidad:** Referencias claras entre artefactos
- **Versionado:** Control de cambios documentado

### 🔄 Proceso de Revisión
1. **Autor** crea el artefacto
2. **Peer Review** por al menos un compañero
3. **Aprobación** por el responsable del área
4. **Integración** al repositorio principal
5. **Notificación** al equipo sobre disponibilidad

---

## Herramientas y Tecnologías

### 📱 Herramientas de Documentación
- **GitHub/GitLab:** Versionado y colaboración
- **Markdown:** Formato de documentación
- **Mermaid:** Diagramas integrados en Markdown
- **VS Code:** Editor principal con extensiones Markdown

### 🎨 Herramientas de Diseño
- **Figma:** Wireframes, mockups y prototipos
- **Canva:** Materiales de presentación
- **Draw.io:** Diagramas técnicos alternativos

### 💻 Herramientas de Desarrollo
- **Git:** Control de versiones de código
- **Docker:** Configuración de ambientes
- **Postman:** Documentación de APIs
- **Jest:** Framework de testing

### 📊 Herramientas de Gestión
- **GitHub Projects:** Seguimiento de tareas
- **Discord:** Comunicación del equipo
- **Google Workspace:** Colaboración y reportes

---

## Métricas de Artefactos

### 📈 Métricas de Completitud
| Categoría | Artefactos Planeados | Completados | Progreso |
|-----------|---------------------|-------------|----------|
| Gestión | 4 | 1 | 25% |
| Requisitos | 5 | 3 | 60% |
| Diseño | 5 | 0 | 0% |
| Arquitectura | 5 | 0 | 0% |
| Implementación | 4 | 0 | 0% |
| Pruebas | 5 | 0 | 0% |
| Seguimiento | 4 | 0 | 0% |

**Progreso Total:** 4/32 artefactos completados (12.5%)

### 📊 Métricas de Calidad
- **Artefactos con revisión por pares:** 100%
- **Artefactos actualizados en últimas 2 semanas:** 100%
- **Artefactos con referencias cruzadas:** 75%
- **Artefactos con control de versiones:** 100%

---

## Gestión de Cambios en Artefactos

### 🔄 Proceso de Actualización
1. **Identificación** de necesidad de cambio
2. **Evaluación** de impacto en otros artefactos
3. **Aprobación** del cambio por stakeholders
4. **Actualización** del artefacto principal
5. **Propagación** de cambios a artefactos dependientes
6. **Comunicación** al equipo

### 📋 Control de Versiones
- Versionado semántico para artefactos críticos
- Tag de Git para versiones importantes
- Log de cambios en commit messages
- Archivo CHANGELOG.md para cambios mayores

---

**Estado de artefactos actualizado:** 29 de Septiembre de 2025  
**Próxima revisión:** 6 de Octubre de 2025  
**Responsable de seguimiento:** Equipo completo (rotativo semanal)

---

*Artefactos organizados para asegurar la calidad y trazabilidad del proyecto* 📋✨
