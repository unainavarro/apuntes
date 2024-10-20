<h1 align="center">Feedback Básicos</h1>

<h2>📑 Contenido</h2>

- [Console](#console)
  - [Imprimir mensajes](#imprimir-mensajes)
  - [Mensajes de advertencia](#mensajes-de-advertencia)
  - [Mensajes de error](#mensajes-de-error)
  - [Interpolación de cadenas](#interpolación-de-cadenas)
  - [Mostrar objetos en tabla](#mostrar-objetos-en-tabla)
  - [Limpiar la consola](#limpiar-la-consola)
  - [Contar elementos](#contar-elementos)
- [Alert](#alert)
- [Prompt](#prompt)
- [Confirm](#confirm)

## Console

La consola de JavaScript, a menudo referida como la "consola del navegador" o "console," es una herramienta que proporciona los navegadores web para interactuar con JavaScript y para depurar código. Puedes acceder a la consola en la mayoría de los navegadores web presionando la tecla F12 o haciendo clic derecho en una página web y seleccionando "Inspeccionar" o "Inspeccionar elemento," luego navegando a la pestaña "Consola."

### Imprimir mensajes

`console.log()`: Imprime mensajes informativos en la consola.

```js
//Texto
console.log("Hola, mundo!");

//Mostrar objetos y arrays
let persona = { nombre: "Juan", edad: 30 };
console.log(persona);

//Ejecutar funciones y expresiones
function suma(a, b) {
  return a + b;
}
console.log(suma(5, 3));

//Interpolación de cadenas
let nombre = "Juan";
console.log(`Hola, ${nombre}!`);
```

### Mensajes de advertencia

`console.warn()`: Muestra mensajes de advertencia en la consola.

```js
console.warn("Esto es una advertencia");
```

### Mensajes de error

`console.error()`: Muestra mensajes de error en la consola.

```js
console.error("Esto es un error");
```

### Interpolación de cadenas

`console.info()`: Muestra mensajes informativos en la consola.

```js
console.info("Información: Esta es una información importante.");
```

### Mostrar objetos en tabla

`console.table()`: Muestra datos en forma de tabla.

```js
let personas = [
  { nombre: "Ana", edad: 30 },
  { nombre: "Carlos", edad: 25 },
  { nombre: "Elena", edad: 35 },
];

console.table(personas);
```

### Limpiar la consola

`console.clear()`: Limpia la consola.

```js
console.log("Este mensaje aparecerá en la consola.");
console.clear(); // Limpiar la consola
```

### Contar elementos

`console.count()`: Realiza un seguimiento de cuántas veces se ha llamado a un determinado log.

```js
console.count("Click"); // Click: 1
console.count("Click"); // Click: 2
console.count("Otro"); // Otro: 1
console.count("Click"); // Click: 3
```

## Alert

La función `alert()` se utiliza para mostrar una ventana emergente con un mensaje para el usuario. Este mensaje se presenta de manera modal, lo que significa que bloquea la interacción con la página web hasta que el usuario interactúa con la alerta.

```js
// Al ejecutar el código aparecerá una ventana emergente en el navegador con el mensaje "¡Hola, mundo!".
let mensaje = "¡Hola, mundo!";
alert(mensaje);
```

> [!IMPORTANT]
>
> Es importante tener en cuenta que las alertas pueden resultar molestas para los usuarios, y su uso excesivo puede afectar negativamente la experiencia del usuario. <br>
> La función alert() se utiliza principalmente para propósitos muy simples o de depuración.

## Prompt

La función `prompt()` se utiliza para mostrar una ventana emergente que solicita al usuario que ingrese información, como texto o números. A menudo, se utiliza para interactuar con el usuario y recopilar datos.

```js
/*
Cuando este código se ejecuta, aparecerá una ventana emergente en el navegador que solicitará al usuario que ingrese su nombre. El valor ingresado por el usuario se almacenará en la variable nombre, y luego se imprimirá un saludo en la consola del navegador.
*/
let nombre = prompt("Por favor, ingresa tu nombre:");
console.log("Hola, " + nombre + "! ¿Cómo estás?");
```

> [!NOTE]
>
> Como práctica general, es recomendable validar y convertir los datos según sea necesario después de usar prompt() para garantizar que estén en el formato correcto. Ten en cuenta que el resultado de prompt() es siempre una cadena de texto, incluso si el usuario ingresa números.

## Confirm

La función `confirm()` se utiliza para mostrar una ventana emergente con un mensaje y botones de confirmación ("Aceptar" y "Cancelar"). El usuario puede hacer clic en uno de estos botones para confirmar o cancelar una acción.

```js
/*
En este ejemplo, se mostrará una ventana emergente con el mensaje "¿Estás seguro de que deseas continuar?" y dos botones: "Aceptar" y "Cancelar". Dependiendo de la opción que elija el usuario, se mostrará un mensaje diferente en la consola del navegador.
*/
let respuesta = confirm("¿Estás seguro de que deseas continuar?");
if (respuesta) {
  console.log("Usuario hizo clic en Aceptar.");
} else {
  console.log("Usuario hizo clic en Cancelar.");
}
```

> [!WARNING]
>
> Utilizar los casos anteriores principalmente para propósitos muy simples o de depuración.
