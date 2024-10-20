<h1 align="center">Conversion</h1>

<h2>📑 Contenido</h2>

- [Conversion y Coercion](#conversion-y-coercion)
  - [Coercion](#coercion)
  - [Conversion](#conversion)
- [Implícito y Explicito](#implícito-y-explicito)
- [String](#string)
- [Numeric](#numeric)
- [Boolean](#boolean)

## Conversion y Coercion

### Coercion

JavaScript es un lenguaje de tipado débil, lo que significa que convierte automáticamente los tipos de datos cuando es necesario. Este proceso se llama coerción de tipo. La coerción de tipo puede ser implícita o explícita.

### Conversion

La conversión de tipo es otro proceso que implica convertir un valor de un tipo a otro. Esto también se puede hacer implícita o explícitamente.

## Implícito y Explicito

La conversión explícita se produce cuando el desarrollador convierte manualmente un tipo de datos en otro.

```js
let str = "123";
let num = Number(str);
```

La conversión implícita se produce cuando JavaScript convierte automáticamente un tipo de datos en otro.

```js
let str = "123";
let num = 456;
let result = str + num; // result es '123456'
```

## String

```js
let value = true;
alert(typeof value); // boolean

value = String(value); // now value is a string "true"
alert(typeof value); // string
```

## Numeric

Automática:

```js
alert("6" / "2"); // 3, strings are converted to numbers
```

Conversion Explicita

```js
let str = "123";
alert(typeof str); // string

let num = Number(str); // becomes a number 123

alert(typeof num); // number
```

## Boolean

```js
alert(Boolean(1)); // true
alert(Boolean(0)); // false

alert(Boolean("hello")); // true
alert(Boolean("")); // false
alert(Boolean(" ")); // spaces, also true (any non-empty string is true)
```
