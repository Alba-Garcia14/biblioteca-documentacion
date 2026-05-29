```mermaid
gantt
    title Biblioteca Digital v1.0
    dateFormat YYYY-MM-DD
    axisFormat %d/%m

    section Diseño
    A1: Diseñar ERD          :done, 2026-06-01, 1d
    A2: Esquema BD           :done, after A1, 1d
    A3: swagger.yaml         :active, after A2, 2d

    section Backend
    A4: GET /libros          :after A3, 1d
    A5: POST /libros         :after A4, 2d

    section Frontend
    A6: Listado de libros    :after A5, 2d
    A7: Formulario prestamo  :after A6, 1d

    section Calidad
    A8: Tests integracion    :after A7, 1d
    A9: UAT con usuarios     :after A8, 1d

    section Despliegue
    A10: Despliegue staging  :after A9, 1d
    A11: Documentacion final :after A10, 1d
    A12: Cierre del proyecto :milestone, after A11, 0d
```
