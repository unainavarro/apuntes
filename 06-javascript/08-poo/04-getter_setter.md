<h1 align="center">Getter y Setter</h1>

<h2>📑 Contenido</h2>

- [Getter](#getter)
- [Setter](#setter)
- [Ejemplos](#ejemplos)
- [En una clase](#en-una-clase)

## Getter

Los **getters** se utilizan para obtener el valor de una propiedad.

```js
const obj = {
  get prop() {
    // Código para obtener el valor de la propiedad
  },
};
```

## Setter

Los **setters** se utilizan para establecer el valor de una propiedad

```js
const obj = {
  set prop(value) {
    // Código para establecer el valor de la propiedad
  },
};
```

## Ejemplos

```js
const persona = {
  nombre: "",
  apellido: "",
  get nombreCompleto() {
    return `${this.nombre} ${this.apellido}`;
  },
  set nombreCompleto(value) {
    const partes = value.split(" ");
    this.nombre = partes[0];
    this.apellido = partes[1];
  },
};

persona.nombreCompleto = "Juan Pérez";
console.log(persona.nombre); // Juan
console.log(persona.apellido); // Pérez
console.log(persona.nombreCompleto); // Juan Pérez
```

## En una clase

```js
class Persona {
  constructor(nombre, edad) {
    this._nombre = nombre;
    this._edad = edad;
  }

  get nombre() {
    return this._nombre;
  }

  set nombre(value) {
    this._nombre = value;
  }

  get edad() {
    return this._edad;
  }

  set edad(value) {
    this._edad = value;
  }
}

const persona1 = new Persona("Juan", 25);
console.log(persona1.nombre); // Juan
console.log(persona1.edad); // 25

persona1.nombre = "Pedro";
persona1.edad = 30;

console.log(persona1.nombre); // Pedro
console.log(persona1.edad); // 30
```
