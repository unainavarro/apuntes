<h1 align="center">RegExp</h1>

<h2>📑 Contenido</h2>

- [RegExp](#regexp)
- [Banderas(flags)](#banderasflags)
  - [Banderas más comunes](#banderas-más-comunes)
- [Métodos](#métodos)
  - [test()](#test)
  - [exec()](#exec)
- [Propiedades](#propiedades)
  - [source()](#source)
  - [flags()](#flags)
  - [global, ignoreCase, multiline, sticky, unicode:](#global-ignorecase-multiline-sticky-unicode)
  - [lastIndex:](#lastindex)

## RegExp

El objeto incorporado RegExp en JavaScript se utiliza para trabajar con expresiones regulares. Las expresiones regulares son patrones utilizados para hacer coincidir combinaciones de caracteres en cadenas de texto. El objeto RegExp proporciona métodos para crear, manipular y trabajar con expresiones regulares.

```js
//Puedes crear una expresión regular utilizando la sintaxis literal de expresiones regulares o utilizando el constructor RegExp():

const expresionRegularLiteral = /patrón/;
const expresionRegularConstructor = new RegExp("patrón");
```

## Banderas(flags)

Las expresiones regulares pueden tener varias banderas (también conocidas como "flags") que modifican su comportamiento.

### Banderas más comunes

- **i (ignoreCase):**
  - Esta bandera indica que la coincidencia debe ser insensible a mayúsculas y minúsculas. Es decir, no distingue entre letras mayúsculas y minúsculas.
  - Por ejemplo, /patrón/i coincidiría con "Patrón", "PATRÓN", "patrón", etc.
- **g (global):**
  - Esta bandera indica que la búsqueda de coincidencias debe ser global, es decir, encuentra todas las coincidencias en lugar de detenerse después de la primera.
  - Por ejemplo, /patrón/g buscaría todas las ocurrencias de "patrón" en una cadena.
- **m (multiline):**
  - Esta bandera afecta al comportamiento de las anclas ^ (inicio de línea) y $ (final de línea).
  - Cuando está activada, ^ y $ también coinciden con el inicio y el final de cada línea dentro de una cadena de texto multilínea.
  - Por ejemplo, /^inicio/m coincidiría con "inicio" al comienzo de una línea dentro de una cadena multilínea.
- **s (dotAll):**
  - Esta bandera hace que el metacarácter . coincida con cualquier carácter, incluido el salto de línea (\n), que normalmente no coincide con `.`.
  - Esta bandera no es ampliamente compatible en todos los navegadores o entornos.

## Métodos

### test()

Este método se utiliza para verificar si una cadena coincide con la expresión regular.<br>
Devuelve true si la cadena coincide con la expresión regular, de lo contrario devuelve false.

```js
const expresion = /patrón/;
console.log(expresion.test("cadena que contiene el patrón")); // true
```

### exec()

Este método se utiliza para encontrar la primera coincidencia de la expresión regular en una cadena. <br>
Devuelve un array con información sobre la coincidencia, o null si no se encuentra ninguna coincidencia.

```js
const expresion = /patrón/;
const resultado = expresion.exec("cadena que contiene el patrón");
console.log(resultado); // ["patrón", index: 19, input: "cadena que contiene el patrón", groups: undefined]
```

## Propiedades

### source()

Devuelve el patrón de la expresión regular como una cadena de texto. <br>
Es útil cuando necesitas acceder al patrón de la expresión regular como una cadena.

```js
const expresion = /patrón/;
console.log(expresion.source); // "patrón"
```

### flags()

Devuelve las banderas de la expresión regular como una cadena de texto.

```js
const expresion = /patrón/gi;
console.log(expresion.flags); // "gi"
```

### global, ignoreCase, multiline, sticky, unicode:

Propiedades booleanas que indican si las banderas g, i, m, y, u están activadas respectivamente.

```js
const expresion = /patrón/g;
console.log(expresion.global); // true
console.log(expresion.ignoreCase); // false
console.log(expresion.multiline); // false
```

### lastIndex:

Indica la posición donde comenzará la próxima búsqueda en una cadena después de usar un método como exec() con la bandera g. <br>
Útil cuando realizas búsquedas en una cadena utilizando una expresión regular con la bandera g.

```js
const expresion = /patrón/g;
expresion.exec("cadena con patrón"); // Ejemplo de búsqueda
console.log(expresion.lastIndex); // 11
```
