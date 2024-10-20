<h1 align="center">Herencia</h1>

<h2>📑 Contenido</h2>

- [Herencia](#herencia)
  - [Ejemplo](#ejemplo)

## Herencia

Las clases también pueden heredar de otras clases usando la palabra clave extends. Esto permite reutilizar el código de una clase base y añadir o modificar funcionalidades en una clase derivada.

### Ejemplo

```js
// Clase padre
class Producto {
  //Constructor
  constructor(nombre, precio) {
    this.nombre = nombre;
    this.precio = precio;
  }

  toString() {
    return `El producto: ${this.nombre} tiene un precio de ${this.precio}€`;
  }
}

// Clase que hereda
class Categoria extends Producto {
  constructor(nombre, precio, categoria) {
    super(nombre, precio);
    this.categoria = categoria;
  }

  formatearCategoria() {
    const producto = super.toString();

    return producto + " La categoria es: " + this.categoria;
  }
}

// Instanciar

const producto = new Producto("Samsung TV", 500);
const productoCat = new Categoria("Samsung TV", 500, "Smart Tv");

console.log(producto.toString());
console.log(productoCat.formatearCategoria());
```
