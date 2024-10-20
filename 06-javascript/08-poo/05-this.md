<h1 align="center">This</h1>

<h2>📑 Contenido</h2>

- [This](#this)
- [Scope Global](#scope-global)
- [En un Método](#en-un-método)
- [En una función](#en-una-función)
- [Funciones Flecha](#funciones-flecha)
- [Bindeo](#bindeo)

## This

This es una palabra clave especial que se refiere al objeto al que pertenece el contexto de ejecución actual. El valor de this depende de cómo se invoca una función y puede cambiar dinámicamente durante la ejecución del programa.

## Scope Global

```js
console.log("Global: " + this === window); //false
console.log(this === window); // true
```

## En un Método

this hace referencia al “propietario” de dicho método.

```js
const coche = {
  ruedas: 4,
  color: "rojo",
  toString: function () {
    return `El coche es ${this.color} tiene ${this.ruedas} ruedas`;
  },
};

console.log(coche.toString());
```

## En una función

Hace referencia al objeto global <br>
En 'use strict' this = undefined

```js
function prueba() {
  return this;
}

console.log(prueba()); //Objeto Window
```

## Funciones Flecha

No bindean su propio this, heredan del scope padre'Exterior'.

```js
const flecha = () => {
  return this;
};

console.log(flecha()); //Objeto Window

const coche2 = {
  ruedas: 4,
  color: "rojo",
  toString: () => {
    return `El coche es ${this.color} tiene ${this.ruedas} ruedas`;
  },
};

console.log(coche2.toString()); // Undefined (Buscar window.color y window.ruedas)
```

## Bindeo

El método bind() crea una nueva función que, al ser invocada, asigna a this el valor que se le pasa por parámetro.

```js
const person = {
  firstName: "MiNombre",
  lastName: "MiApellido",
  fullName: function () {
    return this.firstName + " " + this.lastName;
  },
};

const member = {
  firstName: "MiNombre",
  lastName: "MiApellido",
};

let fullName = person.fullName.bind(member);
console.log(person.fullName());
console.log(fullName());
```
