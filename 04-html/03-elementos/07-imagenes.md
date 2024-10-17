<h1 align="center">Imágenes</h1>

<h2>📑 Contenido</h2>

- [Imágenes](#imágenes)
  - [Cargar una imagen(loading)](#cargar-una-imagenloading)
- [Figure](#figure)
- [Picture](#picture)

## Imágenes

Para insertar imágenes en HTML se utiliza la etiqueta `<img>`.

Sintaxis: <br>
`<img src="Ruta/de/la/imagen" alt="Descripción de la imagen">`

En la ruta de la imagen se pueden poner imágenes locales, imágenes alojadas en el mismo lugar que el proyecto. O También se pueden poner imágenes externas copiando el enlace de la imagen.

```html
<!-- Ejemplo -->
<img
  src="https://images.unsplash.com/photo-1625467883732-b06f641226d8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8ZnJlZSUyMHVzZXxlbnwwfHwwfHw%3D&w=1000&q=80"
  alt="anochecer"
/>
```

### Cargar una imagen(loading)

Mediant el uso del atributo `loading` se puede controlar el momento en el que se carga una imagen. El atributo loading es especialmente útil para optimizar el rendimiento de páginas web con muchas imágenes, ya que permite cargar recursos de manera más eficiente, reduciendo la carga inicial de la página.

- **auto (por defecto):** Este es el valor predeterminado si no se especifica otro. Indica que el navegador debe decidir cuándo cargar el recurso según su propio criterio.

- **eager:** Indica que el recurso debe cargarse de inmediato, sin diferir la carga. Es útil cuando el recurso es crucial para el contenido visible inmediatamente.

- **lazy:** Indica que el recurso debe cargarse de manera diferida, es decir, solo cuando sea necesario. Esto puede ayudar a mejorar el rendimiento de la página, especialmente en imágenes que están fuera de la vista inicial del usuario.

Ejemplo:

```html
<img src="imagen.jpg" alt="Descripción de la imagen" />
<img src="imagen.jpg" alt="Descripción de la imagen" loading="lazy" />
<img src="imagen.jpg" alt="Descripción de la imagen" loading="eager" />
```

> [!WARNING]
>
> Evitar usar este atributo(lazy) con las imágenes que estén situadas en la parte superior de la web ya que esas imágenes serán visibles nada mas cargar la pagina.
>
> Tener en cuenta otros factores como, el servidor, los diferentes navegadores y el tipo de imagen.

## Figure

La etiqueta `<figure>` en HTML se utiliza para encapsular contenido relacionado, generalmente imágenes o gráficos, junto con su descripción o leyenda. Esta etiqueta se usa en combinación con la etiqueta `<figcaption>`, que proporciona la descripción o leyenda del contenido encapsulado.

```html
<figure>
  <img src="imagen.jpg" alt="Descripción de la imagen" />
  <figcaption>Esta es una imagen de ejemplo.</figcaption>
</figure>
```

> [!NOTE]
>
> Al asociar una imagen o un gráfico con su contexto descriptivo, mejora la accesibilidad y la comprensión del contenido.

## Picture

La etiqueta `<picture>` es un contenedor para agrupar varias opciones para mostrar una imagen. Con esta etiqueta podemos establecer una imagen con diferente extension(png,jpg,WebP), en función del tamaño del dispositivo mostrar una imagen u otra. Al añadir imágenes con diferentes resoluciones podemos crear imágenes responsive de manera sencilla.

- `<picture>`: El contenedor que agrupa los demás elementos.
- `<source>`: Hace referencia a las distintas imágenes.
- `<img>`: Es importante poner una imagen al final por si el navegador no es compatible con `<picture>`

```html
<!-- Ejemplo: uso del elemento picture -->

<picture>
  <source
    media="(min-width:650px)"
    srcset="
      https://images.unsplash.com/photo-1625467883732-b06f641226d8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8ZnJlZSUyMHVzZXxlbnwwfHwwfHw%3D&w=1000&q=80
    "
  />
  <source
    media="(min-width:465px)"
    srcset="
      https://images.unsplash.com/photo-1625467883732-b06f641226d8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8ZnJlZSUyMHVzZXxlbnwwfHwwfHw%3D&w=1000&q=80
    "
  />
  <img
    src="https://images.unsplash.com/photo-1625467883732-b06f641226d8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8ZnJlZSUyMHVzZXxlbnwwfHwwfHw%3D&w=1000&q=80"
    alt="Flowers"
    style="width: auto"
  />
</picture>
```

> [!TIP]
>
> Cuando usarlas:
>
> - `<picture>` cuando quieras **optimizar la carga** de imágenes según el tamaño de la pantalla, resolución o características específicas del dispositivo.
> - `<figure> `cuando tengas una imagen que necesita ser **empaquetada** junto **con su contenido asociado**, como una leyenda o descripción.
> - `<img>` cuando solo necesitas mostrar una imagen sin necesidad de una descripción detallada o contenido relacionado.
