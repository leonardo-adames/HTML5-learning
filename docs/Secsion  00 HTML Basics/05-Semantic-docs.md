# BootCamp De HTML5 - Session 00

## 05 Semantica en HTML

### Estructura Semantica del documento

Con más de 100 elementos `HTML` y la capacidad de crear elementos personalizados, existen infinitas formas de marcar tu contenido. Sin embargo, algunas formas, en particular las semánticas, son mejores que otras.

Semántico significa "relacionado con el significado". Escribir código `HTML` semántico significa usar elementos `HTML` para estructurar tu contenido según el significado de cada elemento, no su apariencia.

En esta serie, aún no se abordaron muchos elementos `HTML`, pero, incluso sin conocer `HTML`, los siguientes dos fragmentos de código muestran cómo el lenguaje de marcado semántico puede proporcionar contexto al contenido. Ambos usan un recuento de palabras en lugar de ipsum lorem para ahorrar algo de desplazamiento. Usa tu imaginación para expandir "treinta palabras" a 30 palabras:

El primer fragmento de código usa `<div>` y `<span>`, dos elementos sin valor semántico.

```html
<div>
  <span>Three words</span>
  <div>
    <a>one word</a>
    <a>one word</a>
    <a>one word</a>
    <a>one word</a>
  </div>
</div>
<div>
  <div>
    <div>five words</div>
  </div>
  <div>
    <div>three words</div>
    <div>forty-six words</div>
    <div>forty-four words</div>
  </div>
  <div>
    <div>seven words</div>
    <div>sixty-eight words</div>
    <div>forty-four words</div>
  </div>
</div>
<div>
   <span>five words</span>
</div>
```

**¿Tienes una idea de lo que significan esas palabras? En realidad, no.**

Reescribamos este código con elementos semánticos:

```html
<header>
  <h1>Three words</h1>
  <nav>
    <a>one word</a>
    <a>one word</a>
    <a>one word</a>
    <a>one word</a>
  </nav>
</header>
<main>
  <header>
    <h2>five words</h2>
  </header>
  <section>
    <h2>three words</h2>
    <p>forty-six words</p>
    <p>forty-four words</p>
  </section>
  <section>
    <h3>seven words</h3>
    <p>sixty-eight words</p>
    <p>forty-four words</p>
  </section>
</main>
<footer>
  <p>five words</p>
</footer>
```

¿Qué bloque de código transmitió significado? Si solo usas los elementos no semánticos de `<div>` y `<span>`, no puedes saber qué representa el contenido del primer bloque de código. El segundo ejemplo de código, con elementos semánticos, proporciona suficiente contexto para que una persona que no sabe programar descifre el propósito y el significado sin haber visto nunca una etiqueta `HTML`. Sin duda, proporciona suficiente contexto para que el desarrollador comprenda el esquema de la página, incluso si no entiende el contenido, como el contenido en un idioma extranjero.

En el segundo bloque de código, podemos comprender la arquitectura incluso sin entender el contenido, ya que los elementos semánticos proporcionan significado y estructura. Puedes ver que el primer encabezado es el banner del sitio, y es probable que `<h1>` sea el nombre del sitio. El pie de página es el pie de página del sitio: Las cinco palabras pueden ser una declaración de derechos de autor o la dirección de la empresa.

El lenguaje de marcado semántico no solo facilita la lectura del lenguaje de marcado para los desarrolladores, sino que es fundamental para ayudar a las herramientas automatizadas a descifrar el lenguaje de marcado. Las herramientas para desarrolladores demuestran cómo los elementos semánticos también proporcionan una estructura legible por máquina.

### Modelo de objetos de accesibilidad (AOM)

A medida que el navegador analiza el contenido recibido, compila el modelo de objetos del documento (`DOM`) y el modelo de **objetos CSS** (`CSSOM`). Luego, también compila un árbol de accesibilidad. Los dispositivos de asistencia, como los lectores de pantalla, usan el AOM para analizar e interpretar el contenido. El `DOM` es un árbol de todos los nodos del documento. El AOM es como una versión semántica del DOM.

<p align="center">
  <img src="https://web.dev/static/learn/html/semantic-html/image/a-list-nodes-are-link-ecd99b332edd7_856.png?hl=es-419" width="200" />
  <img src="https://web.dev/static/learn/html/semantic-html/image/a-list-nodes-clear-land-42d8c845e5b74_856.png?hl=es-419" width="200" />
</p>

En la figura 2, hay cuatro roles de puntos de referencia en el segundo bloque de código. Utiliza puntos de referencia semánticos denominados convenientemente `<header>`, `<main>`, `<footer>` y `<nav>` para la "navegación". Los puntos de referencia proporcionan estructura al contenido web y ayudan a indicar secciones importantes del contenido para que los usuarios de lectores de pantalla puedan navegar por ellas con el teclado.

`<header>` y `<footer>` son puntos de referencia, con los roles de banner y contentinfo, respectivamente, cuando no están anidados en otros puntos de referencia. El AOM de Chrome muestra esto de la siguiente manera:

<p align="center">
  <img src="https://web.dev/static/learn/html/semantic-html/image/all-text-nodes-are-listed-3f0a6e26b2d99_856.png?hl=es-419" width="200" />
  <img src="https://web.dev/static/learn/html/semantic-html/image/the-text-nodes-have-desc-9cd0a6c89d981_856.png?hl=es-419" width="200" />

</p>

Si observas las Herramientas para desarrolladores de Chrome, notarás una diferencia significativa entre el modelo de objetos de accesibilidad cuando se usan elementos semánticos y cuando no se usan.

Es bastante claro que el uso de elementos semánticos ayuda a la accesibilidad, mientras que el uso de elementos no semánticos la reduce. En general, el `HTML` es accesible de forma predeterminada. Nuestro trabajo como desarrolladores es proteger la naturaleza accesible predeterminada del `HTML` y maximizar la accesibilidad para nuestros usuarios. Puedes <a href="https://developer.chrome.com/docs/devtools/accessibility/reference?hl=es-419#explore-tree">inspeccionar el AOM en las herramientas para desarrolladores</a>.

### El atributo role

El atributo role describe el rol que tiene un elemento en el contexto del documento. El atributo role es un atributo global, lo que significa que es válido en todos los elementos, definido por la especificación de ARIA en lugar de la especificación de HTML de WHATWG, donde se define casi todo lo demás en esta serie.

Cada elemento semántico tiene un rol implícito, y algunos dependen del contexto. Como vimos en la captura de pantalla de las herramientas para desarrolladores de accesibilidad de Firefox, los elementos `<header>`,`<main>`, `<footer>` y `<nav>` de nivel superior eran todos puntos de referencia, mientras que el elemento `<header>` anidado en `<main>` era una sección. En la captura de pantalla de Chrome, se enumeran los roles de ARIA de estos elementos: `<main>` es main, `<nav>` es navigation y `<footer>`, como era el pie de página del documento, es contentinfo. Cuando `<header>` es el encabezado del documento, el rol predeterminado es banner, que define la sección como el encabezado global del sitio. Cuando un `<header>` o un `<footer>` se anidan dentro de un elemento de seccionamiento, no tienen un rol de referencia. Las capturas de pantalla de ambas herramientas para desarrolladores muestran esto.

Los nombres de los roles de los elementos son importantes para crear el AOM. La semántica de un elemento, o "rol", es importante para las tecnologías de asistencia y, en algunos casos, para los motores de búsqueda. Los usuarios de tecnología de asistencia dependen de la semántica para navegar por el contenido y comprender su significado. El rol del elemento permite que el usuario acceda al contenido que busca rápidamente y, posiblemente, lo que es más importante, el rol le informa al usuario del lector de pantalla cómo interactuar con un elemento interactivo una vez que tiene el enfoque.

Todos los elementos interactivos, como los botones, los vínculos, los rangos y las casillas de verificación, tienen roles implícitos, se agregan automáticamente a la secuencia de tabulación del teclado y admiten la acción predeterminada esperada del usuario. El rol implícito o el valor role explícito le indican al usuario que espere interacciones predeterminadas específicas del elemento.

Con el atributo role, puedes asignar un rol a cualquier elemento, incluso un rol diferente al que implica la etiqueta. Por ejemplo, `<button>` tiene el rol implícito de button. Con role="button", puedes convertir cualquier elemento de forma semántica en un botón: `<p role="button">Click Me</p>`.

Si bien agregar role="button" a un elemento informa a los lectores de pantalla que el elemento es un botón, no cambia la apariencia ni la funcionalidad del elemento. El elemento button proporciona muchas funciones sin que tengas que hacer nada. El elemento button se agrega automáticamente a la secuencia de ordenamiento de pestañas del documento, lo que significa que, de forma predeterminada, se puede enfocar con el teclado. Las teclas Intro y Espacio activan el botón. Los botones también tienen todos los métodos y propiedades que les proporciona la interfaz HTMLButtonElement. Si no usas el botón semántico para tu botón, deberás volver a programar todas esas funciones. Es mucho más fácil usar `<button>`.

Regresa a la captura de pantalla del AOM para el bloque de código no semántico. Aquí, los elementos no semánticos no tienen roles implícitos. Podemos hacer que la versión no semántica sea semántica asignando un rol a cada elemento:

```html
<div role="banner">
  <span role="heading" aria-level="1">Three words</span>
  <div role="navigation">
    <a>one word</a>
    <a>one word</a>
    <a>one word</a>
    <a>one word</a>
  </div>
</div>
```

Si bien el atributo role se puede usar para agregar semántica a cualquier elemento, debes usar elementos con el rol implícito que necesites.

Elementos semánticos
Si te preguntas: "¿Qué elemento representa mejor la función de esta sección del lenguaje de marcado?", es probable que elijas el mejor elemento para el trabajo. El elemento que elijas y, por lo tanto, las etiquetas que uses deben ser adecuados para el contenido que muestras, ya que las etiquetas tienen un significado semántico.

Se debe usar HTML para estructurar el contenido, no para definir su apariencia. La apariencia es el ámbito del CSS. Si bien algunos elementos están definidos para que aparezcan de una manera determinada, no uses un elemento según cómo la hoja de estilo del usuario-agente hace que ese elemento aparezca de forma predeterminada. En cambio, selecciona cada elemento según su significado semántico y su funcionalidad. Codificar HTML de una manera lógica, semántica y significativa ayuda a que se aplique CSS según lo previsto.

Elegir los elementos adecuados para el trabajo a medida que codificas significa que no tendrás que refactorizar ni comentar tu HTML. Si piensas en usar el elemento correcto para el trabajo, la mayoría de las veces elegirás el elemento correcto. Cuando comprendes la semántica de cada elemento y sabes por qué es importante elegir el elemento correcto, puedes tomar la decisión adecuada sin mucho esfuerzo adicional.

A continuación, usa elementos semánticos para crear la <a href="https://web.dev/learn/html/document-structure?hl=es-419">estructura del documento.</a>