# 🗓️ Cronograma de Trabajo - Biblioteca Digital v1.0

```mermaid
gantt
    title Biblioteca Digital v1.0
    dateFormat  YYYY-MM-DD
    axisFormat  %d/%m
    
    section Diseño
    A1: Diseñar ERD           :done,    2026-06-01, 1d
    A2: Esquema BD            :done,    1d
    A3: swagger.yaml          :active,  2d
    
    section Backend
    A4: GET /libros           :         1d
    A5: POST /libros          :         2d
    
    section Frontend
    A6: Listado de libros     :         2d
    A7: Formulario prestamo   :         1d
    
    section Calidad
    A8: Tests integracion     :         1d
    A9: UAT con usuarios      :         1d
    
    section Despliegue
    A10: Despliegue staging   :         1d
    A11: Documentacion final  :         1d
    A12: Cierre del proyecto  :milestone, 0d 
    ```