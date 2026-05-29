```mermaid
gantt
    title Biblioteca Digital v1.0
    dateFormat YYYY-MM-DD
    axisFormat %d/%m

    section Diseño
    A1 Diseñar_ERD          :done, a1, 2026-06-01, 1d
    A2 Esquema_BD           :done, after a1, 1d
    A3 Swagger              :active, after a2, 2d

    section Backend
    A4 Libros_GET           :after a3, 1d
    A5 Libros_POST          :after a4, 2d

    section Frontend
    A6 Listado_libros       :after a5, 2d
    A7 Formulario_prestamo  :after a6, 1d

    section Calidad
    A8 Tests_integracion    :after a7, 1d
    A9 UAT                  :after a8, 1d

    section Despliegue
    A10 Staging             :after a9, 1d
```
    A11 Documentacion       :after a10, 1d
    A12 Cierre              :milestone, after a11, 0d
```
