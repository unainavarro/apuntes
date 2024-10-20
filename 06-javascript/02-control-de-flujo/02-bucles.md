<h1 align="center">Bucles</h1>

<h2>📑 Contenido</h2>

- [Bucles](#bucles)
- [Bucle while](#bucle-while)
- [Bucle do...while](#bucle-dowhile)
- [Bucle for](#bucle-for)
- [Bucle anidado (For dentro de For)](#bucle-anidado-for-dentro-de-for)
- [Bucle for...in](#bucle-forin)
- [Bucle for...of](#bucle-forof)

## Bucles

Los bucles son una estructura de control que permite repetir un bloque de código varias veces. Los bucles son útiles cuando se desea realizar una tarea repetitiva, como iterar sobre una lista de elementos o realizar una operación matemática varias veces.

> [!NOTE]
>
> Es importante tener cuidado al utilizar bucles asegurarse de que la condición en algún momento se vuelva falsa y evite caer en un bucle infinito.

## Bucle while

El bucle while se utiliza para ejecutar un bloque de código mientras una condición específica sea verdadera.

```js
//Contador de 1-5

let contador = 1;

while (contador <= 5) {
  console.log(contador);
  contador++;
}
```

## Bucle do...while

El bucle do...while es una variante del bucle while. La principal diferencia es que en un bucle do...while, la condición se evalúa después de que el bloque de código se ha ejecutado al menos una vez.

Si necesitas que el bloque de código se ejecute al menos una vez antes de que se evalúe la condición, do...while puede ser más apropiado.

```js
//Contador con do...while
let contador = 1;

do {
  console.log(contador);
  contador++;
} while (contador <= 5);
```

## Bucle for

El bucle for es una estructura de control que permite ejecutar un bloque de código repetidamente mientras se cumpla una condición.

Sintaxis: <br>

```js
for (inicialización; condición; actualización) {
  // Código a ejecutar en cada iteración
}
```

- **Inicialización:** Se ejecuta una vez al principio y generalmente se utiliza para inicializar el contador o cualquier variable necesaria.
- **Condición:** Se evalúa antes de cada iteración. Si es verdadera, el bucle continúa; si es falsa, el bucle se detiene.
- **Actualización:** Se ejecuta al final de cada iteración y generalmente se utiliza para actualizar el contador o realizar alguna otra acción.

```js
//Recorrer una lista de compra
let lista = ["Cereales", "Leche", "Melón"];

for (i = 0; i < lista.length; i++) {
  console.log(lista[i]);
}

//Mostrar números del 1-5
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
/*
Puedes usar let para declarar la variable de iteración (i en este caso), lo cual es una buena práctica para tener un ámbito de bloque más controlado.
*/
```

## Bucle anidado (For dentro de For)

Un bucle for dentro de otro bucle for se llama un bucle anidado. Esto es comúnmente utilizado cuando necesitas iterar sobre matrices bidimensionales o realizar operaciones que involucren pares de valores.

```js
for (let i = 1; i <= 3; i++) {
  for (let j = 1; j <= 3; j++) {
    console.log(`i: ${i}, j: ${j}`);
  }
}

/*
Resultado:
i: 1, j: 1
i: 1, j: 2
i: 1, j: 3
i: 2, j: 1
i: 2, j: 2
i: 2, j: 3
i: 3, j: 1
i: 3, j: 2
i: 3, j: 3
*/
```

En este ejemplo, hay dos bucles for anidados. El bucle exterior se encarga de la variable i y se ejecutará tres veces (cuando i es 1, 2 y 3). Dentro de cada iteración del bucle exterior, el bucle interior se encarga de la variable j y se ejecutará también tres veces (cuando j es 1, 2 y 3).

## Bucle for...in

El bucle for...in se utiliza para iterar sobre las propiedades enumerables de un objeto.

Es importante tener en cuenta que este tipo de bucle itera sobre todas las propiedades enumerables del objeto, incluyendo las propiedades que pueda haber heredado del prototipo. Además, el orden de las propiedades no está garantizado, ya que JavaScript no garantiza un orden específico para las propiedades de un objeto.

```js
//Itera sobre las propiedades del objeto persona, y en cada iteración, imprime el nombre de la propiedad y su valor.
const persona = {
  nombre: "Juan",
  edad: 30,
  ciudad: "CiudadDeJuan",
};

for (const propiedad in persona) {
  console.log(propiedad + ": " + persona[propiedad]);
}
```

> [!NOTE]
>
> Debido a las limitaciones y problemas potenciales con for...in, se recomienda considerar el uso de for...of (para iterar sobre elementos de iterables) o Object.keys, Object.values y Object.entries (para trabajar con propiedades específicas de un objeto) en lugar de for...in en ciertos contextos.
>
> Utilizar con fines de depuración, ya que es una forma fácil de comprobar las propiedades de un objeto (mediante la salida a la consola o de otro modo).

## Bucle for...of

El bucle for...of se utiliza para iterar sobre los elementos de estructuras de datos iterables, como arreglos, cadenas, mapas, conjuntos, y otros objetos iterables. No se puede utilizar con objetos normales

```js
//Recorrer un arreglo
const numeros = [1, 2, 3, 4, 5];

for (const numero of numeros) {
  console.log(numero);
}
```

> [!NOTE]
>
> Este tipo de bucle es útil cuando necesitas acceder directamente a los valores de un iterable y no te importa el índice o la clave asociada
