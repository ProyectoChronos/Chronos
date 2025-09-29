# 📊 Métrica de Contribución Individual

## Marco de Evaluación Individual

Para asegurar equidad y transparencia en la evaluación de contribuciones individuales, hemos establecido un sistema de métricas multidimensional que valora diferentes tipos de contribución al proyecto CHRONOS.

---

## Dimensiones de Contribución

### 💻 Contribución Técnica (40% del total)

#### Desarrollo de Código (25%)
**Métricas:**
- Líneas de código contribuidas (ajustado por calidad)
- Pull requests creados y mergeados
- Commits realizados (weighted por impacto)
- Features implementadas completamente

**Recolección:**
- GitHub insights automáticos
- Code review feedback scores
- Feature completion tracking

**Ejemplo de scoring:**
```
Commits (peso 30%): 15 commits = 15 puntos
PRs (peso 40%): 8 PRs mergeados = 32 puntos
Features (peso 30%): 3 features completas = 30 puntos
Total: 77/100 puntos en desarrollo
```

#### Code Reviews y Calidad (15%)
**Métricas:**
- Reviews realizados a otros miembros
- Calidad de feedback en reviews
- Bugs encontrados en código propio vs ajeno
- Adherencia a estándares de código

**Herramientas:**
- GitHub review tracking
- Linting reports
- Bug tracking por autor

### 📚 Contribución Documental (25% del total)

#### Documentación Técnica (15%)
**Métricas:**
- Documentos creados o actualizados
- Calidad de comentarios en código
- Contribución a wikis y READMEs
- Diagramas técnicos creados

#### Documentación de Usuario (10%)
**Métricas:**
- Manuales de usuario escritos
- Tutoriales o guías creadas
- Actualizaciones de documentación
- Screenshots y videos explicativos

### 🏃‍♂️ Contribución de Proceso (20% del total)

#### Liderazgo en Roles (10%)
**Métricas:**
- Desempeño en roles rotativos (Product Owner, Scrum Master, etc.)
- Facilitación de ceremonias de Scrum
- Resolución de impedimentos
- Toma de decisiones efectivas

**Evaluación:**
- Peer evaluation de desempeño en rol
- Métricas específicas del rol (velocity para PO, impedimentos resueltos para SM)
- 360-degree feedback del equipo

#### Participación y Colaboración (10%)
**Métricas:**
- Asistencia a ceremonias de Scrum
- Participación activa en discusiones
- Ayuda proporcionada a compañeros
- Iniciativa en resolución de problemas

### 🎯 Contribución de Calidad (15% del total)

#### Testing y QA (10%)
**Métricas:**
- Tests unitarios escritos
- Test coverage mejoras
- Bugs encontrados y reportados
- Casos de prueba documentados

#### Innovation y Problem Solving (5%)
**Métricas:**
- Soluciones creativas implementadas
- Mejoras de proceso sugeridas
- Investigación técnica realizada
- Knowledge sharing con el equipo

---

## Sistema de Puntuación

### 🎯 Escala de Evaluación

#### Por Dimensión: 0-100 puntos
- **90-100:** Excepcional, excede expectativas significativamente
- **80-89:** Sobresaliente, excede expectativas
- **70-79:** Satisfactorio, cumple expectativas completamente  
- **60-69:** Necesita mejora, cumple parcialmente
- **0-59:** Insatisfactorio, no cumple expectativas básicas

#### Puntuación Final Weighted:
```
Score Final = (Técnica × 0.40) + (Documental × 0.25) + 
              (Proceso × 0.20) + (Calidad × 0.15)
```

### 📊 Matriz de Evaluación Individual

| Miembro | Técnica (40%) | Documental (25%) | Proceso (20%) | Calidad (15%) | **Total** |
|---------|---------------|------------------|---------------|---------------|-----------|
| Carlos  | 85 × 0.40 = 34| 78 × 0.25 = 19.5| 82 × 0.20 = 16.4| 88 × 0.15 = 13.2| **83.1** |
| Ana     | 82 × 0.40 = 32.8| 85 × 0.25 = 21.25| 90 × 0.20 = 18| 80 × 0.15 = 12| **84.05** |
| Guillermo| 88 × 0.40 = 35.2| 80 × 0.25 = 20| 78 × 0.20 = 15.6| 85 × 0.15 = 12.75| **83.55** |
| Valeria | 80 × 0.40 = 32| 90 × 0.25 = 22.5| 85 × 0.20 = 17| 82 × 0.15 = 12.3| **83.8** |
| Edrick  | 87 × 0.40 = 34.8| 75 × 0.25 = 18.75| 80 × 0.20 = 16| 90 × 0.15 = 13.5| **83.05** |

---

## Herramientas de Tracking

### 🤖 Métricas Automatizadas

#### GitHub Analytics:
```yaml
métricas_automáticas:
  commits:
    - total_commits
    - commits_por_semana
    - lineas_agregadas_eliminadas
  pull_requests:
    - prs_creados
    - prs_mergeados
    - prs_revisados
  code_review:
    - reviews_realizados
    - tiempo_promedio_review
    - comentarios_por_review
```

#### Herramientas de Tracking:
- **GitHub Insights:** Contribuciones de código automáticas
- **Discord Bot:** Tracking de participación en meetings
- **Google Sheets:** Manual scoring para aspectos cualitativos
- **Time Tracking:** Opcional, para entender effort distribution

### 📝 Evaluación Manual

#### Weekly Self-Assessment:
Cada miembro completa semanalmente:
```markdown
## Weekly Contribution Report - Semana [X]

### Trabajo Técnico:
- Features/bugs completados: [lista]
- Horas dedicadas: [número]
- Challenges enfrentados: [descripción]

### Colaboración:
- Reviews realizados: [número]
- Ayuda proporcionada: [descripción]
- Ceremonias atendidas: [lista]

### Learning & Growth:
- Nuevas tecnologías aprendidas: [lista]
- Áreas de mejora identificadas: [lista]
- Contribuciones no-técnicas: [descripción]
```

#### Peer Evaluation (Cada 2 sprints):
Evaluación anónima entre compañeros:
```markdown
## Peer Evaluation - [Miembro Evaluado]

### Colaboración (1-5):
- Disponibilidad para ayudar: [ ]
- Calidad de comunicación: [ ]
- Constructividad en discussions: [ ]

### Contribución Técnica (1-5):
- Calidad de código: [ ]
- Cumplimiento de deadlines: [ ]
- Problem-solving skills: [ ]

### Liderazgo (1-5):
- Iniciativa: [ ]
- Responsabilidad en roles: [ ]
- Influencia positiva: [ ]

### Comentarios adicionales:
[Texto libre para feedback constructivo]
```

---

## Reporte de Contribuciones

### 📊 Dashboard Individual

Cada miembro tiene acceso a su dashboard personal:

#### Métricas en Tiempo Real:
- Contribution score actual
- Ranking dentro del equipo (opcional/privado)
- Trends de contribución semanal
- Gaps identificados vs expectativas

#### Goals and OKRs Personales:
```markdown
## Objetivos Individuales - Q4 2025

### Objetivo 1: Expertise Técnico
- KR1: Completar 15 features end-to-end
- KR2: Mantener >85% code quality score
- KR3: Liderar implementación de 1 módulo completo

### Objetivo 2: Team Leadership
- KR1: Desempeñar 2 roles rotativos exitosamente
- KR2: Facilitar 5 ceremonies efectivamente
- KR3: Mentor a compañeros en 10+ sessions

### Objetivo 3: Innovation
- KR1: Proponer 3 mejoras de proceso adoptadas
- KR2: Research y presentar 2 nuevas tecnologías
- KR3: Contribuir con 1 innovation significativa
```

### 📈 Reportes de Sprint

#### Individual Sprint Report:
```markdown
## Sprint [X] - Individual Contribution Report

**Member:** [Nombre]
**Role during Sprint:** [Product Owner/Scrum Master/Developer]

### Quantitative Metrics:
- Story Points completed: X/Y committed
- Code contributions: X commits, Y PRs
- Reviews performed: X reviews
- Bugs fixed: X bugs
- Documentation updated: X documents

### Qualitative Assessment:
- **Key Achievements:** [3-5 bullets]
- **Challenges Overcome:** [2-3 bullets]  
- **Learning Highlights:** [2-3 bullets]
- **Next Sprint Focus:** [3 priorities]

### Peer Feedback Summary:
- **Strengths highlighted:** [themes]
- **Growth areas:** [themes]
- **Impact on team:** [summary]

### Self-Reflection:
- **Satisfaction with contributions (1-5):** [ ]
- **Areas for improvement:** [list]
- **Support needed from team:** [requests]
```

---

## Balanceamiento de Contribuciones

### ⚖️ Equity Monitoring

#### Contribution Balance Tracking:
Monitoreo semanal para asegurar distribución equitativa:

```yaml
balance_check:
  code_contribution:
    target: 20% ± 5% por miembro
    alert_threshold: >30% o <10% por 2 sprints
  
  documentation:
    target: 20% ± 7% por miembro
    rotation: emphasis en diferentes miembros por sprint
  
  leadership_roles:
    target: Equal rotation cada 2 sprints
    tracking: effectiveness score per role
```

#### Rebalancing Actions:
Cuando se detecta desbalance significativo:

1. **Analysis:** Identificar causas (skill gaps, availability, interest)
2. **Discussion:** Team retrospective sobre distribution
3. **Action Plan:** Specific actions para siguiente sprint
4. **Support:** Mentoring, pair programming, training
5. **Monitoring:** Track improvement en próximos sprints

### 🎯 Individual Development Plans

Cada miembro tiene un plan de desarrollo personalizado:

#### Skills Matrix:
| Skill | Current Level | Target Level | Development Plan |
|-------|---------------|--------------|------------------|
| Frontend (React) | 3/5 | 4/5 | Lead 2 UI features, pair program with expert |
| Backend (Node.js) | 2/5 | 4/5 | Complete online course, implement 3 APIs |
| Testing | 2/5 | 3/5 | Write tests for all own features, QA rotation |
| Documentation | 4/5 | 4/5 | Maintain current level, help others |
| Leadership | 3/5 | 4/5 | Take Scrum Master role, facilitate meetings |

---

## Reconocimiento y Motivación

### 🏆 Achievement System

#### Weekly Recognitions:
- **Code Quality Champion:** Best code review scores
- **Documentation Hero:** Most helpful documentation  
- **Team Player:** Most collaborative team member
- **Innovation Award:** Creative solution or process improvement

#### Sprint Awards:
- **MVP of Sprint:** Highest overall contribution score
- **Blocker Buster:** Most impediments resolved
- **Mentor of Sprint:** Most peer helping activity
- **Learning Champion:** Most new skills acquired/shared

#### Project Milestones:
- **Architect Award:** Best technical design contribution
- **UX Hero:** Best user experience innovation
- **Quality Guardian:** Best testing and QA contribution
- **Process Improver:** Best methodology enhancement

### 📜 Contribution Certificates

Al final del proyecto, cada miembro recibe:
- **Individual Contribution Report:** Comprehensive summary
- **Skill Development Certificate:** New competencies acquired
- **Team Leadership Certificate:** Roles successfully performed
- **Project Impact Statement:** Specific contributions to CHRONOS

---

## Escalación y Resolución de Conflictos

### ⚠️ Performance Issues

#### Early Warning System:
- 2 semanas consecutivas con score <70 → Check-in individual
- 3 semanas con contribución desbalanceada → Team discussion
- 4+ semanas con issues → Escalation a profesora

#### Intervention Process:

##### Nivel 1: Peer Support
- Pair programming sessions
- Mentoring por compañeros
- Skill sharing workshops
- Workload redistribution

##### Nivel 2: Team Intervention  
- Team retrospective focused on support
- Role adjustment (mejor fit para skills)
- Timeline adjustment si necesario
- Clear expectations setting

##### Nivel 3: Escalation
- Individual meeting con profesora
- Academic support resources
- Potential project scope adjustment
- Alternative contribution paths

### 🤝 Conflict Resolution

#### Process para Disputes sobre Contributions:
1. **Direct Discussion:** Miembros involucrados discuten directly
2. **Mediation:** Scrum Master facilita discussion
3. **Team Review:** Todo el equipo evalúa la situación
4. **Documentation Review:** Evidence-based analysis
5. **External Mediation:** Profesora como arbitrator final

---

## Reporting y Transparencia

### 📊 Monthly Contribution Report

**Para:** Profesora y stakeholders académicos

```markdown
## Monthly Team Contribution Report - [Mes]

### Overall Team Performance:
- Average contribution score: X/100
- Score distribution: [histogram/chart]
- Improvement trends: [analysis]

### Individual Highlights:
**[Nombre]:** [Key achievements y contributions]
**[Nombre]:** [Key achievements y contributions]
[... para cada miembro]

### Team Dynamics:
- Collaboration score: X/5
- Knowledge sharing instances: X
- Peer support activities: X
- Leadership rotation effectiveness: X/5

### Areas of Excellence:
[Top 3 areas donde el team excelled]

### Growth Opportunities:
[Top 3 areas for improvement identified]

### Intervention Actions Taken:
[Any support/rebalancing measures implemented]
```

### 🔍 Transparency Measures

- **Public Contribution Board:** GitHub project con contributions visibles
- **Team Metrics Dashboard:** Shared Google Sheet con scores
- **Regular Calibration:** Team discussions sobre scoring fairness
- **Appeal Process:** Mechanism para challenge evaluaciones

---

**Sistema de métricas diseñado por:** Ana Lavadores (QA Lead)  
**Aprobado por:** Equipo CHRONOS completo  
**Fecha de implementación:** 29 de Septiembre de 2025  
**Primera evaluación:** 13 de Octubre de 2025  
**Revisión del sistema:** Después del Sprint 3

---

*Métricas diseñadas para promover contribución equitativa, crecimiento individual y éxito del equipo* 📊✨