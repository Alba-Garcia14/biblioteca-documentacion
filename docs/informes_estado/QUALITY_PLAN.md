# 🎯 Plan de Calidad - Biblioteca Digital v1.0

## 🔹 Estrategia QA (Prevención)
| Actividad | Frecuencia | Responsable | Métrica de Éxito |
|-----------|-----------|------------|-----------------|
| Definir DoD por sprint | Por sprint | PM + Equipo | 100% de historias con DoD explícito |
| Revisión de arquitectura | Al inicio de módulo | Tech Lead | 0 refactorizaciones mayores por diseño |
| Capacitación en testing | Trimestral | QA Lead | 100% del equipo aplica buenas prácticas |
| Automatización CI/CD | Continua | DevOps | 0 merges sin validación automática |

## 🔹 Estrategia QC (Detección)
| Tipo de Prueba | Cuándo se Ejecuta | Responsable | Criterio de Aprobación |
|---------------|------------------|------------|----------------------|
| Unitarias | Durante desarrollo | Desarrollador | Cobertura ≥80% en lógica crítica |
| Integración | Antes de merge a main | QA + Devs | 0 errores en flujo completo |
| UAT | Antes de release a producción | Usuario clave + QA | ≥95% de tareas completadas sin ayuda |
| Regresión | En cada push a main | CI/CD + QA | 0 fallos en suite completa |

## 📊 Métricas Clave y Targets
| Métrica | Tipo | Target | Frecuencia de Revisión |
|---------|------|--------|----------------------|
| % Historias con DoD cumplido | QA | ≥95% | Por sprint |
| Cobertura de tests en lógica crítica | QC | ≥80% | Por release |
| Tasa de escape de bugs a producción | QC | <5% | Mensual |
| Tiempo medio para corregir bug | QC | <2 días | Semanal |

> 💡 *Este plan se revisa y ajusta al finalizar cada sprint. 
> Para detalles técnicos, ver `/docs/quality/` en el repositorio.*
