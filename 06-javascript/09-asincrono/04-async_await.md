<h1 align="center">Async-Await</h1>

<h2>📑 Contenido</h2>

- [Async](#async)
- [Await](#await)
- [Ejemplos](#ejemplos)

## Async

La palabra clave await solo se puede usar dentro de una función asíncrona, y sirve para esperar a que una promesa se resuelva y obtener su valor. La ejecución de la función se pausa hasta que la promesa se resuelve, y luego se reanuda con el valor obtenido.

## Await

El uso de await nos permite escribir código asíncrono como si fuera síncrono, lo que facilita su lectura y comprensión. Además, podemos usar try…catch para manejar los posibles errores de las promesas, en lugar de usar el método catch.

## Ejemplos

```js
//Primer Ejemplo
function descargarClientes() {
  return new Promise((resolve) => {
    console.log("Espere...");
    setTimeout(function () {
      resolve("Clientes Descargados");
    }, 3000);
  });
}

async function descarga() {
  try {
    const resultado = await descargarClientes();
    console.log(resultado);
  } catch (error) {
    console.log(error);
  }
}

descarga();

console.log("No para la carga del código");

// Segundo Ejemplo
const datos = [
  {
    id: 1,
    nombre: "juan",
    tel: 123456789,
  },
  {
    id: 2,
    nombre: "maria",
    tel: 789456123,
  },
  {
    id: 3,
    nombre: "Carlos",
    tel: 963258741,
  },
];

const getDatosPromise = () => {
  return new Promise((resolve, reject) => {
    if (datos.length === 0) {
      reject(new Error("no existen datos"));
    }
    setTimeout(() => {
      resolve(datos);
    }, 1500);
  });
};

async function dataAwait() {
  try {
    const datosFinal = await getDatosPromise();
    console.log("Await");
    console.log(datosFinal);
  } catch (error) {
    console.log(error);
  }
}

dataAwait();
```
