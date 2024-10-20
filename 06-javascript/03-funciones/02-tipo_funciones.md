<h1 align="center">Tipo de Funciones</h1>

<h2>📑 Contenido</h2>

- [Funciones Regulares](#funciones-regulares)
- [Funciones Flecha](#funciones-flecha)
- [Funciones Asignadas](#funciones-asignadas)
- [Funciones IIFE(Expresiones de Funciones Ejecutadas Inmediatamente)](#funciones-iifeexpresiones-de-funciones-ejecutadas-inmediatamente)
- [Diferencias y Características](#diferencias-y-características)

## Funciones Regulares

Estas funciones son las más comunes y se utilizan para realizar una tarea específica. Pueden tomar uno o más argumentos y devolver un valor.

```js
console.log("Funciones normales");
function saludar(nombre) {
  console.log("Hola: " + nombre);
}

//Lamar a saludar pasando "nombre " como argumento.
saludar("Un Nombre ");
```

## Funciones Flecha

Estas funciones son una forma más corta de escribir funciones regulares
y se utilizan a menudo en combinación con métodos de matriz como map, filter y reduce.

```js
/*Sintaxis (param1,param2) => { Sentencia};
            (param1,param2) => expresion;
            () => { Sentencia, return ...};
            true => {sentencia} */
console.log("Función Flecha");

let error = (msg) => {
  return "Error:  " + msg;
};

//Otro ejemplo
let error2 = (msg) => "Error:  " + msg;

console.log(error("404"));
console.log(error2("505"));
```

## Funciones Asignadas

Son funciones que se asignan a una variable/constante.

```js
const sumar = function (a, b) {
  return (total = a + b);
};

console.log("Asignada a una variable: " + sumar(4, 6));
```

## Funciones IIFE(Expresiones de Funciones Ejecutadas Inmediatamente)

Son funciones que se ejecutan tan pronto como se definan.

```js
(function () {
  console.log("Función IIFE ");
})();
```

## Diferencias y Características

- **Funciones regulares**
  - Son declaraciones de funciones que siguen la sintaxis tradicional de JavaScript.
  - Se definen utilizando la palabra clave function.
  - Pueden tener un nombre que se utiliza para llamar a la función dentro del código.
  - Tienen su propio contexto de this.
  - Se utilizan comúnmente para la definición de funciones generales en el código.
- **Funciones flecha**
  - Introducidas en ECMAScript 6 (ES6), proporcionan una sintaxis más concisa para definir funciones en JavaScript.
  - Se definen utilizando la sintaxis () => {}.
  - No tienen su propio contexto de this; en su lugar, this en una función flecha se toma del contexto circundante (lexical).
  - Son especialmente útiles en situaciones donde se necesita mantener el contexto de this, como en callbacks de eventos o iteraciones de array.
  - No pueden ser nombradas, lo que significa que generalmente se utilizan para funciones anónimas.
- **Funciones asignadas**
  - Son funciones que se asignan a variables o constantes para ser reutilizadas o pasadas como argumentos a otras funciones.
  - Se pueden definir utilizando tanto la sintaxis de función regular como la de función flecha.
  - Pueden ser nombradas o anónimas, dependiendo de si se les asigna un nombre o se les asigna directamente a una variable.
- **Funciones IIFE**
  - Son funciones que se definen y se ejecutan inmediatamente después de su declaración.
  - Se envuelven en paréntesis para convertirlas en expresiones, seguidas de un par de paréntesis adicionales para ejecutar la función.
  - Se utilizan comúnmente para evitar la contaminación del ámbito global y crear un ámbito privado para variables locales.
  - Son útiles para el encapsulamiento de código y la creación de módulos.

> [!NOTE]
>
> Las diferencias entre estas tipos de funciones radican en su sintaxis, manejo de contexto de this, uso de nombre y comportamiento en el código. Es importante comprender estas diferencias para utilizar el tipo de función más adecuado para cada situación en el desarrollo de aplicaciones JavaScript.
