<h1 align="center">PriorityQueue</h1>

<h2>📑 Contenido</h2>

- [PriorityQueue](#priorityqueue)
- [Declaración y creación](#declaración-y-creación)
- [Características](#características)
- [Operaciones comunes](#operaciones-comunes)
- [Uso recomendado](#uso-recomendado)

## PriorityQueue

PriorityQueue en Java es una implementación de la interfaz Queue que ordena los elementos según su prioridad. Los elementos en una PriorityQueue se almacenan en un orden específico determinado por un comparador o por el orden natural de los elementos. Los elementos con mayor prioridad se colocan al frente de la cola y se procesan antes que los elementos con menor prioridad.

```java
import java.util.PriorityQueue;

public class Main {
    public static void main(String[] args) {
        // Crear una PriorityQueue de enteros
        PriorityQueue<Integer> priorityQueue = new PriorityQueue<>();

        // Agregar elementos a la cola
        priorityQueue.offer(5);
        priorityQueue.offer(10);
        priorityQueue.offer(3);
        priorityQueue.offer(8);

        // Recuperar y eliminar el elemento con la mayor prioridad
        int primerElemento = priorityQueue.poll();
        System.out.println("Primer elemento de la cola: " + primerElemento);

        // Recuperar el elemento con la mayor prioridad sin eliminarlo
        int elementoPrioritario = priorityQueue.peek();
        System.out.println("Elemento prioritario de la cola: " + elementoPrioritario);

        // Imprimir todos los elementos de la cola
        System.out.println("Elementos de la cola:");
        while (!priorityQueue.isEmpty()) {
            System.out.println(priorityQueue.poll());
        }
    }
}
```

## Declaración y creación

- Para utilizar PriorityQueue en Java, necesitas importar la clase PriorityQueue del paquete java.util.

- Puedes crear una PriorityQueue especificando el tipo de elementos que contendrá entre los signos de mayor y menor (<>). Por ejemplo: `PriorityQueue<Integer>` para una PriorityQueue que contiene enteros.

## Características

- PriorityQueue mantiene los elementos ordenados según su prioridad. Los elementos con mayor prioridad se procesan antes que los elementos con menor prioridad.

- Puedes proporcionar un comparador personalizado para definir el orden de los elementos, o utilizar el orden natural de los elementos si son comparables.

- Los elementos en una PriorityQueue no están garantizados para estar en un orden específico más allá del orden definido por su prioridad.

## Operaciones comunes

Las operaciones comunes en una PriorityQueue incluyen:

- offer(elemento): Agrega un elemento a la cola.

- poll(): Recupera y elimina el elemento con la mayor prioridad de la cola.

- peek(): Recupera, pero no elimina, el elemento con la mayor prioridad de la cola.

- size(): Devuelve el número de elementos en la cola.

- isEmpty(): Devuelve true si la cola está vacía, y false en caso contrario.

## Uso recomendado

- PriorityQueue es útil cuando necesitas procesar elementos en un orden específico basado en su prioridad.

- Es adecuado para implementar algoritmos de búsqueda, algoritmos de planificación, y en situaciones donde necesitas manejar elementos con prioridades diferentes.
