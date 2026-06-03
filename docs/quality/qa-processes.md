# 🛡️ QA Processes (Quality Assurance)
## 🎯 Propósito
Definir los procesos, estándares y prácticas preventivas que garantizan que el software se construye correctamente desde el inicio. QA se enfoca en el **CÓMO** trabajamos, no solo en el resultado final.

> 📌 **Alcance:** Aplica a todo el ciclo de vida del proyecto `Biblioteca Digital v1.0`.

---

## 📋 1. Estándares de Proceso

### 1.1 Convenciones de Desarrollo
- **Ramas:** `main` (estable) → `develop` (integración) → `feature/*`, `bugfix/*`, `hotfix/*`
- **Commits:** Formato Conventional Commits (`feat:`, `fix:`, `docs:`, `chore:`, `test:`)
- **Código:** ESLint + Prettier configurados. No se mergea PRs con warnings activos.
- **Documentación:** Todo cambio en API o arquitectura requiere actualización en `/docs/` y ADR correspondiente.

### 1.2 Definition of Ready (DoR) - Antes de Desarrollar
Una historia de usuario solo entra en sprint si cumple:
- [ ] Descripción clara y criterios de aceptación medibles
- [ ] Dependencias externas identificadas y resueltas
- [ ] Mockups/prototipos validados (si aplica UI)
- [ ] Estimación consensuada por el equipo
- [ ] Asignada a un responsable principal

### 1.3 Definition of Done (DoD) - Antes de Cerrar
Una historia se considera terminada solo si:
- [ ] Código implementado y revisado por ≥1 compañero
- [ ] Tests unitarios e integración pasando en CI/CD
- [ ] Cobertura ≥80% en lógica de negocio nueva
- [ ] `swagger.yaml` actualizado (si cambia API)
- [ ] Documentación técnica y de usuario actualizada
- [ ] Desplegado en staging y validado funcionalmente
- [ ] Sin bugs críticos/altos pendientes

---

## 🔄 2. Automatización y Herramientas (Shift-Left QA)

| Proceso | Herramienta | Ejecución | Umbral de Bloqueo |
|--------|-------------|-----------|------------------|
| Linting & Formato | ESLint + Prettier | Cada commit local | ❌ Fallo bloquea commit |
| Validación YAML | `@apidevtools/swagger-cli` | Push a `feature/*` | ❌ Fallo bloquea push |
| Tests Unitarios | Jest | PR → `develop` | ❌ Fallo bloquea merge |
| Análisis Estático | SonarQube / CodeClimate | Merge a `develop` | ⚠️ Advertencias > umbral |
| Despliegue Staging | GitHub Actions + Vercel/Render | Merge a `develop` | ❌ Fallo bloquea release |

---

## 📚 3. Formación y Onboarding

### 3.1 Plan de Inducción para Nuevos Miembros
- [ ] Acceso a repositorio y permisos configurados
- [ ] Sesión de 1h: Arquitectura, stack y convenciones
- [ ] Pair programming en primera tarea (`good first issue`)
- [ ] Revisión de DoR/DoD y flujo de PRs
- [ ] Evaluación a los 7 días: feedback y ajustes

### 3.2 Mejora Continua del Proceso
- **Frecuencia:** Al final de cada sprint (retrospectiva)
- **Entradas:** Métricas QA, bloqueos reportados, feedback de equipo
- **Salidas:** 1-2 acciones concretas para el próximo sprint
- **Registro:** `/docs/quality/retrospectives/`

---

## 🔍 4. Auditorías de Proceso

| Tipo | Frecuencia | Auditor | Alcance | Criterio de Éxito |
|------|-----------|---------|---------|------------------|
| Cumplimiento DoD | Por sprint | Tech Lead / PM | Muestra aleatoria de historias cerradas | ≥95% de historias cumplen DoD completo |
| Estándares de Código | Mensual | SonarCloud + revisión manual | Código en `develop` | 0 duplicación crítica, complejidad ≤15 |
| Documentación | Trimestral | PM + QA | `/docs/`, ADRs, swagger.yaml | 100% de endpoints documentados, ADRs actualizados |

---

## 👥 5. Roles y Responsabilidades

| Rol | Responsabilidad QA Principal |
|-----|-----------------------------|
| **Project Manager** | Garantizar que los procesos se siguen, facilitar retrospectivas, eliminar bloqueos |
| **Tech Lead** | Definir estándares, revisar arquitectura, validar DoD técnico, auditar código |
| **Desarrolladores** | Aplicar convenciones, escribir tests, actualizar docs, participar en code review |
| **QA Engineer** | Diseñar estrategia de pruebas, automatizar validaciones, reportar desviaciones de proceso |

---

📅 **Última Revisión:** `[DD/MM/AAAA]`  
👤 **Aprobado por:** `[Nombre/Rol]`  
🔄 **Próxima Revisión:** `[DD/MM/AAAA]`

> 💡 *Este documento es vivo. Cualquier mejora al proceso debe proponerse vía PR y discutirse en retrospectiva.*
