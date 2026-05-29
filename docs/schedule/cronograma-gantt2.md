```mermaid
gantt
    title Biblioteca Digital v1.0
    dateFormat YYYY-MM-DD
    axisFormat %d/%m

    section Diseño
    A1: Diseñar ERD          :done, a1, 2026-06-01, 1d
    A2: Esquema BD           :done, after a1, 1d
    A3: swagger.yaml         :active, after a2, 2d

    section Backend
    A4: GET /libros          :after a3, 1d
    A5: POST /libros         :after a4, 2d

    section Frontend
    A6: Listado de libros    :after a5, 2d
    A7: Formulario préstamo  :after a6, 1d

    section Calidad
    A8: Tests integración    :after a7, 1d
    A9: UAT con usuarios     :after a8, 1d

    section Despliegue
    A10: Despliegue staging  :after a9, 1d
    A11: Documentación final :after a10, 1d
    A12: Cierre del proyecto :milestone, after a11, 0d
```

🔥 Claves para que NO vuelva a fallar
✔️ SOLO after una_tarea
❌ NO after a1 a2
✔️ milestone siempre con after
✔️ nada de espacios raros en la sintaxis
