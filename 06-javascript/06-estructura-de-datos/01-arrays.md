<h1 align="center">Array</h1>

<h2>📑 Contenido</h2>

- [Array](#array)
  - [Arrays Estáticos](#arrays-estáticos)
  - [Arrays Dinámicos](#arrays-dinámicos)
- [Operaciones con arrays](#operaciones-con-arrays)
  - [Array de prueba](#array-de-prueba)
  - [map()](#map)
  - [filter()](#filter)
  - [forEach()](#foreach)
  - [find()](#find)
  - [sort()](#sort)
  - [some()](#some)
  - [every()](#every)
  - [concat()](#concat)
  - [includes()](#includes)
  - [join()](#join)
  - [reduce()](#reduce)
  - [Diferencia reduce y join](#diferencia-reduce-y-join)
  - [indexOf()](#indexof)
  - [findIndex()](#findindex)
  - [fill()](#fill)
  - [push()](#push)
  - [pop()](#pop)
  - [shift()](#shift)
  - [slice()](#slice)
  - [reverse()](#reverse)
  - [splice()](#splice)
  - [isArray()](#isarray)
  - [from()](#from)

## Array

Los arrays son objetos que permiten almacenar múltiples valores en una sola variable. Estos valores pueden ser de cualquier tipo de datos, como números, cadenas, booleanos, objetos, funciones e incluso otros arrays. Los arrays en JavaScript son dinámicos, lo que significa que su tamaño puede cambiar dinámicamente a medida que se agregan o eliminan elementos.

### Arrays Estáticos

Los arrays estáticos tienen una longitud fija y no se pueden modificar después de su creación.

```js
const array = new Array(3); // Array vacío de tamaño 3
```

### Arrays Dinámicos

Los arrays dinámicos tienen una longitud variable y se pueden modificar después de su creación.

```js
const array = []; // Array vacío (0 elementos)
const letras = ["a", "b", "c"]; // Array con 3 elementos
```

## Operaciones con arrays

### Array de prueba

```js
const array = [1, 2, 3, 4, 5, 6, 7, 8, 9];
```

### map()

Permite recorrer el array y modificar los elementos presentes en él, retornando un nuevo array con la misma longitud que el original.

```js
console.log("----MAP----");

//Sumar 10 a cada elemento
const mapArray = array.map((element) => element + 10);
console.log(mapArray);
```

### filter()

Recorre el array y retorna un nuevo array con aquellos elementos que pasen una determinada condición.

```js
console.log("----FILTER----");

//Buscar el 4 o el 9
const filterArray = array.filter((e) => e == 4 || e == 9);
console.log(filterArray);
```

### forEach()

Permite iterar el contenido de un array.
Recibe un callback que toma como parámetro el elemento actual
de la iteración y el indice del mismo.

```js
console.log("----forEach----");

const iterarArray = array.forEach((element, i) => {
  console.log(`Elemento: ${element} --> Posición: ${i}`);
});
```

### find()

Recorre el array y retorna la primera coincidencia del elemento que se busca.

```js
console.log("----find----");
//Buscar num 4
console.log(array.find((e) => e == 4));
```

### sort()

Ordena los elementos del array y retorna el arreglo ordenado. <br>
Los elementos se ordenarán en orden ascendente (de la A a la Z) por defecto.

```js
console.log("----sort----");

const alph = ["z", "q", "y", "n", "e", "a", "h"];

//Orden descendente
const descArray = alph.sort((a, b) => (a > b ? -1 : 1));
console.log("Descendente: " + descArray);

const ascArray = alph.sort((a, b) => (a > b ? 1 : -1));
console.log("Ascendente: " + ascArray);
```

### some()

Itera el array y retorna un booleano si como mínimo uno de los elementos presentes en el array pasa una condición determinada.

```js
console.log("----some----");

const someArray = array.some((e) => e == 4);
console.log(someArray);

const someArray2 = array.some((e) => e == 0);
console.log(someArray2);
```

### every()

Para que dicho booleano sea true todos los elementos del array deberán pasar la condición dada.

```js
console.log("----every----");

const everyArray = array.every((e) => e > 0);
console.log(everyArray);
```

### concat()

Se utiliza para unir dos o más arrays. <br>
Este método no cambia los arrays existentes, sino que devuelve un nuevo array.

```js
console.log("----concat----");

const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];

const concatArray = arr1.concat(arr2);
console.log(concatArray);
```

### includes()

Determina si un array incluye un determinado elemento y retorna un booleano según corresponda.

```js
console.log("----includes----");

console.log(array.includes(4));
```

### join()

Une todos los elementos de un array en una cadena. Podemos pasarle como parámetro el carácter de separación que debe agregar entre los elementos.

```js
console.log("----join----");

console.log(array.join("-"));
```

### reduce()

Une todos los elementos de un array en una cadena. <br>
Podemos pasarle como parámetro el carácter de separación que debe agregar entre los elementos.

```js
console.log("----reduce----");

const reduceArray = array.reduce(
  (Accumulator, current) => Accumulator + current
);
console.log(reduceArray);
```

### Diferencia reduce y join

join() se utiliza para combinar los elementos de un arreglo **en una sola cadena**, mientras que reduce() se utiliza para reducir los elementos de un arreglo **a un solo valor**.

### indexOf()

Retorna el primer índice en el que se puede encontrar un elemento dado en el array, o retorna -1 si el elemento no esta presente.

```js
console.log("----indexOf----");

console.log(array.indexOf(4));
```

### findIndex()

Retorna el índice del primer elemento de un array que cumpla con la función de prueba proporcionada. En caso contrario devuelve -1.

```js
console.log("----findIndex----");

const findIndex = array.findIndex((e) => e == 7);

console.log(findIndex);
```

### fill()

Cambia todos los elementos de un array por un valor estático, desde el índice de inicio hasta el índice final. Retorna el array modificado.

```js
console.log("----fill----");

//Llenar con 10 desde la posición 3
console.log(array.fill(10, 3));

//Llenar con 10 desde la posición 3 hasta la 7
console.log(array.fill(2, 3, 7));
```

### push()

Cambia todos los elementos de un array por un valor estático, desde el índice de inicio hasta el índice final. Retorna el array modificado.

```js
console.log("----push----");

const lista = ["leche", "cereales", "fruta"];
lista.push("agua");
console.log(lista);
```

### pop()

Elimina el último elemento de un array y lo devuelve. Este método cambia la longitud del array.

```js
console.log("----pop----");

lista.pop();
console.log(lista);
```

### shift()

Elimina el primer elemento del array y lo retorna. Este método modifica la longitud del array.

```js
console.log("----shift----");

lista.shift();

console.log(lista);
```

### slice()

Devuelve una copia de una parte del array dentro de un nuevo array empezando por inicio hasta fin (fin no incluido). <br>
El array original no se modificará.

```js
console.log("----slice----");

const sliceArray = array.slice(2, 4);
console.log(sliceArray);
```

### reverse()

Invierte el orden de los elementos de un array. <br>
El primer elemento pasa a ser el último y el último pasa a ser el primero.

```js
console.log("----reverse----");

console.log(array.reverse());
```

### splice()

Cambia el contenido de un array eliminando elementos existentes y/o agregando nuevos elementos.

```js
console.log("----splice----");

array.splice(1, 0, 44);
console.log(array);
```

### isArray()

Determina si el valor pasado es un Array.

```js
console.log("----isArray----");

console.log(Array.isArray(array));
console.log(Array.isArray("texto"));
```

### from()

Crea una nueva instancia de Array a partir de un objeto iterable.

```js
console.log("----from----");

console.log(Array.from("qwerty"));
// (6) ['q', 'w', 'e', 'r', 't', 'y']
```
