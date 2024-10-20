<h1 align="center">Date</h1>

<h2>📑 Contenido</h2>

- [Date](#date)
  - [Ejemplo](#ejemplo)
- [Métodos Date](#métodos-date)
  - [Mostrar año](#mostrar-año)
  - [Mostrar mes](#mostrar-mes)
  - [Mostrar día de la semana](#mostrar-día-de-la-semana)
  - [Mostrar día](#mostrar-día)
  - [Introducir datos](#introducir-datos)
  - [Resumen](#resumen)

## Date

El objeto incorporado Date se utiliza para trabajar con fechas y horas. Permite crear objetos que representan instantes de tiempo específicos, así como manipular, formatear y realizar cálculos con fechas y horas.

El constructor Date() puede tomar varios tipos de argumentos, como una cadena de fecha, milisegundos desde el 1 de enero de 1970 (también conocido como tiempo Unix), o valores separados para año, mes, día, etc.

### Ejemplo

```js
// Crear fecha
const f1 = new Date();
console.log(f1);

// Fecha concreta
const f2 = new Date("2019-05-7");
console.log(f2);
```

## Métodos Date

El objeto Date también proporciona métodos para realizar operaciones con fechas, como setFullYear(), setMonth(), setDate(), setHours(), etc., para establecer los componentes de la fecha, y métodos como getTime() para obtener el tiempo en milisegundos desde el 1 de enero de 1970.

### Mostrar año

```JS
console.log(f1.getFullYear());
```

### Mostrar mes

```JS
console.log(f1.getMonth() + 1);
```

### Mostrar día de la semana

```JS
console.log(f1.getDay());
```

### Mostrar día

```JS
console.log(f1.getDate());
```

### Introducir datos

```JS
f1.setDate(14);
f1.setFullYear(2014);
f1.setMonth(4 - 1);
console.log(f1);

```

### Resumen

```js
// Crear un objeto Date que representa la fecha y hora actual
const fechaActual = new Date();

// Crear un objeto Date utilizando una cadena de fecha
const fechaEjemplo = new Date("2024-03-13");

// Crear un objeto Date utilizando milisegundos desde el 1 de enero de 1970
const fechaMilisegundos = new Date(1615593600000); // Milisegundos correspondientes al 13 de marzo de 2021

// Crear un objeto Date utilizando valores separados para año, mes y día
const fechaSeparada = new Date(2024, 2, 13); // Meses en JavaScript se indexan desde 0, por lo que 2 representa marzo

// Obtener el año, mes, día, etc. de un objeto Date
const año = fechaActual.getFullYear();
const mes = fechaActual.getMonth(); // Los meses se indexan desde 0, por lo que enero es 0
const dia = fechaActual.getDate();
const hora = fechaActual.getHours();
const minutos = fechaActual.getMinutes();
const segundos = fechaActual.getSeconds();

// Formatear una fecha como una cadena de texto
const cadenaFecha = fechaActual.toString(); // Ejemplo: "Mon Mar 13 2024 12:30:45 GMT-0700 (Pacific Daylight Time)"
```
