<h1 align="center">Constantes</h1>

<h2>📑 Contenido</h2>

- [Constantes](#constantes)

## Constantes

Una constante es una variable cuyo valor no puede ser cambiado después de su inicialización. Esto significa que una vez que se le asigna un valor, ese valor no puede ser modificado durante la ejecución del programa. En Java, las constantes se suelen definir utilizando la palabra clave final, lo que indica que el valor de la variable no cambiará.

**Características:**

- **Valor inmutable:** Una vez que se asigna un valor a una constante, ese valor no puede cambiar durante la ejecución del programa.

- **Definición:** Las constantes se definen utilizando la palabra clave final, seguida del tipo de dato, el nombre de la constante y el valor inicial.

- **Convención de nombres:** Por convención, los nombres de las constantes suelen escribirse en mayúsculas, separando las palabras con guiones bajos (\_), por ejemplo: PI, DIAS_EN_SEMANA, MAXIMO_INTENTOS, etc.

- **Alcance:** Las constantes pueden ser locales o globales, dependiendo de dónde se definan. Si se definen dentro de un método, su alcance se limita a ese método. Si se definen a nivel de clase, su alcance es global y pueden ser accedidas desde cualquier parte de la clase.

- **Inicialización:** Las constantes deben ser inicializadas al momento de su declaración o en el constructor de la clase.

**Ejemplo simple**

```java
public class EjemploConstantesEnMain {
    public static void main(String[] args) {
        // Declaración de constantes en el método main
        final double PRECIO_PRODUCTO = 50.0;
        final int CANTIDAD_PRODUCTOS = 10;

        // Cálculo del total
        double total = PRECIO_PRODUCTO * CANTIDAD_PRODUCTOS;

        // Mostrar el total
        System.out.println("El total es: " + total);
    }
}
```

**Ejemplo más avanzado**

```java
public class EjemploConstantes {
    // Constante global
    public static final double PI = 3.14159;

    // Constantes locales
    public void imprimirMensaje() {
        final String SALUDO = "¡Hola, mundo!";
        System.out.println(SALUDO);
    }

    public static void main(String[] args) {
        // Acceso a la constante global
        System.out.println("Valor de PI: " + EjemploConstantes.PI);

        // Creación de una instancia de la clase
        EjemploConstantes ejemplo = new EjemploConstantes();
        ejemplo.imprimirMensaje();
    }
}
```
