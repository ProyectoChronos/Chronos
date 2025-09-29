# 🎯 Gestión del Proceso

## Planificación del Proyecto

### 📅 Cronograma Maestro

#### Duración Total: 24 semanas (6 meses académicos)
#### Fecha de inicio: 29 de Septiembre de 2025
#### Fecha de entrega: 15 de Marzo de 2026

### 🗓️ Calendario de Entregas

| Hito | Fecha | Entregables |
|------|-------|-------------|
| **Primera Entrega** | 13 de Octubre, 2025 | Documentación inicial, requisitos |
| **Segunda Entrega** | 17 de Noviembre, 2025 | Diseño y arquitectura |
| **Tercera Entrega** | 15 de Diciembre, 2025 | MVP funcional |
| **Cuarta Entrega** | 19 de Enero, 2026 | Características avanzadas |
| **Entrega Final** | 15 de Marzo, 2026 | Sistema completo y documentación |

---

## Estructura de Governance

### 👑 Roles de Liderazgo

#### Project Manager (Rotativo mensual)
**Responsabilidades:**
- Coordinación general del proyecto
- Comunicación con stakeholders externos
- Escalación de impedimentos críticos
- Reporte de estado a profesora

**Calendario de rotación:**
- **Octubre:** Carlos Cauich
- **Noviembre:** Ana Lavadores  
- **Diciembre:** Guillermo Peña
- **Enero:** Valeria Itza
- **Febrero:** Edrick Puc
- **Marzo:** Carlos Cauich

#### Tech Lead (Rotativo por sprint)
**Responsabilidades:**
- Decisiones arquitectónicas y técnicas
- Code review final y estándares
- Resolución de conflictos técnicos
- Mentoring técnico al equipo

#### Quality Assurance Lead (Rotativo por sprint)
**Responsabilidades:**
- Estrategia de testing del proyecto
- Definición de criterios de aceptación
- Validación de Definition of Done
- Reporte de métricas de calidad

---

## Planificación de Sprints

### 🏃‍♂️ Roadmap de Sprints

#### Sprint 0 (Sept 29 - Oct 13): Fundación
**Objetivo:** Establecer bases y documentación inicial
- Configuración de herramientas y repositorio
- Análisis de requisitos detallado
- Definición de arquitectura inicial
- Primera planificación de desarrollo

**Entregables:**
- Documentación de requisitos completa
- Configuración de ambiente de desarrollo
- Plan de proyecto detallado

#### Sprint 1 (Oct 14 - Oct 27): Arquitectura y Diseño
**Objetivo:** Definir diseño y estructura técnica
- Wireframes y mockups de interfaces principales
- Diseño de base de datos
- Definición de APIs principales
- Setup de framework de desarrollo

**Entregables:**
- Documentos de arquitectura
- Prototipos visuales
- Ambiente de desarrollo operativo

#### Sprint 2 (Oct 28 - Nov 10): Core Backend
**Objetivo:** Implementar funcionalidades backend básicas
- Sistema de autenticación y usuarios
- API REST para gestión de tareas
- Modelo de base de datos implementado
- Tests unitarios básicos

#### Sprint 3 (Nov 11 - Nov 24): Core Frontend
**Objetivo:** Implementar interfaces principales
- Sistema de login y registro
- Dashboard principal de usuario
- CRUD de tareas funcional
- Responsive design básico

#### Sprint 4 (Nov 25 - Dec 8): Gamificación Backend
**Objetivo:** Sistema de puntos y logros
- API de gamificación
- Sistema de puntos por acciones
- Logros básicos implementados
- Niveles de usuario

#### Sprint 5 (Dec 9 - Dec 22): Gamificación Frontend
**Objetivo:** Interfaz de gamificación
- Dashboard de progreso y logros
- Visualización de puntos y niveles
- Notificaciones de logros
- Animaciones básicas

#### Sprint 6 (Jan 6 - Jan 19): Herramientas de Bienestar
**Objetivo:** Funcionalidades de bienestar
- Check-in de estado de ánimo
- Temporizador Pomodoro
- Recordatorios de bienestar
- Métricas de bienestar

#### Sprint 7 (Jan 20 - Feb 2): Calendario y Notificaciones
**Objetivo:** Sistema de calendario
- Vista de calendario integrada
- Sistema de notificaciones push
- Integración de fechas límite
- Recordatorios inteligentes

#### Sprint 8 (Feb 3 - Feb 16): Colaboración Básica
**Objetivo:** Funcionalidades colaborativas
- Espacios de trabajo compartidos
- Asignación de tareas en equipo
- Comentarios en tareas
- Notificaciones de equipo

#### Sprint 9 (Feb 17 - Mar 2): Optimización y Testing
**Objetivo:** Estabilización y calidad
- Testing exhaustivo de funcionalidades
- Optimización de rendimiento
- Corrección de bugs críticos
- Documentación de usuario

#### Sprint 10 (Mar 3 - Mar 16): Finalización
**Objetivo:** Preparación para entrega
- Testing final y estabilización
- Documentación completa
- Preparación de presentación
- Deployment final

---

## Gestión de Recursos

### 👥 Asignación de Personas

#### Capacity Planning por Sprint:
**Cada miembro:** 20 horas/semana disponibles  
**Total equipo:** 100 horas/semana  
**Por sprint (2 semanas):** 200 horas totales

#### Distribución de Esfuerzo:
- **Desarrollo:** 60% (120 horas)
- **Testing:** 20% (40 horas)
- **Documentación:** 10% (20 horas)
- **Gestión/Coordinación:** 10% (20 horas)

### 💻 Recursos Técnicos

#### Hardware:
- Laptops personales de cada integrante
- Cuenta en servicios cloud para deployment (GitHub, Vercel, etc.)

#### Software:
- **Gratis/Open Source:** VS Code, Git, Node.js, PostgreSQL
- **Servicios Cloud Gratuitos:** GitHub, Vercel, Supabase/Firebase
- **Herramientas de Diseño:** Figma (plan gratuito)

#### Presupuesto Estimado:
- **$0 USD:** Desarrollo completo con herramientas gratuitas
- **Opcional $50 USD:** Dominio personalizado y servicios premium

---

## Control de Cambios

### 🔄 Proceso de Change Management

#### Tipos de Cambios:
1. **Menor (Minor):** Bug fixes, mejoras pequeñas de UX
2. **Mayor (Major):** Nuevas funcionalidades, cambios de arquitectura
3. **Crítico (Critical):** Cambios que afectan alcance o timeline

#### Proceso de Aprobación:

##### Cambios Menores:
1. Cualquier miembro puede proponer
2. Revisión por Tech Lead
3. Implementación directa si aprobado

##### Cambios Mayores:
1. Propuesta documentada con impacto
2. Discusión en Sprint Planning
3. Votación del equipo completo
4. Aprobación por Product Owner

##### Cambios Críticos:
1. Propuesta formal documentada
2. Análisis de impacto en timeline/recursos
3. Aprobación unanime del equipo
4. Validación con profesora (stakeholder)

### 📝 Change Request Template:

```markdown
## Change Request #[ID]

**Tipo:** [Minor/Major/Critical]
**Solicitante:** [Nombre]
**Fecha:** [YYYY-MM-DD]

### Descripción
[Descripción detallada del cambio]

### Justificación
[Por qué es necesario este cambio]

### Impacto
- **Timeline:** [Días adicionales o ahorrados]
- **Resources:** [Esfuerzo adicional requerido]
- **Scope:** [Funcionalidades afectadas]
- **Risk:** [Riesgos introducidos]

### Alternativas Consideradas
[Otras opciones evaluadas]

### Decisión
- [ ] Aprobado
- [ ] Rechazado
- [ ] Diferido

**Firmas de Aprobación:**
- Product Owner: [ ]
- Tech Lead: [ ]
- Equipo: [ ]
```

---

## Gestión de Riesgos

### ⚠️ Matriz de Riesgos

| ID | Riesgo | Probabilidad | Impacto | Score | Mitigación |
|----|--------|--------------|---------|-------|------------|
| R01 | Miembro del equipo abandona proyecto | Baja | Alto | 6 | Rotación de roles, documentación completa |
| R02 | Problemas técnicos complejos | Media | Alto | 9 | Spikes de investigación, mentoring externo |
| R03 | Scope creep sin control | Alta | Medio | 9 | Product Owner fuerte, change control |
| R04 | Conflictos en el equipo | Baja | Alto | 6 | Retrospectivas, escalación temprana |
| R05 | Tecnología elegida inadecuada | Media | Medio | 6 | Prototipos tempranos, spike solutions |
| R06 | Tiempo insuficiente por otras materias | Alta | Medio | 9 | Sprints flexibles, priorización estricta |
| R07 | Pérdida de código o trabajo | Baja | Alto | 6 | Git, backups automatizados |
| R08 | Problemas de comunicación | Media | Medio | 6 | Standups regulares, herramientas colaborativas |

### 🛡️ Plan de Mitigación de Riesgos Top 3:

#### R02 & R03 & R06 (Score 9): Problemas técnicos, scope creep, tiempo insuficiente

**Estrategias:**
1. **Time-boxing estricto:** Máximo 4 horas para investigar antes de pedir ayuda
2. **MVP approach:** Priorización ruthless de características core
3. **Buffer planning:** 20% de tiempo adicional en estimaciones
4. **Escalación rápida:** Comunicación inmediata de impedimentos
5. **Scope freezing:** No cambios mayores después del Sprint 6

---

## Comunicación y Reporting

### 📊 Reportes Regulares

#### Sprint Report (Cada 2 semanas):
**Para:** Profesora supervisora  
**Contenido:**
- Objetivos del sprint vs. logros reales
- Métricas de velocity y burndown
- Impedimentos encontrados y resoluciones
- Próximos objetivos y riesgos

#### Monthly Status Report:
**Para:** Stakeholders académicos  
**Contenido:**
- Progress general del proyecto (% completion)
- Milestone status y fecha estimada
- Budget/resource status
- Key decisions tomadas
- Risk updates

#### Weekly Team Sync:
**Interno del equipo**  
**Contenido:**
- Individual progress updates
- Cross-team dependencies
- Upcoming deadlines
- Resource needs

### 📞 Canales de Comunicación

#### Comunicación Interna:
- **Discord:** Chat diario y notificaciones
- **WhatsApp Grupo:** Comunicación urgente
- **Google Meet:** Ceremonias de Scrum
- **GitHub:** Communication técnica y code reviews

#### Comunicación Externa:
- **Email:** Reportes formales a profesora
- **Google Drive:** Documentos colaborativos
- **Calendario Compartido:** Fechas importantes

---

## Métricas de Gestión

### 📈 KPIs del Proyecto

#### Delivery Metrics:
- **Velocity:** Story points completados por sprint (target: 25-30)
- **Burndown Rate:** % de backlog completado (target: linear)
- **Sprint Completion:** % de commitment completado (target: >90%)

#### Quality Metrics:
- **Code Coverage:** % de código con tests (target: >80%)
- **Bug Rate:** Bugs por story point (target: <0.1)
- **Tech Debt:** Time spent on refactoring (target: <20%)

#### Team Metrics:
- **Attendance:** % asistencia a ceremonias (target: >95%)
- **Contribution Balance:** Distribución equitativa de commits
- **Satisfaction:** Team happiness index (1-5, target: >4)

### 📊 Dashboard de Proyecto

**Herramientas de Tracking:**
- **GitHub Projects:** Kanban board y progress tracking
- **GitHub Insights:** Code contributions y activity
- **Google Sheets:** Manual metrics tracking
- **Discord Bot:** Automated reminders y status

---

## Gestión de Calidad

### ✅ Quality Gates por Sprint

#### Definition of Ready (para User Stories):
- [ ] Criterios de aceptación claros y testeable
- [ ] Estimación completada por el equipo
- [ ] Dependencias identificadas y manejadas
- [ ] UI mockups disponibles (si aplica)

#### Definition of Done (para Sprint):
- [ ] Todas las user stories completadas según DoD
- [ ] Code coverage >80% mantenido
- [ ] No bugs críticos pendientes
- [ ] Documentación actualizada
- [ ] Sprint review y retrospective completadas

### 🔍 Proceso de Code Review

#### Criterios de Code Review:
- **Functionality:** ¿El código hace lo que debe hacer?
- **Readability:** ¿Es fácil de leer y entender?
- **Performance:** ¿Hay optimizaciones obvias necesarias?
- **Security:** ¿Hay vulnerabilidades evidentes?
- **Testing:** ¿Los tests cubren casos importantes?

#### Code Review Guidelines:
- Mínimo 1 reviewer, preferiblemente 2
- Reviewer no puede ser el autor
- Reviews completadas dentro de 24 horas
- Comentarios constructivos y específicos
- Aprobación requerida antes de merge

---

## Procedimientos de Emergencia

### 🚨 Escalación de Problemas

#### Nivel 1: Problema de desarrollo (Developer → Tech Lead)
- Timeline: Inmediato
- Scope: Problemas técnicos individuales
- Resolution: Mentoring, pair programming, research time

#### Nivel 2: Problema de sprint (Tech Lead → Scrum Master)
- Timeline: Dentro de 24 horas
- Scope: Impedimentos que afectan sprint goals
- Resolution: Re-planning, resource re-allocation

#### Nivel 3: Problema de proyecto (Scrum Master → Project Manager)
- Timeline: Dentro de 48 horas
- Scope: Issues que afectan milestones o entregas
- Resolution: Scope adjustment, timeline revision

#### Nivel 4: Problema crítico (Project Manager → Profesora)
- Timeline: Inmediato
- Scope: Riesgos a integridad del proyecto
- Resolution: Intervention externa, major changes

### 🔄 Contingency Planning

#### Escenario: Pérdida de miembro del equipo
**Response:**
1. Redistribución inmediata de tareas críticas
2. Re-planning de sprints afectados
3. Potential scope reduction
4. Escalación a profesora para apoyo

#### Escenario: Problema técnico mayor
**Response:**
1. Time-box de 8 horas para research
2. Consultoría externa (profesores, seniors)
3. Alternative technology evaluation
4. Potential architecture pivot

#### Escenario: Timeline compression
**Response:**
1. Feature prioritization ruthless
2. MVP scope reduction
3. Quality gates relaxation (temporary)
4. Extended work hours (temporary)

---

**Plan de gestión elaborado por:** Project Manager - Carlos Cauich  
**Aprobado por:** Equipo CHRONOS completo  
**Fecha:** 29 de Septiembre de 2025  
**Próxima revisión:** 13 de Octubre de 2025 (Primera entrega)

---

*Gestión estructurada para asegurar entrega exitosa y aprendizaje del equipo* 🎯✨