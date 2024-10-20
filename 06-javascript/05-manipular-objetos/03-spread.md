<h1 align="center">Spread</h1>

<h2>📑 Contenido</h2>

- [Spread](#spread)
- [Arrays](#arrays)
  - [Concatenar dos arrays con spread](#concatenar-dos-arrays-con-spread)
- [Cadenas/String](#cadenasstring)
- [Funciones](#funciones)
- [Objetos](#objetos)

## Spread

Spread es una forma de expandir un objeto iterable, como un array o una cadena, en lugares donde se esperan cero o más argumentos (para llamadas de función) o elementos (para literales de array). También se puede usar para copiar las propiedades de un objeto en otro objeto, creando un nuevo objeto con las propiedades combinadas.

## Arrays

```js
console.log(Math.max(0, 4, 9, 14, 19)); //19

const array = [0, 4, 9, 14, 19];
console.log(Math.max(array)); //NaN
console.log(Math.max(...array)); //19
```

### Concatenar dos arrays con spread

```js
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const arrTotal = [...arr1, ...arr2];

console.log(arrTotal);
```

## Cadenas/String

```js
let quijote = "En un lugar de la Mancha, de cuyo nombre no quiero acordarme";
console.log([...quijote]);
```

## Funciones

```js
function suma(a, b, c) {
  return a + b + c;
}
const arrSumar = [3, 3, 4];
console.log(suma(...arrSumar));
```

## Objetos

```js
const persona = { nombre: "Ana", edad: 25 };
const direccion = { calle: "Mayor", numero: 10 };
const personaConDireccion = { ...persona, ...direccion }; // equivalente a Object.assign({}, persona, dirección)
console.log(personaConDireccion); // {nombre: 'Ana', edad: 25, calle: 'Mayor', numero: 10}
```
