<h1 align="center">This</h1>

<h2>📑 Contenido</h2>

- [This](#this)
  - [Acceso a campos](#acceso-a-campos)
  - [Invocación de métodos](#invocación-de-métodos)
  - [Referencia al constructor](#referencia-al-constructor)

## This

En la programación orientada a objetos (POO), this es una referencia implícita a la instancia actual de una clase. Se utiliza para hacer referencia a los campos y métodos de la propia instancia dentro de los métodos de la misma clase.

### Acceso a campos

Se utiliza para acceder a los campos de la instancia actual, especialmente cuando tienen el mismo nombre que los parámetros del método.

```java
public class Persona {
    private String nombre;

    public Persona(String nombre) {
        this.nombre = nombre; // this se usa para distinguir entre el parámetro nombre y el campo nombre
    }
}
```

### Invocación de métodos

Se utiliza para invocar a otros métodos de la misma instancia.

```java
public class Persona {
    private String nombre;

    public void setNombre(String nombre) {
        this.nombre = nombre;
        validarNombre();
    }

    private void validarNombre() {
        // Lógica de validación del nombre
    }
}
```

### Referencia al constructor

Se utiliza para llamar a otro constructor de la misma clase desde un constructor.

```java
public class Persona {
    private String nombre;
    private int edad;

    public Persona() {
        this("Nombre por defecto", 0); // Llamada al constructor con parámetros
    }

    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
}
```
