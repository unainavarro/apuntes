<h1 align="center">Condicionales</h1>

<h2>📑 Contenido</h2>

- [Condicional if \& else if](#condicional-if--else-if)
  - [Ejemplo](#ejemplo)
- [Operador ternario](#operador-ternario)
  - [Ejemplo](#ejemplo-1)
- [Condicional switch](#condicional-switch)
  - [Ejemplo](#ejemplo-2)

## Condicional if & else if

La estructura condicional if se utiliza para ejecutar un bloque de código si una condición especificada se evalúa como verdadera.

### Ejemplo

```js
// Resultado: Es false
console.log("---IF---");
if (false) {
  console.log("Es true");
} else {
  console.log("Es false");
}

//Comprobar si puede votar(mayor o igual a 18)
let edad = 18;

if (edad >= 18) {
  console.log("Eres mayor de edad. Puedes votar.");
} else {
  console.log("Eres menor de edad. No puedes votar.");
}
//Resultado: Eres mayor de edad. Puedes votar.

//Multiples condiciones: Calificar nota a,b,c
let puntos = 75;

if (puntos >= 90) {
  console.log("Aprobaste con una A");
} else if (puntos >= 80) {
  console.log("Aprobaste con una B");
} else if (puntos >= 70) {
  console.log("Aprobaste con una C");
} else {
  console.log("No aprobaste. Debes esforzarte más.");
}
//Resultado: Aprobaste con una C
```

> [!NOTE]
>
> La condición en un if debe ser una expresión que se pueda evaluar como verdadera o falsa. Puede ser una comparación (>, <, >=, <=, ===, !==), una expresión lógica (&& para "y", || para "o"), o cualquier otra expresión que devuelva un valor booleano.

## Operador ternario

El operador ternario es una forma abreviada de escribir una estructura condicional if...else. Tanto el operador ternario como la estructura if...else se utilizan para tomar decisiones basadas en condiciones.

Sintaxis: <br>
`condición ? expresión_si_verdadero : expresión_si_falso;`

### Ejemplo

```js
//Comprobar si puede votar(mayor o igual a 18)
let edad = 20;
let mensaje =
  edad >= 18
    ? "Eres mayor de edad. Puedes votar."
    : "Eres menor de edad. No puedes votar.";

console.log(mensaje);

//Otro ejemplo
true ? "Es true" : "Es Falso";
//Resultado: Es true
```

## Condicional switch

La estructura switch en JavaScript se utiliza para realizar múltiples comprobaciones basadas en el valor de una expresión.

### Ejemplo

```js
//Comprobar el valor de color
const color = "azul";

switch (color) {
  case "rojo":
    console.log("Color es rojo");
  case "azul":
    console.log("Color es azul");
}

//Día de la semana según su numero
let diaDeLaSemana = 3;
let nombreDia;

switch (diaDeLaSemana) {
  case 1:
    nombreDia = "Lunes";
    break;
  case 2:
    nombreDia = "Martes";
    break;
  case 3:
    nombreDia = "Miércoles";
    break;
  case 4:
    nombreDia = "Jueves";
    break;
  case 5:
    nombreDia = "Viernes";
    break;
  case 6:
    nombreDia = "Sábado";
    break;
  case 7:
    nombreDia = "Domingo";
    break;
  default:
    nombreDia = "Día no válido";
}

console.log("Hoy es " + nombreDia);
//Resultado: Hoy es Miércoles

//El bloque default se ejecutará si ninguno de los casos coincide con el valor de la expresión.
```

> [!IMPORTANT]
>
> Es importante tener en cuenta que en JavaScript, el switch compara valores utilizando el operador de igualdad estricta (===), lo que significa que también se compara el tipo de dato.
