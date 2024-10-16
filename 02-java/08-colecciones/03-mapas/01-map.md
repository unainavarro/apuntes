 <h1 align="center">Map</h1> 
 
 <h2>📑 Contenido</h2> 
 
- [Map](#map)
- [Declaración y creación](#declaración-y-creación)
- [Características](#características)
- [Operaciones comunes](#operaciones-comunes)
- [Implementaciones de Map](#implementaciones-de-map)
- [Uso recomendado](#uso-recomendado)
 
 ## Map

Un Map en Java es una interfaz que representa una colección de pares clave-valor, donde cada clave está asociada a un único valor. Cada clave en un mapa es única y se utiliza para recuperar su valor asociado. Los mapas en Java son parte del framework de colecciones y se utilizan comúnmente para mapear claves a valores y realizar búsquedas eficientes.

```java
import java.util.HashMap;
import java.util.Map;

public class Main {
    public static void main(String[] args) {
        // Crear un HashMap de Strings (clave) a Integers (valor)
        Map<String, Integer> mapa = new HashMap<>();

        // Agregar elementos al mapa
        mapa.put("Juan", 25);
        mapa.put("María", 30);
        mapa.put("Pedro", 28);

        // Acceder a un valor por su clave
        int edadDeMaria = mapa.get("María");
        System.out.println("La edad de María es: " + edadDeMaria);

        // Verificar si una clave está presente
        boolean contienePedro = mapa.containsKey("Pedro");
        System.out.println("¿El mapa contiene a Pedro? " + contienePedro);

        // Eliminar un elemento del mapa
        mapa.remove("Juan");

        // Imprimir todos los pares clave-valor del mapa
        System.out.println("Elementos del mapa:");
        for (Map.Entry<String, Integer> entry : mapa.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }

        // Obtener el tamaño del mapa
        int tamaño = mapa.size();
        System.out.println("Tamaño del mapa: " + tamaño);

        // Verificar si el mapa está vacío
        boolean vacio = mapa.isEmpty();
        System.out.println("¿El mapa está vacío? " + vacio);
    }
}
```

## Declaración y creación

- La interfaz Map está ubicada en el paquete java.util de Java, por lo que necesitas importarla para usarla.

- Puedes crear un Map utilizando una de sus implementaciones, como HashMap, TreeMap o LinkedHashMap.

## Características

- Un mapa en Java almacena elementos como pares clave-valor, donde cada clave está asociada a un único valor.

- Las claves en un mapa son únicas; no pueden haber claves duplicadas.

- Los valores pueden ser duplicados y pueden ser de cualquier tipo, incluidos objetos y colecciones.

## Operaciones comunes

Las operaciones comunes en un mapa incluyen:

- put(clave, valor): Asocia el valor especificado con la clave especificada en el mapa.

- get(clave): Devuelve el valor asociado con la clave especificada, o null si el mapa no contiene la clave.

- remove(clave): Elimina la entrada asociada con la clave especificada del mapa, si está presente.

- containsKey(clave): Devuelve true si el mapa contiene una entrada para la clave especificada, y false en caso contrario.

- containsValue(valor): Devuelve true si el mapa contiene una o más entradas con el valor especificado.

- size(): Devuelve el número de pares clave-valor en el mapa.

- isEmpty(): Devuelve true si el mapa no contiene entradas.

## Implementaciones de Map

- HashMap: Implementación que utiliza una tabla hash para almacenar las entradas. No garantiza ningún orden particular de las claves.

- TreeMap: Implementación que mantiene las claves ordenadas según su orden natural o según un comparador personalizado.

- LinkedHashMap: Implementación que mantiene el orden de inserción de las claves.

## Uso recomendado

- Utiliza un mapa cuando necesites asociar claves únicas con valores.

- Es útil para realizar búsquedas eficientes por clave y recuperar valores asociados.

- Puede ser utilizado en una variedad de situaciones, como la implementación de diccionarios, la representación de relaciones entre entidades y la realización de conteos o seguimientos.
