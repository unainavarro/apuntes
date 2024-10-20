<h1 align="center">Window</h1>

<h2>📑 Contenido</h2>

- [Window](#window)
- [Pantalla](#pantalla)
- [Eventos de Tiempo](#eventos-de-tiempo)
- [Eventos de Tiempo](#eventos-de-tiempo-1)

## Window

## Pantalla

```html
<p id="mostrar"></p>
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

## Eventos de Tiempo

```js
const nombre = prompt("Insertar nombre");
alert("Hola: " + nombre);

const asistir = confirm("Asistirás¿?");
asistir ? alert("Si asistirás") : alert("No asistirás");
```

## Eventos de Tiempo

```js
// Establezca un temporizador y ejecute una función de devolución de llamada una vez que expire el temporizador.
const saludar = setTimeout(() => {
  alert("Hola: ");
}, 5000);

// Ejecute una función de devolución de llamada repetidamente con un retraso fijo entre cada llamada.
const spam = setInterval(() => {
  console.log("Spam");
}, 1000);
```
