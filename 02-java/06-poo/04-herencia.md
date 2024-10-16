<h1 align="center">Herencia</h1>

<h2>📑 Contenido</h2>

- [Herencia](#herencia)
- [Principios de la herencia en Java](#principios-de-la-herencia-en-java)
- [Características](#características)

## Herencia

La herencia es un concepto fundamental en la Programación Orientada a Objetos (POO) que permite crear nuevas clases basadas en clases existentes. En Java, la herencia se logra mediante la relación "es un" (o "is-a" en inglés), donde una clase (subclase o clase derivada) puede heredar atributos y métodos de otra clase (superclase o clase base).

La herencia en Java es una técnica poderosa para la reutilización de código y la organización de clases en una jerarquía lógica. Permite una mayor modularidad y facilita la extensión y mantenimiento del código. Sin embargo, se debe tener cuidado al diseñar jerarquías de clases para evitar problemas como la sobrecarga de clases y la violación del principio de substitución de Liskov.

> [!NOTE]
>
> El principio de sustitución de Liskov (Liskov Substitution Principle, LSP) establece que los objetos de una superclase deben poder ser reemplazados por objetos de sus subclases sin afectar la integridad del programa.

## Principios de la herencia en Java

- **Clase Base (Superclase):** La clase que se extiende o de la que se hereda se conoce como superclase o clase base.

- **Clase Derivada (Subclase):** La clase que hereda de otra clase se conoce como subclase o clase derivada

**Sintaxis**

```java
// Clase base (superclase)
class Figura {
    void dibujar() {
        System.out.println("Dibujando una figura");
    }
}

// Clase derivada (subclase)
class Circulo extends Figura {
    void dibujar() {
        System.out.println("Dibujando un círculo");
    }
}
```

## Características

- Herencia de atributos y métodos: Las subclases heredan los atributos y métodos públicos o protegidos de la superclase.

- Extensión: Las subclases pueden agregar nuevos atributos y métodos, y también pueden sobrescribir los métodos heredados de la superclase.

- Acceso a miembros heredados: Las subclases pueden acceder a los miembros heredados de la superclase utilizando los modificadores de acceso adecuados (public, protected).

- Jerarquía de clases: La herencia en Java puede formar una jerarquía de clases, donde las subclases pueden heredar de otras subclases, creando una cadena de herencia.
