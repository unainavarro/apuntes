<h1 align="center">Introducción HTML</h1>

<h2>📑 Contenido</h2>

- [¿Qué es HTML?](#qué-es-html)
- [¿Para qué sirve HTML?](#para-qué-sirve-html)
- [HTML y el Navegador](#html-y-el-navegador)
- [Carga de recursos](#carga-de-recursos)

## ¿Qué es HTML?

HTML, siglas de HyperText Markup Language (Lenguaje de Marcado de Hipertexto), es el lenguaje estándar utilizado para crear y diseñar páginas web.
HTML proporciona una estructura básica para el contenido de una página web, utilizando etiquetas y elementos que definen diferentes partes de un documento, como encabezados, párrafos, listas, enlaces, imágenes, formularios, entre otros. Estas etiquetas permiten al navegador interpretar y mostrar correctamente el contenido de la página.

> [!IMPORTANT]
>
> HTML se combina con otros lenguajes de programación como CSS (Cascading Style Sheets) para controlar el diseño y la presentación visual de la página, y JavaScript para agregar interactividad y dinamismo a la web.

## ¿Para qué sirve HTML?

HTML sirve para crear y estructurar documentos web.

- **Definir la estructura de la página:** HTML permite definir la estructura básica de una página web, como encabezados, párrafos, listas, secciones, entre otros elementos.
- **Incorporar contenido multimedia:** HTML permite insertar imágenes, videos, audio y otros tipos de contenido multimedia en una página web.
- **Crear enlaces:** HTML facilita la creación de enlaces entre diferentes páginas web, permitiendo a los usuarios navegar de una página a otra.
- **Crear formularios:** HTML proporciona elementos para crear formularios interactivos que los usuarios pueden completar y enviar datos, como registros, comentarios o pedidos.
- **Facilitar la accesibilidad:** HTML incluye características que permiten mejorar la accesibilidad de las páginas web para personas con discapacidades, como la adición de etiquetas semánticas y atributos específicos.

## HTML y el Navegador

HTML se renderiza en un navegador web, lo que significa que el navegador interpreta el código HTML y lo muestra visualmente en la pantalla del usuario.

**Proceso básico de renderizado**

1. **Análisis del código HTML:** El navegador lee el código HTML línea por línea y lo analiza para identificar las etiquetas, elementos y atributos.
2. **Creación del DOM (Document Object Model):** Basándose en el código HTML, el navegador crea un árbol de objetos que representa la estructura del documento. Este árbol se conoce como el DOM y se utiliza para representar la estructura lógica del documento HTML.
3. **Construcción del árbol de renderizado:** Además del DOM, el navegador construye un árbol de renderizado que representa la estructura visual de la página. Este árbol tiene en cuenta la información de estilo y diseño definida en el HTML y en las hojas de estilo CSS asociadas.
4. **Determinación de estilos:** El navegador interpreta y aplica las reglas de estilo definidas en el CSS para determinar cómo se verá visualmente cada elemento HTML.
5. **Renderización:** Una vez que se ha construido el árbol de renderizado y se han aplicado los estilos, el navegador comienza a renderizar la página web, dibujando cada elemento en la pantalla de acuerdo con las especificaciones visuales definidas en el código HTML y CSS(si tiene).
6. **Interactividad y dinamismo:** Si el HTML incluye elementos interactivos o dinámicos, como scripts de JavaScript, el navegador también ejecutará estos scripts para agregar funcionalidades adicionales a la página, como animaciones, eventos de usuario o actualizaciones en tiempo real.

## Carga de recursos

En general, los navegadores web cargan los recursos en el orden en que aparecen en el código HTML. Por lo tanto, el HTML se carga primero, seguido del CSS y luego del JavaScript. Sin embargo, esto no significa necesariamente que se apliquen en ese orden. Es importante tener en cuenta las técnicas como la carga asíncrona de recursos CSS y JavaScript pueden cambiar el orden de carga y ejecución de estos recursos.
