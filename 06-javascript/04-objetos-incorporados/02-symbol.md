<h1 align="center">Symbol</h1>

<h2>📑 Contenido</h2>

- [Symbol](#symbol)
  - [Ejemplos](#ejemplos)

## Symbol

Symbol es un tipo de dato primitivo y también es un objeto incorporado. Fue introducido en ECMAScript 6 (ES6) para representar **valores únicos e inmutables**, y se utiliza principalmente como identificadores para las propiedades de los objetos.

Los símbolos son útiles principalmente para evitar colisiones de nombres de propiedad en objetos, ya que los símbolos son siempre únicos.

### Ejemplos

```js
// Crear Símbolo
const miSymbol = Symbol();

// Agregar descripción, útil para propósitos de depuración
const miSymbolConDescripcion = Symbol("Descripción de mi Symbol");

// Dos símbolos con el mismo nombre NO SON IGUALES.
const symbol1 = Symbol("Descripción");
const symbol2 = Symbol("Descripción");

console.log(symbol1 === symbol2); // Output: false

// Evitar colisiones de nombres de propiedad en objetos.
// Utilizar como claves de propiedades en objetos para garantizar que no haya conflictos con nombres de propiedades existentes.

const miSymbol = Symbol("clave_unica");

const objeto = {};
objeto[miSymbol] = "valor único";

console.log(objeto[miSymbol]); // Output: "valor único"
```
