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
