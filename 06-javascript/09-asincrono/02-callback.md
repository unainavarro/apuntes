<h1 align="center">Callback</h1>

<h2>📑 Contenido</h2>

- [Callback](#callback)
  - [Función callback simple](#función-callback-simple)
  - [Función callback con argumentos](#función-callback-con-argumentos)
  - [Función callback anónima](#función-callback-anónima)

## Callback

Los callbacks son una parte importante de JavaScript y una vez que entiendas cómo funcionan, mejorarás mucho en JavaScript. En JavaScript, las funciones son objetos. Podemos pasar funciones como parámetros a otras funciones y llamarlas dentro de las funciones externas. Esto se llama “callback”.

Así que una función que se pasa a otra función como parámetro es una función callback.

Los callbacks aseguran que una función no se va a ejecutar antes de que se complete una tarea, sino que se ejecutará justo después de que la tarea se haya completado. Nos ayuda a desarrollar código JavaScript asíncrono y nos mantiene a salvo de problemas y errores.

### Función callback simple

```js
function imprimir(callback) {
  callback();
}
```

### Función callback con argumentos

```js
function sumar(a, b, callback) {
  let resultado = a + b;
  callback(resultado);
}
```

### Función callback anónima

```js
setTimeout(function () {
  console.log("¡Hola mundo!");
}, 1000);
```
