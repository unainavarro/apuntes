<h1 align="center">Collections synchronizedList</h1>

<h2>📑 Contenido</h2>

- [Collections.synchronizedList](#collectionssynchronizedlist)
- [Uso](#uso)
- [Sincronización](#sincronización)
- [Uso recomendado](#uso-recomendado)

## Collections.synchronizedList

Collections.synchronizedList en Java es un método que devuelve una versión sincronizada de una lista dada. Cuando una lista se sincroniza, significa que se asegura que solo un subproceso pueda acceder a la lista en un momento dado, lo que evita que varios subprocesos accedan simultáneamente y potencialmente causen corrupción de datos o condiciones de carrera.

```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        // Crear una lista
        List<Integer> listaOriginal = new ArrayList<>();

        // Crear una lista sincronizada a partir de la lista original
        List<Integer> listaSincronizada = Collections.synchronizedList(listaOriginal);

        // Agregar elementos a la lista sincronizada
        listaSincronizada.add(1);
        listaSincronizada.add(2);
        listaSincronizada.add(3);

        // Imprimir la lista sincronizada
        System.out.println("Lista sincronizada:");
        synchronized (listaSincronizada) {
            for (int elemento : listaSincronizada) {
                System.out.println(elemento);
            }
        }
    }
}
```

## Uso

- Collections.synchronizedList se utiliza para obtener una versión sincronizada de cualquier lista en Java.

- Toma una lista existente como argumento y devuelve una instancia de lista que es sincronizada, lo que significa que todas las operaciones en esta lista están sincronizadas y son seguras para subprocesos.

## Sincronización

- Cuando una lista se sincroniza utilizando Collections.synchronizedList, cada método de la lista está sincronizado, lo que significa que solo un subproceso puede acceder a la lista a la vez.

- Esto evita condiciones de carrera y corrupción de datos cuando múltiples subprocesos intentan acceder y modificar la lista simultáneamente.

## Uso recomendado

- Collections.synchronizedList es útil cuando necesitas utilizar una lista en un entorno de subprocesos múltiples y quieres asegurarte de que las operaciones en la lista sean seguras para subprocesos.

- Es útil en situaciones donde varias partes del programa necesitan acceder y modificar una lista compartida al mismo tiempo.
