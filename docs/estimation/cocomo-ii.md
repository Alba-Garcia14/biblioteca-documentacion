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
markdown
## ⚙️ Scale Factors (SF) - Evaluación para Biblioteca Digital

| Factor | Descripción | Valor (0-5) | Justificación |
|--------|-------------|------------|--------------|
| **SF1: Precedence** | ¿Es el primer proyecto de este tipo? | 2 (Bajo) | Equipo ha hecho CRUDs similares antes |
| **SF2: Development Flexibility** | ¿Qué tan rígidos son los requisitos? | 3 (Nominal) | Requisitos estables pero con margen para ajustes UX |
| **SF3: Architecture/Risk Resolution** | ¿Se resolvieron riesgos arquitectónicos temprano? | 2 (Bajo) | Arquitectura simple, riesgos técnicos mínimos |
| **SF4: Team Cohesion** | ¿Qué tan experimentado y cohesionado es el equipo? | 3 (Nominal) | Equipo pequeño, se conocen, pero es su primer proyecto juntos |
| **SF5: Process Maturity** | ¿Qué tan maduro es el proceso de desarrollo? | 2 (Bajo) | Usan Git, PRs, CI básico, pero sin métricas formales |

📊 Cálculo de B:
• Suma de SF = 2 + 3 + 2 + 3 + 2 = **12**
• Fórmula: B = 0.91 + 0.01 × (Suma SF)
• B = 0.91 + 0.01 × 12 = **1.03**

## 💰 Cost Drivers (EM) - Evaluación para Biblioteca Digital

### 🧑 Producto del Software
| Factor | Valor | Multiplicador | Justificación |
|--------|-------|--------------|--------------|
| RELY (Fiabilidad requerida) | Alto | 1.15 | Errores en préstamos generan reclamaciones |
| DATA (Tamaño de BD) | Nominal | 1.00 | ~10K registros, bien indexados |
| CPLX (Complejidad) | Alto | 1.30 | Reglas de negocio en préstamos + validaciones ISBN |

### 🖥️ Plataforma de Ejecución
| Factor | Valor | Multiplicador | Justificación |
|--------|-------|--------------|--------------|
| TIME (Restricciones de tiempo) | Nominal | 1.00 | No es tiempo real, respuesta <2s es suficiente |
| STOR (Restricciones de memoria) | Nominal | 1.00 | Cloud escalable, sin límites estrictos |
| PLAT (Volatilidad de plataforma) | Bajo | 0.95 | Stack maduro (Node+React+Postgres) |

### 👥 Personal
| Factor | Valor | Multiplicador | Justificación |
|--------|-------|--------------|--------------|
| ACAP (Capacidad de analistas) | Alto | 0.85 | PM con experiencia en proyectos similares |
| AEXP (Experiencia en aplicación) | Nominal | 1.00 | Equipo conoce dominio bibliotecario |
| PCAP (Capacidad de programadores) | Alto | 0.85 | Devs senior en stack seleccionado |
| PEXP (Experiencia en plataforma) | Alto | 0.88 | Experiencia previa con Node/React |
| LTEX (Experiencia en lenguaje) | Alto | 0.91 | JavaScript/TypeScript dominado por el equipo |

### 🛠️ Proyecto
| Factor | Valor | Multiplicador | Justificación |
|--------|-------|--------------|--------------|
| TOOL (Uso de herramientas) | Alto | 0.90 | VS Code, GitHub Actions, Swagger, testing frameworks |
| SITE (Desarrollo distribuido) | Nominal | 1.00 | Equipo en misma ubicación (o remoto bien coordinado) |
| SCED (Ajuste por cronograma) | Nominal | 1.00 | Cronograma realista, sin compresión artificial |

### 🔧 Factores NO aplicados (se omiten o =1.00)
• RUSE (Reutilización de software): No aplica (poca reutilización externa)  
• DOCU (Documentación): Nominal (1.00) - documentación estándar  
• PVOL (Volatilidad de requisitos): Bajo (0.95) - requisitos estables  
• MULT (Multi-site): Nominal (1.00) - equipo co-locado  
• etc.

## 🧮 Cálculo Final - Post-Architecture Model

### Datos de entrada:
• A = 2.94 (constante calibrada de COCOMO II)
• Size = 11.5 KSLOC (ajustado)
• B = 1.03 (calculado con Scale Factors)
• ∏EMi = 0.92 (producto de Cost Drivers)

### Fórmula:
E = A × (Size)^B × ∏EMi

### Cálculo paso a paso:
1. Size^B = 11.5^1.03 = 11.5 × 11.5^0.03 ≈ 11.5 × 1.077 ≈ **12.39**
2. A × Size^B = 2.94 × 12.39 ≈ **36.43**
3. E = 36.43 × 0.92 ≈ **33.5 Personas-Mes**

✅ Esfuerzo estimado: **33.5 PM**
