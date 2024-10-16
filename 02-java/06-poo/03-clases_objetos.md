<h1 align="center">Clases y Objetos</h1>

<h2>📑 Contenido</h2>

- [Clases](#clases)
  - [Atributos](#atributos)
  - [Métodos](#métodos)
  - [Constructor](#constructor)
- [Objetos](#objetos)

## Clases

Una clase en Java es una plantilla para crear objetos. Define los atributos y métodos que tendrán los objetos de esa clase. Los atributos representan el estado de los objetos (datos), mientras que los métodos representan su comportamiento (funciones).

### Atributos

Los atributos son variables que representan el estado de un objeto. Cada objeto creado a partir de una clase tiene su propia copia de los atributos de esa clase. Los atributos describen las características o propiedades de un objeto.

### Métodos

Los métodos son funciones que definen el comportamiento de un objeto. Representan las acciones que pueden realizar los objetos de una clase. Los métodos pueden acceder y modificar los atributos de un objeto y realizar otras operaciones relacionadas con el objeto.

### Constructor

Un constructor es un tipo especial de método que se utiliza para inicializar objetos de una clase. El constructor tiene el mismo nombre que la clase y no tiene un tipo de retorno explícito. Se invoca automáticamente cuando se crea un objeto utilizando la palabra clave new.

```java
public class Persona {
    // Atributos
    private String nombre;
    private int edad;

    // Constructor
    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }

    // Métodos
    public String getNombre() {
        return nombre;
    }

    public int getEdad() {
        return edad;
    }
}
```

## Objetos

Un objeto en Java es una instancia específica de una clase. Se crea utilizando la palabra clave new seguida del constructor de la clase. Los objetos pueden acceder a los atributos y métodos definidos en su clase correspondiente.

```java
public class Main {
    public static void main(String[] args) {
        // Crear un objeto de la clase Persona
        Persona persona1 = new Persona("Juan", 30);

        // Acceder a los atributos y métodos del objeto
        System.out.println("Nombre: " + persona1.getNombre());
        System.out.println("Edad: " + persona1.getEdad());
    }
}
```
