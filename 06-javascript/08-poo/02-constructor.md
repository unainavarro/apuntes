<h1 align="center">Constructor</h1>

<h2>📑 Contenido</h2>

- [Constructor](#constructor)

## Constructor

El constructor en JavaScript es un método especial que se utiliza para crear e inicializar un objeto creado a partir de una clase.
El método constructor se define dentro de la clase y se llama automáticamente cuando se crea una instancia de la clase.

```js
//Sintaxis
class MyClass {
  constructor() {
    // Código para inicializar el objeto
  }
}
```

El método constructor puede tomar argumentos que se utilizan para inicializar las propiedades del objeto.
Si no se define un método constructor, se utiliza el constructor predeterminado que no toma ningún argumento y no hace nada.

```js
class Persona {
  constructor(nombre, edad) {
    this.nombre = nombre;
    this.edad = edad;
  }
}

const persona1 = new Persona("Juan", 25);
console.log(persona1.nombre); // Juan
console.log(persona1.edad); // 25
```
