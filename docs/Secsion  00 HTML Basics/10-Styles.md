# BootCamp De HTML5 Session-00

## 10-Los Estilos

<div align='center'>

 <!--<![Image](https://github.com/user-attachments/assets/a47615e6-f177-4598-b943-e5526f035a1e)-->
</div>
<br>

<div align='center'><h2>Definición</h2></div>

Los estilos en HTML se manejan principalmente con CSS (Cascading Style Sheets), permitiendo separar contenido de presentación para diseñar colores, fuentes y diseño, y se aplican de tres formas: en línea (atributo style), internos (etiqueta `<style>` en `<head>`) y externos (archivo .css vinculado), siendo esta última la mejor práctica para sitios completos. CSS define la apariencia, y los métodos de aplicación controlan dónde y cómo se aplica el estilo, con CSS externo prevaleciendo sobre los internos y en línea.

El atribut `style`o HTML se utiliza para agregar estilos a un elemento, como color, fuente, tamaño y más.

## El atributo de estilo HTML

La configuración del estilo de un elemento HTML se puede realizar mediante el styleatributo .

El styleatributo HTML tiene la siguiente sintaxis:

```html
<tagname style="property:value;">
```

La propiedad es una propiedad CSS. El valor es un valor CSS.

Aprenderá más sobre CSS más adelante en este tutorial.

## Color de fondo

La propiedad CSS background-colordefine el color de fondo de un elemento HTML.

**Ejemplo**

Establezca el color de fondo de una página en azul pálido:

```html
<body style="background-color:powderblue;">

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
```

**Establecer el color de fondo para dos elementos diferentes:**

**Ejemplo**

```html
<body>

<h1 style="background-color:powderblue;">This is a heading</h1>
<p style="background-color:tomato;">This is a paragraph.</p>

</body>
```

## Color del texto

La colorpropiedad CSS define el color del texto para un elemento HTML:

Ejemplo

```html
<h1 style="color:blue;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>
```

**Resultado:**

<h1 style="color:blue;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>

---

## Fuentes

La font-familypropiedad CSS define la fuente que se utilizará para un elemento HTML:

**Ejemplo**

```html
<h1 style="font-family:verdana;">This is a heading</h1>
<p style="font-family:courier;">This is a paragraph.</p>
```

**Resultado:**
<h1 style="font-family:verdana;">This is a heading</h1>
<p style="font-family:courier;">This is a paragraph.</p>

---

## Tamaño del texto

La font-sizepropiedad CSS define el tamaño del texto de un elemento HTML:

**Ejemplo**

```html
<h1 style="font-size:300%;">This is a heading</h1>
<p style="font-size:160%;">This is a paragraph.</p>
```

**Resultado:**

<h1 style="font-size:300%;">This is a heading</h1>
<p style="font-size:160%;">This is a paragraph.</p>

---

## Alineación de texto

La text-alignpropiedad CSS define la alineación horizontal del texto para un elemento HTML:

**Ejemplo**

```html
<h1 style="text-align:center;">Centered Heading</h1>
<p style="text-align:center;">Centered paragraph.</p>
```

**Resultado:**

<h1 style="text-align:center;">Centered Heading</h1>
<p style="text-align:center;">Centered paragraph.</p>

---

## Resumen del capítulo

Utilice el styleatributo para estilizar elementos HTML

Usar background-colorcomo color de fondo

Usar colorpara colores de texto

Usar font-familypara fuentes de texto

Usar font-sizepara tamaños de texto

Úselo text-alignpara alinear texto
