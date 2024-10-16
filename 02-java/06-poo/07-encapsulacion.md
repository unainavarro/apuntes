<h1 align="center">Encapsulación</h1>

<h2>📑 Contenido</h2>

- [Encapsulación](#encapsulación)
- [Beneficios de la encapsulación](#beneficios-de-la-encapsulación)
- [Getter y Setter](#getter-y-setter)
  - [Getters](#getters)
  - [Setters](#setters)
  - [Beneficios de los getters y setters](#beneficios-de-los-getters-y-setters)

## Encapsulación

La encapsulación es uno de los cuatro conceptos fundamentales de la Programación Orientada a Objetos (POO), junto con la abstracción, la herencia y el polimorfismo. Es un principio de diseño que consiste en ocultar los detalles internos de un objeto y restringir el acceso directo a los datos, de manera que solo puedan ser modificados mediante métodos proporcionados por la propia clase.

En Java, la encapsulación se logra definiendo los campos de una clase como privados y proporcionando métodos públicos para acceder a estos campos (getters) y para modificarlos (setters). Esto se conoce como acceso controlado a los datos.

```java
public class CuentaBancaria {
    private double saldo; // Campo privado

    // Método para obtener el saldo
    public double getSaldo() {
        return saldo;
    }

    // Método para depositar dinero en la cuenta
    public void depositar(double cantidad) {
        if (cantidad > 0) {
            saldo += cantidad;
        }
    }

    // Método para retirar dinero de la cuenta
    public void retirar(double cantidad) {
        if (cantidad > 0 && saldo >= cantidad) {
            saldo -= cantidad;
        }
    }
}
```

## Beneficios de la encapsulación

- **Control de acceso:** Evita el acceso no autorizado y la modificación accidental de los datos.

- **Abstracción:** Oculta los detalles internos de implementación, lo que facilita la comprensión y el uso de la clase por parte de otros programadores.

- **Mantenimiento del código:** Permite cambiar la implementación interna de una clase sin afectar a los clientes que utilizan la clase.

- **Seguridad:** Ayuda a mantener la integridad de los datos y a prevenir errores y problemas de seguridad.

## Getter y Setter

Los getters y setters son métodos utilizados en la programación orientada a objetos para acceder y modificar los valores de los campos (o atributos) de una clase de manera controlada, siguiendo el principio de encapsulación.

### Getters

Los getters son métodos públicos que se utilizan para obtener el valor de un campo privado de una clase. Permiten acceder a los valores de los campos desde fuera de la clase.

```java
public class Persona {
    private String nombre;

    // Getter para el campo nombre
    public String getNombre() {
        return nombre;
    }
}
```

### Setters

Los setters son métodos públicos que se utilizan para modificar el valor de un campo privado de una clase. Permiten cambiar los valores de los campos desde fuera de la clase.

```java
public class Persona {
    private String nombre;

    // Setter para el campo nombre
    public void setNombre(String nombre) {
        this.nombre = nombre;
    }
}
```

### Beneficios de los getters y setters

- **Control de acceso:** Permiten acceder y modificar los campos de una clase de manera controlada, siguiendo el principio de encapsulación.

- **Validación:** Los setters pueden incluir lógica de validación para garantizar que los valores asignados sean válidos.

- **Flexibilidad:** Permiten cambiar la implementación interna de una clase sin afectar a los clientes que utilizan la clase.

- **Abstracción:** Ocultan los detalles de implementación de los campos, lo que facilita la comprensión y el uso de la clase.
