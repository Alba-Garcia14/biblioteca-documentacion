# Manual de Generación de Archivos Markdown con VS Code

> Guía de referencia rápida para crear y editar documentos `.md` usando Visual Studio Code

---

## Índice

1. [¿Qué es Markdown?](#qué-es-markdown)
2. [Configuración de VS Code](#configuración-de-vs-code)
3. [Crear un archivo Markdown](#crear-un-archivo-markdown)
4. [Sintaxis básica](#sintaxis-básica)
5. [Sintaxis avanzada](#sintaxis-avanzada)
6. [Extensiones recomendadas](#extensiones-recomendadas)
7. [Atajos de teclado en VS Code](#atajos-de-teclado-en-vs-code)
8. [Vista previa](#vista-previa)
9. [Exportar a otros formatos](#exportar-a-otros-formatos)

---

## ¿Qué es Markdown?

Markdown es un lenguaje de marcado ligero que permite dar formato a texto plano usando símbolos simples. Los archivos Markdown tienen extensión `.md` o `.markdown` y son ampliamente usados en documentación, README de proyectos, blogs y wikis.

---

## Configuración de VS Code

### Instalación

1. Descarga VS Code desde [https://code.visualstudio.com](https://code.visualstudio.com)
2. Instala la aplicación siguiendo el asistente

### Ajustes recomendados para Markdown

Abre la paleta de comandos con `Ctrl+Shift+P` (Windows/Linux) o `Cmd+Shift+P` (macOS) y escribe **"Open User Settings (JSON)"**. Añade las siguientes opciones:

```json
{
  "[markdown]": {
    "editor.wordWrap": "on",
    "editor.quickSuggestions": false,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "markdown.preview.fontSize": 16,
  "markdown.preview.lineHeight": 1.6
}
```

---

## Crear un archivo Markdown

### Desde el explorador de VS Code

1. Abre una carpeta con `Archivo > Abrir carpeta`
2. En el explorador lateral, haz clic derecho y selecciona **"Nuevo archivo"**
3. Escribe el nombre con extensión `.md`, por ejemplo: `documento.md`

### Desde la terminal integrada

Abre la terminal con `` Ctrl+` `` y ejecuta:

```bash
# Windows (PowerShell)
New-Item documento.md

# macOS / Linux
touch documento.md
```

---

## Sintaxis básica

### Encabezados

Los encabezados se crean con el símbolo `#`. Cuantos más `#`, menor es el nivel.

```markdown
# Encabezado nivel 1
## Encabezado nivel 2
### Encabezado nivel 3
#### Encabezado nivel 4
##### Encabezado nivel 5
###### Encabezado nivel 6
```

> **Parámetro importante:** Siempre deja un espacio entre `#` y el texto. `#Título` no es válido; `# Título` sí lo es.

---

### Énfasis de texto

| Efecto | Sintaxis | Resultado |
|--------|----------|-----------|
| Negrita | `**texto**` o `__texto__` | **texto** |
| Cursiva | `*texto*` o `_texto_` | *texto* |
| Negrita + cursiva | `***texto***` | ***texto*** |
| Tachado | `~~texto~~` | ~~texto~~ |

---

### Párrafos y saltos de línea

```markdown
Un párrafo es simplemente una o más líneas de texto consecutivas.

Para crear un nuevo párrafo, deja una línea en blanco entre bloques de texto.

Para un salto de línea sin nuevo párrafo,  
añade dos espacios al final de la línea anterior.
```

---

### Listas

**Lista no ordenada** — usa `-`, `*` o `+`:

```markdown
- Elemento uno
- Elemento dos
  - Sub-elemento (indentado con 2 espacios)
  - Otro sub-elemento
- Elemento tres
```

**Lista ordenada** — usa números seguidos de punto:

```markdown
1. Primer paso
2. Segundo paso
   1. Sub-paso
   2. Otro sub-paso
3. Tercer paso
```

> **Nota:** En listas ordenadas, el número real no importa. Markdown los renumera automáticamente. Puedes usar `1.` en todos.

---

### Vínculos e imágenes

**Enlace:**

```markdown
[Texto del enlace](https://www.ejemplo.com)
[Enlace con título](https://www.ejemplo.com "Título opcional")
```

**Imagen:**

```markdown
![Texto alternativo](ruta/imagen.png)
![Logo](https://ejemplo.com/logo.png "Título opcional")
```

> La diferencia entre enlace e imagen es el `!` inicial en las imágenes.

---

### Citas

```markdown
> Esto es una cita.
>
> Puede tener varios párrafos.
>> Y citas anidadas.
```

---

### Código

**Código en línea** — usa comillas invertidas `` ` ``:

```markdown
Usa el comando `npm install` para instalar dependencias.
```

**Bloque de código** — usa tres comillas invertidas ` ``` ` con el lenguaje opcional:

````markdown
```javascript
function saludar(nombre) {
  return `Hola, ${nombre}!`;
}
```

```python
def saludar(nombre):
    return f"Hola, {nombre}!"
```

```bash
echo "Hola Mundo"
```
````

---

### Línea horizontal

Tres o más guiones, asteriscos o guiones bajos en una línea sola:

```markdown
---
***
___
```

---

## Sintaxis avanzada

> Esta sintaxis es parte de **GitHub Flavored Markdown (GFM)** y puede no estar disponible en todos los renderizadores.

### Tablas

```markdown
| Columna 1 | Columna 2 | Columna 3 |
|-----------|:---------:|----------:|
| Izquierda | Centrado  | Derecha   |
| Dato A    | Dato B    | Dato C    |
```

**Alineación:**

| Símbolo | Efecto |
|---------|--------|
| `|---|` | Izquierda (por defecto) |
| `|:---:|` | Centrado |
| `|---:|` | Derecha |

---

### Listas de tareas

```markdown
- [x] Tarea completada
- [ ] Tarea pendiente
- [ ] Otra tarea pendiente
```

---

### Notas al pie

```markdown
Esto tiene una nota al pie[^1].

[^1]: Aquí está el contenido de la nota al pie.
```

---

### Texto resaltado y subíndices / superíndices

> Soporte varía según el renderizador:

```markdown
==texto resaltado==        <!-- resaltado -->
H~2~O                      <!-- subíndice -->
x^2^                       <!-- superíndice -->
```

---

### Bloques de advertencia (Callouts)

Soportados en GitHub y algunos procesadores:

```markdown
> [!NOTE]
> Información relevante que el lector debe tener en cuenta.

> [!WARNING]
> Advertencia importante antes de continuar.

> [!TIP]
> Consejo útil para el lector.
```

---

### Anchors y referencias internas

```markdown
## Mi sección {#mi-seccion}

[Ir a Mi Sección](#mi-seccion)
```

---

## Extensiones recomendadas para VS Code

Instala las extensiones desde `Ctrl+Shift+X`:

| Extensión | ID | Descripción |
|-----------|----|-------------|
| **Markdown All in One** | `yzhang.markdown-all-in-one` | Atajos, autocompletado, TOC automático |
| **Markdown Preview Enhanced** | `shd101wyy.markdown-preview-enhanced` | Vista previa avanzada con exportación |
| **Prettier** | `esbenp.prettier-vscode` | Formateador automático de Markdown |
| **markdownlint** | `davidanson.vscode-markdownlint` | Validación de estilo y sintaxis |
| **Paste Image** | `mushan.vscode-paste-image` | Pegar imágenes del portapapeles directamente |

---

## Atajos de teclado en VS Code

### Generales

| Acción | Windows/Linux | macOS |
|--------|--------------|-------|
| Abrir paleta de comandos | `Ctrl+Shift+P` | `Cmd+Shift+P` |
| Vista previa Markdown | `Ctrl+Shift+V` | `Cmd+Shift+V` |
| Vista previa al lado | `Ctrl+K V` | `Cmd+K V` |
| Terminal integrada | `` Ctrl+` `` | `` Cmd+` `` |
| Buscar y reemplazar | `Ctrl+H` | `Cmd+H` |
| Guardar archivo | `Ctrl+S` | `Cmd+S` |

### Con la extensión Markdown All in One

| Acción | Windows/Linux | macOS |
|--------|--------------|-------|
| Negrita | `Ctrl+B` | `Cmd+B` |
| Cursiva | `Ctrl+I` | `Cmd+I` |
| Generar tabla de contenidos | `Ctrl+Shift+P` → "Create TOC" | igual |
| Incrementar nivel de encabezado | `Ctrl+Shift+]` | `Cmd+Shift+]` |
| Decrecer nivel de encabezado | `Ctrl+Shift+[` | `Cmd+Shift+[` |

---

## Vista previa

VS Code incluye vista previa nativa de Markdown:

- **`Ctrl+Shift+V`** — abre la vista previa en una pestaña nueva
- **`Ctrl+K V`** — abre la vista previa al lado del editor

La vista previa se actualiza en tiempo real mientras escribes.

---

## Exportar a otros formatos

### Con la extensión Markdown Preview Enhanced

1. Abre la vista previa (`Ctrl+Shift+P` → "Markdown Preview Enhanced: Open Preview")
2. Haz clic derecho en la vista previa
3. Selecciona el formato de exportación:
   - **HTML** → `Export → HTML`
   - **PDF** → `Export → PDF` (requiere Puppeteer o Prince)
   - **Word (.docx)** → `Export → Word`

### Con Pandoc (línea de comandos)

Pandoc es una herramienta universal de conversión de documentos. Instálala desde [https://pandoc.org](https://pandoc.org).

```bash
# Markdown a HTML
pandoc documento.md -o documento.html

# Markdown a PDF (requiere LaTeX instalado)
pandoc documento.md -o documento.pdf

# Markdown a Word
pandoc documento.md -o documento.docx

# Markdown a PDF con estilos personalizados
pandoc documento.md -o documento.pdf --css=estilos.css

# Múltiples archivos Markdown en un solo documento
pandoc cap1.md cap2.md cap3.md -o libro.pdf
```

---

## Referencia rápida de sintaxis

```
# H1          ## H2         ### H3
**negrita**   *cursiva*     ~~tachado~~
`código`      [link](url)   ![img](ruta)
> cita        ---           - lista
1. ordenada   - [x] tarea   | tabla |
```

---

*Manual generado para Visual Studio Code · Markdown versión CommonMark + GFM*