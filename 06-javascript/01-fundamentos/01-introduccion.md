<h1 align="center">Introducción JS</h1>

<h2>📑 Contenido</h2>

- [¿Qué es JavaScript?](#qué-es-javascript)
- [¿Para qué sirve?](#para-qué-sirve)
- [Enlazar o agregar JavaScript](#enlazar-o-agregar-javascript)
- [use strict](#use-strict)
  - [Ventajas](#ventajas)

## ¿Qué es JavaScript?

JavaScript es un lenguaje de programación ampliamente utilizado que se utiliza principalmente para crear contenido interactivo en páginas web. Es un lenguaje de scripting del lado del cliente, lo que significa que se ejecuta en el navegador web del usuario en lugar de en el servidor.

JavaScript es un componente fundamental de la web moderna y se ha convertido en uno de los lenguajes de programación más populares debido a su versatilidad y su capacidad para funcionar en múltiples plataformas y dispositivos. Además de su uso en el desarrollo web, JavaScript también se utiliza en entornos de servidor a través de plataformas como Node.js, lo que permite a los desarrolladores crear aplicaciones web completas utilizando un solo lenguaje de programación tanto en el lado del cliente como en el del servidor.

## ¿Para qué sirve?

- **Interactividad en páginas web:** JavaScript se utiliza principalmente para hacer que las páginas web sean interactivas y dinámicas. Puede manipular el contenido de la página en tiempo real, responder a eventos del usuario como clics de ratón y pulsaciones de teclas, y actualizar partes específicas de una página sin necesidad de recargarla por completo.
- **Validación de formularios:**JavaScript se usa para verificar los datos ingresados por el usuario en formularios web para garantizar que sean correctos antes de enviarlos al servidor. Esto ayuda a mejorar la experiencia del usuario y a reducir errores en los datos ingresados.
- **Manipulación del DOM:** El Document Object Model (DOM) es una representación en memoria de la estructura de una página web. JavaScript permite manipular el DOM para cambiar el contenido, el estilo y la estructura de una página web dinámicamente en respuesta a acciones del usuario o eventos del navegador.
- **Desarrollo de aplicaciones web:** Con el uso de bibliotecas y frameworks como React, Angular y Vue.js, JavaScript se utiliza para crear aplicaciones web complejas y de una sola página (SPA) que ofrecen una experiencia de usuario similar a la de las aplicaciones de escritorio.
- **Comunicación con el servidor:** JavaScript permite realizar solicitudes HTTP asíncronas para enviar y recibir datos del servidor web sin tener que recargar toda la página. Esto se hace comúnmente utilizando la tecnología AJAX (Asynchronous JavaScript and XML) o utilizando APIs modernas como Fetch o Axios.
- **Desarrollo de juegos y aplicaciones móviles:** JavaScript se utiliza cada vez más para crear juegos en línea, aplicaciones móviles híbridas y aplicaciones de escritorio utilizando plataformas como Electron.

## Enlazar o agregar JavaScript

1. **Incorporación directa en el HTML:** Puedes incluir el código JavaScript directamente en el HTML utilizando la etiqueta `<script>`.

   ```html
   <!-- HTML -->
   <script>
     // Tu código JavaScript aquí
   </script>
   ```

2. **Archivo externo:** También puedes enlazar un archivo JavaScript externo utilizando la etiqueta `<script>` con el atributo src, que apunta al archivo JavaScript que deseas incluir.

   ```html
   <!-- HTML -->
   <script src="archivo.js"></script>

   <!-- URL completa -->
   <script src="https://cdnjs.cloudflare.com/ajax/libs/lodash.js/4.17.11/lodash.js"></script>
   ```

   > [!IMPORTANT]
   >
   > Si la etiqueta `<script>` contiene el atributo src el código de dentro no funcionara.

3. **Eventos en línea:** Puedes añadir código JavaScript directamente a ciertos eventos HTML utilizando atributos de evento.

   ```html
   <!-- HTML -->
   <button onclick="miFuncion()">Haz clic</button>
   ```

> [!NOTE]
>
> Como regla general, solo los scripts más simples se colocan en el HTML. Los más complejos residen en archivos separados.
>
> La ventaja de un archivo separado es que el navegador lo descargará y lo almacenará en caché.
>
> Otras páginas que hacen referencia al mismo script lo tomarán del caché en lugar de descargarlo, por lo que >el archivo solo se descarga una vez.
>
> Eso reduce el tráfico y hace que las páginas sean más rápidas.

## use strict

`"use strict" `es una declaración en JavaScript que se utiliza para activar el modo estricto en todo el código contenido dentro de un script o una función. Cuando se utiliza "use strict", el código se ejecuta en un contexto más seguro y restrictivo, lo que ayuda a evitar errores comunes y a escribir un código más robusto.

```js
"use strict";

// Código en modo estricto
function myFunction() {
  // En este contexto, el modo estricto está activado
  var x = 10;
  console.log(x);
}
```

### Ventajas

- **Errores más visibles:** Algunos comportamientos no seguros o no recomendados en JavaScript lanzarán errores en tiempo de ejecución en lugar de simplemente causar comportamientos inesperados.
- **Mayor seguridad:** Algunas características de JavaScript que pueden ser propensas a errores o inseguras son desactivadas o restringidas en modo estricto, lo que ayuda a evitar problemas de seguridad.
- **Mejores prácticas de programación:** El modo estricto también promueve el uso de mejores prácticas de codificación, como la declaración adecuada de variables con var, let o const, evitando el uso de palabras clave reservadas como nombres de variables, entre otros.

> [!NOTE]
>
> JavaScript admite POO con lo cual el use strict no es esencial al usar ese paradigma, pero al empezar ayuda
> para ver los errores y aprender buenas practicas.
