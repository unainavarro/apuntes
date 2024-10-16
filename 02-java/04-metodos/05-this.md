<h1 align="center">This</h1>

<h2>📑 Contenido</h2>

- [This](#this)
- [Referencia a campos de instancia](#referencia-a-campos-de-instancia)
- [Llamada a métodos de la instancia actual](#llamada-a-métodos-de-la-instancia-actual)
- [Constructor llamando a otro constructor](#constructor-llamando-a-otro-constructor)

## This

This es una palabra clave que se refiere a la instancia actual de la clase en la que se encuentra. Se utiliza dentro de la definición de un método para hacer referencia a los campos (variables de instancia) y métodos de la propia clase.

## Referencia a campos de instancia

Se utiliza para distinguir entre los campos de instancia y los parámetros del método o las variables locales cuando tienen el mismo nombre.

```java
public class Persona {
    private String nombre;

    public void setNombre(String nombre) {
        this.nombre = nombre; // "this.nombre" se refiere al campo de instancia, mientras que "nombre" se refiere al parámetro del método
    }
}
```

## Llamada a métodos de la instancia actual

Se utiliza para llamar a otros métodos de la misma instancia dentro de un método.

```java
public class Persona {
    public void saludar() {
        System.out.println("Hola, soy " + this.getNombre()); // Llama al método getNombre() de la misma instancia
    }

    public String getNombre() {
        return "Juan";
    }
}
```

## Constructor llamando a otro constructor

Se utiliza para llamar a otro constructor de la misma clase desde un constructor. Esto se hace normalmente dentro del primer statement de un constructor.

```java
public class Persona {
    private String nombre;
    private int edad;

    public Persona() {
        this("Nombre por defecto", 18); // Llama al constructor con los parámetros proporcionados
    }

    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
}
```
