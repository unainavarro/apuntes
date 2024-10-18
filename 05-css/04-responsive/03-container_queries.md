<h1 align="center">Container Queries</h1>

<h2>📑 Contenido</h2>

- [Container Queries](#container-queries)
- [Concepto Hipotético](#concepto-hipotético)

## Container Queries

Las "container queries" (consultas de contenedor) son una característica muy esperada en el mundo del diseño web y CSS. A diferencia de las "media queries", que permiten aplicar estilos basados en las características del dispositivo, las "container queries" permiten aplicar estilos basados en las características del contenedor en el que se encuentra un elemento HTML.

Por ejemplo, supongamos que tienes un componente de tarjeta en tu página web que se utiliza en diferentes secciones con diferentes anchos de contenedor. Con las "container queries", podrías escribir reglas de estilo que se apliquen dependiendo del ancho específico del contenedor que contiene cada tarjeta, en lugar del ancho de la ventana del navegador.

Las "container queries" permitirían un mayor nivel de modularidad y reutilización en el diseño web, ya que los componentes podrían ser más autosuficientes y adaptarse mejor a su entorno sin necesidad de conocer el contexto global de la página.

Actualmente, las "container queries" están en desarrollo y no están ampliamente disponibles en los navegadores web. Sin embargo, hay algunos experimentos y propuestas en curso en la comunidad de CSS para abordar esta necesidad. Una de las propuestas más prometedoras es el uso de la función @container en CSS, que permitiría escribir estilos basados en el contenedor padre de un elemento.

## Concepto Hipotético

Ejemplo de cómo podrían funcionar si estuvieran disponibles. Por ahora, esto sería un concepto hipotético:

```html
<div class="container">
  <div class="element">
    <!-- Contenido del elemento -->
  </div>
</div>
```

```css
.container {
  width: 50%; /* Ancho del contenedor */
}

.element {
  /* Estilos base del elemento */
}

@container (min-width: 400px) {
  .element {
    /* Estilos aplicados al elemento cuando el contenedor es al menos 400px de ancho */
    background-color: yellow;
  }
}

@container (min-width: 800px) {
  .element {
    /* Estilos aplicados al elemento cuando el contenedor es al menos 800px de ancho */
    background-color: lightblue;
  }
}
```
