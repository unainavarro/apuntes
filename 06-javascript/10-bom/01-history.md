<h1 align="center">History</h1>

<h2>📑 Contenido</h2>

- [History](#history)
- [Ejemplo](#ejemplo)

## History

Manipulando el historial del navegador

## Ejemplo

```html
<!-- HTML -->
<p id="ver"></p>
<hr />

<button onclick="siguienteURL()">Adelante</button>
<button onclick="go()">Ir</button>
<button onclick="anteriorURL()">Atrás</button>
```

```js
// JavaScript
const verDatos = `
//Devuelve Número de URLs en el historial: <br> Num URL: ${history.length}
`;
document.getElementById("ver").innerHTML = verDatos;

//Devolver URL anterior

const anteriorURL = () => {
  history.back();
};
const siguienteURL = () => {
  history.forward();
};
const go = () => {
  const num = prompt("Numero");
  if (isNaN(num)) {
    alert("Eso no es un número");
  } else {
    history.go(num);
  }
};
```
