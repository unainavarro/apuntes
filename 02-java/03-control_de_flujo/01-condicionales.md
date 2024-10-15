<h1 align="center">Condicionales</h1>

<h2>📑 Contenido</h2>

- [if else](#if-else)
- [else if](#else-if)
- [if ternario(operador)](#if-ternariooperador)
- [switch](#switch)

## if else

Los condicionales if se utilizan para tomar decisiones en función de una condición booleana.

**Ejemplo**

```java
public class Main {
    public static void main(String[] args) {
        int edad = 20;

        if (edad >= 18) {
            System.out.println("Eres mayor de edad.");
        } else {
            System.out.println("Eres menor de edad.");
        }
    }
}
```

## else if

Los condicionales else if en Java son una extensión del condicional if que te permite comprobar múltiples condiciones en secuencia.

**Ejemplo**

```java
public class Main {
    public static void main(String[] args) {
        int edad = 20;

        if (edad < 13) {
            System.out.println("Eres un niño.");
        } else if (edad < 18) {
            System.out.println("Eres un adolescente.");
        } else if (edad < 65) {
            System.out.println("Eres un adulto.");
        } else {
            System.out.println("Eres un adulto mayor.");
        }
    }
}
```

## if ternario(operador)

En Java, el operador ternario (?:) es una forma compacta de escribir expresiones condicionales en una sola línea. Se compone de tres partes: una expresión booleana seguida de un signo de interrogación (?), una expresión que se evalúa si la expresión booleana es verdadera, seguida de un colon (:), y una expresión que se evalúa si la expresión booleana es falsa.

**Ejemplo**

```java
public class Main {
    public static void main(String[] args) {
        int edad = 20;
        String estado;

        estado = (edad >= 18) ? "Mayor de edad" : "Menor de edad";

        System.out.println("El estado es: " + estado);
    }
}
```

> [!NOTE]
>
> El operador ternario es útil cuando necesitas asignar un valor a una variable basado en una condición simple y quieres mantener tu código compacto y legible. Sin embargo, debes tener cuidado de no abusar de su uso, ya que en algunos casos puede hacer que el código sea menos legible si se utiliza de forma excesiva.

## switch

`Switch` es una estructura de control que se utiliza para tomar decisiones basadas en el valor de una expresión. Es una forma más compacta y legible que usar una serie de declaraciones if-else anidadas cuando necesitas evaluar múltiples casos.

**Ejemplo**

```java
public class Main {
    public static void main(String[] args) {
        int diaDeLaSemana = 3;
        String nombreDelDia;

        switch (diaDeLaSemana) {
            case 1:
                nombreDelDia = "Lunes";
                break;
            case 2:
                nombreDelDia = "Martes";
                break;
            case 3:
                nombreDelDia = "Miércoles";
                break;
            case 4:
                nombreDelDia = "Jueves";
                break;
            case 5:
                nombreDelDia = "Viernes";
                break;
            case 6:
                nombreDelDia = "Sábado";
                break;
            case 7:
                nombreDelDia = "Domingo";
                break;
            default:
                nombreDelDia = "Día no válido";
        }

        System.out.println("El día número " + diaDeLaSemana + " es " + nombreDelDia + ".");
    }
}
```

> [!NOTE]
>
> La estructura de control switch es útil cuando tienes una variable que puede tomar varios valores distintos y quieres ejecutar un bloque de código diferente para cada valor posible.
