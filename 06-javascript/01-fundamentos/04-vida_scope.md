<h1 align="center">Vida y Scope(Ámbito)</h1>

<h2>📑 Contenido</h2>

- [Vida Útil](#vida-útil)
- [Ámbito(Alcance o Scope)](#ámbitoalcance-o-scope)
  - [Ámbito de bloque](#ámbito-de-bloque)
  - [Ámbito de función](#ámbito-de-función)
  - [Ámbito globales](#ámbito-globales)

## Vida Útil

La "vida útil de una variable" se refiere al período durante el cual una variable existe en la memoria de un programa y puede ser utilizada para almacenar y manipular datos. En términos generales, la vida útil de una variable comienza cuando se declara y se asigna un valor, y termina cuando ya no es accesible y puede ser eliminada de la memoria.

- La duración de una variable JavaScript comienza cuando se declara.
- Las variables de función (locales) se eliminan cuando se completa la función.
- En un explorador web, las variables globales se eliminan al cerrar el explorador ventana (o pestaña).
- Las variables declaradas con let tienen un alcance de bloque, lo que significa que solo están disponibles dentro del bloque en el que se declaran.
- Las variables declaradas con var tienen un alcance de función, lo que significa que están disponibles en toda la función en la que se declaran.
- Una vez que se ha ejecutado la función o el bloque de código en el que se declaró la variable, la variable ya no está disponible en la memoria.

## Ámbito(Alcance o Scope)

El "ámbito" (también conocido como "alcance") en programación se refiere al contexto en el que una variable es válida y puede ser utilizada. Es decir, define dónde y cuándo una variable puede ser referenciada y accedida en un programa.

### Ámbito de bloque

Antes de ES6 (2015), JavaScript solo tenía alcance global y alcance de función.
ES6 introdujo dos nuevas palabras clave importantes de JavaScript: let y const.
Estas dos palabras clave proporcionan Ámbito de bloque (Block Scope) en JavaScript.
No se puede acceder a las variables declaradas dentro de un bloque { } Desde fuera del bloque:

```js
{
  let x = 2;
}
// x can NOT be used here

{
  var x = 2;
}
// x CAN be used here
```

### Ámbito de función

Las variables declaradas dentro de una función JavaScript, se convierten en LOCAL a la función.
Las variables locales tienen un ámbito de función: Solo se puede acceder a ellos desde la función.

```js
// code here can NOT use carName

function myFunction() {
  let carName = "Volvo";
  // code here CAN use carName
}

// code here can NOT use carName
```

### Ámbito globales

Una variable declarada fuera de una función, se convierte en GLOBAL.

```js
let carName = "Volvo";
// code here can use carName

function myFunction() {
  // code here can also use carName
}
```
