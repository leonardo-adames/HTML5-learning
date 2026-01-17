# BootCamp De HTML5 - Session 00

## 03 Estructura en HTML

### Estructura del documento

Los documentos HTML incluyen una declaración de tipo de documento y el elemento raíz `<html>`. El encabezado y el cuerpo del documento se anidan en el elemento `<html>`. Si bien el encabezado del documento no es visible para el visitante vidente, es fundamental que el sitio funcione. Contiene toda la metainformación, incluida la información de los motores de búsqueda y los resultados de redes sociales, los íconos de la pestaña del navegador y el acceso directo a la pantalla principal de un dispositivo móvil, y el comportamiento y la presentación de tu contenido. En esta sección, descubrirás los componentes que, aunque no están visibles, están presentes en casi todas las páginas web.

Para crear el sitio **MachineLearningWorkshop.com** (`MLW`), empieza por incluir los componentes que deben considerarse esenciales para cada página web: el tipo de documento, el lenguaje humano del contenido, el grupo de caracteres y, por supuesto, el título o nombre del sitio o la aplicación.

---

### Agregar a todos los documentos HTML

Hay varias características que se deben considerar esenciales para todas y cada una de las páginas web. Los navegadores seguirán renderizando contenido si faltan estos elementos, pero los incluyen. siempre.

---

### `<!DOCTYPE htm>`

Lo primero que hay en un documento HTML es el preámbulo. Para HTML, solo necesitas `<!DOCTYPE html>`. Esto puede parecer un elemento HTML, pero no lo es. Es un tipo especial de nodo llamado "doctype". El doctype le indica al navegador que use el modo de estándares. Si se omite, los navegadores usarán un modo de renderización diferente, conocido como modo no estándar. Incluir el doctype ayuda a prevenir el modo no estándar.

### `<html>`

El elemento `<html>` es el elemento raíz de un documento HTML. Es el elemento superior de `<head>` y `<body>`, y contiene todo lo que está en el documento HTML, excepto el doctype. Si se omite, será implícito, pero es importante incluirlo, ya que este es el elemento en el que se declara el idioma del contenido del documento.

### Idioma del contenido

El atributo de idioma lang agregado a la etiqueta `<html>` define el idioma principal del documento. El valor del atributo lang es un código de idioma ISO de dos o tres letras seguido de la región. La región es opcional, pero se recomienda usarla, ya que el idioma puede variar mucho entre regiones. Por ejemplo, el francés es muy diferente en Canadá `(fr-CA)` en comparación con Burkina Faso `(fr-BF)`. Esta declaración de idioma permite que los lectores de pantalla, los motores de búsqueda y los servicios de traducción conozcan el idioma del documento.

El atributo lang no se limita a la etiqueta `<html>`. Si la página contiene texto en un idioma distinto al del documento principal, se debe usar el atributo lang para identificar las excepciones al idioma principal del documento. Al igual que cuando se incluye en el encabezado, el atributo lang en el cuerpo no tiene efecto visual. Solo agrega semántica, lo que permite que las tecnologías de accesibilidad y los servicios automatizados conozcan el idioma del contenido afectado.

Además de configurar el idioma del documento y las excepciones a ese idioma base, el atributo se puede usar en selectores CSS. Puedes segmentar tus anuncios para **`<span lang="fr-fr">`**Ceci n'est pas une pipe.**`</span>`** con los selectores de idioma y atributo `[lang|="fr"]` y :`lang(fr)`.

### `<head>`

Anidados entre las etiquetas `<html>` de apertura y cierre, encontramos los dos elementos secundarios, `<head>` y `<body>`:

```html
<!DOCTYPE html>         <!--DEFINE EL TIPO DE COCUMENTO-->
<html lang="en-US">     <!--DEFINE TODO EL COCUMENTO HMTL + IDIOMA (APERTURA)-->
  <head>                <!--CONTENEDOR DE METADATOS DEL COCUMENTO (APERTURA)-->
  </head>               <!--CONTENEDOR DE METADATOS DEL COCUMENTO (CIERRE)-->
  <body>                <!--CUERPO DEL COCUMENTO (APERTURA)-->
  </body>               <!--CUERPO DEL COCUMENTO (CIERRE)-->
</html>                 <!--DEFINE TODO EL COCUMENTO HMTL (CIERRE)-->
```

El `<head>`, o encabezado de metadatos del documento, contiene todos los metadatos de un sitio o una aplicación. El cuerpo incluye el contenido visible. El resto de esta sección se centra en los componentes que se encuentran anidados dentro de la `<head></head>` de apertura y cierre.

### Componentes obligatorios dentro de <head>

Los metadatos del documento, incluidos el título, el grupo de caracteres, la configuración del viewport, la descripción, la URL base, los vínculos a las hojas de estilo y los íconos, se encuentran en el elemento `<head>`. Si bien es posible que no necesites todas estas funciones, incluye siempre el grupo de caracteres, el título y la configuración del viewport.

### Codificación de caracteres

El primer elemento de `<head>` debe ser la declaración de codificación de caracteres de charset. Se encuentra antes del título para garantizar que el navegador pueda procesar los caracteres de ese título y todos los caracteres del resto del documento.

La <a href="https://html.spec.whatwg.org/multipage/parsing.html#documentEncoding">codificación predeterminada</a> en la mayoría de los navegadores es windows-1252, según la configuración regional. Sin embargo, debes usar `UTF-8`, ya que habilita la codificación de uno a cuatro bytes para todos los caracteres, incluso aquellos que ni siquiera sabías que existían. Además, es el tipo de codificación requerido por `HTML5`.

Para establecer la codificación de caracteres en UTF-8, incluye lo siguiente:

```HTML
<meta charset="utf-8" />
```

Si declaras `UTF-8` (no distingue mayúsculas de minúsculas), incluso puedes incluir emojis en el título.

La codificación de caracteres se hereda en todo el contenido del documento, incluso en `<style>` y `<script>`. Esta pequeña declaración significa que puedes incluir emojis en los nombres de las clases y en la API del selector (nuevamente, no lo hagas). Si usas emojis, asegúrate de usarlos de una manera que mejore la usabilidad sin dañar la accesibilidad.

### Título del documento

Tu página principal y todas las páginas adicionales deben tener un título único. El contenido del título del documento, el texto entre las etiquetas `<title>` de apertura y cierre, se muestra en la pestaña del navegador, la lista de ventanas abiertas, el historial, los resultados de la búsqueda y, a menos que se redefinen con <a href="https://web.dev/learn/html/metadata?hl=es-419">etiquetas`<meta>`</a>, en tarjetas de redes sociales.

```html
<title>Machine Learning Workshop</title>
```

### Metadatos de viewport

La otra metaetiqueta que debe considerarse esencial es la <a href="https://web.dev/learn/design/intro?hl=es-419#a_meta_element_for_viewport">viewport</a>, que ayuda a mejorar la capacidad de respuesta del sitio y permite que el contenido se procese correctamente de forma predeterminada, sin importar el ancho de la viewport. Si bien la <a href="https://developer.mozilla.org/es/docs/Web/HTML/Reference/Elements/meta/name/viewport">metaetiqueta de la ventana de visualización</a> existe desde junio de 2007, cuando se lanzó el primer iPhone, <a href="https://drafts.csswg.org/css-viewport/#viewport-meta">se documentó en una especificación recientemente</a>. Ya que permite controlar el tamaño y la escala de un viewport, y evita que se reduzca el tamaño del contenido del sitio para que se ajuste a un sitio de 960 px en una pantalla de 320 px, es definitivamente recomendable.

```html
<meta name="viewport" content="width=device-width" />
```

El código anterior significa "hacer que el sitio sea responsivo, comenzando por hacer que el ancho del contenido sea el ancho de la pantalla". Además de `width`, puedes configurar el zoom y la escalabilidad, pero ambos tienen valores accesibles de forma predeterminada. Si quieres ser explícito, incluye lo siguiente:

```html
<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=1" />
```

La vista del puerto es parte de la <a href="https://dequeuniversity.com/rules/axe/4.4/meta-viewport">auditoría de accesibilidad de Lighthouse</a>. que tu sitio pasará si es escalable y no tiene un tamaño máximo establecido.

Hasta ahora, el esquema de nuestro archivo HTML es el siguiente:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Machine Learning Workshop</title>
    <meta name="viewport" content="width=device-width" />
  </head>
  <body>

  </body>
</html>
```

**OTROS CONTENIDOS DE `<head>`**

Se incluye mucho más en `<head>`. Todos los metadatos, de hecho. La mayoría de los elementos que encontrarás en `<head>` se tratan aquí, a la vez que se guarda una gran cantidad de opciones de `<meta>` para el siguiente capítulo.

Ya viste el grupo de metacaracteres y el título del documento, pero hay muchos más metadatos además de las etiquetas `<meta>` que se deben incluir.

<a href="https://web.dev/learn/html/document-structure?continue=https%3A%2F%2Fweb.dev%2Flearn%2Fhtml&hl=es-419#article-https://web.dev/learn/html/document-structure&hl=es-419">Click aqui ara Saber mas</a>
