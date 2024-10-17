<h1 align="center">Atributos</h1>

<h2>📑 Contenido</h2>

- [¿Qué son los atributos?](#qué-son-los-atributos)
- [Atributos Requeridos](#atributos-requeridos)
- [Atributos Opcionales](#atributos-opcionales)
- [Atributos Globales](#atributos-globales)
- [Atributos para `<meta>`](#atributos-para-meta)
  - [Específicos del elemento:](#específicos-del-elemento)
  - [Ejemplo](#ejemplo)
- [Atributos de Evento](#atributos-de-evento)
- [Atributos Booleanos](#atributos-booleanos)
  - [Ejemplo](#ejemplo-1)
- [Atributos Enumerados](#atributos-enumerados)
  - [Ejemplo](#ejemplo-2)

## ¿Qué son los atributos?

Los atributos HTML son propiedades que se utilizan para proporcionar información adicional sobre elementos HTML. Los atributos se especifican dentro de las etiquetas HTML y tienen un nombre y un valor.

Ejemplo:

```html
<!-- La etiqueta <p></p> que se utiliza para inserta párrafos. -->

<p class="texto">Contenido</p>

<!-- 
    Atributo: `<class=”texto”>` 
    Nombre-Atributo: class
    Valor-Atributo: texto    
-->
```

Los atributos de un elemento sirven para añadir valores adicionales, controlar el comportamiento y modificar elementos. Existen atributos requeridos, opcionales, globales y de evento.

Los atributos requeridos y opcionales modifican elementos concretos, mientras que los globales se pueden aplicar a la mayoría de elementos. Los atributos de evento permiten que los elementos ejecuten scripts en ciertas situaciones. Este tipo de eventos se usan generalmente con JavaScript.

## Atributos Requeridos

Como su propio nombre indica son atributos requeridos para que el elemento funcione.

```HTML
<!-- Para que una imagen funcione es necesario que lleve el atributo src -->
<img src="ruta/de/la/imagen.png">

<!-- Para que un enlace funcione es necesario que lleve el atributo href -->
<a href="ruta/del/enlace">Pincha aquí</a>
```

> [!NOTE]
>
> Las comillas de los atributos nombreAtributo="valorAtributo" no son obligatorias a no ser que el valor este separado por un espacio. **Recomendable utilizarlas**.

## Atributos Opcionales

No son necesarios para que el elemento funcione pero ayudan a mejorar su uso.

```HTML
<!--
Para que una imagen funcione no es necesario que lleve el atributo alt pero es recomendado.
alt en una imagen es importante para la accesibilidad web ya que  proporciona un texto alternativo que describe el contenido de la imagen.
-->

<img src="ruta/de/la/imagen.png" alt="Descripción de la imagen">
```

> [!NOTE]
>
> - Es recomendable proporcionar descripciones claras y descriptivas en el atributo alt, evitando textos genéricos como "imagen" o dejarlo en blanco.
> - Los motores de búsqueda utilizan el texto alternativo como parte de su análisis de contenido de la página, un buen uso de alt puede mejorar la indexación de la página en los motores de búsqueda y proporcionar una mejor experiencia de usuario.
> - Si la imagen no se carga correctamente el texto alternativo proporciona información sobre el contenido de la imagen.

## Atributos Globales

Estos atributos se pueden usar para cualquier etiqueta.
Son útiles para mejorar la consistencia y la apariencia de una página web.

**Atributos Globales más utilizados:**

- **class:** Añadir una clase al elemento.
- **id:** Añadir un identificador ÚNICO al elemento.
- **style:** Añadir estilo en linea al elemento.
- **title:** Establecer un titulo al elemento.

```HTML
<!-- Ejemplo -->
    <p class="bordes-rosas" id="parrafoUnico"></p>

    <img class="bordes-rosas" id="imagenUnica" src="ruta/de/la/imagen.png">
```

**Otros Atributos Globales:**

- **lang:** Especifica el idioma principal del contenido dentro del elemento.
- **dir:** Define la dirección de escritura del texto en el elemento (LTR o RTL).
- **accesskey:** Establece una tecla de acceso rápido para enfocar o activar el elemento.
- **tabindex:** Controla el orden de navegación por teclado de los elementos enfocables.
- **hidden:** Oculta el elemento de la vista del usuario.
- **contenteditable:** Permite que el contenido del elemento sea editable por el usuario.
- **spellcheck:** Habilita o deshabilita la verificación ortográfica para el contenido editable.
- **data:** Permite almacenar datos personalizados en el elemento con nombres personalizados.
- **role:** Especifica el rol del elemento en la accesibilidad web.
- **aria:** Atributos de ARIA (Accessible Rich Internet Applications) para mejorar la accesibilidad.
- **draggable:** Indica si el elemento se puede arrastrar y soltar.
- **translate:** Indica si el contenido del elemento debe ser traducido automáticamente.

> [!NOTE]
>
> Estos atributos son muy útiles a la hora de mejorar la accesibilidad.

## Atributos para `<meta>`

La etiqueta meta puede contener 3 tipos diferentes de atributos: globales, específicos del elemento y de controlador de eventos.
Estos atributos se utilizan principalmente para proporcionar información sobre la página web a los motores de búsqueda y navegadores.

### Específicos del elemento:

- **charset:** Especifica la codificación de caracteres del documento.
  - utf-8: codificación para la mayoría de textos e idiomas.
- **name:** Especifica el nombre del metadato.
- **content:** Especifica el valor del metadato.
- **http-equiv:** Se utiliza para los encabezados de mensajes de respuesta http.
- **scheme:** Especifica un esquema para interpretar el valor de la propiedad.

### Ejemplo

```HTML
<!-- Ejemplos -->
 <head>
    <!-- Permite establecer como se va a comportar el responsive en nuestra página. -->
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <meta name="description" content="Pagina sobre HTML">
  <meta name="keywords" content="html, etiquetas">
  <meta name="author" content="Admin">
  <meta name="application-name" content="Aprende HTML">
  <meta name = "revised" content = "Aprende HTML, 9/9/2099" />
  <meta name="generator" content="VSCode">
  <!-- Se actualiza cada 5segundos y redirecciona a google -->
  <meta http-equiv = "refresh" content = "5; url = http://www.google.com" />
  <meta name="id.libro" content="978-3-44-148710-0" scheme="ISBN">
</head>
```

## Atributos de Evento

Estos atributos se usan generalmente con JavaScript, añaden eventos y funciones a los elementos. Estos atributos se suelen asociar a funciones que ejecuten lo que hacer en caso de que se ejecute el evento.

_Algunos ejemplos:_

- **onclick:** Ejecuta la acción cuando se realiza un clic sobre el elemento.
- **onmousedown:** Ejecuta la acción cuando se detecta el botón pulsado del ratón.
- **onmouseup:** Ejecuta la acción cuando se detecta que se ha soltado el botón del ratón.
- **onload:** Ejecuta la acción cuando se carga el documento
- **onresize:** Ejecuta la acción cuando se ha modificado el tamaño de la ventana del navegador
- **onfocus:** Ejecuta la acción cuando el elemento obtiene el foco bien sea a través del ratón o por navegación tabulada.
- **onsubmit:** Ejecuta la acción cuando el formulario es enviado.

```HTML
<!-- Ejemplo -->
 <p onclick="funcion()">Texto de relleno</p>

 <script>
    funcion(){
        //TODO Acción para el evento.
    }
 </script>
```

## Atributos Booleanos

En HTML no existe un atributo booleano en el sentido estricto, pero algunos atributos se pueden utilizar en forma de atributos booleanos.
Un atributo booleano se considera "verdadero" si está presente y "falso" si está ausente. La forma en que funcionan depende de si están presentes o ausentes en el elemento HTML correspondiente.

> [!CAUTION]
>
> Estos atributos no siguen la sintaxis de nombre="valor" como el resto de atributos.
> Se escribe solo el nombre del atributo.

**Algunos atributos "booleanos":**

`autofocus, inert, checked, disabled, required, reversed, allowfullscreen, default,loop, autoplay, controls, muted, readonly, multiple,y selected.`

### Ejemplo

```html
<!-- disabled: Este atributo se utiliza para deshabilitar un elemento HTML -->
<button disabled>Botón deshabilitado</button>
<input type="text" disabled />

<!-- checked: Se utiliza con elementos de entrada de tipo checkbox o radio para preseleccionar una opción -->
<input type="checkbox" checked /> Casilla marcada
<input type="radio" name="opciones" value="opcion1" checked /> Opción 1

<!-- readonly: Este atributo se utiliza para hacer que un campo de entrada de texto o área de texto sea de solo lectura. -->
<input type="text" readonly value="Este campo es de solo lectura" />
<textarea readonly>Este es un área de texto de solo lectura</textarea>

<!-- required: Se utiliza con elementos de entrada como input para especificar que un campo debe completarse antes de enviar un formulario. -->
<input type="text" required />
```

> [!TIP]
>
> Los atributos booleanos son útiles con JavaScript para ocultar un elemento de forma rápida simplemente agregando el atributo.

## Atributos Enumerados

Los atributos enumerados son aquellos que tienen un conjunto limitado de valores predefinidos y solo pueden tomar uno de esos valores específicos. Estos atributos se utilizan principalmente para definir configuraciones o propiedades con opciones discretas.

### Ejemplo

```html
<!-- Type: define el tipo de campo de entrada que se debe utilizar -->
<input type="text" />
<input type="password" />
<input type="checkbox" />

<!-- 
Target: se utiliza para especificar dónde se abrirá el enlace cuando se hace clic en él.
"_blank" (para abrir en una nueva ventana o pestaña).
"_self" (para abrir en la misma ventana actual).
 -->
<a href="https://www.ejemplo.com" target="_blank"
  >Abrir enlace en nueva ventana</a
>
<a href="https://www.ejemplo2.com" target="_self"
  >Abrir enlace en la misma ventana</a
>

<!-- rel: se utiliza para especificar la relación entre la página actual y la página vinculada.
Valores("nofollow", "noopener," "noreferrer"...) -->
<a href="https://www.ejemplo.com" rel="nofollow">Enlace con atributo rel</a>
```

> [!IMPORTANT]
>
> Como no todos los atributos valen para todas las etiquetas. Es mas fácil verlos de forma individual, con listas, tablas, multimedia, texto..
