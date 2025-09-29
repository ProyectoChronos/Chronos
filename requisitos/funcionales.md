# ⚙️ Requisitos Funcionales

## RF-001: Gestión de Usuarios

### RF-001.1: Registro de Usuarios
**Descripción:** El sistema debe permitir el registro de nuevos usuarios  
**Prioridad:** Alta  
**Actor:** Usuario no registrado

**Criterios de Aceptación:**
- El usuario puede registrarse con email y contraseña
- El sistema valida formato de email y fortaleza de contraseña
- Se envía email de verificación al registrarse
- El usuario debe verificar su email para activar la cuenta

### RF-001.2: Autenticación
**Descripción:** El sistema debe permitir el login y logout de usuarios  
**Prioridad:** Alta  
**Actor:** Usuario registrado

**Criterios de Aceptación:**
- Login con email/username y contraseña
- Opción "Recordarme" para sesiones persistentes
- Logout seguro que invalida la sesión
- Recuperación de contraseña por email

### RF-001.3: Gestión de Perfil
**Descripción:** Los usuarios pueden gestionar su información personal  
**Prioridad:** Media  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Editar nombre, foto de perfil y preferencias
- Cambiar contraseña
- Configurar zona horaria y idioma
- Eliminar cuenta permanentemente

## RF-002: Gestión de Tareas

### RF-002.1: Crear Tareas
**Descripción:** Los usuarios pueden crear nuevas tareas  
**Prioridad:** Alta  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Crear tarea con título (obligatorio) y descripción (opcional)
- Asignar fecha límite, prioridad (1-5) y categoría
- Agregar etiquetas personalizadas
- Crear subtareas dentro de una tarea principal

### RF-002.2: Gestionar Tareas
**Descripción:** Los usuarios pueden editar, completar y eliminar tareas  
**Prioridad:** Alta  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Editar todos los campos de una tarea existente
- Marcar tareas como completadas o pendientes
- Eliminar tareas individuales o en lote
- Mover tareas entre categorías

### RF-002.3: Organizar Tareas
**Descripción:** Los usuarios pueden organizar sus tareas de diferentes maneras  
**Prioridad:** Alta  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Filtrar tareas por estado, prioridad, categoría, fecha
- Ordenar tareas por diferentes criterios
- Buscar tareas por título, descripción o etiquetas
- Agrupar tareas por proyectos o categorías

### RF-002.4: Subtareas
**Descripción:** Los usuarios pueden crear y gestionar subtareas  
**Prioridad:** Media  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Crear múltiples subtareas dentro de una tarea
- Marcar subtareas como completadas independientemente
- Ver progreso de tarea principal basado en subtareas
- Eliminar o editar subtareas individualmente

## RF-003: Sistema de Gamificación

### RF-003.1: Sistema de Puntos
**Descripción:** Los usuarios ganan puntos por completar actividades  
**Prioridad:** Alta  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Otorgar puntos base por completar tareas (10 puntos)
- Puntos adicionales por tareas de alta prioridad (25 puntos)
- Bonus por completar tareas antes de tiempo (+50% puntos)
- Puntos por mantener rachas diarias de actividad

### RF-003.2: Niveles y Progreso
**Descripción:** El sistema debe mostrar niveles basados en puntos acumulados  
**Prioridad:** Alta  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Calcular nivel basado en puntos totales
- Mostrar progreso hacia siguiente nivel
- Desbloquear características por alcanzar niveles
- Mostrar historial de niveles alcanzados

### RF-003.3: Logros y Insignias
**Descripción:** Los usuarios pueden desbloquear logros específicos  
**Prioridad:** Media  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Definir logros por diferentes acciones (primera tarea, racha semanal, etc.)
- Notificar cuando se desbloquea un logro
- Mostrar colección de logros en perfil
- Compartir logros alcanzados

### RF-003.4: Rachas y Consistencia
**Descripción:** El sistema debe trackear rachas de actividad diaria  
**Prioridad:** Media  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Contar días consecutivos con actividad
- Mostrar racha actual y récord personal
- Resetear racha si no hay actividad por un día
- Bonus de puntos por mantener rachas largas

## RF-004: Herramientas de Bienestar

### RF-004.1: Check-in de Estado de Ánimo
**Descripción:** Los usuarios pueden registrar su estado de ánimo diariamente  
**Prioridad:** Media  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Escala de 1-5 para registrar estado de ánimo
- Opción de agregar notas sobre el estado
- Un check-in por día máximo
- Historial de estados de ánimo

### RF-004.2: Temporizador Pomodoro
**Descripción:** Temporizador integrado para sesiones de enfoque  
**Prioridad:** Media  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Timer configurable (por defecto 25 minutos trabajo, 5 descanso)
- Notificaciones sonoras al completar sesiones
- Contador de sesiones Pomodoro por día
- Estadísticas de tiempo de enfoque

### RF-004.3: Recordatorios de Bienestar
**Descripción:** El sistema envía recordatorios relacionados con bienestar  
**Prioridad:** Baja  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Recordatorio de hidratación cada 2 horas
- Recordatorio de descanso visual cada 20 minutos
- Recordatorio de movimiento cada hora sentada
- Configuración personalizable de recordatorios

## RF-005: Sistema de Notificaciones

### RF-005.1: Notificaciones de Tareas
**Descripción:** Los usuarios reciben recordatorios sobre sus tareas  
**Prioridad:** Alta  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Notificación de tareas que vencen hoy
- Recordatorio de tareas vencidas
- Notificación personalizable antes de fecha límite
- Opción de posponer notificaciones

### RF-005.2: Notificaciones de Gamificación
**Descripción:** Notificaciones sobre logros y progreso gamificado  
**Prioridad:** Media  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Notificación al desbloquear logros
- Alerta al subir de nivel
- Recordatorio de racha en peligro
- Celebración de hitos importantes

### RF-005.3: Configuración de Notificaciones
**Descripción:** Los usuarios pueden personalizar sus notificaciones  
**Prioridad:** Media  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Habilitar/deshabilitar tipos específicos de notificaciones
- Configurar horarios de notificaciones (modo no molestar)
- Elegir métodos de notificación (push, email)
- Configurar frecuencia de recordatorios

## RF-006: Calendario Integrado

### RF-006.1: Vista de Calendario
**Descripción:** Los usuarios pueden ver sus tareas en formato calendario  
**Prioridad:** Media  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Vista mensual, semanal y diaria del calendario
- Mostrar tareas según fecha límite
- Indicadores visuales de carga de trabajo por día
- Navegación entre períodos de tiempo

### RF-006.2: Gestión desde Calendario
**Descripción:** Los usuarios pueden gestionar tareas desde la vista calendario  
**Prioridad:** Media  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Crear nuevas tareas directamente en el calendario
- Arrastrar y soltar tareas para cambiar fechas
- Ver detalles de tarea al hacer clic
- Marcar tareas como completadas desde calendario

## RF-007: Colaboración Básica

### RF-007.1: Espacios de Trabajo Compartidos
**Descripción:** Los usuarios pueden crear espacios colaborativos  
**Prioridad:** Baja  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Crear espacios de trabajo con nombre y descripción
- Invitar otros usuarios por email
- Roles básicos: administrador y miembro
- Ver actividad del espacio de trabajo

### RF-007.2: Tareas Compartidas
**Descripción:** Los usuarios pueden asignar tareas a otros miembros  
**Prioridad:** Baja  
**Actor:** Miembro de espacio de trabajo

**Criterios de Aceptación:**
- Asignar tareas a miembros específicos del espacio
- Ver tareas asignadas por otros
- Notificaciones de asignaciones
- Comentarios básicos en tareas compartidas

## RF-008: Reportes y Estadísticas

### RF-008.1: Dashboard Personal
**Descripción:** Los usuarios ven un resumen de su actividad y progreso  
**Prioridad:** Media  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Resumen de tareas completadas hoy/semana/mes
- Gráfico de progreso de puntos y niveles
- Estado de racha actual
- Próximas tareas importantes

### RF-008.2: Estadísticas de Productividad
**Descripción:** Los usuarios pueden ver análisis de su productividad  
**Prioridad:** Baja  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Gráficos de tareas completadas por período
- Análisis de patrones de productividad por día/hora
- Estadísticas de tiempo de enfoque (Pomodoro)
- Correlación entre estado de ánimo y productividad

## RF-009: Configuración y Personalización

### RF-009.1: Preferencias de Usuario
**Descripción:** Los usuarios pueden personalizar la aplicación  
**Prioridad:** Media  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Cambiar tema visual (claro/oscuro)
- Configurar idioma de la interfaz
- Establecer zona horaria
- Personalizar sonidos de notificación

### RF-009.2: Gestión de Categorías
**Descripción:** Los usuarios pueden crear y gestionar categorías personalizadas  
**Prioridad:** Media  
**Actor:** Usuario autenticado

**Criterios de Aceptación:**
- Crear categorías con nombre y color personalizado
- Editar y eliminar categorías existentes
- Asignar iconos a categorías
- Reorganizar orden de categorías

---

**Total de Requisitos Funcionales:** 24 requisitos principales  
**Distribución por Prioridad:**
- Alta: 10 requisitos (42%)
- Media: 11 requisitos (46%)
- Baja: 3 requisitos (12%)

---

*Requisitos funcionales diseñados para crear una experiencia completa de productividad y bienestar* ⚙️✨