<h1 align="center">Variables</h1>

<h2>📑 Contenido</h2>

- [¿Qué son las variables?](#qué-son-las-variables)
- [Declarar variables](#declarar-variables)
  - [var](#var)
  - [Let](#let)
  - [Const](#const)
- [Expresiones y Declaraciones](#expresiones-y-declaraciones)
  - [Expresiones](#expresiones)
  - [Declaraciones](#declaraciones)

## ¿Qué son las variables?

En programación, una variable es un espacio reservado en la memoria que se utiliza para almacenar datos y cuyo valor puede cambiar durante la ejecución de un programa. Las variables tienen un nombre único que se utiliza para hacer referencia a ellas y un tipo de dato que define qué tipo de valores pueden almacenar

Javascript es un lenguaje débilmente tipado,no se indica de qué tipo es una variable al declararla y su valor puede cambiar de tipo.

## Declarar variables

`let`, `const` y `var` son palabras clave utilizadas para declarar variables en JavaScript. Cada una tiene su propio alcance y comportamiento.

### var

Las variables var existen en toda la función que se declara.

```js
//Ejemplo variable Var

console.log("---Var---");

var pruebaVar = 1;
console.log("Fuera de un bloque: " + pruebaVar);

if (true) {
  var pruebaVar = 2;
  console.log("Dentro de un bloque: " + pruebaVar);
}

console.log("Final: " + pruebaVar);
```

### Let

Las variables let sólo existen en el bloque que se declaran.

```js
//Ejemplo variable Let

console.log("---Let---");

let pruebaLet = 1;
console.log("Fuera de un bloque: " + pruebaLet);

if (true) {
  let pruebaLet = 2;
  console.log("Dentro de un bloque: " + pruebaLet);
}

console.log("Final: " + pruebaLet);
```

### Const

Las variables constantes presentan un ámbito de bloque.
el valor de una constante no puede cambiarse a través de la reasignación.

Las constantes no se pueden redeclarar.

```js
//Ejemplo variable Const

const url = "https://www.const.com";
```

> [!NOTE]
>
> ¿Cuando usarlas?
>
> En general, es una buena práctica **utilizar const siempre que sea posible**, ya que esto ayuda a evitar errores y hace que el código sea más fácil de leer y mantener. Si necesitas **reasignar una variable, utiliza let**. Solo utiliza **var si necesitas compatibilidad** con versiones anteriores de JavaScript o si necesitas un alcance diferente.

## Expresiones y Declaraciones

### Expresiones

Una expresión es cualquier fragmento de código que produce un valor. Puede ser tan simple como un valor literal, como 5 o "hola", o más complejo, como una operación aritmética o una llamada a una función.

- Las expresiones pueden aparecer en muchos contextos diferentes en JavaScript, como asignaciones, condiciones, llamadas a funciones, entre otros.
- Es importante tener en cuenta que una expresión siempre tiene un valor, incluso si ese valor es undefined o null.

```js
5;
("hola");
3 + 4;
function();
```

### Declaraciones

Una declaración es una instrucción que declara o define algo en el código. Puede ser una declaración de variable, una declaración de función, una declaración de bucle, entre otros.

- Las declaraciones no necesariamente producen un valor como lo hacen las expresiones, pero son necesarias para controlar el flujo del programa y para definir la estructura y el comportamiento del código.
- Las declaraciones definen la estructura del código y pueden **contener expresiones dentro de ellas.**

```js
let x = 5;
function saludar() {
  console.log("Hola");
}
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

> [!NOTE]
>
> Las expresiones producen un valor, las declaraciones definen o declaran algo en el código, como variables, funciones, bucles, etc.
