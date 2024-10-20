<h1 align="center">Operadores</h1>

<h2>📑 Contenido</h2>

- [Operadores](#operadores)
  - [Operadores Aritméticos:](#operadores-aritméticos)
  - [Operadores de Comparación:](#operadores-de-comparación)
  - [Operadores de Asignación:](#operadores-de-asignación)
  - [Operadores Lógicos:](#operadores-lógicos)
  - [Operadores de Concatenación de Cadenas:](#operadores-de-concatenación-de-cadenas)
  - [Operadores de Incremento y Decremento:](#operadores-de-incremento-y-decremento)
  - [Operadores Ternarios:](#operadores-ternarios)
  - [Operador de Propagación (Spread Operator):](#operador-de-propagación-spread-operator)
  - [Operador Rest](#operador-rest)
- [Ejemplos Extra](#ejemplos-extra)

## Operadores

JavaScript incluye una variedad de operadores que se utilizan para realizar operaciones en valores y variables. Estos operadores se dividen en diferentes categorías según su funcionalidad.

Los operadores de comparación retornan un valor booleano.
Ten cuidado al usar comparaciones como > o < con variables que ocasionalmente pueden ser null/undefined. Revisar por separado si hay null/undefined es una buena idea.

### Operadores Aritméticos:

- `+` (Suma)
- `-` (Resta)
- `*` (Multiplicación)
- `/ `(División)
- `%` (Módulo, devuelve el resto de una división)
- `**` (Exponente)

```js
// Ejemplo suma
let a = 5;
let b = 3;
let suma = a + b; // suma es igual a 8
```

### Operadores de Comparación:

- `==` (Igual a)
- `!=` (No igual a)
- `===` (Igual a estricto, verifica igualdad de valor y tipo de dato)
- `!==` (No igual a estricto)
- `>` (Mayor que)
- `<` (Menor que)
- `>=` (Mayor o igual que)
- `<=` (Menor o igual que)

```js
//Comparar números
let a = 5;
let b = "5";
a == b; // true, valores iguales
a === b; // false, tipos de datos diferentes
```

### Operadores de Asignación:

- `=` (Asignación)
- `+=, -=, \*=, /=` (Operadores de asignación compuesta)

```js
// Asignar un valor
let x = 10;
x += 5; // x ahora es igual a 15
```

### Operadores Lógicos:

- `&&` (Y lógico)
- `||` (O lógico)
- `!` (Negación lógica)

```js
// Comparar edades
let edad = 20;
let esMayorDeEdad = edad >= 18 && edad <= 65; // esMayorDeEdad es true
```

### Operadores de Concatenación de Cadenas:

- `+` (Concatenación de cadenas)

```js
//Concatenar Cadena
let nombre = "Juan";
let apellido = "Pérez";
let nombreCompleto = nombre + " " + apellido; // "Juan Pérez"
```

### Operadores de Incremento y Decremento:

- `++` (Incremento)
- `--` (Decremento)

```js
// Crear un contador.(Utilizados en while)
let contador = 0;
contador++; // Incrementa en 1, contador es igual a 1
```

### Operadores Ternarios:

`condición ? valorSiVerdadero : valorSiFalso`

```js
//Condicional para determinar si es mayor o menor de edad.
let edad = 25;
let mensaje = edad >= 18 ? "Es mayor de edad" : "Es menor de edad";
```

### Operador de Propagación (Spread Operator):

Permite descomponer o expandir elementos de un iterable (como un array o un objeto iterable) en lugares donde se esperan múltiples elementos. Se representa mediante tres puntos suspensivos (`...`).

```js
//Copiar y combinar un arreglo.
let numeros = [1, 2, 3];
let otrosNumeros = [...numeros, 4, 5]; // [1, 2, 3, 4, 5]

//Clonar un objeto
let originalObjeto = { nombre: "Juan", edad: 30 };
let copiaObjeto = { ...originalObjeto };
console.log(copiaObjeto); // { nombre: "Juan", edad: 30 }
```

### Operador Rest

El operador rest, también representado por tres puntos suspensivos (...), se utiliza para recoger argumentos restantes en funciones o para recoger elementos restantes en destructuración de arrays o objetos.

> [!NOTE]
> A diferencia del operador de propagación(spread), que se usa para expandir elementos, el operador rest se utiliza para agrupar elementos restantes.
>
> - **Spread:** Expande elementos.
> - **Rest:** Agrupa elementos.

```js
// Recoge todos los elementos restantes después de primero y segundo en un array llamado resto.
const [primero, segundo, ...resto] = [1, 2, 3, 4, 5];
console.log(primero); // 1
console.log(segundo); // 2
console.log(resto); // [3, 4, 5]
```

## Ejemplos Extra

```js
//Comparaciones números
alert(2 > 1); // true (correcto)
alert(2 == 1); // false (incorrecto)
alert(2 != 1); // true (correcto)

//Comparaciones cadenas
/*
Compara por orden “de diccionario” o “lexicográfico”.
Si los primeros caracteres de ambas cadenas son los mismos, compare los segundos caracteres de la misma manera.
Si ambas cadenas tienen la misma longitud, entonces son iguales. De lo contrario, la cadena más larga es mayor.
Una letra mayúscula "A" no es igual a la minúscula "a". ¿Cuál es mayor? La "a" minúscula. ¿Por qué? Porque el carácter en minúsculas tiene un mayor índice en la tabla de codificación interna que utiliza JavaScript (Unicode).
*/
alert("Z" > "A"); // true
alert("Glow" > "Glee"); // true
alert("Bee" > "Be"); // true

//Igualdad estricta
alert(0 == false); // true
alert("" == false); // true
alert(0 === false); // falso, porque los tipos son diferentes

//El valor undefined no debe compararse con otros valores:
//Trata cualquier comparación con undefined/null (excepto la igualdad estricta ===) con sumo cuidado.
alert(null == undefined); // true
alert(null === undefined); // false
alert(undefined > 0); // false (1)
alert(undefined < 0); // false (2)
alert(undefined == 0); // false (3)
```
