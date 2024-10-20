<h1 align="center">SetInterval y SetTimeout</h1>

<h2>📑 Contenido</h2>

- [SetInterval](#setinterval)
- [SetTimeout](#settimeout)

## SetInterval

La función setInterval() es una función de temporizador en JavaScript que se utiliza para programar una tarea para que se ejecute repetidamente después de un tiempo determinado.

setInterval(función, tiempo);

```js
function imprimirMensaje() {
  console.log("¡Hola, mundo!");
}

setInterval(imprimirMensaje, 3000);
```

## SetTimeout

El método global setTimeout() establece un temporizador que ejecuta una función o especifica pieza de código una vez que expira el temporizador.

setTimeout(función, tiempo);

```js
function imprimirMensaje() {
  console.log("¡Hola, mundo!");
}

setTimeout(imprimirMensaje, 3000);

//Otro ejemplo

const saludo = setTimeout(function () {
  alert("¡Hola, mundo!");
}, 3000);
```

