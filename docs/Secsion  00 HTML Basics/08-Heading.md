<h1 align="center">BootCamp De HTML5 Session-0</h1>

<h2 align="center">0.5-Los Encabezados</h2>

<div align='center'>

 <![Image](https://github.com/user-attachments/assets/a47615e6-f177-4598-b943-e5526f035a1e)

</div>

<h2 align="center">Definición</h2>

Los encabezados HTML son títulos o subtítulos que desea mostrar en una página web.

Los encabezados en HTML son etiquetas (de `<h1>` a `<h6>`) que definen títulos y subtítulos en una página web, creando una jerarquía para organizar el contenido, mejorar la legibilidad y facilitar la comprensión a motores de búsqueda (SEO), siendo `<h1>` el título principal y más importante, y los siguientes niveles para secciones y subsecciones. También existe la etiqueta semántica `<header>`, que agrupa contenido introductorio como logotipos o menús, pero los encabezados de contenido son `<h1>` a `<h6>`.

## Tipos y uso

`<h1>` (Encabezado 1): El título más importante de la página, resume su tema principal y debe usarse solo una vez.

`<h2>` (Encabezado 2): Subtítulos principales que dividen el contenido en secciones clave.

`<h3>` a `<h6>`: Subtítulos de menor jerarquía para organizar subsecciones dentro de las secciones `<h2>`, y así sucesivamente, hasta `<h6>`.

### Ejemplo

<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>

Los encabezados HTML se definen con las etiquetas `<h1>`to `<h6>`.

`<h1>`define el encabezado más importante. `<h6>`define el encabezado menos importante.

### Ejemplo De Heaging

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

**Nota:** Los navegadores agregan automáticamente algunos espacios en blanco (un margen) antes y después de un encabezado.

## Importancia para SEO y experiencia de usuario

**Jerarquía:** Establecen una estructura clara que ayuda a los motores de búsqueda a entender la importancia y organización del contenido.<br>
**Legibilidad:** Permiten a los usuarios escanear rápidamente la página para encontrar la información que buscan, mejorando la experiencia de usuario (UX).<br>
**Buenas prácticas:** Se recomienda no saltarse niveles (ej., de `<h1>` a `<h3>` sin pasar por `<h2>`) para mantener una estructura lógica y semántica.<br>

## Diferencia con `<header>`

La etiqueta `<header>` es un contenedor semántico para contenido introductorio (logo, navegación), mientras que `<h1>` a `<h6>` son los títulos y subtítulos del contenido en sí.

## Los encabezados son importantes

Los motores de búsqueda utilizan los encabezados para indexar la estructura y el contenido de sus páginas web.<br>
Los usuarios suelen hojear una página por sus encabezados. Es importante usar encabezados para mostrar la estructura del documento.

` <h1>`Los encabezados deben usarse para los encabezados principales, seguidos de `<h2>`los encabezados, luego los menos importantes `<h3>`, y así sucesivamente.

### Por ejemplo

```html
<h1>- Título de la página
<h2>- Títulos de las secciones
<h3>- Subsecciones
```

### Ejemplo 2

```html
<h1>Travel Guide</h1>

<h2>Europe</h2>
<h3>France</h3>
<h3>Italy</h3>

<h2>Asia</h2>
<h3>India</h3>
<h3>Thailand</h3>
```

**Consejo:** utilice sólo uno `<h1>`por página: representa el tema o título principal.<br>
**Nota:** Use encabezados HTML solo para encabezados. No los use para agrandar el texto ni para que aparezcan en negrita .

## Encabezados más grandes

Cada encabezado HTML tiene un tamaño predeterminado. Sin embargo, puede especificar el tamaño de cualquier encabezado con el styleatributo, usando la font-sizepropiedad CSS:

### Ejemplo 3

```html
<h1 style="font-size:60px;">Heading 1</h1>
```
<br></br>

<div align="center">
    <h2>Referencia de etiquetas HTML</h2>
</div>

La referencia de etiquetas de W3Schools contiene información adicional sobre estas etiquetas y sus atributos.

<div align="center">

| Tag             | Description                         |
| --------------- | ----------------------------------- |
| `<html>`        | Define la raíz de un documento HTML |
| `<body>`        | Define el cuerpo del documento      |
| `<h1>` a `<h6>` | Define los encabezados HTML         |

</div>

<br>

## 📚 Fuente Bilbiográfica verificable:

**MDN Web Docs – HTML elements reference**
<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element" target="_blabk">CLik Aquí Para Ver La Fuente</a>


**WHATWG – HTML Living Standard**
<a href="https://html.spec.whatwg.org/" target="_blabk">CLik Aquí Para Ver La Fuente</a>

<br>

## Lista completa de todas las etiquetas HTML disponibles, visita nuestra <a href="https://www.w3schools.com/tags/default.asp" target="_blamk">Referencia de etiquetas HTML.</a> también en el capítulo 0.4 de esta sección encontrarás la lista completa.
