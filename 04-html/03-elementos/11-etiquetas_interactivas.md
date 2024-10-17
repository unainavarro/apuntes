<h1 align="center">Etiquetas Interactivas</h1>

<h2>📑 Contenido</h2>

- [¿Qué son las etiquetas interactivas?](#qué-son-las-etiquetas-interactivas)
- [Details](#details)
- [Menu](#menu)
- [Popover](#popover)
- [Contenido Editable](#contenido-editable)
- [Dialog](#dialog)
  - [Ejemplo con JavaScript](#ejemplo-con-javascript)
  - [Ejemplo con CSS](#ejemplo-con-css)
- [Meter](#meter)

## ¿Qué son las etiquetas interactivas?

Las etiquetas HTML5 interactivas son aquellas que permiten al usuario interactuar con la página web de alguna forma, como mostrar u ocultar información, seleccionar opciones, introducir datos, etc.

> [!NOTE]
>
> Ya hemos visto elementos interactivos en [formularios](./05-Formularios.md) y en [audio y video](./07-Audio&Video.md).

## Details

Crea un elemento desplegable que muestra información adicional cuando el usuario hace clic en él.

- **`<details>`** Crea un elemento desplegable. Etiqueta contenedora.
  - **`<details open>`** Visible por defecto.
- **`<summary>`** Título del desplegable. Aparece siempre, se encuentre desplegado o no.

```HTML
<!-- Ejemplo <details>-->
<details>
    <summary>Click</summary>
    <p>Texto aleatorio.</p>
</details>
```

## Menu

Esta etiqueta define un menú de comandos o acciones que el usuario puede ejecutar.

> [!CAUTION]
>
> No confundir con la etiqueta `<nav>`, `<menu>`en este momento no es compatible con la mayoría de navegadores.

```HTML
<!-- Ejemplo <details>-->
<menu type="toolbar">
  <command label="Guardar" onclick="save()">
  <command label="Imprimir" onclick="print()">
  <command label="Compartir" onclick="share()">
</menu>
```

## Popover

Los popover sirven para crear elementos emergentes(contenido por encima de otro contenido).

- Por defecto se posiciona en el centro de la pantalla.
- Podemos cambiar su CSS [popover]{ código css}
  - Selectores:
    - **::backdrop** Aplica estilos al fondo de la página cuando se muestra el popover.
    - **:popover-open** Aplica estilos a un popover que se esté actualmente visible.

```HTML
<!-- HTML -->
<button popovertarget="mensaje" popovertargetaction="toggle">
    Mostrar Mensaje
</button>

<div id="mensaje" popover>
    <p>Esto es un mensaje de prueba</p>
</div>
```

```CSS
/* CSS */
[popover]::backdrop {
    background: tomato;
}

[popover]:popover-open {
    font-size: 2rem;
}
```

## Contenido Editable

Al utilizar el atributo **contenteditable** sobre una etiqueta HTML le damos la capacidad al usuario de editar el contenido de texto.

```HTML
<h1 contenteditable>Título editable</h1>
<div contenteditable>
  <p>Texto editable</p>
</div>
```

## Dialog

La etiqueta `<dialog>` en HTML se utiliza para representar una ventana de diálogo o un cuadro de diálogo dentro de una página web. Los diálogos son ventanas modales que se utilizan para interactuar con el usuario, y `<dialog>` proporciona una forma estándar de crear y manipular estos elementos en HTML.

### Ejemplo con JavaScript

```html
<!-- HTML -->
<button id="mostrarDialogo">Mostrar Diálogo</button>

<dialog id="miDialogo">
  <p>Este es un contenido de diálogo.</p>
  <button id="cerrarDialogo">Cerrar</button>
</dialog>
```

```js
//JavaScript

// Obtener referencias a elementos
var botonMostrar = document.getElementById("mostrarDialogo");
var dialogo = document.getElementById("miDialogo");
var botonCerrar = document.getElementById("cerrarDialogo");

// Configurar eventos
botonMostrar.addEventListener("click", function () {
  dialogo.showModal();
});

botonCerrar.addEventListener("click", function () {
  dialogo.close();
});
```

---

### Ejemplo con CSS

```html
<!-- HTML -->
<input type="checkbox" id="mostrarDialogo" />
<label for="mostrarDialogo">Mostrar Diálogo</label>

<dialog id="miDialogo">
  <p>Este es un contenido de diálogo.</p>
  <label for="mostrarDialogo">Cerrar</label>
</dialog>
```

```css
/* CSS */
#miDialogo {
  display: none;
}

#mostrarDialogo:checked ~ #miDialogo {
  display: block;
}
```

## Meter

La etiqueta `<meter>` en HTML se utiliza para representar valores en un rango conocido o medidas de métricas. Se utiliza para mostrar barras de progreso, indicadores de nivel, entre otros.

```html
<!-- HTML -->
<meter value="70" min="0" max="100">70%</meter>
```
