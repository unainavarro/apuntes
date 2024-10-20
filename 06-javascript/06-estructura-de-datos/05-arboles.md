<h1 align="center">Árboles</h1>

<h2>📑 Contenido</h2>

- [Árboles](#árboles)
  - [Ejemplo](#ejemplo)
  - [Explicación](#explicación)

## Árboles

Los árboles son una estructura de datos no lineal que consta de nodos conectados de forma jerárquica. Cada nodo puede tener cero o más nodos hijos, y un nodo puede tener solo un nodo padre (excepto el nodo raíz, que no tiene padre). Los árboles se utilizan para representar jerarquías de datos, como estructuras de directorios en un sistema de archivos, árboles genealógicos, estructuras de documentos HTML, etc.

### Ejemplo

```js
class Nodo {
  constructor(valor) {
    this.valor = valor;
    this.hijos = [];
  }

  agregarHijo(valor) {
    const nuevoNodo = new Nodo(valor);
    this.hijos.push(nuevoNodo);
  }
}

class Arbol {
  constructor(valorRaiz) {
    this.raiz = new Nodo(valorRaiz);
  }

  agregarNodo(valorPadre, valorHijo) {
    const nodoPadre = this.buscarNodo(this.raiz, valorPadre);
    if (nodoPadre) {
      nodoPadre.agregarHijo(valorHijo);
    } else {
      console.log(`No se encontró el nodo con valor ${valorPadre}`);
    }
  }

  buscarNodo(nodo, valor) {
    if (nodo.valor === valor) {
      return nodo;
    } else if (nodo.hijos.length > 0) {
      for (const hijo of nodo.hijos) {
        const resultado = this.buscarNodo(hijo, valor);
        if (resultado) {
          return resultado;
        }
      }
    }
    return null;
  }
}

// Ejemplo de uso
const arbol = new Arbol("A");
arbol.agregarNodo("A", "B");
arbol.agregarNodo("A", "C");
arbol.agregarNodo("B", "D");
arbol.agregarNodo("B", "E");
arbol.agregarNodo("C", "F");

console.log(arbol);
```

### Explicación

En este ejemplo, tenemos dos clases: Nodo y Árbol. La clase Nodo representa un nodo en el árbol con un valor y una lista de hijos. La clase Árbol representa el árbol en sí mismo y tiene un método agregarNodo para agregar un nuevo nodo al árbol, y un método buscarNodo para buscar un nodo con un valor específico en el árbol.

Al ejecutar este código, verás que se crea un árbol con la raíz 'A' y se agregan varios nodos como hijos de la raíz ('B', 'C', etc.). Este es un ejemplo simple de un árbol en JavaScript, y puedes expandirlo agregando más funcionalidades según sea necesario.
