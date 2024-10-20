<h1 align="center">Number</h1>

<h2>📑 Contenido</h2>

- [Number](#number)
- [Crear objeto Numbers](#crear-objeto-numbers)
- [Propiedades de Number](#propiedades-de-number)
  - [Number.MAX\_VALUE:](#numbermax_value)
  - [Number.MIN\_VALUE:](#numbermin_value)
  - [Number.POSITIVE\_INFINITY:](#numberpositive_infinity)
  - [Number.NEGATIVE\_INFINITY:](#numbernegative_infinity)
  - [Number.NaN:](#numbernan)
  - [Number.EPSILON:](#numberepsilon)
- [Métodos de Number](#métodos-de-number)
  - [Number.isNaN(value)](#numberisnanvalue)
  - [Number.isInteger()](#numberisinteger)
  - [Number.isFinite()](#numberisfinite)
  - [Number.toFixed(digits)](#numbertofixeddigits)
  - [Number.toPrecision(precision)](#numbertoprecisionprecision)
  - [Number.toString(radix)](#numbertostringradix)
  - [Number.parseInt()](#numberparseint)

## Number

El objeto incorporado Number se utiliza para trabajar con valores numéricos. Puedes utilizar este objeto para realizar diversas operaciones y manipulaciones con números.

## Crear objeto Numbers

Puedes crear un objeto Number utilizando el constructor Number():

```js
//Con constructor
let num = new Number(44);

//Sin constructor
let num = 44;
```

> [!NOTE]
>
> En general, se recomienda utilizar la forma literal para crear números, ya que es más sencilla y más eficiente en términos de rendimiento.

## Propiedades de Number

El objeto Number tiene varias propiedades incorporadas que proporcionan información o valores relacionados con los números.

### Number.MAX_VALUE:

Representa el valor máximo finito positivo que puede ser representado en JavaScript.

```js
// Mayor valor positivo representable
console.log(Number.MAX_VALUE); //Resultado: 1.7976931348623157e+308
```

### Number.MIN_VALUE:

Representa el valor positivo más pequeño que puede ser representado en JavaScript.

```js
// Menor valor positivo representable
console.log(Number.MIN_VALUE); //Resultado: 5e-324
```

### Number.POSITIVE_INFINITY:

Representa el valor positivo infinito, que se obtiene al exceder el valor máximo representable.

```js
// Infinito positivo
console.log(Number.POSITIVE_INFINITY); //Resultado: Infinity
```

### Number.NEGATIVE_INFINITY:

Representa el valor negativo infinito, que se obtiene al exceder el valor mínimo representable.

```js
// Infinito negativo
console.log(Number.NEGATIVE_INFINITY); //Resultado: -Infinity
```

### Number.NaN:

Representa el valor "Not a Number" (no es un número), que se obtiene cuando se realiza una operación que no produce un número válido.

```js
// Not a Number
console.log(Number.NaN); //Resultado: NaN
```

### Number.EPSILON:

Representa la diferencia entre 1 y el número más pequeño que puede ser representado de forma distinta a 1.

```js
// Diferencia entre 1 y el siguiente número representable
console.log(Number.EPSILON); //Resultado: 2.220446049250313e-16
```

> [!NOTE]
>
> Estas propiedades son útiles para realizar comparaciones y operaciones con números en JavaScript. Por ejemplo, puedes usar Number.MAX_VALUE para verificar si un número es demasiado grande para ser representado con precisión en JavaScript. También puedes usar Number.EPSILON para comparar números en punto flotante con una tolerancia pequeña y manejar problemas de precisión.

## Métodos de Number

Además de las propiedades, el objeto Number también proporciona varios métodos que puedes utilizar para realizar operaciones numéricas y manipulaciones.

### Number.isNaN(value)

Comprueba si un valor es NaN.

```js
const x = 10;
const a = "texto";

console.log(Number.isNaN(NaN)); // true
console.log(Number.isNaN(x * "hola")); //true
console.log(Number.isNaN(45)); //false
console.log(isNaN(x * "hola")); //true
```

### Number.isInteger()

El método Number.isInteger() determina si el valor pasado es de tipo entero.

```js
console.log(Number.isInteger(0)); // true
console.log(Number.isInteger(1)); // true
console.log(Number.isInteger(0.1)); // false
console.log(Number.isInteger(NaN)); // false
console.log(Number.isInteger(Infinity)); // false
```

### Number.isFinite()

El método Number.isFinite() determina si el valor pasado es un número finito.

```js
console.log(Number.isFinite(Infinity)); // false
console.log(Number.isFinite(0)); // true
console.log(Number.isFinite(NaN)); // false
console.log(Number.isFinite(-Infinity)); // false
console.log(Number.isFinite(1 / 0)); // false
console.log(Number.isFinite(0 / 1)); // true
```

### Number.toFixed(digits)

Formatea un número utilizando una cantidad específica de dígitos decimales.

```js
let num = 3.14159;
let numFixed = num.toFixed(2); // Redondea a 2 decimales: "3.14"
```

### Number.toPrecision(precision)

Formatea un número utilizando una cantidad específica de dígitos significativos.

```js
let num = 3.14159;
let numPrecision = num.toPrecision(3); // "3.14"
```

### Number.toString(radix)

Convierte un número a una cadena. El parámetro opcional radix especifica la base numérica (entre 2 y 36).

```js
let num = 42;
let numStr = num.toString(); // "42"
// Cambiar base
console.log(num.toString(2)); //Binario
console.log(num.toString(8)); //Octal
console.log(num.toString(16)); //Hexadecimal
```

### Number.parseInt()

El método estático Number.parseInt() analiza un argumento de cadena y devuelve un número entero de la raíz o base especificada.

```js
console.log(Number.isInteger(13.45)); //false
console.log(Number.isInteger(13)); //true
```
