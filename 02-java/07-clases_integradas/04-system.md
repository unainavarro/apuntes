<h1 align="center">System</h1>

<h2>📑 Contenido</h2>

- [System](#system)
- [Métodos importantes](#métodos-importantes)

## System

La clase System en Java proporciona acceso a ciertas propiedades y funciones relacionadas con el sistema en el que se está ejecutando la aplicación Java. Aunque no es una clase integrada en el sentido estricto como String o Math, es una clase muy útil para interactuar con el entorno del sistema.

## Métodos importantes

- **exit(int status):** Termina la ejecución del programa Java con el código de estado especificado.

- **currentTimeMillis():** Devuelve la hora actual en milisegundos desde el Epoch (1 de enero de 1970 UTC).

- **gc():** Solicita al recolector de basura (garbage collector) que ejecute una recogida de basura.

- **getProperty(String key):** Obtiene el valor de la propiedad del sistema con la clave especificada.

- **setProperty(String key, String value):** Establece el valor de la propiedad del sistema con la clave especificada.

- **getenv(String name):** Obtiene el valor de una variable de entorno específica del sistema.

- **arraycopy(Object src, int srcPos, Object dest, int destPos, int length):** Copia una porción de un arreglo desde la posición de origen hasta un arreglo destino, comenzando en la posición especificada.

- **getSecurityManager():** Obtiene el administrador de seguridad actual para la aplicación.

- **setSecurityManager(SecurityManager s):** Establece el administrador de seguridad para la aplicación.

```java
public class Main {
    public static void main(String[] args) {
        // Obtener la hora actual en milisegundos
        long currentTime = System.currentTimeMillis();
        System.out.println("Current Time: " + currentTime);

        // Copiar elementos de un arreglo a otro
        int[] sourceArray = {1, 2, 3, 4, 5};
        int[] destArray = new int[5];
        System.arraycopy(sourceArray, 0, destArray, 0, sourceArray.length);
        System.out.println("Destination Array: " + Arrays.toString(destArray));

        // Obtener el valor de una propiedad del sistema
        String javaVersion = System.getProperty("java.version");
        System.out.println("Java Version: " + javaVersion);

        // Obtener el valor de una variable de entorno
        String homeDirectory = System.getenv("HOME");
        System.out.println("Home Directory: " + homeDirectory);
    }
}
```
