<h1 align="center">ArrayDeque</h1>

<h2>📑 Contenido</h2>

- [ArrayDeque](#arraydeque)
- [Declaración y creación](#declaración-y-creación)
- [Características](#características)
- [Uso recomendado](#uso-recomendado)

## ArrayDeque

ArrayDeque en Java es una implementación de la interfaz Deque que utiliza un arreglo dinámico para almacenar los elementos. El nombre "ArrayDeque" proviene de "Array Double Ended Queue", lo que significa que la estructura de datos admite operaciones de cola y pila. Es decir, puedes agregar o quitar elementos tanto al principio como al final de la deque.

```java
import java.util.ArrayDeque;

public class Main {
    public static void main(String[] args) {
        // Crear una ArrayDeque de enteros
        ArrayDeque<Integer> deque = new ArrayDeque<>();

        // Agregar elementos al principio y al final de la deque
        deque.addFirst(1);
        deque.addLast(2);
        deque.addLast(3);

        // Eliminar y obtener el primer elemento de la deque
        int primerElemento = deque.removeFirst();
        System.out.println("Primer elemento de la deque: " + primerElemento);

        // Eliminar y obtener el último elemento de la deque
        int ultimoElemento = deque.removeLast();
        System.out.println("Último elemento de la deque: " + ultimoElemento);

        // Imprimir todos los elementos de la deque
        System.out.println("Elementos de la deque:");
        for (int elemento : deque) {
            System.out.println(elemento);
        }
    }
}
```

## Declaración y creación

- La clase ArrayDeque está ubicada en el paquete java.util de Java, por lo que necesitas importarla para usarla.

- Puedes crear una ArrayDeque especificando el tipo de elementos que contendrá entre los signos de mayor y menor (<>). Por ejemplo: `ArrayDeque<Integer>` para una ArrayDeque que contiene enteros.

## Características

- ArrayDeque es una estructura de datos de tamaño dinámico que no tiene un límite fijo de capacidad.

- Admite operaciones eficientes de inserción y eliminación tanto al principio como al final de la deque, con complejidad de tiempo constante amortizado O(1).

- Puedes utilizar métodos como addFirst(elemento) y addLast(elemento) para agregar elementos al principio y al final de la deque, respectivamente. Y métodos como removeFirst() y removeLast() para eliminar y devolver el primer y último elemento de la deque, respectivamente.

## Uso recomendado

- ArrayDeque es útil cuando necesitas una estructura de datos de tamaño dinámico que admita operaciones eficientes tanto de cola como de pila.

- Es adecuado para implementar algoritmos donde necesitas acceso rápido a los elementos en los extremos de la deque, como en un algoritmo de búsqueda en anchura (BFS) o en una cola de prioridad sin orden.
