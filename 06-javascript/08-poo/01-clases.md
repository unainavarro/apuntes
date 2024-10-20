<h1 align="center">Clases</h1>

<h2>📑 Contenido</h2>

- [Clases](#clases)
- [Instanciar](#instanciar)

## Clases

Las clases son una forma de crear objetos con propiedades y métodos específicos, usando una sintaxis más clara y simple que la herencia basada en prototipos.

```js
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
```

## Instanciar

Para crear una instancia de una clase, puedes usar el operador new seguido del nombre de la clase y los argumentos que se pasan al constructor.

```js
const producto = new Producto("Samsung TV", 500);

console.log(producto.toString());
```
