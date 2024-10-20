<h1 align="center">Hoisting</h1>

<h2>📑 Contenido</h2>

- [Hoisting](#hoisting)
  - [Ejemplos](#ejemplos)
- [Undefined vs ReferenceError](#undefined-vs-referenceerror)
  - [Undefined](#undefined)
  - [ReferenceError](#referenceerror)

## Hoisting

El hoisting en JavaScript es un comportamiento que permite usar funciones y variables antes de que se hayan declarado. En otras palabras, el intérprete de JavaScript “alza” las declaraciones de funciones y variables a la parte superior de su ámbito antes de la ejecución.

### Ejemplos

```js
//Variables
console.log(foo);
var foo = "foo";
```

Este código genera **undefined** en lugar de un error, a pesar de que foo se asigna después de la línea console.log. Esto se debe a que el intérprete de JavaScript divide la declaración y asignación de funciones y variables, y “alza” las declaraciones a la parte superior del ámbito antes de la ejecución.

```js
//Funciones
foo();

function foo() {
  console.log("foo");
}
```

> [!IMPORTANT]
>
> Tener en cuenta que solo las declaraciones se “alzan”, no las asignaciones.

## Undefined vs ReferenceError

### Undefined

En JavaScript, a una **variable no declarada** se le asigna el valor **undefined** en la ejecución y también es de tipo undefined.

### ReferenceError

En JavaScript, se produce un ReferenceError al intentar acceder a una variable no declarada previamente.
