<h1 align="center">Linked List</h1>

<h2>📑 Contenido</h2>

- [Linked List](#linked-list)
  - [Ejemplos](#ejemplos)
  - [Explicación](#explicación)

## Linked List

Una lista enlazada (linked list) es una estructura de datos que consta de nodos, donde cada nodo contiene un valor y una referencia (o puntero) al siguiente nodo en la secuencia. Una lista enlazada puede implementarse utilizando objetos y referencias entre ellos para representar los nodos.

### Ejemplos

```js
class Nodo {
  constructor(valor) {
    this.valor = valor;
    this.siguiente = null;
  }
}

class ListaEnlazada {
  constructor() {
    this.cabeza = null;
  }

  agregar(valor) {
    const nuevoNodo = new Nodo(valor);
    if (!this.cabeza) {
      this.cabeza = nuevoNodo;
    } else {
      let nodoActual = this.cabeza;
      while (nodoActual.siguiente) {
        nodoActual = nodoActual.siguiente;
      }
      nodoActual.siguiente = nuevoNodo;
    }
  }

  imprimir() {
    let nodoActual = this.cabeza;
    while (nodoActual) {
      console.log(nodoActual.valor);
      nodoActual = nodoActual.siguiente;
    }
  }
}

// Ejemplo de uso
const lista = new ListaEnlazada();
lista.agregar(1);
lista.agregar(2);
lista.agregar(3);
lista.imprimir();
```

### Explicación

En este ejemplo, tenemos dos clases: Nodo y ListaEnlazada. La clase Nodo representa un nodo en la lista enlazada, con un valor y una referencia al siguiente nodo (siguiente). La clase ListaEnlazada representa la lista enlazada en sí misma, y tiene un método agregar para agregar un nuevo nodo al final de la lista, y un método imprimir para imprimir todos los valores en la lista enlazada.

Al ejecutar este código, verás que la lista enlazada contiene los valores 1, 2, y 3 en la secuencia en que fueron agregados.
