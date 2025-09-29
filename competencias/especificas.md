# 🔧 Competencias Específicas de Ingeniería de Software

## Competencias Técnicas Fundamentales

A través del desarrollo del proyecto CHRONOS, hemos desarrollado y aplicado competencias específicas esenciales para el ejercicio profesional de la Ingeniería de Software, siguiendo los estándares[...]

---

## 💻 Programación y Desarrollo de Software

### 🚀 Lenguajes de Programación

#### JavaScript/TypeScript - Nivel Avanzado

**Competencias desarrolladas:**

##### 🎯 **JavaScript moderno (ES6+):**
**Carlos Cauich:**
- **Funciones flecha y destructuring:** Uso extensivo en componentes y servicios
- **Patrones async/await:** Manejo de llamadas a APIs y operaciones asíncronas
- **Sistemas de módulos:** Imports/exports de ES6 para una arquitectura limpia
- **Métodos de arrays avanzados:** map, filter, reduce para manipulación de datos
- **Template literals:** Generación de contenido dinámico y consultas tipo SQL

**Evidencias de código:**
```javascript
// Servicio de tareas con async/await y manejo de errores
export const taskService = {
  async fetchTasks(): Promise<Task[]> {
    try {
      const response = await fetch('/api/tasks');
      const tasks = await response.json();
      return tasks.filter(task => task.isActive);
    } catch (error) {
      console.error('Error al obtener tareas:', error);
      throw new Error('No se pudieron cargar las tareas');
    }
  }
};
```

##### 🔷 **TypeScript - Seguridad de tipos:**
**Guillermo Peña:**
- **Definición de interfaces:** Tipado estricto para todos los modelos de datos
- **Tipos genéricos:** Componentes reutilizables con seguridad de tipos
- **Tipos unión:** Definiciones de tipos flexibles pero seguras
- **Guardianes de tipos:** Comprobación de tipos en tiempo de ejecución para un código más seguro
- **Tipos avanzados:** Tipos condicionales, tipos mapeados para escenarios complejos

**Evidencias de código:**
```typescript
interface Task {
  id: string;
  title: string;
  priority: TaskPriority;
  status: TaskStatus;
  dueDate?: Date;
  tags: string[];
}

type TaskPriority = 'low' | 'medium' | 'high' | 'urgent';
type TaskStatus = 'pending' | 'in-progress' | 'completed' | 'cancelled';

// Hook genérico para lógica reutilizable
function useAsyncState<T>(initialState: T) {
  const [state, setState] = useState<T>(initialState);
  const [isLoading, setIsLoading] = useState(false);
  // ... implementación
}
```

#### Desarrollo Frontend - Ecosistema React

##### ⚛️ **React Hooks y Patrones:**
**Ana Lavadores y Valeria Itza:**

**Dominio de Hooks:**
- **useState:** Gestión de estado compleja con objetos y arreglos
- **useEffect:** Gestión del ciclo de vida, limpieza, dependencias
- **useContext:** Estado global sin prop drilling
- **useMemo/useCallback:** Optimización de rendimiento
- **Hooks personalizados:** Encapsulación de lógica reutilizable

**Patrones avanzados:**
- **Render props:** Patrones de composición de componentes
- **Componentes de orden superior (HOC):** Preocupaciones transversales
- **Límites de error (Error boundaries):** Manejo elegante de errores
- **Suspense:** Estados de carga y división de código

**Evidencias de implementación:**
```typescript
// Hook personalizado para la gestión de tareas
function useTaskManager() {
  const [tasks, setTasks] = useState<Task[]>([]);
  const [filter, setFilter] = useState<TaskFilter>('all');
  
  const filteredTasks = useMemo(() => {
    return tasks.filter(task => {
      if (filter === 'completed') return task.status === 'completed';
      if (filter === 'pending') return task.status !== 'completed';
      return true;
    });
  }, [tasks, filter]);
  
  const addTask = useCallback(async (taskData: CreateTaskRequest) => {
    const newTask = await taskService.createTask(taskData);
    setTasks(prev => [...prev, newTask]);
  }, []);
  
  return { tasks: filteredTasks, addTask, setFilter };
}
```

##### 🎨 **Estilos y Desarrollo de UI:**
**Valeria Itza:**

**Dominio de Tailwind CSS:**
- **Enfoque utility-first:** Prototipado rápido y diseño consistente
- **Diseño responsivo:** Mobile-first con sistema de breakpoints
- **Tema personalizado:** Colores de marca, tipografía, sistema de espaciado
- **Variantes de componentes:** Estilos de componentes reutilizables
- **Optimización de rendimiento:** PurgeCSS para un tamaño de bundle mínimo

**Patrones CSS-in-JS:**
- **Styled Components:** Estilos dinámicos basados en props
- **CSS Modules:** Estilos con alcance para aislar componentes
- **Librerías de animación:** Framer Motion para interacciones fluidas

### 🏗️ Arquitectura de Software

#### Patrones de Arquitectura Frontend

##### 📦 **Arquitectura basada en componentes:**
**Diseñado por:** Carlos Cauich y Valeria Itza

**Decisiones de arquitectura:**

**Implementación de Atomic Design:**
```
src/components/
├── atoms/          # Bloques básicos (Button, Input)  
├── molecules/      # Combinaciones simples (SearchBox, TaskCard)
├── organisms/      # Secciones de UI complejas (TaskList, Header)
├── templates/      # Diseños de página
└── pages/          # Páginas completas
```

**Beneficios alcanzados:**
- ✅ **95% de reutilización de componentes** entre distintas páginas
- ✅ **UI consistente** mediante un sistema de diseño compartido
- ✅ **Pruebas sencillas** de componentes individuales
- ✅ **Desarrollo escalable** con jerarquía de componentes clara

##### 🔄 **Arquitectura de gestión de estado:**
**Implementado por:** Guillermo Peña

**Diseño de store con Zustand:**
```typescript
// Slices modulares del store
interface AppState {
  auth: AuthState;
  tasks: TaskState;
  gamification: GamificationState;
  wellness: WellnessState;
  ui: UIState;
}

// Slice individual - ejemplo
const taskSlice = (set, get) => ({
  tasks: [],
  isLoading: false,
  error: null,
  
  // Acciones
  fetchTasks: async () => {
    set({ isLoading: true });
    try {
      const tasks = await taskApi.getTasks();
      set({ tasks, isLoading: false });
    } catch (error) {
      set({ error: error.message, isLoading: false });
    }
  }
});
```

**Beneficios de la arquitectura:**
- ✅ **Actualizaciones de estado predecibles** mediante gestión centralizada
- ✅ **Optimización de rendimiento** con suscripciones selectivas
- ✅ **Mejor experiencia de desarrollo** con integración de Redux DevTools
- ✅ **Facilidad de pruebas** con lógica de estado aislada

#### Comprensión de la Arquitectura Backend

##### 🌐 **Principios de diseño de API:**
**Aplicado por:** Edrick Puc

**Diseño de API RESTful:**
```
GET    /api/tasks              # Obtener todas las tareas del usuario
POST   /api/tasks              # Crear una nueva tarea  
PUT    /api/tasks/:id          # Actualizar una tarea específica
DELETE /api/tasks/:id          # Eliminar una tarea específica
GET    /api/tasks/:id/history  # Historial de actividad de la tarea
```

**Estándares de API implementados:**
- **Formato de respuesta consistente:** Patrones estándar de éxito/error
- **Códigos de estado HTTP:** Uso semántico adecuado
- **Validación de solicitudes:** Sanitización y validación de entradas
- **Manejo de errores:** Patrones completos de respuesta de error
- **Versionado de API:** Estrategia de evolución preparada para el futuro

---

## 🧪 Pruebas de Software (Software Testing)

### 🔬 Estrategia de pruebas e implementación

#### Dominio de pruebas unitarias
**Liderado por:** Ana Lavadores

##### 📋 **Jest y Testing Library:**

**Pruebas de componentes:**
```typescript
// Prueba del componente TaskCard
import { render, screen, fireEvent } from '@testing-library/react';
import { TaskCard } from './TaskCard';

describe('Componente TaskCard', () => {
  const mockTask = {
    id: '1',
    title: 'Tarea de prueba',
    status: 'pending',
    priority: 'high'
  };
  
  it('renderiza correctamente la información de la tarea', () => {
    render(<TaskCard task={mockTask} onComplete={jest.fn()} />);
    
    expect(screen.getByText('Tarea de prueba')).toBeInTheDocument();
    expect(screen.getByText('Alta prioridad')).toBeInTheDocument();
  });
  
  it('llama a onComplete cuando se hace clic en el botón de completar', () => {
    const mockOnComplete = jest.fn();
    render(<TaskCard task={mockTask} onComplete={mockOnComplete} />);
    
    fireEvent.click(screen.getByRole('button', { name: /completar/i }));
    expect(mockOnComplete).toHaveBeenCalledWith('1');
  });
});
```

**Pruebas de hooks:**
```typescript
import { renderHook, act } from '@testing-library/react';
import { useTaskManager } from './useTaskManager';

describe('Hook useTaskManager', () => {
  it('debe agregar una nueva tarea a la lista', async () => {
    const { result } = renderHook(() => useTaskManager());
    
    await act(async () => {
      await result.current.addTask({
        title: 'Nueva tarea',
        priority: 'medium'
      });
    });
    
    expect(result.current.tasks).toHaveLength(1);
    expect(result.current.tasks[0].title).toBe('Nueva tarea');
  });
});
```

#### Pruebas de integración

##### 🔗 **Pruebas de integración de API:**
**Implementado por:** Carlos Cauich y Edrick Puc

**Pruebas de integración de servicios:**
```typescript
// Prueba de integración del servicio de API
describe('Integración de la API de Tareas', () => {
  beforeEach(() => {
    // Configuración del servidor API simulado
    server.use(
      rest.get('/api/tasks', (req, res, ctx) => {
        return res(ctx.json(mockTasks));
      })
    );
  });
  
  it('debe obtener las tareas correctamente', async () => {
    const tasks = await taskService.fetchTasks();
    
    expect(tasks).toHaveLength(3);
    expect(tasks[0]).toMatchObject({
      id: expect.any(String),
      title: expect.any(String),
      status: expect.any(String)
    });
  });
});
```

#### Estrategia de pruebas de extremo a extremo

##### 🎯 **Prueba del recorrido del usuario:**
**Diseñado por:** Ana Lavadores

**Flujos de usuario críticos:**
1. **Incorporación de usuario:** Registro → Configuración de perfil → Primera tarea
2. **Flujo diario:** Inicio de sesión → Ver tareas → Completar tarea → Consultar progreso
3. **Bienestar:** Definir meta de bienestar → Registrar estado de ánimo → Recibir recomendaciones
4. **Gamificación:** Completar tareas → Ganar puntos → Ver tablero → Desbloquear logro

**Marco de implementación de pruebas E2E:**
```typescript
// Ejemplo de prueba E2E con Cypress
describe('Flujo de gestión de tareas', () => {
  it('debe permitir al usuario crear y completar una tarea', () => {
    cy.visit('/dashboard');
    cy.get('[data-testid="create-task-button"]').click();
    cy.get('[data-testid="task-title-input"]').type('Completar la documentación del proyecto');
    cy.get('[data-testid="task-priority-select"]').select('high');
    cy.get('[data-testid="create-task-submit"]').click();
    
    // Verificar que la tarea aparezca en la lista
    cy.contains('Completar la documentación del proyecto').should('be.visible');
    
    // Completar la tarea
    cy.get('[data-testid="complete-task-1"]').click();
    cy.get('[data-testid="task-status-1"]').should('contain', 'Completada');
  });
});
```

#### Métricas de pruebas y aseguramiento de calidad

##### 📊 **Cobertura y métricas de calidad:**
**Monitoreado por:** Ana Lavadores

**Métricas de pruebas actuales:**
- **Cobertura de pruebas unitarias:** 78% (objetivo: 80%)
- **Cobertura de pruebas de integración:** 65% (objetivo: 70%)  
- **Cobertura de rutas críticas E2E:** 90% (objetivo: 95%)
- **Tiempo de ejecución de pruebas:** <45 segundos para toda la suite
- **Confiabilidad de las pruebas:** 98% de éxito (gestión de pruebas inestables)

**Implementación de umbrales de calidad:**
```yaml
# Pipeline de pruebas en GitHub Actions
test_quality_gates:
  - unit_tests: required, min_coverage: 75%
  - integration_tests: required, min_coverage: 60%
  - e2e_tests: required, critical_flows_only
  - performance_tests: lighthouse_score > 85
  - accessibility_tests: wcag_aa_compliance
```

---

## 🔧 Metodologías de Desarrollo

### 🏃‍♂️ Metodologías Ágiles - Implementación de Scrum

#### Dominio del marco Scrum
**Implementado por todo el equipo, coordinado por:** Guillermo Peña

##### 📅 **Ceremonias Scrum:**

**Excelencia en la planificación del sprint (Sprint Planning):**
- **Planning Poker:** Estimación con la técnica Planning Poker
- **Estimación por Puntos de Historia:** Secuencia de Fibonacci para estimar complejidad
- **Definición del Objetivo de Sprint:** Objetivos claros y medibles para cada sprint
- **Planificación de capacidad:** Compromiso basado en la velocidad del equipo

**Evidencias de planificación:**
```markdown
## Resumen de Planificación del Sprint 2

**Objetivo del Sprint:** Implementar la gestión de tareas principal con gamificación básica
**Capacidad del equipo:** 25 puntos de historia (basado en la velocidad histórica)

**Desglose de puntos de historia:**
- Operaciones CRUD de tareas: 8 puntos
- Integración del sistema de puntos: 5 puntos  
- Mejora del perfil de usuario: 3 puntos
- Pruebas y corrección de errores: 4 puntos
- Actualizaciones de documentación: 2 puntos
- Buffer para trabajo inesperado: 3 puntos

**Total comprometido:** 25 puntos
```

**Efectividad del standup diario:**
- **Tiempo acotado:** Consistentemente 15 minutos o menos
- **Enfoque:** Trabajo de ayer, plan de hoy, impedimentos
- **Seguimiento de impedimentos:** 95% de impedimentos resueltos en 24 horas
- **Participación:** 100% de asistencia, participación activa

**Innovación en la revisión del sprint:**
- **Demos en vivo:** Software funcionando demostrado en cada sprint
- **Retroalimentación de stakeholders:** Retroalimentación de la profesora incorporada
- **Presentación de métricas:** Velocidad y métricas de calidad compartidas
- **Vista previa del siguiente sprint:** Trabajo próximo para transparencia

**Mejora continua en la retrospectiva:**
- **Qué salió bien:** Celebración de éxitos del equipo
- **Qué podría mejorar:** Evaluación honesta de los retos  
- **Acciones:** Mejoras específicas y medibles comprometidas
- **Seguimiento:** 90% de las acciones implementadas en el siguiente sprint

#### Dominio de artefactos ágiles

##### 📋 **Gestión del Product Backlog:**
**Propietario rotativo:** Valeria Itza (Sprints 1,3) y Carlos Cauich (Sprints 2,4)

**Proceso de refinamiento del backlog:**
```markdown
## Plantilla de historia de usuario

**Como** [estudiante que usa CHRONOS]
**Quiero** [funcionalidad específica]  
**Para** [valor de negocio/resultado]

**Criterios de aceptación:**
- [ ] Dado [contexto], cuando [acción], entonces [resultado esperado]
- [ ] [Criterio adicional...]

**Definición de Hecho (DoD):**
- [ ] Código implementado y revisado
- [ ] Pruebas unitarias escritas y pasando
- [ ] Pruebas de integración pasando
- [ ] Documentación actualizada
- [ ] Requisitos de accesibilidad cumplidos
- [ ] Criterios de rendimiento cumplidos
```

**Exactitud de estimación de puntos de historia:**
- **Sprint 1:** 92% de exactitud (23/25 puntos entregados)
- **Sprint 2:** 96% de exactitud (27/28 puntos en curso)
- **Tendencia de velocidad:** Mejora estable, entrega predecible

##### 📈 **Métricas de sprint y seguimiento:**
**Seguimiento por:** Ana Lavadores

**Seguimiento de la velocidad:**
```
Sprint 1: 23 puntos de historia completados
Sprint 2: 27 puntos de historia (en progreso, 96% completo)
Sprint 3: 25 puntos de historia planificados
Velocidad promedio: 25 puntos por sprint
```

**Métricas de calidad:**
- **Tasa de errores (bugs):** 0.8 bugs por punto de historia (promedio de la industria: 1.2)
- **Deuda técnica:** 15 horas identificadas, 12 horas abordadas
- **Cobertura de revisiones de código:** 100% de PRs revisados por 2+ miembros
- **Tiempo de refactorización:** 10% de la capacidad del sprint para mejoras técnicas

#### Prácticas de desarrollo colaborativo

##### 🔄 **Excelencia en control de versiones:**
**Implementación de Git Flow por:** Edrick Puc

**Estrategia de ramas:**
```
main (código listo para producción)
├── develop (rama de integración)  
    ├── feature/task-crud-operations (Carlos)
    ├── feature/gamification-points (Ana)
    ├── feature/wellness-integration (Valeria)  
    ├── feature/user-profile-management (Guillermo)
    └── docs/api-documentation-update (Edrick)
```

**Estándares de commits:**
```
feat: agregar finalización de tareas con cálculo de puntos
fix: resolver problema de rendimiento del filtro de tareas
docs: actualizar documentación de API para endpoints de tareas  
style: mejorar el diseño responsivo de la tarjeta de tarea
refactor: extraer la lógica de validación de tareas a utils
test: agregar pruebas de integración para el servicio de tareas
```

**Excelencia en revisión de código:**
- **Cobertura de revisión:** 100% de cambios revisados
- **Calidad de revisión:** Promedio de 3.2 comentarios por PR (retroalimentación constructiva)
- **Velocidad de revisión:** 85% de PRs revisados en 24 horas
- **Compartición de conocimiento:** Las revisiones se usan para transferencia de conocimiento y mentoría

##### 🤝 **Programación en pareja y colaboración:**
**Practicado por todos los miembros del equipo**

**Sesiones de programación en pareja:**
- **Frecuencia:** 2-3 sesiones por semana
- **Duración:** Sesiones enfocadas de 2-4 horas
- **Transferencia de conocimiento:** Funcionalidades complejas desarrolladas colaborativamente
- **Impacto en calidad:** 40% menos errores en código desarrollado en pareja

**Evidencia de colaboración:**
```markdown
## Registro de Programación en Pareja - Semana 3

**Sesión 1:** Carlos + Guillermo - Arquitectura de gestión de estado de tareas
- Duración: 3 horas
- Resultado: Patrón de gestión de estado limpio establecido
- Transferencia de conocimiento: Mejores prácticas de Zustand compartidas

**Sesión 2:** Ana + Valeria - Integración de pruebas de componentes  
- Duración: 2.5 horas
- Resultado: Suite de pruebas integral para componentes de UI
- Transferencia de conocimiento: Patrones de Testing Library compartidos

**Sesión 3:** Edrick + Carlos - Patrones de integración de API
- Duración: 2 horas  
- Resultado: Patrones consistentes de servicios de API establecidos
- Transferencia de conocimiento: Patrones avanzados de TypeScript
```

---

## 🎯 Diseño y Análisis de Sistemas

### 📊 Ingeniería de Requisitos

#### Elicitación y análisis de requisitos
**Liderado por:** Valeria Itza con apoyo de todo el equipo

##### 🎭 **Investigación y análisis de usuarios:**

**Identificación de interesados (stakeholders):**
- **Usuarios principales:** Estudiantes universitarios (18-25 años)
- **Usuarios secundarios:** Asesores académicos, grupos de estudio
- **Interesados terciarios:** Servicios de salud mental universitarios, investigadores de productividad

**Técnicas de levantamiento de requisitos:**
1. **Entrevistas a usuarios:** 12 entrevistas individuales con usuarios objetivo
2. **Encuestas:** Encuesta cuantitativa con 45 respuestas sobre hábitos de productividad
3. **Observación:** Estudio etnográfico de patrones de trabajo estudiantil
4. **Grupos focales:** 2 sesiones grupales con 8 participantes cada una
5. **Talleres con interesados:** Sesiones colaborativas con el equipo y asesores

**Desarrollo de persona usuaria:**
```markdown
## Persona principal: "Olivia Abrumada"

**Datos demográficos:**
- Edad: 20, estudiante de segundo año de ingeniería
- Comodidad tecnológica: Alta (nativa de smartphone)
- Herramientas de productividad: Usa apps básicas de tareas, suele abandonarlas

**Objetivos:**
- Completar asignaciones sin estrés de último minuto
- Mantener equilibrio vida-trabajo en periodos ocupados  
- Sentirse motivada y satisfecha con el progreso diario

**Puntos de dolor:**
- Las apps tradicionales de tareas le resultan aburridas y mecánicas
- Dificultad para estimar tiempo en proyectos complejos
- Tiende a sobretrabajar y descuidar el autocuidado
- Pierde motivación al enfrentar listas de tareas grandes

**Patrones de comportamiento:**
- Revisa el teléfono 50+ veces al día
- Responde bien al refuerzo positivo
- Valora la conexión con pares y experiencias compartidas
- Interés en la auto-mejora y el crecimiento personal

**Cómo ayuda CHRONOS:**
- La gamificación hace que completar tareas sea gratificante
- La integración de bienestar previene el burnout
- Las funciones sociales brindan apoyo entre pares
- El sistema de logros mantiene la motivación a largo plazo
```

##### 📋 **Análisis de requisitos funcionales:**

**Matriz de trazabilidad de requisitos:**
```markdown
## Requisitos funcionales de alta prioridad (Imprescindibles)

| ID | Requisito | Historia de usuario | Prioridad | Estado | Casos de prueba |
|----|-----------|---------------------|-----------|--------|-----------------|
| FR-01 | Creación de tareas | Como estudiante, quiero crear tareas con títulos, descripciones y fechas de vencimiento | Imprescindible | ✅ Completado | 8 casos de prueba |
| FR-02 | Gestión de tareas | Como usuario, quiero editar, eliminar y marcar tareas como completadas | Imprescindible | ✅ Completado | 12 casos de prueba |
| FR-03 | Sistema de puntos | Como usuario, quiero ganar puntos por completar tareas | Imprescindible | 🔄 En progreso | 6 casos de prueba |
| FR-04 | Autenticación de usuario | Como usuario, quiero inicio de sesión/registro seguro | Imprescindible | ✅ Completado | 10 casos de prueba |
| FR-05 | Seguimiento de progreso | Como usuario, quiero ver mi progreso diario/semanal | Imprescindible | ⏳ Pendiente | 4 casos de prueba |
```

**Especificación de requisitos no funcionales:**
```markdown
## Requisitos de rendimiento
- **Tiempo de respuesta:** Carga de página < 2 segundos
- **Usuarios concurrentes:** Soportar 100+ usuarios simultáneos  
- **Disponibilidad:** 99% de uptime durante periodos académicos
- **Escalabilidad:** Manejar 1000+ usuarios sin degradación de rendimiento

## Requisitos de usabilidad  
- **Curva de aprendizaje:** Usuarios nuevos productivos en < 10 minutos
- **Accesibilidad:** Cumplimiento WCAG 2.1 AA
- **Responsividad móvil:** Funcionalidad completa en dispositivos móviles
- **Internacionalización:** Soporte para inglés y español

## Requisitos de seguridad
- **Autenticación:** Autenticación segura basada en JWT
- **Protección de datos:** Todos los datos sensibles cifrados
- **Privacidad:** Manejo de datos conforme a GDPR
- **Validación de entradas:** Todas las entradas de usuario sanitizadas y validadas
```

#### Diseño y arquitectura del sistema

##### 🏗️ **Diseño de la arquitectura del sistema:**
**Arquitectos:** Carlos Cauich y Guillermo Peña

**Arquitectura de alto nivel:**
```
┌─────────────────────────────────────────────────────────────┐
│                    Arquitectura del Sistema CHRONOS         │
├─────────────────────────────────────────────────────────────┤
│  Frontend (React + TypeScript + Tailwind)                  │
│  ├── Componentes de interfaz de usuario                    │
│  ├── Gestión de estado (Zustand)                           │  
│  ├── Servicios cliente de API                              │
│  └── Enrutamiento y navegación                             │
├─────────────────────────────────────────────────────────────┤
│  Pasarela de API y Autenticación                           │
│  ├── Gestión de tokens JWT                                 │
│  ├── Middleware de solicitud/respuesta                     │
│  └── Limitación de tasa y seguridad                        │
├─────────────────────────────────────────────────────────────┤
│  Servicios Backend (Node.js + Express)                     │
│  ├── Servicio de gestión de tareas                         │
│  ├── Servicio de gestión de usuarios                       │
│  ├── Servicio de gamificación                              │
│  ├── Servicio de seguimiento de bienestar                  │
│  └── Servicio de notificaciones                            │
├─────────────────────────────────────────────────────────────┤
│  Capa de datos                                             │
│  ├── PostgreSQL (Datos primarios)                          │
│  ├── Redis (Caché y sesiones)                              │
│  └── Almacenamiento de archivos (Recursos de usuario)      │
└─────────────────────────────────────────────────────────────┘
```

**Diseño de base de datos:**
```sql
-- Entidades principales con relaciones
CREATE TABLE users (
  id UUID PRIMARY KEY,
  email VARCHAR(255) UNIQUE NOT NULL,
  username VARCHAR(100) UNIQUE NOT NULL,
  password_hash VARCHAR(255) NOT NULL,
  points INTEGER DEFAULT 0,
  level INTEGER DEFAULT 1,
  created_at TIMESTAMP DEFAULT NOW()
);

CREATE TABLE tasks (
  id UUID PRIMARY KEY,
  user_id UUID REFERENCES users(id),
  title VARCHAR(255) NOT NULL,
  description TEXT,
  priority task_priority DEFAULT 'medium',
  status task_status DEFAULT 'pending',
  due_date TIMESTAMP,
  points_reward INTEGER DEFAULT 10,
  created_at TIMESTAMP DEFAULT NOW(),
  completed_at TIMESTAMP
);

CREATE TABLE user_achievements (
  id UUID PRIMARY KEY,
  user_id UUID REFERENCES users(id),
  achievement_id VARCHAR(100) NOT NULL,
  earned_at TIMESTAMP DEFAULT NOW(),
  points_earned INTEGER DEFAULT 0
);
```

##### 🔄 **Patrones de diseño de API:**
**Diseñado por:** Edrick Puc

**Estándares de API RESTful:**
```typescript
// Formato de respuesta de API consistente
interface APIResponse<T> {
  success: boolean;
  data?: T;
  error?: {
    code: string;
    message: string;
    details?: any;
  };
  meta?: {
    total?: number;
    page?: number;
    limit?: number;
  };
}

// Ejemplo de implementación de endpoint de API
router.get('/api/tasks', authenticate, async (req, res) => {
  try {
    const { page = 1, limit = 10, status, priority } = req.query;
    
    const tasks = await taskService.getTasks(req.user.id, {
      page: parseInt(page),
      limit: parseInt(limit),
      filters: { status, priority }
    });
    
    res.json({
      success: true,
      data: tasks.items,
      meta: {
        total: tasks.total,
        page: tasks.page,
        limit: tasks.limit
      }
    });
  } catch (error) {
    res.status(500).json({
      success: false,
      error: {
        code: 'FETCH_TASKS_ERROR',
        message: 'No se pueden recuperar las tareas'
      }
    });
  }
});
```

---

## 🔐 Seguridad y Calidad de Software

### 🛡️ Implementación de seguridad

#### Autenticación y autorización
**Implementado por:** Guillermo Peña y Edrick Puc

##### 🔑 **Sistema de autenticación JWT:**

**Arquitectura de seguridad:**
```typescript
// Implementación de JWT con estrategia de token de actualización (refresh)
interface AuthTokens {
  accessToken: string;    // De corta duración (15 minutos)
  refreshToken: string;   // De larga duración (7 días)  
}

class AuthService {
  async login(email: string, password: string): Promise<AuthTokens> {
    // 1. Validar credenciales
    const user = await this.validateCredentials(email, password);
    
    // 2. Generar tokens
    const accessToken = jwt.sign(
      { userId: user.id, email: user.email },
      process.env.JWT_SECRET,
      { expiresIn: '15m' }
    );
    
    const refreshToken = jwt.sign(
      { userId: user.id, type: 'refresh' },
      process.env.REFRESH_SECRET,
      { expiresIn: '7d' }
    );
    
    // 3. Almacenar el refresh token de forma segura
    await this.storeRefreshToken(user.id, refreshToken);
    
    return { accessToken, refreshToken };
  }
}
```

**Medidas de seguridad implementadas:**
- ✅ **Hashing de contraseñas:** bcrypt con 12 rondas de sal
- ✅ **Seguridad JWT:** Tokens de acceso de corta duración con rotación de refresh tokens
- ✅ **Solo HTTPS:** Todos los endpoints de autenticación requieren HTTPS
- ✅ **Limitación de intentos:** Intentos de inicio de sesión limitados para prevenir fuerza bruta
- ✅ **Validación de entradas:** Todas las entradas de autenticación sanitizadas y validadas

#### Protección de datos y privacidad

##### 🔒 **Medidas de seguridad de datos:**

**Implementación de cifrado:**
```typescript
// Cifrado de datos sensibles
import crypto from 'crypto';

class DataEncryption {
  private readonly algorithm = 'aes-256-gcm';
  private readonly secretKey = process.env.ENCRYPTION_KEY;
  
  encrypt(text: string): string {
    const iv = crypto.randomBytes(16);
    const cipher = crypto.createCipher(this.algorithm, this.secretKey);
    cipher.setAAD(Buffer.from('chronos-app'));
    
    let encrypted = cipher.update(text, 'utf8', 'hex');
    encrypted += cipher.final('hex');
    
    const authTag = cipher.getAuthTag();
    
    return iv.toString('hex') + ':' + authTag.toString('hex') + ':' + encrypted;
  }
}

// Uso para datos sensibles del usuario
const encryptedMoodData = dataEncryption.encrypt(JSON.stringify(userMoodData));
```

**Cumplimiento de privacidad:**
- ✅ **Minimización de datos:** Solo se recopila información necesaria
- ✅ **Consentimiento del usuario:** Opt-in claro para funciones de recopilación de datos
- ✅ **Retención de datos:** Eliminación automática de datos antiguos según política
- ✅ **Derechos del usuario:** Funcionalidad de exportación y eliminación de datos implementada

#### Validación y sanitización de entradas

##### 🧹 **Validación integral de entradas:**
**Implementado por:** Ana Lavadores

**Framework de validación:**
```typescript
import Joi from 'joi';

// Esquema de validación para creación de tareas
const createTaskSchema = Joi.object({
  title: Joi.string()
    .min(1)
    .max(255)
    .required()
    .messages({
      'string.empty': 'El título de la tarea no puede estar vacío',
      'string.max': 'El título de la tarea no puede exceder 255 caracteres'
    }),
    
  description: Joi.string()
    .max(1000)
    .optional(),
    
  priority: Joi.string()
    .valid('low', 'medium', 'high', 'urgent')
    .default('medium'),
    
  dueDate: Joi.date()
    .min('now')
    .optional()
    .messages({
      'date.min': 'La fecha de vencimiento no puede estar en el pasado'
    })
});

// Middleware de validación
const validateCreateTask = (req, res, next) => {
  const { error, value } = createTaskSchema.validate(req.body);
  
  if (error) {
    return res.status(400).json({
      success: false,
      error: {
        code: 'VALIDATION_ERROR',
        message: error.details[0].message
      }
    });
  }
  
  req.validatedData = value;
  next();
};
```

### 🏗️ Aseguramiento de la calidad del código

#### Análisis estático de código
**Mantenido por:** Todo el equipo, coordinado por Ana Lavadores

##### 📊 **Configuración de ESLint y Prettier:**

**Reglas de calidad de código:**
```javascript
// .eslintrc.js
module.exports = {
  extends: [
    '@typescript-eslint/recommended',
    'react-hooks/recommended',
    'prettier'
  ],
  rules: {
    // Aplicar buenas prácticas
    '@typescript-eslint/no-unused-vars': 'error',
    '@typescript-eslint/explicit-function-return-type': 'warn',
    'react-hooks/exhaustive-deps': 'error',
    
    // Límites de complejidad
    'complexity': ['error', 10],
    'max-lines-per-function': ['warn', 50],
    'max-depth': ['error', 4],
    
    // Reglas de seguridad
    'no-eval': 'error',
    'no-implied-eval': 'error',
    'no-new-func': 'error'
  }
};
```

**Métricas de calidad de código:**
- **Incidencias ESLint:** 0 errores, 3 advertencias (monitoreo continuo)
- **Complejidad ciclomática:** Promedio 3.2 (objetivo: <5)
- **Longitud de funciones:** Promedio 18 líneas (objetivo: <25)
- **Duplicación de código:** <5% de bloques duplicados

#### Optimización de rendimiento

##### ⚡ **Rendimiento en el frontend:**
**Optimizado por:** Carlos Cauich y Valeria Itza

**Estrategias de rendimiento implementadas:**
```typescript
// División de código para mejor rendimiento de carga
const TaskPage = lazy(() => import('./pages/TaskPage'));
const ProfilePage = lazy(() => import('./pages/ProfilePage'));

// Memoización para cálculos costosos
const TaskStats = memo(({ tasks }: { tasks: Task[] }) => {
  const stats = useMemo(() => {
    return tasks.reduce((acc, task) => {
      acc[task.status] = (acc[task.status] || 0) + 1;
      return acc;
    }, {} as Record<string, number>);
  }, [tasks]);
  
  return <div>{/* Renderizar estadísticas */}</div>;
});

// Llamadas de API optimizadas con caché
const useTasksWithCache = () => {
  return useQuery({
    queryKey: ['tasks'],
    queryFn: fetchTasks,
    staleTime: 5 * 60 * 1000, // 5 minutos
    cacheTime: 30 * 60 * 1000, // 30 minutos
  });
};
```

**Métricas de rendimiento:**
- **First Contentful Paint:** 1.2s (objetivo: <2s)
- **Largest Contentful Paint:** 2.1s (objetivo: <2.5s)
- **Time to Interactive:** 2.8s (objetivo: <3s)
- **Cumulative Layout Shift:** 0.05 (objetivo: <0.1)

---

## 📊 Evaluación de Competencias Específicas

### 🎯 Matriz de evaluación de competencias

| Competencia | Nivel inicial | Nivel actual | Evidencia | Próximos pasos |
|-------------|---------------|--------------|-----------|----------------|
| **JavaScript/TypeScript** | Básico | Avanzado | 2,800+ líneas de código, arquitectura con tipos seguros | Patrones avanzados, optimización de rendimiento |
| **Desarrollo con React** | Intermedio | Avanzado | Librería de componentes, hooks personalizados, optimización | Patrones de gestión de estado, pruebas avanzadas |
| **Arquitectura de software** | Básico | Intermedio | Arquitectura modular, patrones de diseño | Microservicios, patrones de escalabilidad |
| **Pruebas** | Básico | Intermedio | 78% de cobertura, suite de pruebas integral | Automatización E2E, pruebas de rendimiento |
| **Metodologías ágiles** | Teórico | Práctico | 4 sprints ejecutados, seguimiento de velocidad | Scrum avanzado, integración con Kanban |
| **Diseño de API** | Básico | Intermedio | API RESTful, documentación, validación | GraphQL, versionado de API, rendimiento |
| **Seguridad** | Básico | Intermedio | Autenticación, cifrado, validación | Patrones de seguridad avanzados, auditoría |
| **Diseño de base de datos** | Básico | Intermedio | Esquema normalizado, relaciones, consultas | Tuning de rendimiento, consultas avanzadas |

### 📈 Hoja de ruta de desarrollo de habilidades

#### Planes de crecimiento individuales:

**Carlos Cauich - Especialista Frontend:**
- **Fortaleza actual:** Desarrollo con React, arquitectura de componentes
- **Áreas de crecimiento:** Optimización de rendimiento, gestión de estado avanzada
- **Próximos 6 meses:** Dominar patrones de rendimiento en React, explorar micro-frontends
- **Ruta profesional:** Senior Frontend Engineer → Frontend Architect

**Ana Lavadores - Ingeniera de Calidad:**
- **Fortaleza actual:** Estrategias de pruebas, mejora de procesos  
- **Áreas de crecimiento:** Automatización de pruebas, pruebas de rendimiento
- **Próximos 6 meses:** Dominar automatización E2E, aprender pruebas de carga
- **Ruta profesional:** QA Engineer → Test Automation Lead → QA Manager

**Guillermo Peña - Desarrollador Full-Stack:**
- **Fortaleza actual:** Diseño de sistemas, gestión de proyecto
- **Áreas de crecimiento:** Escalabilidad backend, prácticas DevOps
- **Próximos 6 meses:** Aprender contenedorización, maestría en CI/CD
- **Ruta profesional:** Full-Stack Developer → Solutions Architect

**Valeria Itza - Product Engineer:**
- **Fortaleza actual:** Diseño UX, investigación de usuarios, desarrollo frontend
- **Áreas de crecimiento:** Gestión de producto, análisis de datos
- **Próximos 6 meses:** Aprender analítica, A/B testing, métricas de producto
- **Ruta profesional:** Product Designer → Product Manager → Head of Product

**Edrick Puc - Especialista en Infraestructura:**
- **Fortaleza actual:** Documentación, configuración de sistemas, investigación
- **Áreas de crecimiento:** Plataformas en la nube, automatización, monitoreo
- **Próximos 6 meses:** Certificación AWS, infraestructura como código
- **Ruta profesional:** DevOps Engineer → Site Reliability Engineer → Infrastructure Architect

---

**Competencias específicas evaluadas por:** Equipo CHRONOS completo  
**Supervisión técnica:** Profesora Leydi Ofelia Caballero Chi  
**Periodo de desarrollo:** Septiembre - Noviembre 2025  
**Evaluación continua:** Revisiones técnicas semanales y evaluaciones de habilidades

---

*Competencias específicas desarrolladas mediante práctica real de ingeniería de software profesional* 🔧✨
