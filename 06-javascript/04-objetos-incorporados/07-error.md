<h1 align="center">Error</h1>

<h2>📑 Contenido</h2>

- [Error](#error)
  - [Propiedades](#propiedades)
  - [Propiedades Adicionales](#propiedades-adicionales)
  - [Métodos](#métodos)
  - [Ejemplo](#ejemplo)

## Error

El objeto incorporado Error en JavaScript se utiliza para representar errores en tiempo de ejecución. Es la clase base para otros tipos de errores en JavaScript, como SyntaxError, ReferenceError, TypeError, etc. Cuando ocurre un error durante la ejecución de un programa, JavaScript crea un objeto Error con información sobre el error, como un mensaje descriptivo y una pila de llamadas, y lo lanza (throw) para indicar que ha ocurrido un problema.

### Propiedades

- **name:** Una cadena que representa el nombre del tipo de error. Por ejemplo, para un error de referencia (ReferenceError), el valor de name sería "ReferenceError".
- **message:** Una cadena que proporciona información sobre el error, generalmente un mensaje descriptivo que explica lo que causó el error.
- **stack:** Una cadena que representa la pila de llamadas en el momento en que se creó el objeto Error. Esta propiedad es opcional y puede no estar disponible en todos los navegadores.

### Propiedades Adicionales

- **SyntaxError:**
  - **fileName:** El nombre del archivo que causó el error de sintaxis.
  - **lineNumber:** El número de línea dentro del archivo donde se produjo el error de sintaxis.
  - **columnNumber:** El número de columna dentro de la línea donde se produjo el error de sintaxis.
- **ReferenceError, TypeError,RangeError,EvalError :**
  - message: Mensaje específico que describe el error de referencia.
  - name: Nombre del tipo de error, que en este caso sería "ReferenceError".
  - stack: La pila de llamadas en el momento en que se creó el error.

### Métodos

- **toString():** Devuelve una cadena que representa el error, incluyendo tanto el nombre como el mensaje del error.
- **toJSON():** Devuelve un objeto serializable que representa el error. Esto es útil cuando necesitas convertir el error a un formato que puede ser transmitido a través de una red, por ejemplo, en una API REST.
- **toLocaleString():** Devuelve una cadena localizada que representa el error. Esto es útil cuando necesitas mostrar el error en el idioma del usuario.

### Ejemplo

```js
// Crear instancias de objetos Error
const miError = new Error("Ha ocurrido un error.");

console.log(miError.name); // Output: "Error"
console.log(miError.message); // Output: "Ha ocurrido un error."
console.log(miError.stack); // (Dependerá del entorno y el momento en que se haya creado el error)

// SyntaxError
try {
  throw new SyntaxError("Error de sintaxis.");
} catch (error) {
  console.log(error instanceof SyntaxError); // Output: true
  console.log(error instanceof Error); // Output: true
}
```
