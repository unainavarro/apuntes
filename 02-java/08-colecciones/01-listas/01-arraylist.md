<h1 align="center">ArrayList</h1>

<h2>📑 Contenido</h2>

- [ArrayList](#arraylist)
- [Características](#características)
- [Declaración y creación](#declaración-y-creación)
- [Operaciones comunes](#operaciones-comunes)
- [Eficiencia](#eficiencia)
- [Uso recomendado](#uso-recomendado)

## ArrayList

Un ArrayList en Java es una estructura de datos que implementa la interfaz List y utiliza un array dinámico para almacenar elementos.

```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        // Crear un ArrayList
        ArrayList<String> lista = new ArrayList<>();

        // Agregar elementos
        lista.add("Hola");
        lista.add("Mundo");
        lista.add("!");

        // Acceder a elementos por índice
        String elemento = lista.get(0);
        System.out.println("Elemento en el índice 0: " + elemento);

        // Modificar elementos
        lista.set(2, "Java");
        System.out.println("ArrayList modificado: " + lista);

        // Eliminar elementos
        lista.remove(1);
        System.out.println("ArrayList después de eliminar elemento en el índice 1: " + lista);

        // Tamaño del ArrayList
        int tamaño = lista.size();
        System.out.println("Tamaño del ArrayList: " + tamaño);

        // Iterar sobre elementos
        System.out.println("Elementos del ArrayList:");
        for (String item : lista) {
            System.out.println(item);
        }

        // Verificar si un elemento está presente
        boolean contiene = lista.contains("Java");
        System.out.println("¿El ArrayList contiene 'Java'? " + contiene);

        // Eliminar todos los elementos
        lista.clear();
        System.out.println("ArrayList después de limpiar: " + lista);
    }
}
```

## Características

- Un ArrayList en Java es una implementación de la interfaz List que utiliza un array dinámico para almacenar elementos.

- A diferencia de los arrays estáticos, un ArrayList puede cambiar de tamaño dinámicamente según sea necesario.

- Los elementos en un ArrayList están ordenados y pueden contener duplicados.
  Permite acceder, insertar, modificar y eliminar elementos de manera eficiente.

## Declaración y creación

- Para crear un ArrayList en Java, primero necesitas importar la clase ArrayList del paquete java.util.

- Puedes declarar un ArrayList especificando el tipo de elementos que contendrá entre los signos de mayor y menor (<>). Por ejemplo: `ArrayList<String>` para un ArrayList que contiene Strings.

## Operaciones comunes

- Agregar elementos: Utiliza el método add(elemento) para agregar un elemento al final del ArrayList.

- Acceder elementos: Utiliza el método get(indice) para acceder a un elemento por su índice.

- Modificar elementos: Utiliza el método set(indice, elemento) para reemplazar un elemento en un índice específico.

- Eliminar elementos: Utiliza el método remove(indice) para eliminar un elemento por su índice, o remove(elemento) para eliminar la primera ocurrencia de un elemento.

- Tamaño del ArrayList: Utiliza el método size() para obtener el número de elementos en el ArrayList.

- Iterar sobre elementos: Puedes utilizar un bucle for-each para iterar sobre todos los elementos del ArrayList.

- Verificar si un elemento está presente: Utiliza el método contains(elemento) para verificar si un elemento está presente en el ArrayList.

- Eliminar todos los elementos: Utiliza el método clear() para eliminar todos los elementos del ArrayList.

## Eficiencia

- En general, las operaciones de agregar, eliminar y acceder elementos tienen una complejidad de tiempo de O(1) en promedio.

- Sin embargo, la inserción y eliminación en posiciones intermedias puede ser más costosa (O(n)), ya que requiere desplazar los elementos adyacentes.

## Uso recomendado

- ArrayList es adecuado cuando necesitas una colección dinámica de elementos y el acceso aleatorio es común.

- No es eficiente para inserciones y eliminaciones frecuentes en posiciones intermedias, ya que esto puede requerir desplazamientos de elementos.
