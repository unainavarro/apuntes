<h1 align="center">Map y Weak Map</h1>

<h2>📑 Contenido</h2>

- [Map](#map)
  - [Objetos y Map](#objetos-y-map)
  - [Recorrer Map forEach()](#recorrer-map-foreach)
  - [Recorrer Map forEach()](#recorrer-map-foreach-1)
  - [Clonar un Map](#clonar-un-map)
- [Weak Map](#weak-map)
  - [Restricciones](#restricciones)
  - [Ejemplo](#ejemplo)

## Map

El objeto **Map** contiene pares clave-valor y recuerda la inserción original Orden de las llaves. Cualquier valor (tanto objetos como valores primitivos) se puede utilizar como ya sea una clave o un valor.

```js
const map1 = new Map();

map1.set("a", 1);
map1.set("b", 2);
map1.set("c", 3);

console.log(map1.get("a"));
// Expected output: 1

map1.set("a", 97);

console.log(map1.get("a"));
// Expected output: 97

console.log(map1.size);
// Expected output: 3

map1.delete("b");

console.log(map1.size);
// Expected output: 2
```

### Objetos y Map

El uso correcto para almacenar datos en el mapa es a través del método. set(key, value)

```js
const contacts = new Map();
contacts.set("Jessie", { phone: "213-555-1234", address: "123 N 1st Ave" });
contacts.has("Jessie"); // true
contacts.get("Hilary"); // undefined
contacts.set("Hilary", { phone: "617-555-4321", address: "321 S 2nd St" });
contacts.get("Jessie"); // {phone: "213-555-1234", address: "123 N 1st Ave"}
contacts.delete("Raymond"); // false
contacts.delete("Jessie"); // true
console.log(contacts.size); // 1
```

### Recorrer Map forEach()

La función toma dos argumentos: el valor del elemento y la clave del elemento.

```js
// Crear un objeto Map
var miMapa = new Map();
miMapa.set("uno", 1);
miMapa.set("dos", 2);
miMapa.set("tres", 3);

// Recorrer el objeto Map
miMapa.forEach(function (valor, clave) {
  console.log(clave + " = " + valor);
});
```

### Recorrer Map forEach()

La función toma dos argumentos: el valor del elemento y la clave del elemento.

```js
const myMap = new Map();
myMap.set(0, "zero");
myMap.set(1, "one");

for (const [key, value] of myMap) {
  console.log(`${key} = ${value}`);
}
// 0 = zero
// 1 = one

for (const key of myMap.keys()) {
  console.log(key);
}
// 0
// 1

for (const value of myMap.values()) {
  console.log(value);
}
// zero
// one

for (const [key, value] of myMap.entries()) {
  console.log(`${key} = ${value}`);
}
// 0 = zero
// 1 = one
```

### Clonar un Map

```js
const original = new Map([[1, "one"]]);

const clone = new Map(original);

console.log(clone.get(1)); // one
console.log(original === clone); // false (useful for shallow comparison)
```

## Weak Map

WeakMap es una estructura de datos en JavaScript introducida en ECMAScript 6 (ES6) que proporciona una colección de pares clave/valor donde las claves son objetos y los valores pueden ser de cualquier tipo. La característica principal de un WeakMap es que las referencias a los objetos utilizados como claves no impiden que los objetos sean recolectados por el recolector de basura (garbage collector) si no hay otras referencias a esos objetos en otro lugar de la aplicación.

Los objetos utilizados como claves en un WeakMap no impiden la eliminación de esos objetos de la memoria si ya no son necesarios en la aplicación, lo que puede ser útil en ciertos casos, como en el manejo de asociaciones débiles.

### Restricciones

- Las claves deben ser objetos.
- No tienen el método size ni métodos relacionados con la obtención de todas las claves o valores.
- No son iterables.

### Ejemplo

```js
let weakMap = new WeakMap();

// Objeto clave
let objetoClave = {};

// Asignar un valor al objeto clave en el WeakMap
weakMap.set(objetoClave, "Valor asociado con el objeto clave");

// Obtener el valor asociado con la clave del objeto
console.log(weakMap.get(objetoClave)); // Resultado: "Valor asociado con el objeto clave"

// Eliminar la referencia al objeto clave
objetoClave = null;

// Intentar obtener el valor asociado con la clave del objeto nuevamente
console.log(weakMap.get(objetoClave)); // Resultado: undefined
```
