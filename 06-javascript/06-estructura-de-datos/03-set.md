<h1 align="center">Set</h1>

<h2>📑 Contenido</h2>

- [Set](#set)
  - [Recorrer Set](#recorrer-set)
- [WeakSet](#weakset)
- [Set vs Map](#set-vs-map)

## Set

El objeto Set permite almacenar valores únicos de cualquier tipo, ya sean valores primitivos o referencias a objetos.

```js
const mySet1 = new Set();

mySet1.add(1); // Set(1) { 1 }
mySet1.add(5); // Set(2) { 1, 5 }
mySet1.add(5); // Set(2) { 1, 5 }
mySet1.add("some text"); // Set(3) { 1, 5, 'some text' }
const o = { a: 1, b: 2 };
mySet1.add(o);

mySet1.add({ a: 1, b: 2 }); // o is referencing a different object, so this is okay

mySet1.has(1); // true
mySet1.has(3); // false, since 3 has not been added to the set
mySet1.has(5); // true
mySet1.has(Math.sqrt(25)); // true
mySet1.has("Some Text".toLowerCase()); // true
mySet1.has(o); // true

mySet1.size; // 5

mySet1.delete(5); // removes 5 from the set
mySet1.has(5); // false, 5 has been removed

mySet1.size; // 4, since we just removed one value

mySet1.add(5); // Set(5) { 1, 'some text', {...}, {...}, 5 } - a previously deleted item will be added as a new item, it will not retain its original position before deletion

console.log(mySet1); // Set(5) { 1, "some text", {…}, {…}, 5 }
```

### Recorrer Set

```js
for (const item of mySet1) {
  console.log(item);
}
// 1, "some text", { "a": 1, "b": 2 }, { "a": 1, "b": 2 }, 5

for (const item of mySet1.keys()) {
  console.log(item);
}
// 1, "some text", { "a": 1, "b": 2 }, { "a": 1, "b": 2 }, 5

for (const item of mySet1.values()) {
  console.log(item);
}
// 1, "some text", { "a": 1, "b": 2 }, { "a": 1, "b": 2 }, 5

// key and value are the same here
for (const [key, value] of mySet1.entries()) {
  console.log(key);
}
// 1, "some text", { "a": 1, "b": 2 }, { "a": 1, "b": 2 }, 5

// Convert Set object to an Array object, with Array.from
const myArr = Array.from(mySet1); // [1, "some text", {"a": 1, "b": 2}, {"a": 1, "b": 2}, 5]

// the following will also work if run in an HTML document
mySet1.add(document.body);
mySet1.has(document.querySelector("body")); // true

// converting between Set and Array
const mySet2 = new Set([1, 2, 3, 4]);
console.log(mySet2.size); // 4
console.log([...mySet2]); // [1, 2, 3, 4]

// intersect can be simulated via
const intersection = new Set([...mySet1].filter((x) => mySet2.has(x)));

// difference can be simulated via
const difference = new Set([...mySet1].filter((x) => !mySet2.has(x)));

// Iterate set entries with forEach()
mySet2.forEach((value) => {
  console.log(value);
});
// 1
// 2
// 3
// 4
```

## WeakSet

WeakSet permite almacenar objetos únicos de manera débil, es decir, sin impedir que los objetos contenidos sean recolectados por el recolector de basura (garbage collector) si no hay otras referencias a esos objetos en otro lugar de la aplicación. Un WeakSet solo puede contener objetos y no permite almacenar valores primitivos.

Al igual que WeakMap, la principal característica de un WeakSet es que los objetos almacenados no previenen que sean recolectados por el recolector de basura si no hay otras referencias a esos objetos.

```js
let weakSet = new WeakSet();

// Crear algunos objetos
let objeto1 = {};
let objeto2 = {};
let objeto3 = {};

// Agregar los objetos al WeakSet
weakSet.add(objeto1);
weakSet.add(objeto2);

// Verificar si el WeakSet contiene los objetos
console.log(weakSet.has(objeto1)); // Resultado: true
console.log(weakSet.has(objeto2)); // Resultado: true
console.log(weakSet.has(objeto3)); // Resultado: false

// Eliminar un objeto del WeakSet
weakSet.delete(objeto2);

// Verificar si el WeakSet sigue conteniendo el objeto eliminado
console.log(weakSet.has(objeto2)); // Resultado: false
```

## Set vs Map

La principal diferencia entre Set y Map es que Set almacena valores únicos sin claves, mientras que Map almacena pares clave-valor.
