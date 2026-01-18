# BootCamp De HTML5 Session-00

## 09-Los Parrafos

<div align='center'>

 <!--<![Image](https://github.com/user-attachments/assets/a47615e6-f177-4598-b943-e5526f035a1e)-->

</div>

### Definición

En `HTML`, los párrafos se crean con la etiqueta `<p>` y `</p>`, agrupando texto y separándolo automáticamente con espacio en blanco, y son elementos de bloque que ocupan el ancho completo de la página, a diferencia de los saltos de línea simples que se hacen con `<br>`. Es crucial usar `<p>` para contenido semántico de texto (oraciones y frases) y no solo para espaciar líneas, ya que HTML ignora los saltos de línea dentro de la etiqueta `<p>` y los muestra juntos, como se explica en.

### Uso de la etiqueta `<p>`

Apertura y cierre: Se abre con `<p>` y se cierra con `</p>`.
Contenido: El texto o frases van entre las etiquetas: `<p>` Este es un párrafo de texto.</p>.
Salto de línea vs. Párrafo:
Párrafo ( `<p>` ): Crea un bloque de texto, agrega espacio antes y después, y trata los saltos de línea internos como si fueran uno solo.
Salto de línea ( `<br>` ): Solo inserta un retorno de carro dentro de un mismo párrafo (no necesita cierre), según detalla.
Bloque: Es un elemento de "bloque", ocupando todo el ancho disponible, lo que genera separación natural con otros elementos de bloque, como se indica en esta fuente y esta otra.

### Ejemplo Práctico

```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de Párrafos</title>
</head>
<body>
    <p>Este es el primer párrafo. Se mostrará con espacio arriba y abajo.</p>
    <p>Este es el segundo párrafo, separado del primero.</p>
    <p>Puedes poner varias líneas aquí, y HTML las unirá en un solo párrafo:<br>
       Esta es una nueva línea dentro del mismo párrafo.<br>
       Como ves, los saltos internos no separan el bloque.</p>
</body>
</html>

```

**En resumen:** Usa `<p>` para marcar secciones de texto que son párrafos semánticos y `<br>` para saltos de línea forzados dentro de esos párrafos, según explican.

### Visualización HTML

No puedes estar seguro de cómo se mostrará el `HTML`.

Las pantallas grandes o pequeñas y las ventanas redimensionadas crearán resultados diferentes.

Con `HTML`, no es posible cambiar la visualización agregando espacios o líneas adicionales en el código HTML.

El navegador eliminará automáticamente cualquier espacio y línea adicional cuando se muestre la página:

Ejemplo

```html
<p>
This paragraph
contains a lot of lines
in the source code,
but the browser
ignores it.
</p>

<p>
This paragraph
contains         a lot of spaces
in the source         code,
but the        browser
ignores it.
</p>
```

### Reglas horizontales HTML

La etiqueta `<hr>` define un salto temático en una página HTML y generalmente se muestra como una regla horizontal.

El elemento `<hr>` se utiliza para separar contenido (o definir un cambio) en una página HTML:

Ejemplo

```html
<h1>This is heading 1</h1>
<p>This is some text.</p>
<hr>
<h2>This is heading 2</h2>
<p>This is some other text.</p>
<hr>
```

La etiqueta `<hr>` es una etiqueta vacía, lo que significa que no tiene etiqueta final.

### Saltos de línea HTML

El elemento `<br>` en HTML define un salto de línea.

Úse `<br>`si desea un salto de línea (una nueva línea) sin comenzar un nuevo párrafo:

**Ejemplo**

```html
<p>This is<br>a paragraph<br>with line breaks.</p>
La <br>etiqueta es una etiqueta vacía, lo que significa que no tiene etiqueta final.
```

### El problema del poema

Este poema se mostrará en una sola línea:

**Ejemplo**

```html
<p>
  My Bonnie lies over the ocean.

  My Bonnie lies over the sea.

  My Bonnie lies over the ocean.

  Oh, bring back my Bonnie to me.
</p>
```

### Solución: El elemento HTML `<pre>`

El elemento `<pre>` en HTML define texto preformateado.

El texto dentro de un elemento `<pre>` se muestra en una fuente de ancho fijo (generalmente Courier) y conserva tanto los espacios como los saltos de línea:

Ejemplo

```html
<pre>
  My Bonnie lies over the ocean.

  My Bonnie lies over the sea.

  My Bonnie lies over the ocean.

  Oh, bring back my Bonnie to me.
</pre>
```
