 <h1 align="center">LinkedHashMap</h1> 
 
 <h2>📑 Contenido</h2> 
 
- [LinkedHashMap](#linkedhashmap)
- [Declaración y creación](#declaración-y-creación)
- [Características](#características)
- [Iteración](#iteración)
- [Eficiencia](#eficiencia)
- [Uso recomendado](#uso-recomendado)
 
 ## LinkedHashMap

LinkedHashMap en Java es una implementación de la interfaz Map que mantiene el orden de inserción de los elementos. Combina las características de HashMap y LinkedHashMap: al igual que HashMap, permite un acceso rápido a los elementos basado en sus claves, y al igual que LinkedHashMap, mantiene el orden de inserción de los elementos.

```java
import java.util.LinkedHashMap;
import java.util.Map;

public class Main {
    public static void main(String[] args) {
        // Crear un LinkedHashMap de Strings (clave) a Integers (valor)
        Map<String, Integer> linkedHashMap = new LinkedHashMap<>();

        // Agregar elementos al LinkedHashMap
        linkedHashMap.put("Juan", 25);
        linkedHashMap.put("María", 30);
        linkedHashMap.put("Pedro", 28);

        // Acceder a un valor por su clave
        int edadDeMaria = linkedHashMap.get("María");
        System.out.println("La edad de María es: " + edadDeMaria);

        // Eliminar un elemento del LinkedHashMap
        linkedHashMap.remove("Juan");

        // Imprimir todos los pares clave-valor del LinkedHashMap
        System.out.println("Elementos del LinkedHashMap:");
        for (Map.Entry<String, Integer> entry : linkedHashMap.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }

        // Obtener el tamaño del LinkedHashMap
        int tamaño = linkedHashMap.size();
        System.out.println("Tamaño del LinkedHashMap: " + tamaño);
    }
}
```

## Declaración y creación

- Para utilizar LinkedHashMap en Java, necesitas importar la clase LinkedHashMap del paquete java.util.

- Puedes crear un LinkedHashMap especificando el tipo de las claves y los valores entre los signos de mayor y menor (<>). Por ejemplo: `LinkedHashMap<String, Integer>` para un LinkedHashMap que mapea cadenas a enteros.

## Características

- LinkedHashMap mantiene el orden de inserción de los elementos, lo que significa que los elementos se recuperan en el mismo orden en que fueron insertados.

- Al igual que HashMap, LinkedHashMap proporciona un acceso rápido a los elementos basado en sus claves.

- Permite claves nulas y valores nulos, al igual que HashMap.

## Iteración

- La iteración sobre un LinkedHashMap se realiza en el orden en que se insertaron los elementos.

- Esto significa que si iteras sobre un LinkedHashMap, obtendrás los elementos en el mismo orden en que fueron insertados.

## Eficiencia

- Al igual que HashMap, las operaciones básicas (inserción, eliminación, búsqueda) en un LinkedHashMap tienen un tiempo de ejecución promedio constante (O(1)).

- Sin embargo, mantener el orden de inserción agrega una pequeña sobrecarga de memoria y rendimiento en comparación con HashMap.

## Uso recomendado

- LinkedHashMap es útil cuando necesitas mantener el orden de inserción de los elementos y al mismo tiempo acceder rápidamente a los elementos por sus claves.

- Es adecuado para casos de uso donde el orden de los elementos es importante, como el procesamiento de registros de datos o la representación de instrucciones en un programa.
