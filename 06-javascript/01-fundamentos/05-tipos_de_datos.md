<h1 align="center">Tipos de Datos</h1>

<h2>📑 Contenido</h2>

- [Tipos de datos](#tipos-de-datos)
  - [Tipos](#tipos)
  - [Ejemplo](#ejemplo)
- [Tipado dinámico](#tipado-dinámico)
  - [Ejemplo](#ejemplo-1)

## Tipos de datos

El último estándar ECMAScript define ocho tipos de datos. Los otros elementos fundamentales(No primitivos) en el lenguaje son los Objetos y las funciones. Puedes pensar en objetos como contenedores con nombre para los valores, y las funciones como procedimientos que puedes programar en tu aplicación.

### Tipos

- **Número (Number):** Representa valores numéricos. Pueden ser enteros o números de punto flotante. Ejemplos: 42, 3.14159.
- **Cadena de texto (String):** Representa secuencias de caracteres. Se pueden crear utilizando comillas simples o dobles. Ejemplos: "Hola, mundo", 'JavaScript'.
- **Booleano (Boolean):** Representa un valor de verdadero o falso. Puede ser true o false.
- **Nulo (Null):** Representa la ausencia intencional de cualquier valor u objeto. null es un valor primitivo en JavaScript.
- **Indefinido (Undefined):** Representa una variable que se ha declarado pero aún no se le ha asignado un valor. También se usa como el valor de retorno predeterminado de funciones que no tienen una declaración de retorno.
- **Símbolo (Symbol):** Introducido en ECMAScript 6 (ES6), los símbolos son valores primitivos únicos que se utilizan, por ejemplo, como propiedades de objetos para evitar colisiones de nombres.
- **BigInt (BigInt):** Introducido en ECMAScript 11 (ES11), BigInt representa números enteros más grandes de lo que se puede representar con el tipo de dato Number. Se crean añadiendo "n" al final de un número.
- **Objeto (Object):** Representa una colección de pares clave-valor. Los objetos pueden contener propiedades y métodos. Los objetos son estructuras de datos complejas y versátiles en JavaScript.

### Ejemplo

```js
let numero = 42; // Número
let texto = "Hola, mundo"; // Cadena de texto
let esVerdadero = true; // Booleano
let nulo = null; // Nulo
let indefinido; // Indefinido
let simbolo = Symbol("ejemplo"); // Símbolo
let objeto = { nombre: "John", edad: 30 }; // Objeto
let numeroGrande = 1234567890123456789012345678901234567890n; // BigInt
```

> [!NOTE]
>
> Excepto Object el resto son tipos de datos primitivos.
>
> Los datos primitivos representan valores simples y únicos. Los objetos pueden contener múltiples valores y métodos, mientras que los datos primitivos representan valores simples sin métodos asociados.

## Tipado dinámico

JavaScript es un lenguaje tipado dinámicamente. Esto significa que no tienes que especificar el tipo de dato de una variable cuando la declaras. También significa que los tipos de datos se convierten automáticamente según sea necesario durante la ejecución del script.

### Ejemplo

```js
//Conversion automática

var conversion = 40;

conversion = "De numero a cadena";

conversion = true;
```
