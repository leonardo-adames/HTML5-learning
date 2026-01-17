<h1 align="center">BootCamp De HTML5 Session-0</h1>

<h2 align="center">0.4-Los Atributos</h2>

<hr>

<div align='center'>
    <img src="https://desarrolloweb.readthedocs.io/en/latest/_images/AtributeExample.png"
    width=950px;/>
</div>

<h2 align="center">Definición</h2>

Los atributos en HTML son pares nombre/valor que se añaden a las etiquetas de apertura para proporcionar información adicional o configurar el comportamiento y la funcionalidad de un elemento, como especificar la fuente de una imagen (src) o el destino de un enlace (href), mejorando la interactividad y la accesibilidad de una página web.

<hr>

<h2>Características y ejemplos:</h2>

* **Definición:** Son palabras especiales dentro de la etiqueta de apertura (`<tag>`) que modifican o dan contexto al elemento.
* **Sintaxis:** Se escriben como nombre="valor" dentro de la etiqueta de apertura, separados por espacios, por ejemplo: `<img src="imagen.jpg" alt="Descripción">`.
* **Función:** Ajustan el comportamiento o la visualización predeterminada de un elemento
* **Todos los elementos HTML** pueden tener atributos
* **Los atributos** proporcionan información adicional sobre los elementos
* **Los atributos** siempre se especifican en la etiqueta de inicio
* **Los atributos** suelen aparecer en pares nombre/valor como: `nombre="valor"`.

<hr>

<h2>Ejemplos comunes:</h2>

* **href:** Define la URL de destino para los enlaces (`<a>`).
* **src:** Especifica la ruta de un recurso, como una imagen (<`img>`).
* **alt:** Proporciona texto alternativo para imágenes, crucial para accesibilidad y SEO.
* **class:** Permite agrupar elementos para aplicar estilos CSS o manipularlos con JavaScript.
* **id:** Asigna un identificador único a un elemento.
* **style:** Aplica estilos CSS directamente al elemento.

<hr>

<h2>Tipos de atributos:</h2>

* **Globales:** Se pueden usar en casi todos los elementos HTML (ej. id, class, style, title).
* **Específicos:** Solo funcionan con ciertos elementos (ej. href solo con `<a>`, src con `<img>` y `<script>`).
* **De evento:** Ejecutan código JavaScript cuando ocurre un evento (ej. onclick, onmouseover).
* **Data:** Atributos personalizados para almacenar datos específicos del elemento (data-nombre).

En resumen, los atributos son esenciales para que HTML no solo defina la estructura, sino también el propósito y la interactividad de cada parte de una página web.

---
<br></br>

<h1 align="center">BootCamp De HTML5 Session-0</h1>

<h2 align="center">0.4-Tipos Atributos</h2>

## El atributo href

La `<a>`etiqueta define un hipervínculo. El hrefatributo especifica la URL de la página a la que dirige el enlace:

### Ejemplo De `href`

```html
<a href="https://www.w3schools.com">Visit W3Schools</a>
```

**Aprenderá más sobre los enlaces en nuestro capítulo Enlaces HTML.**

## El atributo `src`

La `<img>`etiqueta se utiliza para incrustar una imagen en una página HTML. El srcatributo especifica la ruta a la imagen que se mostrará:

### Ejemplo De src

```html
<img src="img_girl.jpg">
```

### Hay dos formas de especificar la URL en el src atributo

* **1. URL absoluta:** Enlaces a una imagen externa alojada en otro sitio web. Ejemplo: `src="https://www.w3schools.com/images/img_girl.jpg"`.

* **Notas:** Las imágenes externas pueden estar sujetas a derechos de autor. Si no obtiene permiso para usarlas, podría estar infringiendo las leyes de derechos de autor. Además, no puede controlar las imágenes externas; podrían ser eliminadas o modificadas repentinamente.

* **2. URL relativa:** Enlaza a una imagen alojada en el sitio web. En este caso, la URL no incluye el nombre de dominio. Si la URL comienza sin barra, será relativa a la página actual. Ejemplo: `src="img_girl.jpg"`. Si la URL comienza con barra, será relativa al dominio. Ejemplo: `src="/images/img_girl.jpg"`.

* **Consejo:** Casi siempre es mejor usar `URL relativas`. No se romperán si cambias de dominio.

## Los atributos de ``width y `heigth`

La `<img>`etiqueta también debe contener los atributos `width` y `height`, que especifican el ancho y la altura de la imagen (en píxeles):

### Ejemplo De img

```html
<img src="img_girl.jpg" width="500" height="600">
```

## El atributo `alt`

El atributo requerido altde la `<img>` etiqueta especifica un texto alternativo para una imagen si, por algún motivo, esta no se puede mostrar. Esto puede deberse a una conexión lenta, a un error en el srcatributo o a que el usuario utiliza un lector de pantalla.

### Ejemplo De alt

```html
<img src="img_girl.jpg" alt="Girl with a jacket">
```

Veamos lo que sucede si intentamos mostrar una imagen que no existe:

```html
<img src="img_typo.jpg" alt="Girl with a jacket">
```

## El atributo de `style`

El atributo `style` se utiliza para agregar estilos a un elemento, como color, fuente, tamaño y más.

### Ejemplo De style

```html
<p style="color:red;">This is a red paragraph.</p>
```

**Aprenderá más sobre los estilos en nuestro capítulo Estilos HTML.**

## El atributo `lang`

Siempre debe incluir el langatributo dentro de la `<html>`etiqueta para declarar el idioma de la página web. Esto facilita la navegación en motores de búsqueda y navegadores.

El siguiente ejemplo especifica el inglés como idioma:

```html
<!DOCTYPE html>
<html lang="en">
<body>
...
</body>
</html>
```

También se pueden añadir códigos de país al código de idioma en el lang atributo. Así, los dos primeros caracteres definen el idioma de la página HTML y los dos últimos, el país.

El siguiente ejemplo especifica inglés como idioma y Estados Unidos como país:

```html
<!DOCTYPE html>
<html lang="en-US">
<body>
...
</body>
</html>
```

**Puede ver todos los códigos de idioma en nuestra Referencia de código de idioma HTML.**

## El Atributo `title`

El atributo `title` define información adicional sobre un elemento.<br>El valor del atributo de título se mostrará como información sobre herramientas cuando pase el mouse sobre el elemento:

### Ejemplo De title

```html
<p title="I'm a tooltip">This is a paragraph.</p>
```

**Sugerimos:** utilice siempre atributos en minúsculas<br>El estándar HTML no requiere nombres de atributos en minúsculas.

El atributo de título (y todos los demás atributos) se pueden escribir en mayúsculas o minúsculas como title o TITLE .<br>
Sin embargo, la buena practica recomienda atributos en minúscula en HTML y exige atributos en minúscula para tipos de documentos más estrictos como XHTML.

**Sugerimos:** Siempre citar los valores de los atributos<br>
El estándar HTML no requiere comillas alrededor de los valores de los atributos, Sin embargo, se recomienda usar comillas en HTML y las exige para tipos de documentos más estrictos como XHTML.

Bien:

```html
<a href="https://www.w3schools.com/html/">Visit our HTML tutorial</a>
```

Malo:

```html
<a href=https://www.w3schools.com/html/>Visit our HTML tutorial</a>

```

A veces es necesario usar comillas. Este ejemplo no mostrará correctamente el atributo de título porque contiene un espacio:

### Ejemplo

```html
<p title=Description of W3Schools>
```

<div class="wd-embed" style="height: 300px; width: 100%">
  <iframe allow="camera; clipboard-read; clipboard-write; encrypted-media; geolocation; microphone; midi;" loading="lazy" src="https://codepen.io/web-dot-dev/embed/GRGzbXR?height=300&amp;theme-id=dark&amp;default-tab=html%2Cresult&amp;editable=true" style="height: 100%; width: 100%; border: 0;" data-title="Pen GRGzbXR de web-dot-dev en Codepen"></iframe>
</div>

## ¿Comillas simples o dobles?

Las comillas dobles `" "` alrededor de los valores de atributos son las más comunes en HTML, pero también se pueden utilizar comillas simples.<br>
En algunas situaciones, cuando el valor del atributo en sí contiene comillas dobles, es necesario utilizar comillas simples `' '`:

```html
<p title='John "ShotGun" Nelson'>
```

O viceversa:

```html
<p title="John 'ShotGun' Nelson">
```

### Resumen del capítulo

* **Todos los elementos** ´HTML´ pueden tener atributos<br>
* **El atributo href** de `<a>`especifica la URL de la página a la que va el enlace.<br>
* **El atributo src** de `<img>`especifica la ruta a la imagen que se mostrará<br>
* **Los atributos `height` y  `width` proporcionan información de tamaño para las imágenes`<img>`<br>
* **El atributo alt** de `<img>`proporciona un texto alternativo para una imagen.<br>
* **El atributo style** se utiliza para agregar estilos a un elemento, como color, fuente, tamaño y más.<br>
* **El atributo lang** de la `<html>`etiqueta declara el idioma de la página web.<br>
* **El atributo title** define información adicional sobre un elemento.

<br></br>

## Referencia de atributos HTML

Una lista completa de todos los atributos para cada elemento HTML se encuentra en nuestra: <a href= "https://www.w3schools.com/tags/ref_attributes.asp" target="_blank">Referencia de atributos HTML</a> .

**La siguiente tabla enumera todos los `atributos HTML` y en qué elementos se pueden utilizar:**

<br></br>

<div align="center">
    <b>🧠 1. Atributos Globales (Global Attributes)</b>
</div>

<hr>
<div align="center">

| Attribute       | Belongs to        | Description                                                                       |
| --------------- | ----------------- | --------------------------------------------------------------------------------- |
| accesskey       | Global Attributes | Especifica una tecla de acceso rápido para activar o enfocar un elemento          |
| class           | Global Attributes | Especifica uno o más nombres de clase para un elemento                            |
| contenteditable | Global Attributes | Especifica si el contenido de un elemento es editable o no                        |
| data-*          | Global Attributes | Se utiliza para almacenar datos personalizados privados de la página o aplicación |
| dir             | Global Attributes | Especifica la dirección del texto del contenido                                   |
| draggable       | Global Attributes | Especifica si un elemento es arrastrable o no                                     |
| enterkeyhint    | Global Attributes | Especifica el texto de la tecla Enter en un teclado virtual                       |
| hidden          | Global Attributes | Especifica que un elemento aún no es relevante o ha dejado de serlo               |
| id              | Global Attributes | Especifica un identificador único para un elemento                                |
| inert           | Global Attributes | Especifica que el navegador debe ignorar esta sección                             |
| inputmode       | Global Attributes | Especifica el modo del teclado virtual                                            |
| lang            | Global Attributes | Especifica el idioma del contenido del elemento                                   |
| popover         | Global Attributes | Especifica un elemento emergente (popover)                                        |
| spellcheck      | Global Attributes | Especifica si se debe comprobar la ortografía y gramática                         |
| style           | Global Attributes | Especifica un estilo CSS en línea para un elemento                                |
| tabindex        | Global Attributes | Especifica el orden de tabulación de un elemento                                  |
| title           | Global Attributes | Especifica información adicional sobre un elemento                                |
| translate       | Global Attributes | Especifica si el contenido debe traducirse o no                                   |


</div>

<br></br>

<div align="center">
    <b>🧾 2. Atributos de Formularios (Forms & Inputs).</b>
</div>

<div align="center">

| Attribute      | Belongs to                                                                                                          | Description                                                                    |
| -------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| accept         | `<input>`                                                                                                           | Especifica los tipos de archivos que el servidor acepta                        |
| accept-charset | `<form>`                                                                                                            | Especifica las codificaciones de caracteres usadas en el envío del formulario  |
| action         | `<form>`                                                                                                            | Especifica dónde enviar los datos del formulario                               |
| autocomplete   | `<form>, <input>`                                                                                                   | Especifica si el formulario o campo debe usar autocompletado                   |
| autofocus      | `<button>, <input>, <select>, <textarea>`                                                                           | Especifica que el elemento obtiene el foco automáticamente al cargar la página |
| checked        | `<input>`                                                                                                           | Especifica que un input debe estar preseleccionado                             |
| dirname        | `<input>, <textarea>`                                                                                               | Especifica que se enviará la dirección del texto                               |
| disabled       | `<button>, <fieldset>, <input>, <optgroup>, <option>, <select>, <textarea>`                                         | Especifica que el elemento o grupo debe estar deshabilitado                    |
| enctype        | `<form>`                                                                                                            | Especifica cómo deben codificarse los datos al enviarse                        |
| for            | `<label>, <output>`                                                                                                 | Especifica a qué elemento del formulario está asociado                         |
| form           | `<button>, <fieldset>, <input>, <label>, <meter>, <object>, <output>, <select>, <textarea>`                         | Especifica el formulario al que pertenece el elemento                          |
| formaction     | `<button>, <input>`                                                                                                 | Especifica dónde enviar los datos del formulario (solo submit)                 |
| list           | `<input>`                                                                                                           | Hace referencia a un elemento `<datalist>`                                     |
| max            | `<input>, <meter>, <progress>`                                                                                      | Especifica el valor máximo permitido                                           |
| maxlength      | `<input>, <textarea>`                                                                                               | Especifica el número máximo de caracteres permitidos                           |
| method         | `<form>`                                                                                                            | Especifica el método HTTP usado para enviar el formulario                      |
| min            | `<input>, <meter>`                                                                                                  | Especifica el valor mínimo permitido                                           |
| multiple       | `<input>, <select>`                                                                                                 | Permite introducir más de un valor                                             |
| name           | `<button>, <fieldset>, <form>, <iframe>, <input>, <map>, <meta>, <object>, <output>, <param>, <select>, <textarea>` | Especifica el nombre del elemento                                              |
| novalidate     | `<form>`                                                                                                            | Especifica que el formulario no debe validarse al enviarse                     |
| pattern        | `<input>`                                                                                                           | Especifica una expresión regular para validar el valor                         |
| placeholder    | `<input>, <textarea>`                                                                                               | Especifica una pista corta del valor esperado                                  |
| readonly       | `<input>, <textarea>`                                                                                               | Especifica que el campo es de solo lectura                                     |
| required       | `<input>, <select>, <textarea>`                                                                                     | Especifica que el campo debe completarse antes de enviar                       |
| rows           | `<textarea>`                                                                                                        | Especifica el número visible de líneas                                         |
| size           | `<input>, <select>`                                                                                                 | Especifica el ancho o número de opciones visibles                              |
| step           | `<input>`                                                                                                           | Especifica los intervalos legales de valores                                   |
| type           | `<a>, <button>, <embed>, <input>, <link>, <menu>, <object>, <script>, <source>, <style>`                            | Especifica el tipo de elemento                                                 |
| value          | `<button>, <input>, <li>, <option>, <meter>, <progress>, <param>`                                                   | Especifica el valor del elemento                                               |
| wrap           | `<textarea>`                                                                                                        | Especifica cómo se ajusta el texto al enviarse                                 |


</div>

<br></br>

<div align="center">
    <b>🎥3. Atributos Multimedia</b>
</div>

<div align="cente">

| Attribute | Belongs to                                                                         | Description                                                  |
| --------- | ---------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| autoplay  | `<audio>, <video>`                                                                 | Especifica que el audio o video se reproduce automáticamente |
| controls  | `<audio>, <video>`                                                                 | Especifica que se muestren controles de reproducción         |
| loop      | `<audio>, <video>`                                                                 | Especifica que el medio se repita                            |
| muted     | `<video>, <audio>`                                                                 | Especifica que el audio esté silenciado                      |
| poster    | `<video>`                                                                          | Especifica una imagen mientras se descarga el video          |
| preload   | `<audio>, <video>`                                                                 | Especifica cómo debe cargarse el medio                       |
| src       | `<audio>, <embed>, <iframe>, <img>, <input>, <script>, <source>, <track>, <video>` | Especifica la URL del archivo multimedia                     |
| srcdoc    | `<iframe>`                                                                         | Especifica el contenido HTML del iframe                      |
| srclang   | `<track>`                                                                          | Especifica el idioma de los subtítulos                       |
| srcset    | `<img>, <source>`                                                                  | Especifica imágenes alternativas según el contexto           |
| sizes     | `<img>, <link>, <source>`                                                          | Especifica el tamaño del recurso                             |
| usemap    | `<img>, <object>`                                                                  | Especifica un mapa de imagen del lado del cliente            |
| width     | `<canvas>, <embed>, <iframe>, <img>, <input>, <object>, <video>`                   | Especifica el ancho del elemento                             |
| height    | `<canvas>, <embed>, <iframe>, <img>, <input>, <object>, <video>`                   | Especifica la altura del elemento                            |

</div>

<br></br>

<div align="center">
    <b>🧩 4. Atributos de Eventos</b>
</div>

<div alig="center">


| Attribute   | Belongs to                                                    | Description                                                |
| ----------- | ------------------------------------------------------------- | ---------------------------------------------------------- |
| onclick     | All visible elements                                          | Script que se ejecuta cuando se hace clic                  |
| onchange    | All visible elements                                          | Script que se ejecuta cuando cambia el valor               |
| oninput     | All visible elements                                          | Script que se ejecuta cuando hay entrada del usuario       |
| onsubmit    | `<form>`                                                      | Script que se ejecuta al enviar un formulario              |
| onload      | `<body>, <iframe>, <img>, <input>, <link>, <script>, <style>` | Script que se ejecuta cuando el elemento termina de cargar |
| onfocus     | All visible elements                                          | Script que se ejecuta cuando el elemento obtiene el foco   |
| onblur      | All visible elements                                          | Script que se ejecuta cuando el elemento pierde el foco    |
| onkeydown   | All visible elements                                          | Script que se ejecuta al presionar una tecla               |
| onkeyup     | All visible elements                                          | Script que se ejecuta al soltar una tecla                  |
| onmouseover | All visible elements                                          | Script que se ejecuta al pasar el mouse                    |
| onmouseout  | All visible elements                                          | Script que se ejecuta al salir el mouse                    |
| onwheel     | All visible elements                                          | Script que se ejecuta al usar la rueda del mouse           |


</div>

<div align="center">
    <b>📚 Fuentes Bibliográfica</b>
</div>

## 1️⃣ MDN Web Docs (Mozilla Foundation)

**Autor** institucional: Mozilla Foundation<br>
**Título:** HTML attribute reference<br>
**Descripción:** Documentación técnica oficial y mantenida sobre atributos HTML, eventos, atributos globales y específicos por elemento.<br>
**URL:**
https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes<br>
**Eventos HTML:**
https://developer.mozilla.org/en-US/docs/Web/Events<br>
**Atributos globales:**
https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes

<hr>

## 2️⃣ WHATWG – HTML Living Standard

**Autor institucional:** WHATWG (Web Hypertext Application Technology Working Group)<br>
**Título:** HTML Living Standard<br>
**Descripción:** Especificación oficial y normativa de HTML (estándar vivo).<br>
**URL:**
https://html.spec.whatwg.org/

<hr>

## 3️⃣ W3Schools – HTML Attribute Reference

**Autor institucional:** Refsnes Data<br>
**Título:** HTML Attribute Reference<br>
**Descripción:** Referencia práctica y estructurada de atributos HTML, muy alineada con el formato de tu tabla original.<br>
**URL:**
https://www.w3schools.com/tags/ref_attributes.asp<br>
**Eventos HTML:**
https://www.w3schools.com/jsref/dom_obj_event.asp

<hr>

## 4️⃣ W3C (World Wide Web Consortium) — Referencia histórica

**Autor institucional:** World Wide Web Consortium (W3C)<br>
**Título:** HTML5 Specification<br>
**Descripción:** Especificación histórica de HTML5 (ya no es el estándar activo).<br>
**URL:**
https://www.w3.org/TR/html52/
