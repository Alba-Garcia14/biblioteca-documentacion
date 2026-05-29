# 🧮 Estimación COCOMO II - Biblioteca Digital v1.0

## 📦 Descomposición por Módulos

| Módulo | Funcionalidades | KSLOC Estimado | Justificación |
|--------|---------------|---------------|--------------|
| **Auth** | Login, roles, sesiones | 0.8 | JWT + middleware de autorización |
| **Libros** | CRUD + búsqueda + validación ISBN | 2.1 | Lógica de negocio + validaciones complejas |
| **Usuarios** | CRUD bibliotecarios/lectores | 1.2 | Gestión básica con validaciones |
| **Préstamos** | Flujo completo + multas + notificaciones | 3.5 | Módulo más complejo con reglas de negocio |
| **API Docs** | Swagger + ejemplos + validación | 0.6 | Configuración + documentación automática |
| **Frontend** | React components + integración API | 2.8 | UI responsive + manejo de estado + errores |
| **Infra/DevOps** | CI/CD, scripts, config | 0.5 | GitHub Actions + docker + variables |
| **Tests** | Unitarios + integración + E2E | 1.5 | Cobertura >80% en lógica crítica |
| **TOTAL** | | **13.0 KSLOC** | |

