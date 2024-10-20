<h1 align="center">Desestructuración</h1>

<h2>📑 Contenido</h2>

- [Desestructuración](#desestructuración)
  - [Arrays](#arrays)
  - [Objetos](#objetos)
  - [Array de Objetos](#array-de-objetos)
  - [Objetos en Funciones](#objetos-en-funciones)
  - [Arrays en Funciones](#arrays-en-funciones)

## Desestructuración

La desestructuración es una expresión de JavaScript que permite desempacar valores de arreglos o propiedades de objetos en distintas variables. En otras palabras, podemos extraer datos de arreglos y objetos y asignarlos a variables.

### Arrays

```js
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

let [primero] = arr;
console.log(primero);

let [, , , cuarto] = arr;
console.log(cuarto);

let [uno, ...resto] = arr;
console.log(resto);
```

### Objetos

```js
const producto = {
  nombre: "Monitor",
  precio: 300,
  disponible: true,
};

const { precio, disponible } = producto;
console.log(precio + " " + disponible);
```

### Array de Objetos

```js
let alumnos = [
  { nombre: "juan", rol: "admin" },
  { nombre: "maria", rol: "user" },
  { nombre: "marcos", rol: "Super admin" },
  { nombre: "pedro", rol: "user" },
  { nombre: "mario", rol: "boss" },
];

let [, , marcos] = alumnos;
console.log(marcos);

let [, maria, ...otros] = alumnos;
console.log(maria);
console.log(otros);
```

### Objetos en Funciones

```js
function obtenerNombreCompleto(persona) {
  const { nombre, apellido } = persona;
  return `${nombre} ${apellido}`;
}

const persona = { nombre: "Juan", apellido: "Pérez" };
console.log(obtenerNombreCompleto(persona)); // Output: "Juan Pérez"
```

### Arrays en Funciones

```js
function obtenerElementos([primerElemento, segundoElemento]) {
  return `Primer elemento: ${primerElemento}, Segundo elemento: ${segundoElemento}`;
}

const array = [10, 20, 30];
console.log(obtenerElementos(array)); // Output: "Primer elemento: 10, Segundo elemento: 20"
```
