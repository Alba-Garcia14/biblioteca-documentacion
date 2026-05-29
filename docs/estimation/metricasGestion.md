| Métrica | Cálculo | Resultado | Interpretación |
|---------|---------|-----------|---------------|
| **Personal promedio** | E ÷ TDEV = 33.5 ÷ 10.2 | **~3.3 personas** | Equipo óptimo: 3-4 personas en paralelo |
| **Productividad** | Size ÷ E = 11.5 KSLOC ÷ 33.5 PM | **343 LOC/PM** | Dentro de rangos típicos (200-500 LOC/PM) |
| **Coste estimado** | E × €4.500/PM (coste medio) | **~€150.750** | Presupuesto base para negociación |
| **Coste por KLOC** | Coste ÷ Size = €150.750 ÷ 11.5 | **~€13.100/KLOC** | Benchmark para futuros proyectos |

| Palanca | Acción concreta | Impacto estimado |
|---------|----------------|-----------------|
| 🔧 Mejorar TOOL | Adoptar plantillas de código, generators | ∏EMi: 0.90 → 0.85 → -5% esfuerzo |
| 👥 Invertir en PCAP | Formación en React/Node antes de empezar | PCAP: Alto → Muy Alto → -7% esfuerzo |
| 📋 Reducir CPLX | Simplificar reglas de negocio en MVP | CPLX: Alto → Nominal → -23% esfuerzo* |
| 🔄 Reutilizar más | Usar librerías validadas para validación ISBN | RUSE: aplicar → -10% Size efectivo |

*⚠️ Reducir complejidad puede afectar valor entregado: evaluar con stakeholders.
