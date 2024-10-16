<h1 align="center">Stack</h1>

<h2>📑 Contenido</h2>

- [Stack](#stack)
- [Declaración y creación](#declaración-y-creación)
- [Características](#características)
- [Operaciones comunes](#operaciones-comunes)
- [Uso recomendado](#uso-recomendado)

## Stack

Un Stack en Java es una estructura de datos que representa una pila, siguiendo el principio de LIFO (Last In, First Out). En otras palabras, el último elemento que se añade a la pila es el primero en ser eliminado. Java proporciona una implementación de Stack a través de la clase java.util.Stack.

> [!NOTE]
>
> La clase java.util.Stack en Java es una implementación específica de una pila que se basa en un Vector, que a su vez está basado en un array. No obstante, debido a que la clase Stack hereda de Vector, posee las características de una lista en cierta medida. Pero en términos de comportamiento y diseño, se comporta como una pila más que como una lista.

```java
import java.util.Stack;

public class Main {
    public static void main(String[] args) {
        // Crear un Stack de enteros
        Stack<Integer> pila = new Stack<>();

        // Agregar elementos a la pila
        pila.push(10);
        pila.push(20);
        pila.push(30);

        // Ver el elemento en la parte superior de la pila
        int elementoSuperior = pila.peek();
        System.out.println("Elemento en la parte superior de la pila: " + elementoSuperior);

        // Eliminar elementos de la pila
        int elementoEliminado = pila.pop();
        System.out.println("Elemento eliminado de la pila: " + elementoEliminado);

        // Verificar si la pila está vacía
        boolean vacia = pila.empty();
        System.out.println("¿La pila está vacía? " + vacia);
    }
}
```

## Declaración y creación

- Para utilizar un Stack en Java, necesitas importar la clase Stack del paquete java.util.

- Puedes crear un Stack especificando el tipo de elementos que contendrá entre los signos de mayor y menor (<>). Por ejemplo: Stack<Integer> para un Stack que contiene enteros.

## Características

- Un Stack en Java implementa todas las operaciones de una pila estándar, como push (empujar), pop (sacar), peek (mirar sin sacar) y empty (vaciar).

- El método push se utiliza para agregar elementos a la parte superior de la pila.

- El método pop se utiliza para eliminar y devolver el elemento en la parte superior de la pila.

- El método peek se utiliza para obtener el elemento en la parte superior de la pila sin eliminarlo.

- El método empty se utiliza para verificar si la pila está vacía.

## Operaciones comunes

Las operaciones más comunes en un Stack son:

- push(elemento): Agrega un elemento a la parte superior de la pila.

- pop(): Elimina y devuelve el elemento en la parte superior de la pila.

- peek(): Devuelve el elemento en la parte superior de la pila sin eliminarlo.

- empty(): Verifica si la pila está vacía.

- search(elemento): Busca el elemento en la pila y devuelve su posición relativa desde la parte superior de la pila (siendo 1 el índice del elemento en la parte superior).

## Uso recomendado

- Los Stacks son útiles cuando necesitas un orden específico para tus datos, como procesar elementos en orden inverso al que fueron agregados.

- Son ampliamente utilizados en algoritmos de evaluación de expresiones matemáticas, algoritmos de búsqueda en profundidad (DFS), entre otros.
