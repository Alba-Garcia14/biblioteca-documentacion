### ✅ Reglas para Definir Actividades Efectivas
🔹 **Verbos accionables**: "Implementar", "Validar", "Documentar" (no "Trabajar en...", "Revisar...")
🔹 **Entregables tangibles**: Código, documento, configuración, test (no "progreso", "avance")
🔹 **Duración estimable**: 4-40 horas ideal; si >40h, descomponer más
🔹 **Asignable**: Una persona o par puede ejecutarla sin dependencias externas no gestionadas

# 🗓️ Cronograma Base - Biblioteca Digital v1.0

## 📊 Vista Resumen por Sprint

### Sprint 1: Fundamentos (01-14 jun 2026)
| Semana | Actividades Clave | Hitos | Owner Principal |
|--------|-----------------|-------|----------------|
| 1 | • Diseñar ERD<br>• Esquema BD<br>• Crear tabla libros | ✅ Modelo de datos aprobado | María |
| 2 | • GET /libros<br>• POST /libros + validación<br>• Documentar swagger<br>• Tests integración | ✅ API base funcional + documentada | María + Carlos |

### Sprint 2: Flujo de Préstamo (15-28 jun 2026)
| Semana | Actividades Clave | Hitos | Owner Principal |
|--------|-----------------|-------|----------------|
| 3 | • Autenticación bibliotecarios<br>• Lógica de disponibilidad<br>• Frontend: listado + búsqueda | ✅ Módulo Libros completo | María + Carlos |
| 4 | • Frontend: formulario préstamo<br>• Endpoint POST /prestamos<br>• Pruebas E2E | ✅ Flujo préstamo funcional en staging | Carlos + Ana |

### Sprint 3: Pulido + Lanzamiento (29 jun - 12 jul 2026)
| Semana | Actividades Clave | Hitos | Owner Principal |
|--------|-----------------|-------|----------------|
| 5 | • Mejoras UX (validaciones en tiempo real)<br>• Pruebas de usabilidad con 3 usuarios | ✅ Feedback de usuarios incorporado | Carlos + Ana |
| 6 | • Corrección de bugs críticos<br>• Despliegue en producción<br>• Documentación final | 🎯 MVP lanzado + aceptado | Equipo completo |

## 🔗 Dependencias Críticas (Camino Crítico)
```mermaid
graph LR
    A[ERD aprobado] --> B[Esquema BD]
    B --> C[Tabla libros]
    C --> D[GET /libros]
    D --> E[POST /libros]
    E --> F[swagger.yaml]
    F --> G[Tests integración]
    G --> H[UAT usuarios]
    H --> I[Despliegue producción]
```