# 🗓️ Cronograma Gantt - Biblioteca Digital v1.0

```mermaid

gantt

    title Biblioteca Digital v1.0 - Cronograma de Desarrollo
    dateFormat  YYYY-MM-DD
    axisFormat  %d/%m
    
    section Diseño
    A1: Diseñar ERD           :done,    a1, 2026-05-27, 1d
    A2: Esquema BD            :done,    a2, after a1, 1d
    A3: swagger.yaml          :active,  a3, after a1, 2d
    
    section Desarrollo Backend
    A4: GET /libros           :         a4, after a2 a3, 1d
    A5: POST /libros          :         a5, after a4, 2d
    # 🗓️ Cronograma Gantt - Biblioteca Digital v1.0

```mermaid

gantt

    title Biblioteca Digital v1.0 - Cronograma de Desarrollo
    dateFormat  YYYY-MM-DD
    axisFormat  %d/%m
    
    section Diseño
    A1: Diseñar ERD           :done,    a1, 2026-06-01, 1d
    A2: Esquema BD            :done,    a2, after a1, 1d
    A3: swagger.yaml          :active,  a3, after a1, 2d
    
    section Desarrollo Backend
    A4: GET /libros           :         a4, after a2 a3, 1d
    A5: POST /libros          :         a5, after a4, 2d
    
    section Desarrollo Frontend
    A6: Listado de libros     :         a6, after a4, 2d
    A7: Formulario préstamo   :         a7, after a5 a6, 1d
    
    section Calidad
    A8: Tests integración     :         a8, after a5 a7, 1d
    A9: UAT con usuarios      :         a9, after a8, 1d
    
    section Despliegue
    A10: Despliegue staging   :         a10, after a9, 1d
    A11: Documentación final  :         a11, after a10, 1d
    A12: Cierre del proyecto  :milestone, m1, after a11, 0d 
Leyenda de estados:
✅ :done = Completado
🔵 :active = En progreso
⚪ : = Pendiente
🎯 :milestone = Hito (duración 0)

    section Desarrollo Frontend
    A6: Listado de libros     :         a6, after a4, 2d
    A7: Formulario préstamo   :         a7, after a5 a6, 1d
    
    section Calidad
    A8: Tests integración     :         a8, after a5 a7, 1d
    A9: UAT con usuarios      :         a9, after a8, 1d
    
    section Despliegue
    A10: Despliegue staging   :         a10, after a9, 1d
    A11: Documentación final  :         a11, after a10, 1d
    A12: Cierre del proyecto  :milestone, m1, after a11, 0d 

Leyenda de estados:

✅ :done = Completado
🔵 :active = En progreso
⚪ : = Pendiente
🎯 :milestone = Hito (duración 0)
