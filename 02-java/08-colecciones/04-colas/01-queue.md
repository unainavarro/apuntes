<h1 align="center">Queue </h1>

<h2>📑 Contenido</h2>

- [Queue](#queue)
- [Declaración y creación](#declaración-y-creación)
- [Características](#características)
- [Implementaciones comunes](#implementaciones-comunes)
- [Uso recomendado](#uso-recomendado)

## Queue

Queue en Java es una interfaz que representa una colección de elementos ordenados en el que el elemento más antiguo (el primero que se agregó) se procesa primero. Se siguen los principios del modelo FIFO (First-In-First-Out), lo que significa que el primer elemento en entrar es el primero en salir.

```java
import java.util.Queue;
import java.util.LinkedList;

public class Main {
    public static void main(String[] args) {
        // Crear una cola usando LinkedList
        Queue<String> cola = new LinkedList<>();

        // Agregar elementos a la cola
        cola.offer("Primer elemento");
        cola.offer("Segundo elemento");
        cola.offer("Tercer elemento");

        // Ver el primer elemento de la cola sin eliminarlo
        String primerElemento = cola.peek();
        System.out.println("Primer elemento de la cola: " + primerElemento);

        // Eliminar y obtener el primer elemento de la cola
        String elementoEliminado = cola.poll();
        System.out.println("Elemento eliminado de la cola: " + elementoEliminado);

        // Imprimir todos los elementos de la cola
        System.out.println("Elementos de la cola:");
        for (String elemento : cola) {
            System.out.println(elemento);
        }
    }
}
```

## Declaración y creación

- La interfaz Queue está ubicada en el paquete java.util de Java, por lo que necesitas importarla para usarla.

- No puedes crear instancias directas de la interfaz Queue porque es una interfaz. Debes usar una de sus implementaciones, como LinkedList o PriorityQueue, para crear una cola.

## Características

- Los elementos en una cola se agregan al final y se eliminan del principio (el primero en entrar es el primero en salir, FIFO).

- Las implementaciones de Queue en Java no permiten elementos duplicados.

- Puedes utilizar métodos como offer(elemento) para agregar un elemento al final de la cola, poll() para eliminar y devolver el primer elemento de la cola, y peek() para ver el primer elemento sin eliminarlo.

## Implementaciones comunes

- LinkedList: Implementación que utiliza una lista enlazada para almacenar los elementos de la cola. Es flexible y eficiente para operaciones de inserción y eliminación al principio o al final de la cola.

- PriorityQueue: Implementación que utiliza una cola de prioridad para almacenar los elementos de la cola. Los elementos se procesan en orden basado en su prioridad.

## Uso recomendado

- Queue es útil cuando necesitas procesar elementos en el orden en que fueron agregados, como en un sistema de tareas o en la implementación de un algoritmo de búsqueda.

- Es adecuado para situaciones donde el orden de los elementos es importante y se necesita un acceso rápido al primer elemento de la cola.
