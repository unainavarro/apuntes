<h1 align="center">Rest</h1>

<h2>📑 Contenido</h2>

- [Rest](#rest)
  - [En parámetros de función](#en-parámetros-de-función)
  - [En destructuración de arrays:](#en-destructuración-de-arrays)

## Rest

Rest es una característica introducida en ECMAScript 6 que permite a una función aceptar un número variable de argumentos como un array.

### En parámetros de función

Cuando se utiliza como parámetro de función, el operador de descanso permite capturar un número arbitrario de argumentos y los almacena en un array.

```js
function sumar(...numeros) {
  return numeros.reduce((total, numero) => total + numero, 0);
}

console.log(sumar(1, 2, 3, 4)); // Resultado: 10
console.log(sumar(1, 2)); // Resultado: 3
```

### En destructuración de arrays:

El operador de descanso también puede ser utilizado en la destructuración de arrays para capturar los elementos restantes de un array en una nueva variable.

```js
const [primerElemento, segundoElemento, ...restoElementos] = [1, 2, 3, 4, 5];
console.log(primerElemento); // Resultado: 1
console.log(segundoElemento); // Resultado: 2
console.log(restoElementos); // Resultado: [3, 4, 5]
```

> [!NOTE]
>
> El operador de descanso es muy útil para simplificar el manejo de funciones que pueden aceptar un número variable de argumentos o para manipular arrays de forma más eficiente.
