<h1 align="center">Forma Imperativa y Declarativa</h1>

<h2>📑 Contenido</h2>

- [Forma Imperativa](#forma-imperativa)
  - [Ejemplo](#ejemplo)
- [Forma Declarativa](#forma-declarativa)
  - [Ejemplo](#ejemplo-1)

## Forma Imperativa

En la programación imperativa, defines explícitamente los pasos que se deben seguir para lograr un resultado. En el caso de la manipulación de objetos, esto implicaría manipular directamente las propiedades y métodos del objeto.

### Ejemplo

```js
// Objeto a manipular
let persona = {
  nombre: "Juan",
  edad: 30,
};

// Manipulación imperativa
persona.edad = persona.edad + 1;
console.log(persona); // { nombre: 'Juan', edad: 31 }
```

## Forma Declarativa

En la programación declarativa, defines qué resultado quieres lograr sin especificar los pasos individuales para llegar a ese resultado. En el caso de la manipulación de objetos, esto podría implicar el uso de funciones y métodos que realicen la manipulación deseada.

### Ejemplo

```js
// Objeto a manipular
let persona = {
  nombre: "Juan",
  edad: 30,
};

// Manipulación declarativa
function aumentarEdad(persona) {
  return { ...persona, edad: persona.edad + 1 };
}

let nuevaPersona = aumentarEdad(persona);
console.log(nuevaPersona); // { nombre: 'Juan', edad: 31 }
```

> [!NOTE]
>
> La programación imperativa se preocupa por los detalles de cómo se realizan las acciones, mientras que la programación declarativa se enfoca en definir el resultado deseado sin preocuparse por los detalles de implementación. Cada enfoque tiene sus ventajas y desventajas, y la elección entre ellos depende del problema específico que se esté abordando y de las preferencias del programador.
