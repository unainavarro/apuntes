<h1 align="center">String</h1>

<h2>📑 Contenido</h2>

- [String](#string)
- [Crear objeto String](#crear-objeto-string)
- [Propiedades/Métodos de String](#propiedadesmétodos-de-string)
  - [length](#length)
  - [charAt(index)](#charatindex)
  - [concat(string1, string2, ...)](#concatstring1-string2-)
  - [toUpperCase() y toLowerCase()](#touppercase-y-tolowercase)
  - [indexOf(subcadena)](#indexofsubcadena)
  - [slice(inicio, fin)](#sliceinicio-fin)
  - [search(cadena)](#searchcadena)
  - [include(cadena)](#includecadena)
  - [slice()](#slice)
  - [split()](#split)

## String

El objeto incorporado String se utiliza para trabajar con cadenas de texto. Las cadenas en JavaScript son secuencias de caracteres y se pueden manipular utilizando métodos proporcionados por el objeto String.

## Crear objeto String

Puedes crear un objeto Number utilizando el constructor Number():

```js
//Con constructor
let cadenaObjeto = new String("Hola, soy un objeto String.");

//Sin constructor
let cadenaLiteral = "Hola, soy una cadena literal.";
```

> [!NOTE]
>
> Usar la forma literal

## Propiedades/Métodos de String

Las cadenas de texto son primitivas, pero también se pueden tratar como objetos debido a la naturaleza de lenguaje de JavaScript. Aunque las cadenas primitivas no son objetos y no tienen propiedades, JavaScript proporciona un objeto String que tiene métodos incorporados que se pueden utilizar para realizar diversas operaciones con cadenas.

### length

La propiedad length devuelve la longitud de una cadena.

```js
let str = "Hola, mundo!";
console.log(str.length); // Devuelve la longitud de la cadena: 13
```

### charAt(index)

El método charAt() devuelve el carácter en la posición especificada.

```js
let str = "JavaScript";
console.log(str.charAt(0)); // Devuelve el primer carácter: "J"
```

### concat(string1, string2, ...)

El método concat() combina dos o más cadenas y devuelve una nueva cadena.

```js
let str1 = "Hola";
let str2 = "Mundo";
let resultado = str1.concat(", ", str2, "!");
console.log(resultado); // "Hola, Mundo!"
```

### toUpperCase() y toLowerCase()

Estos métodos devuelven una nueva cadena con todos los caracteres en mayúsculas o minúsculas, respectivamente.

```js
let str = "Hola, Mundo!";
console.log(str.toUpperCase()); // "HOLA, MUNDO!"
console.log(str.toLowerCase()); // "hola, mundo!"
```

### indexOf(subcadena)

El método indexOf() devuelve la posición de la primera ocurrencia de una subcadena.

```js
let str = "Hola, Mundo!";
console.log(str.indexOf("Mundo")); // Devuelve la posición de "Mundo": 6
```

### slice(inicio, fin)

El método slice() devuelve una porción de la cadena desde el índice de inicio hasta el índice de fin (sin incluir el carácter en el índice de fin).

```js
let str = "JavaScript";
console.log(str.slice(0, 4)); // "Java"
```

### search(cadena)

El método search() se utiliza para buscar una expresión regular dentro de una cadena de texto. Devuelve la posición del primer carácter de la primera coincidencia encontrada, o -1 si no se encuentra ninguna coincidencia. Si se proporciona una expresión regular sin la bandera g, search() buscará solo la primera coincidencia.

```js
const cadena = "La vida es bella";

console.log(cadena.search("vida")); // Output: 3
console.log(cadena.search(/bella/)); // Output: 11
console.log(cadena.search("noexiste")); // Output: -1
```

### include(cadena)

El método include() se utiliza para verificar si una cadena de texto contiene otra cadena específica. Devuelve true si la cadena de texto contiene la cadena especificada, y false en caso contrario.

La búsqueda se realiza utilizando el operador de igualdad estricta (===).

```js
let str = "JavaScript";
console.log(str.includes("hola")); // devuelve false
console.log(str.includes("Jav")); // devuelve true
```

### slice()

slice() se utiliza para extraer una parte de una cadena de texto y devolver esa parte como una nueva cadena. No modifica la cadena original. Puede tomar uno o dos argumentos.

```js
const cadena = "abcdefgh";
console.log(cadena.slice(2)); // Output: "cdefgh"
console.log(cadena.slice(2, 5)); // Output: "cde"
console.log(cadena.slice(-3)); // Output: "fgh"
```

### split()

split() divide una cadena de texto en un array de subcadenas basadas en un delimitador especificado y devuelve ese array. Puede tomar uno o dos argumentos y si se omite el delimitador, split() dividirá la cadena en caracteres individuales..

```js
const cadena = "apple,banana,orange";
console.log(cadena.split(",")); // Output: ["apple", "banana", "orange"]
console.log(cadena.split(",", 2)); // Output: ["apple", "banana"]
console.log(cadena.split("")); // Output: ["a", "p", "p", "l", "e", ",", "b", "a", "n", "a", "n", "a", ",", "o", "r", "a", "n", "g", "e"]
```
