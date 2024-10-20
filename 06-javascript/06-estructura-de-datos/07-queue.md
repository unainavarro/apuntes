<h1 align="center">Queue(cola)</h1>

<h2>📑 Contenido</h2>

- [Queue](#queue)
  - [Ejemplo](#ejemplo)
  - [Explicación](#explicación)

## Queue

Una cola (queue) es una estructura de datos que sigue el principio de "primero en entrar, primero en salir" (FIFO, por sus siglas en inglés), lo que significa que el primer elemento agregado a la cola es el primero en ser eliminado. En JavaScript, puedes implementar una cola utilizando un array y aprovechar los métodos push() y shift() para agregar y eliminar elementos, respectivamente.

### Ejemplo

```js
class Cola {
  constructor() {
    this.elementos = [];
  }

  // Agregar un elemento al final de la cola
  enqueue(elemento) {
    this.elementos.push(elemento);
  }

  // Eliminar y devolver el primer elemento de la cola
  dequeue() {
    return this.elementos.shift();
  }

  // Devolver el primer elemento de la cola sin eliminarlo
  front() {
    return this.elementos[0];
  }

  // Verificar si la cola está vacía
  isEmpty() {
    return this.elementos.length === 0;
  }

  // Devolver el tamaño de la cola
  size() {
    return this.elementos.length;
  }

  // Limpiar la cola
  clear() {
    this.elementos = [];
  }
}

// Ejemplo de uso
const cola = new Cola();
cola.enqueue(1);
cola.enqueue(2);
cola.enqueue(3);

console.log(cola.front()); // Resultado: 1
console.log(cola.dequeue()); // Resultado: 1
console.log(cola.front()); // Resultado: 2
console.log(cola.size()); // Resultado: 2
```

### Explicación

En este ejemplo, creamos una clase Cola con métodos para agregar elementos al final de la cola (enqueue()), eliminar y devolver el primer elemento de la cola (dequeue()), obtener el primer elemento sin eliminarlo (front()), verificar si la cola está vacía (isEmpty()), obtener el tamaño de la cola (size()), y limpiar la cola (clear()).

Al ejecutar este código, verás cómo se utilizan los métodos de la cola para agregar, eliminar y acceder a los elementos de la cola.
