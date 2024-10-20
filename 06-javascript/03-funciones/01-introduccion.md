<h1 align="center">Funciones</h1>

<h2>📑 Contenido</h2>

- [Funciones](#funciones)
- [Hoisting](#hoisting)
  - [Ejemplo](#ejemplo)

## Funciones

Las funciones son bloques de código reutilizable que se pueden definir una vez y luego llamar en cualquier momento durante la ejecución del programa.

```js
console.log("Funciones normales");
function saludar(nombre) {
  console.log("Hola: " + nombre);
}

//Lamar a saludar pasando "nombre " como argumento.
saludar("Un Nombre ");
```

## Hoisting

El hoisting de funciones es un comportamiento en JavaScript en el que las declaraciones de funciones son "elevadas" al principio de su ámbito de ejecución durante la fase de compilación, independientemente de dónde estén declaradas en el código fuente. Esto significa que, incluso si una función se declara más adelante en el código, puede ser invocada antes de su declaración sin provocar un error.

### Ejemplo

```js
saludar(); // Esto funcionará sin errores

function saludar() {
  console.log("¡Hola!");
}
```

Esto se debe a que, durante la fase de compilación, la declaración de la función saludar() se "eleva" al principio del ámbito de ejecución. Por lo tanto, la función está disponible para ser invocada en cualquier parte del ámbito, incluso antes de su declaración.

> [!IMPORTANT]
>
> Tener en cuenta que solo la declaración de la función se eleva durante el hoisting, no las asignaciones de funciones.
>
> ```js
> saludar(); // Esto dará un error: TypeError: saludar is not a function
> var saludar = function () {
>   console.log("¡Hola!");
> };
> ```
