# 📁 Organización del Repositorio

## Estructura del Repositorio CHRONOS

Para mantener orden, facilitar colaboración y asegurar escalabilidad del proyecto, hemos definido una estructura organizativa clara que separa responsabilidades y facilita la navegación del código.

---

## 🌳 Árbol de Directorios

### Estructura Principal

```
chronos/
├── 📄 README.md                    # Página principal del proyecto
├── 📄 package.json                 # Dependencies y scripts Node.js
├── 📄 tsconfig.json               # Configuración TypeScript
├── 📄 tailwind.config.js          # Configuración Tailwind CSS
├── 📄 vite.config.ts              # Configuración Vite build tool
├── 📄 postcss.config.js           # Configuración PostCSS
├── 📄 .gitignore                  # Archivos ignorados por Git
├── 📄 .env.example                # Variables de entorno template
├── 📄 LICENSE                     # Licencia del proyecto
├── 📄 CONTRIBUTING.md             # Guías de contribución
│
├── 📁 src/                        # Código fuente principal
│   ├── 📁 components/             # Componentes React reutilizables
│   ├── 📁 pages/                  # Páginas principales de la app
│   ├── 📁 hooks/                  # Custom React hooks
│   ├── 📁 services/               # Services para APIs y data
│   ├── 📁 store/                  # State management (Zustand)
│   ├── 📁 types/                  # TypeScript type definitions
│   ├── 📁 utils/                  # Utility functions y helpers
│   └── 📄 main.tsx                # Entry point de la aplicación
│
├── 📁 public/                     # Assets públicos estáticos
│   ├── 📄 index.html              # HTML template principal
│   ├── 📁 icons/                  # Iconos de la aplicación
│   └── 📁 images/                 # Imágenes estáticas
│
├── 📁 assets/                     # Assets de desarrollo
│   ├── 📁 mockups/                # Wireframes y mockups
│   ├── 📁 designs/                # Designs finales UI/UX
│   └── 📁 presentations/          # Slides y presentations
│
├── 📁 docs/                       # Documentación completa
│   ├── 📄 api-reference.md        # API documentation
│   ├── 📄 user-manual.md          # Manual del usuario
│   ├── 📄 technical-docs.md       # Documentación técnica
│   └── 📄 requirements.md         # Requirements analysis
│
├── 📁 tests/                      # Testing suite completo
│   ├── 📁 unit/                   # Unit tests
│   ├── 📁 integration/            # Integration tests
│   ├── 📁 e2e/                    # End-to-end tests
│   └── 📄 jest.config.js          # Jest testing configuration
│
├── 📁 config/                     # Configuration files
│   ├── 📄 database.config.js      # Database configuration
│   ├── 📄 auth.config.js          # Authentication setup
│   └── 📄 api.config.js           # API endpoints configuration
│
├── 📁 producto/                   # Documentación Académica Sección 1
│   ├── 📄 descripcion.md          # Descripción del producto
│   ├── 📄 usuarios.md             # User personas y scenarios
│   └── 📄 propuesta-valor.md      # Value proposition canvas
│
├── 📁 requisitos/                 # Documentación Académica Sección 2
│   ├── 📄 funcionales.md          # Requirements funcionales
│   ├── 📄 no-funcionales.md       # Requirements no funcionales
│   ├── 📄 priorizacion.md         # Priorización MoSCoW
│   └── 📄 artefactos.md           # Artefactos de requirements
│
├── 📁 proceso/                    # Documentación Académica Sección 3
│   ├── 📄 descripcion.md          # Descripción del proceso
│   ├── 📄 gestion.md              # Gestión del proyecto
│   ├── 📄 metricas.md             # Métricas de contribución
│   └── 📄 organizacion.md         # Este archivo - organización
│
├── 📁 competencias/               # Documentación Académica Sección 5
│   ├── 📄 genericas.md            # Competencias genéricas
│   └── 📄 especificas.md          # Competencias específicas
│
└── 📄 presentacion.md             # Documentación Académica Sección 4
```

---

## 📂 Organización Detallada por Carpeta

### 🔧 `/src/` - Código Fuente Principal

#### Responsabilidades por Carpeta:

##### 📁 `/src/components/`
**Propósito:** Componentes React reutilizables y modulares  
**Organización:**
```
components/
├── ui/                            # Componentes base (Button, Input, etc.)
│   ├── Button/
│   │   ├── Button.tsx
│   │   ├── Button.test.tsx
│   │   └── Button.module.css
│   ├── Input/
│   └── Modal/
├── layout/                        # Componentes de layout
│   ├── Header/
│   ├── Sidebar/
│   └── Footer/
├── task/                          # Task-related components
│   ├── TaskCard/
│   ├── TaskList/
│   └── TaskForm/
├── gamification/                  # Gamification components
│   ├── ProgressBar/
│   ├── AchievementBadge/
│   └── LeaderBoard/
└── wellness/                      # Wellness tracking components
    ├── MoodTracker/
    ├── BreakReminder/
    └── WellnessStats/
```

**Estándares:**
- Cada componente en su propia carpeta
- Archivo principal + test + estilos
- Documentación JSDoc para props
- Export barrel files (`index.ts`) para clean imports

##### 📁 `/src/pages/`
**Propósito:** Páginas principales de la aplicación  
**Organización:**
```
pages/
├── HomePage/                      # Landing page
├── DashboardPage/                 # Main user dashboard  
├── TasksPage/                     # Task management
├── ProfilePage/                   # User profile management
├── WellnessPage/                  # Wellness tracking
├── LeaderboardPage/               # Gamification rankings
└── SettingsPage/                  # App settings
```

**Estándares:**
- Una página por feature principal
- Co-located components específicos de página
- Lazy loading para performance
- SEO metadata apropiado

##### 📁 `/src/hooks/`
**Propósito:** Custom React hooks para lógica reutilizable  
**Ejemplos:**
```typescript
// useTask.ts - Task management logic
// useAuth.ts - Authentication logic  
// useWellness.ts - Wellness tracking logic
// useLocalStorage.ts - Local storage wrapper
// useTimer.ts - Task timer functionality
```

**Estándares:**
- Prefijo `use` obligatorio
- Single responsibility principle
- Comprehensive testing
- TypeScript strict typing

##### 📁 `/src/services/`
**Propósito:** API calls, data fetching y business logic  
**Organización:**
```
services/
├── api/                           # API communication
│   ├── taskApi.ts
│   ├── userApi.ts
│   └── wellnessApi.ts
├── auth/                          # Authentication service
│   ├── authService.ts
│   └── tokenManager.ts
├── storage/                       # Data persistence
│   ├── localStorage.ts
│   └── sessionStorage.ts
└── notifications/                 # Push notifications
    └── notificationService.ts
```

##### 📁 `/src/store/`
**Propósito:** State management con Zustand  
**Organización:**
```
store/
├── slices/                        # Individual store slices
│   ├── authSlice.ts
│   ├── taskSlice.ts
│   ├── wellnessSlice.ts
│   └── gamificationSlice.ts
├── middleware/                    # Custom middleware
│   ├── persistMiddleware.ts
│   └── loggerMiddleware.ts
└── index.ts                       # Combined store
```

##### 📁 `/src/types/`
**Propósito:** TypeScript type definitions  
**Organización:**
```
types/
├── api.ts                         # API response types
├── user.ts                        # User-related types
├── task.ts                        # Task-related types
├── wellness.ts                    # Wellness tracking types
├── gamification.ts                # Gamification types
└── common.ts                      # Shared/utility types
```

##### 📁 `/src/utils/`
**Propósito:** Utility functions y helpers  
**Ejemplos:**
```typescript
// dateUtils.ts - Date formatting/manipulation
// validationUtils.ts - Form validation helpers
// formatUtils.ts - Data formatting utilities
// constants.ts - App-wide constants
// helpers.ts - General helper functions
```

---

### 🧪 `/tests/` - Testing Strategy

#### Organización por Tipo de Test:

##### 📁 `/tests/unit/`
**Propósito:** Unit tests para componentes y functions individuales  
**Estructura espejo del src:**
```
unit/
├── components/
│   ├── ui/
│   ├── task/
│   └── wellness/
├── hooks/
├── services/
└── utils/
```

**Estándares:**
- Test files: `*.test.ts` or `*.spec.ts`
- Coverage mínimo: 80% para utils, 70% para components
- Jest + Testing Library para React components
- Mock de dependencies externas

##### 📁 `/tests/integration/`
**Propósito:** Integration tests para features completas  
**Organización:**
```
integration/
├── task-management/               # Complete task workflows
├── user-authentication/          # Auth flows end-to-end
├── wellness-tracking/             # Wellness feature integration
└── api-integration/               # API service integration
```

##### 📁 `/tests/e2e/`
**Propósito:** End-to-end tests con Cypress/Playwright  
**Organización:**
```
e2e/
├── user-journeys/                 # Complete user scenarios
│   ├── new-user-onboarding.spec.ts
│   ├── daily-task-management.spec.ts
│   └── wellness-goal-setting.spec.ts
├── regression/                    # Regression test suite
└── fixtures/                      # Test data y mocks
```

---

### 📚 `/docs/` - Documentación Técnica

#### Organización de Documentación:

##### 📄 `api-reference.md`
**Contenido:**
- API endpoints documentation
- Request/response schemas
- Authentication requirements
- Rate limiting y error handling

##### 📄 `user-manual.md`  
**Contenido:**
- User onboarding guide
- Feature walkthroughs
- FAQ y troubleshooting
- Best practices para users

##### 📄 `technical-docs.md`
**Contenido:**
- Architecture overview
- Technology stack decisions
- Development workflow
- Deployment procedures

##### 📄 `requirements.md`
**Contenido:**
- Functional requirements detailed
- Non-functional requirements analysis
- Use case scenarios
- Acceptance criteria

---

### ⚙️ `/config/` - Configuration Management

#### Files de Configuración:

##### 📄 `database.config.js`
```javascript
// Database connection settings
// Environment-specific configurations
// Migration y seeding settings
```

##### 📄 `auth.config.js`
```javascript
// JWT settings
// OAuth provider configurations  
// Session management settings
```

##### 📄 `api.config.js`
```javascript
// API base URLs per environment
// Request timeout configurations
// Default headers y interceptors
```

---

## 🔄 Workflow de Organización

### 📝 File Naming Conventions

#### Archivos TypeScript/JavaScript:
- **Components:** PascalCase (`TaskCard.tsx`, `UserProfile.tsx`)
- **Hooks:** camelCase con prefix (`useTaskTimer.ts`, `useAuth.ts`)
- **Services:** camelCase (`taskService.ts`, `apiClient.ts`)  
- **Types:** camelCase (`userTypes.ts`, `apiTypes.ts`)
- **Utils:** camelCase (`dateUtils.ts`, `validationHelpers.ts`)

#### Archivos de Documentación:
- **Markdown:** kebab-case (`user-manual.md`, `api-reference.md`)
- **Config files:** kebab-case (`tailwind.config.js`, `jest.config.js`)

### 📁 Folder Naming Conventions:
- **All folders:** kebab-case (`task-management/`, `user-profile/`)
- **Component folders:** PascalCase para match component name (`TaskCard/`)

---

## 🚦 Branch Strategy y Organization

### Branch Naming Convention:

#### Feature Branches:
```
feature/task-timer-implementation
feature/wellness-mood-tracker  
feature/gamification-achievements
```

#### Bug Fix Branches:
```
bugfix/task-completion-notification
bugfix/user-profile-image-upload
```

#### Documentation Branches:
```
docs/api-reference-update
docs/user-manual-wellness-section
```

### 📂 Directory Ownership:

#### Responsabilidad por Carpeta:
- **Carlos:** `/src/components/task/`, `/src/services/api/taskApi.ts`
- **Ana:** `/tests/`, `/src/utils/`, quality assurance overall
- **Guillermo:** `/src/store/`, `/src/hooks/`, state management
- **Valeria:** `/src/components/ui/`, `/assets/designs/`, UI/UX
- **Edrick:** `/config/`, `/docs/`, infrastructure y documentation

#### Shared Ownership:
- **`/src/pages/`:** Todos contribuyen según features asignadas
- **`/src/types/`:** Shared definitions, requieren review de 2+ miembros
- **Root config files:** Changes requieren team approval

---

## 📋 Code Organization Standards  

### 🏗️ Architecture Patterns

#### Component Architecture:
```typescript
// TaskCard/TaskCard.tsx
interface TaskCardProps {
  task: Task;
  onComplete: (id: string) => void;
  onEdit: (id: string) => void;
}

export const TaskCard: React.FC<TaskCardProps> = ({
  task,
  onComplete,
  onEdit
}) => {
  // Component logic here
  return (
    // JSX here
  );
};

export default TaskCard;
```

#### Service Pattern:
```typescript  
// services/api/taskApi.ts
class TaskApiService {
  private baseURL = '/api/tasks';
  
  async getTasks(): Promise<Task[]> {
    // Implementation
  }
  
  async createTask(task: CreateTaskRequest): Promise<Task> {
    // Implementation  
  }
}

export const taskApi = new TaskApiService();
```

#### Store Pattern (Zustand):
```typescript
// store/slices/taskSlice.ts
interface TaskState {
  tasks: Task[];
  isLoading: boolean;
  error: string | null;
}

interface TaskActions {
  fetchTasks: () => Promise<void>;
  addTask: (task: CreateTaskRequest) => Promise<void>;
  updateTask: (id: string, updates: Partial<Task>) => Promise<void>;
}

export const useTaskStore = create<TaskState & TaskActions>((set, get) => ({
  // Implementation
}));
```

---

## 📊 Quality Gates y Organization

### 🔍 Pre-commit Hooks:
- **Linting:** ESLint + Prettier formatting
- **Type checking:** TypeScript strict mode  
- **Testing:** Run unit tests para affected files
- **Documentation:** Ensure README updates si needed

### 📈 File Size Guidelines:
- **Components:** Max 200 lines (refactor si larger)
- **Services:** Max 300 lines (split into multiple classes)
- **Utils:** Max 150 lines per file
- **Test files:** No limit (comprehensive testing preferred)

### 🎯 Import Organization:
```typescript
// External libraries (react, lodash, etc.)
import React from 'react';
import { useState, useEffect } from 'react';
import clsx from 'clsx';

// Internal modules (services, store, etc.) 
import { taskApi } from '@/services/api/taskApi';
import { useTaskStore } from '@/store/slices/taskSlice';

// Components (from specific to general)
import { TaskCard } from '@/components/task/TaskCard';
import { Button } from '@/components/ui/Button';

// Types  
import type { Task } from '@/types/task';

// Relative imports last
import './TaskList.module.css';
```

---

## 🔄 Maintenance y Evolution

### 📅 Regular Maintenance Tasks:

#### Weekly (Rotating responsibility):
- Clean up unused files y dependencies
- Update documentation para new features
- Review y merge dependabot PRs
- Archive completed branches

#### Monthly (Team activity):
- Dependency audit y updates
- Code smell analysis y refactoring
- Performance analysis y optimization
- Documentation accuracy review

#### Quarterly (Major reviews):
- Architecture review y evolution
- Folder structure optimization
- Workflow improvement proposals
- Technology stack evaluation

### 🔄 Evolution Guidelines:

#### Adding New Features:
1. **Planning:** Document new folder/file needs
2. **Structure:** Follow established patterns
3. **Integration:** Update related docs/configs
4. **Testing:** Add appropriate test coverage
5. **Documentation:** Update relevant documentation

#### Refactoring Existing Code:
1. **Analysis:** Identify affected files/folders
2. **Plan:** Document refactoring scope
3. **Execute:** Make changes incrementally
4. **Validate:** Ensure all tests pass
5. **Document:** Update organizational docs

---

## 🎯 Success Metrics

### 📊 Organization Quality Metrics:

#### Repository Health:
- **File findability:** <10 seconds to locate any file
- **Build time:** <2 minutes para full build
- **Test execution:** <30 seconds para unit tests
- **Dependency health:** Zero critical vulnerabilities

#### Developer Experience:
- **Onboarding time:** New developer productive en <4 hours
- **Feature development:** Clear path from idea to implementation
- **Bug resolution:** Easy to locate y fix issues
- **Code reuse:** >70% component reusability

#### Documentation Coverage:
- **API coverage:** 100% endpoints documented
- **Component coverage:** >90% components documented  
- **Process coverage:** All workflows documented
- **Troubleshooting:** Common issues covered

---

**Organización diseñada por:** Guillermo Cárdenas (Infrastructure Lead)  
**Aprobado por:** Equipo CHRONOS completo  
**Última actualización:** 29 de Septiembre de 2025  
**Próxima revisión:** 15 de Noviembre de 2025  

---

*Estructura organizativa diseñada para escalabilidad, mantenibilidad y colaboración efectiva del equipo* 📁✨