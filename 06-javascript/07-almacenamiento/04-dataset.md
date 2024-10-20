<h1 align="center">Dataset</h1>

<h2>📑 Contenido</h2>

- [Dataset](#dataset)
  - [Ejemplo](#ejemplo)

## Dataset

Dataset es una forma de acceder a los atributos de datos (data attributes) de un elemento HTML. Los atributos de datos son atributos HTML que permiten almacenar datos personalizados en elementos HTML, los cuales pueden ser útiles para almacenar información adicional que no está directamente relacionada con la presentación visual del elemento.

### Ejemplo

```html
<!-- HTML -->
<div
  id="miElemento"
  data-nombre="Juan"
  data-edad="30"
  data-ciudad="Barcelona"
></div>
```

```js
const elemento = document.getElementById("miElemento");

console.log(elemento.dataset.nombre); // Resultado: "Juan"
console.log(elemento.dataset.edad); // Resultado: "30"
console.log(elemento.dataset.ciudad); // Resultado: "Barcelona"
```

> [!NOTE]
>
> Los nombres de los atributos de datos son case-sensitive en HTML, lo que significa que data-nombre y data-Nombre se consideran diferentes atributos de datos. Sin embargo, en JavaScript, las propiedades de dataset son case-insensitive, lo que significa que puedes acceder a ellas utilizando camelCase sin preocuparte por la capitalización.
