<h1 align="center">Stack(pila)</h1>

<h2>📑 Contenido</h2>

- [Stack](#stack)
  - [Ejemplo](#ejemplo)
  - [Explicación](#explicación)

## Stack

Una pila (stack) es una estructura de datos que sigue el principio de "último en entrar, primero en salir" (LIFO, por sus siglas en inglés), lo que significa que el último elemento agregado a la pila es el primero en ser eliminado. En JavaScript, puedes implementar una pila utilizando un array y aprovechar los métodos push() y pop() para agregar y eliminar elementos, respectivamente.

### Ejemplo

```js
class Pila {
  constructor() {
    this.elementos = [];
  }

  // Agregar un elemento a la pila
  push(elemento) {
    this.elementos.push(elemento);
  }

  // Eliminar y devolver el elemento superior de la pila
  pop() {
    return this.elementos.pop();
  }

  // Devolver el elemento superior de la pila sin eliminarlo
  peek() {
    return this.elementos[this.elementos.length - 1];
  }

  // Verificar si la pila está vacía
  isEmpty() {
    return this.elementos.length === 0;
  }

  // Devolver el tamaño de la pila
  size() {
    return this.elementos.length;
  }

  // Limpiar la pila
  clear() {
    this.elementos = [];
  }
}

// Ejemplo de uso
const pila = new Pila();
pila.push(1);
pila.push(2);
pila.push(3);

console.log(pila.peek()); // Resultado: 3
console.log(pila.pop()); // Resultado: 3
console.log(pila.peek()); // Resultado: 2
console.log(pila.size()); // Resultado: 2
```

### Explicación

En este ejemplo, creamos una clase Pila con métodos para agregar elementos (push()), eliminar elementos (pop()), obtener el elemento superior sin eliminarlo (peek()), verificar si la pila está vacía (isEmpty()), obtener el tamaño de la pila (size()), y limpiar la pila (clear()).

Al ejecutar este código, verás cómo se utilizan los métodos de la pila para agregar, eliminar y acceder a los elementos de la pila.
