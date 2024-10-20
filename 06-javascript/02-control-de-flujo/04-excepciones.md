<h1 align="center">Manejo de errores</h1>

<h2>📑 Contenido</h2>

- [Manejo de errores(Excepciones)](#manejo-de-erroresexcepciones)
  - [Ejemplos](#ejemplos)

## Manejo de errores(Excepciones)

El manejo de errores se realiza a través de las sentencias `try`, `catch`, `finally`, y, opcionalmente, `throw`. Estos elementos forman parte del manejo de excepciones. Debemos intentar capturar los posibles errores de nuestro código antes de que se produzcan.

- **try:** En este bloque, colocas el código que quieres probar. Si ocurre un error durante la ejecución de este bloque, se pasa al bloque catch.
- **catch:** En este bloque, colocas el código que se ejecutará si se produce un error en el bloque try. El parámetro error captura el objeto de la excepción, permitiéndote acceder a información sobre el error.
- **finally:** Este bloque es opcional y se ejecuta siempre, ocurra o no un error en el bloque. Util para cerrar recursos, operaciones de limpieza...
- **throw:** se utiliza para lanzar una excepción manualmente.

### Ejemplos

```js
//Manejar posibles errores de una función que sirve para dividir
try {
  // Bloque de código que podría generar un error
  const resultado = dividir(10, 0); // Intentando dividir por cero
  console.log(resultado); // Esta línea no se ejecutará si hay un error
} catch (error) {
  // Bloque de código que se ejecuta si se produce un error
  console.error("Se produjo un error: " + error.message);
} finally {
  // Bloque de código opcional que se ejecuta siempre
  console.log("Este bloque siempre se ejecuta");
}

function dividir(a, b) {
  if (b === 0) {
    throw new Error("No se puede dividir por cero");
  }
  return a / b;
}

//Intentar retirar más monedas de las que se tienen en el saldo.

//Lanzar excepción
function banco(saldo, retirar) {
  if (saldo < retirar) {
    throw (
      "No puedes retirar más monedas que las que tienes en tu saldo: " + saldo
    );
  }
  return saldo - retirar;
}

//Recuperar excepción
try {
  console.log(banco(100, 150) + " monedas");
} catch (error) {
  console.log(error);
}

//Ejemplo anterior utilizando el objeto error.

function banco(saldo, retirar) {
  if (saldo < retirar) {
    throw new Error(
      "No puedes retirar más monedas que las que tienes en tu saldo: " + saldo
    );
  }
  return saldo - retirar;
}

try {
  console.log(banco(100, 150) + " monedas");
} catch (error) {
  console.log(error.message);
}
```
