<h1 align="center">Iterador</h1>

<h2>📑 Contenido</h2>

- [Iteradores](#iteradores)
  - [Ejemplo](#ejemplo)
- [Métodos Entries, Values y Key](#métodos-entries-values-y-key)
  - [Ejemplos](#ejemplos)

## Iteradores

En JavaScript, los iteradores son objetos que proporcionan una forma de recorrer secuencialmente una colección de elementos, como por ejemplo, los elementos de un array, los caracteres de una cadena de texto, o las propiedades de un objeto. Permiten acceder a cada elemento de la colección en orden y realizar operaciones sobre ellos.

Los iteradores en JavaScript están implementados utilizando el protocolo del iterador, que define un método next() que devuelve el siguiente elemento de la secuencia. Cada vez que se llama al método next(), se avanza al siguiente elemento y se devuelve un objeto con dos propiedades: value, que es el valor del elemento actual, y done, que es un booleano que indica si la iteración ha terminado o no.

> [!NOTE]
>
> Los iteradores son utilizados en muchas partes de JavaScript, como en los bucles `for...of, forEach(), map() filter()`.

### Ejemplo

```js
// Implementa un iterador personalizado que permite recorrer un carrito de compras

function crearIterador(carrito) {
  let i = 0; // Se inicializa un contador para el índice del carrito

  return {
    // Se devuelve un objeto con un método llamado siguiente
    siguiente: () => {
      // El método siguiente devuelve un objeto con las propiedades 'fin' y 'valor'
      let fin = i >= carrito.length; // Se comprueba si el índice es mayor o igual a la longitud del carrito
      let valor = !fin ? carrito[i++] : undefined; // Se obtiene el elemento actual del carrito y se incrementa el contador, o se establece el valor como undefined si ya se llegó al final del carrito

      return {
        fin: fin, // Se devuelve un booleano que indica si se ha llegado al final del carrito
        valor: valor, // Se devuelve el valor del elemento actual del carrito
      };
    },
  };
}

const carrito = ["Producto 1", "Producto 2", "Producto 3", "Producto 4"]; // Se define un array de elementos

const recorrerCarrito = crearIterador(carrito); // Se llama a la función crearIterador para crear un iterador sobre el carrito

console.log(recorrerCarrito.siguiente()); // Se llama al método siguiente del iterador y se imprime el resultado
console.log(recorrerCarrito.siguiente()); // Se llama al método siguiente del iterador y se imprime el resultado
console.log(recorrerCarrito.siguiente()); // Se llama al método siguiente del iterador y se imprime el resultado
console.log(recorrerCarrito.siguiente()); // Se llama al método siguiente del iterador y se imprime el resultado
console.log(recorrerCarrito.siguiente()); // Se llama al método siguiente del iterador y se imprime el resultado
```

## Métodos Entries, Values y Key

Los métodos entries(), values() y keys() son métodos disponibles en los objetos iterables en JavaScript, como arrays y objetos. Cada uno de estos métodos devuelve un objeto iterador que permite recorrer los elementos de la estructura de datos iterable de una manera específica.

- **entries():**
  - El método entries() retorna un objeto iterador que contiene pares clave-valor para cada elemento en el iterable, en el mismo orden que el iterador por defecto de un bucle for...of
  - Cada elemento del iterador retornado por entries() es un array de dos elementos, donde el primer elemento es la clave y el segundo es el valor asociado a esa clave.
- **values():**
  - El método values() retorna un objeto iterador que contiene los valores de cada elemento en el iterable, en el mismo orden que el iterador por defecto de un bucle for...of.
- **keys():**
  - El método keys() retorna un objeto iterador que contiene las claves de cada elemento en el iterable, en el mismo orden que el iterador por defecto de un bucle for...of.

### Ejemplos

```js
const ciudades = ["Berlin", "Amsterdam", "Madrid", "Paris"];
const ordenes = new Set([123, 231, 131, 102]);
const datos = new Map();

datos.set("nombre", "Unai");
datos.set("profesión", "Desarrollador Web");

// entries a las ciudades
for (let entry of ciudades.entries()) {
  console.log(entry);
}

// entries a las ordenes
for (let entry of ordenes.entries()) {
  console.log(entry);
}

// entries a los datos
for (let entry of datos.entries()) {
  console.log(entry);
}

// Values iterator
// values a las ciudades
for (let value of ciudades.values()) {
  console.log(value);
}

// values a las ordenes
for (let value of ordenes.values()) {
  console.log(value);
}

// values a los datos
for (let value of datos.values()) {
  console.log(value);
}

// Keys iterator
// keys a las ciudades
for (let keys of ciudades.keys()) {
  console.log(keys);
}

// keys a las ordenes
for (let keys of ordenes.keys()) {
  console.log(keys);
}

// keys a los datos
for (let keys of datos.keys()) {
  console.log(keys);
}

// Default
for (let ciudad of ciudades) {
  console.log(ciudad);
}

for (let orden of ordenes) {
  console.log(orden);
}

for (let dato of datos) {
  console.log(dato);
}

// Iterar en un string

const mensaje = "Aprendiendo JavaScript";

// Forma vieja
for (let i = 0; i < mensaje.length; i++) {
  console.log(mensaje[i]);
}

// forma nueva
for (let letra of mensaje) {
  console.log(letra);
}

// Iterar en un NODE LIST
const enlaces = document.getElementsByTagName("a");

for (let enlace of enlaces) {
  console.log(enlace.href);
}
```
