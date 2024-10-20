<h1 align="center">Hash Table</h1>

<h2>📑 Contenido</h2>

- [Hash Table](#hash-table)
  - [Ejemplo](#ejemplo)
  - [Explicación](#explicación)

## Hash Table

Una tabla hash (hash table) es una estructura de datos que implementa una asociación de tipo clave-valor. Utiliza una función de dispersión (hash function) para mapear las claves a ubicaciones en una estructura de almacenamiento, generalmente un array, lo que permite un acceso rápido a los valores asociados con las claves.

En JavaScript, puedes implementar una tabla hash utilizando un objeto, ya que los objetos de JavaScript son colecciones de pares clave-valor. Sin embargo, si deseas una implementación más personalizada o necesitas lidiar con colisiones de claves (múltiples claves que se asignan a la misma ubicación en la tabla hash), puedes crear tu propia clase de tabla hash.

### Ejemplo

```js
class HashTable {
  constructor() {
    this.tamano = 10; // Tamaño inicial de la tabla hash
    this.tabla = new Array(this.tamano);
  }

  // Función de dispersión simple
  hash(key) {
    let hash = 0;
    for (let i = 0; i < key.length; i++) {
      hash += key.charCodeAt(i);
    }
    return hash % this.tamano;
  }

  // Método para insertar un par clave-valor en la tabla hash
  insertar(key, valor) {
    const indice = this.hash(key);
    if (!this.tabla[indice]) {
      this.tabla[indice] = [];
    }
    this.tabla[indice].push([key, valor]);
  }

  // Método para obtener un valor dado una clave
  obtener(key) {
    const indice = this.hash(key);
    if (!this.tabla[indice]) return undefined;
    for (const entrada of this.tabla[indice]) {
      if (entrada[0] === key) {
        return entrada[1];
      }
    }
    return undefined;
  }
}

// Ejemplo de uso
const tablaHash = new HashTable();
tablaHash.insertar("uno", 1);
tablaHash.insertar("dos", 2);
console.log(tablaHash.obtener("uno")); // Resultado: 1
console.log(tablaHash.obtener("dos")); // Resultado: 2
```

### Explicación

En este ejemplo, creamos una clase HashTable con métodos para calcular la función de dispersión (hash()), insertar pares clave-valor en la tabla hash (insertar()), y obtener valores dado una clave (obtener()). La función de dispersión simplemente suma los valores de los códigos ASCII de los caracteres de la clave y luego toma el módulo del tamaño de la tabla hash para calcular el índice.

Esta es una implementación básica y simplificada de una tabla hash en JavaScript. Dependiendo de tus necesidades, podrías expandirla agregando manejo de colisiones, métodos para eliminar pares clave-valor, cambiar el tamaño de la tabla dinámicamente, etc.
