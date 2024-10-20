<h1 align="center">Objetos</h1>

<h2>📑 Contenido</h2>

- [Objeto Literal](#objeto-literal)
  - [Objeto con Métodos](#objeto-con-métodos)
  - [Objetos Anidados](#objetos-anidados)
  - [Propiedades Computadas](#propiedades-computadas)
- [Objeto incorporado Object](#objeto-incorporado-object)
  - [Métodos de Object](#métodos-de-object)
    - [Objeto de prueba](#objeto-de-prueba)
    - [Object.create()](#objectcreate)
    - [Object.keys()](#objectkeys)
    - [Object.values()](#objectvalues)
    - [Object.entries()](#objectentries)
    - [Object.assign()](#objectassign)
    - [Object.freeze()](#objectfreeze)
    - [Object.seal()](#objectseal)
    - [Object.getPrototypeOf()](#objectgetprototypeof)

## Objeto Literal

Un objeto literal es una forma de definir y crear objetos utilizando una sintaxis más compacta y directa. Un objeto literal consiste en una lista de pares clave-valor, donde las claves (o nombres de propiedades) son cadenas o símbolos, y los valores pueden ser de cualquier tipo de dato, incluyendo otros objetos.

```js
// Objeto literal con propiedades
let persona = {
  nombre: "Juan",
  edad: 30,
  ciudad: "CiudadDeJuan",
};

console.log(persona.nombre); // Acceder a una propiedad: "Juan"
```

### Objeto con Métodos

Cuando se crea un objeto y se le asignan funciones como propiedades, es común referirse a estas funciones como "métodos" del objeto. Los métodos son simplemente funciones que están asociadas a un objeto particular.

Se accede a ellos utilizando la notación de punto (objeto.propiedad) o la notación de corchetes (objeto['propiedad']).

Los métodos permiten encapsular funcionalidades relacionadas con el objeto y mejorar la modularidad y legibilidad del código.

```js
// Objeto literal con métodos
let persona = {
  nombre: "Juan",
  edad: 30,
  ciudad: "CiudadDeJuan",
  // Método para mostrar información
  mostrarInformacion: function () {
    console.log(
      `Nombre: ${this.nombre}, Edad: ${this.edad}, Ciudad: ${this.ciudad}`
    );
  },
  // Método para saludar
  saludar: function () {
    console.log(`Hola, soy ${this.nombre}!`);
  },
};

// Llamada a métodos
persona.mostrarInformacion(); // Salida: Nombre: Juan, Edad: 30, Ciudad: CiudadDeJuan
persona.saludar(); // Salida: Hola, soy Juan!
```

> [!NOTE]
>
> La palabra clave `this` hace referencia al propio objeto en el contexto de la llamada al método.

### Objetos Anidados

Los objetos anidados en JavaScript se refieren a la creación de objetos dentro de otros objetos. Esto permite organizar y estructurar datos de manera más compleja y jerárquica.

```js
// Objeto con objetos anidados
let persona = {
  nombre: "Juan",
  edad: 30,
  direccion: {
    calle: "123 Calle Principal",
    ciudad: "CiudadDeJuan",
    codigoPostal: "12345",
  },
  contactos: {
    telefono: "555-1234",
    correo: "juan@example.com",
  },
};

// Acceder a propiedades de objetos anidados
console.log(persona.nombre); // "Juan"
console.log(persona.direccion.ciudad); // "CiudadDeJuan"
console.log(persona.contactos.telefono); // "555-1234"
```

> [!NOTE]
>
> Ten en cuenta que, cuando trabajas con objetos anidados, debes considerar la lectura y escritura de propiedades de manera adecuada, teniendo en cuenta la jerarquía de los objetos. La notación de punto o corchetes te permite acceder a cualquier nivel de profundidad en los objetos anidados.

### Propiedades Computadas

Las propiedades computadas son una característica que te permite definir el nombre de una propiedad de objeto dinámicamente, utilizando expresiones o variables. Esta característica está disponible a partir de ECMAScript 2015 (también conocido como ES6).

Esto es especialmente útil cuando necesitas crear propiedades de objetos de manera dinámica o cuando el nombre de la propiedad debe basarse en algún cálculo o entrada externa.

```js
//Ejemplo añadir edad dinámica
let claveDinamica = "edad";

let persona = {
  nombre: "Juan",
  [claveDinamica]: 30,
};

console.log(persona.nombre); // Acceder a una propiedad directa: "Juan"
console.log(persona[claveDinamica]); // Acceder a una propiedad computada: 30

//Ejemplo agregar un prefijo al apellido
let prefijo = "apellido";

let persona = {
  [prefijo + "_paterno"]: "Gómez",
  [prefijo + "_materno"]: "Pérez",
};

console.log(persona.apellido_paterno); // "Gómez"
console.log(persona.apellido_materno); // "Pérez"
```

## Objeto incorporado Object

La clase Object en JavaScript representa uno de los tipos de datos en JavaScript. Se utiliza para almacenar varias colecciones indexadas y entidades más complejas. Los objetos se pueden crear utilizando el constructor Object() o la sintaxis literal / inicializador de objeto. La mayoría de los objetos en JavaScript son instancias de Object.

### Métodos de Object

#### Objeto de prueba

```js
const portatil = {
  marca: "HP",
  modelo: "4044",
  disponible: true,
  toString() {
    console.log(
      `El portatil ${this.marca} modelo ${this.modelo} ${(this.disponible = true
        ? "esta disponible"
        : "no esta disponible")} `
    );
  },
};
```

#### Object.create()

Se usa para crear un nuevo objeto y vincularlo al prototipo de un objeto existente.

```js
console.log("----create----");

portatil.toString();

const lenovo = Object.create(portatil);
lenovo.marca = "lenovo";
lenovo.modelo = "ln-900";
lenovo.disponible = true;

lenovo.toString();
```

#### Object.keys()

Crea una matriz que contiene las claves de un objeto.

```js
console.log("----keys----");

const keys = Object.keys(portatil);
console.log(keys);

//Iterar matriz
keys.forEach((key) => {
  let valor = portatil[key];
  console.log(`${key} => ${valor}`);
});
```

#### Object.values()

Crea una matriz que contiene los valores de un objeto.

```JS
console.log("----values----");

const values = Object.values(portatil);

console.log(values);
```

#### Object.entries()

Crea una matriz anidada con los pares clave-valor de un objeto.

```JS
console.log("----entries----");

const entries = Object.entries(lenovo);

console.log(entries);
console.log(entries[0][0]);
console.log(entries[0][1]);

entries.forEach((entry) => {
  let key = entries[0];
  let value = entries[1];

  console.log(`${key} => ${value}`);
});
```

#### Object.assign()

Copia valores de un objeto a otro. <br>
Podemos crear dos objetos y fusionarlos con Object.assign().

```js
console.log("----assign----");

const alumno = {
  nombre: "Pedro",
  correo: "email@dominio.com",
};

const info = {
  curso: "Programación",
  tutor: "Alfredo",
};

const alumnoTotal = Object.assign(alumno, info);

console.log(alumnoTotal);
```

#### Object.freeze()

Impide la modificación de propiedades y valores de un objeto,
y evita que se agreguen propiedades a un objeto o que se eliminen de él.

```JS
console.log("----freeze----");

const coche = {
  ruedas: 4,
  color: "rojo",
};

const nuevoCoche = Object.freeze(coche);

nuevoCoche.ruedas = 8;
console.log(nuevoCoche);
console.log(Object.isFrozen(nuevoCoche));
```

#### Object.seal()

Impide la adición de nuevas propiedades a un objeto,
pero permite la modificación de propiedades existentes.

```JS
console.log("----seal----");

const nuevoAlumno = Object.seal(alumno);

nuevoAlumno.nombre = "Mario";
nuevoAlumno.tel = "612345678";

console.log(nuevoAlumno);
```

#### Object.getPrototypeOf()

Se usa para obtener la propiedad interna oculta `[[Prototype]]` de un objeto.

```js
console.log("----getPrototypeOf----");

const num = [0, 1, 2, 3, 4];

console.log(Object.getPrototypeOf(num));
console.log(Object.getPrototypeOf(num) === Array.prototype);
```
