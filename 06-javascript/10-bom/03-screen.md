<h1 align="center">Screen</h1>

<h2>📑 Contenido</h2>

- [Screen](#screen)
  - [Ejemplo](#ejemplo)

## Screen

El objeto screen contiene información sobre la pantalla del visitante.

### Ejemplo

```html
<p id="ver"></p>
```

```js
const verDatos = `
//Tamaño Pantalla: <br>
Ancho: ${screen.width}<br>
Alto:${screen.width}<br>
<hr>
//Tamaño Pantalla SIN BARRA: <br>
Ancho: ${screen.availWidth}<br>
Alto:${screen.availHeight}<br>
<hr>
//Profundidad de color: <br>
Color-Depth: ${screen.colorDepth}<br>
<hr>

`;
document.getElementById("ver").innerHTML = verDatos;
```
