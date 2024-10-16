<h1 align="center">Polimorfismo</h1>

<h2>📑 Contenido</h2>

- [Polimorfismo](#polimorfismo)
- [Sobrecarga de Métodos (Polimorfismo de compilación)](#sobrecarga-de-métodos-polimorfismo-de-compilación)
- [Sobrescritura de Métodos (Polimorfismo de tiempo de ejecución)](#sobrescritura-de-métodos-polimorfismo-de-tiempo-de-ejecución)
- [Beneficios del Polimorfismo](#beneficios-del-polimorfismo)

## Polimorfismo

El polimorfismo es un concepto clave en la Programación Orientada a Objetos (POO) que permite que un objeto pueda tomar múltiples formas. En Java, el polimorfismo se puede lograr de dos maneras: mediante la sobrecarga de métodos y mediante la sobrescritura de métodos (también conocida como polimorfismo de tiempo de ejecución o de subtipos).

## Sobrecarga de Métodos (Polimorfismo de compilación)

La sobrecarga de métodos es cuando una clase tiene dos o más métodos con el mismo nombre pero con diferentes parámetros. La selección del método adecuado para llamar se realiza en tiempo de compilación, según los tipos y la cantidad de argumentos pasados.

```java
class Calculadora {
    int sumar(int a, int b) {
        return a + b;
    }

    double sumar(double a, double b) {
        return a + b;
    }
}
```

## Sobrescritura de Métodos (Polimorfismo de tiempo de ejecución)

La sobrescritura de métodos es cuando una subclase proporciona una implementación específica de un método que ya está definido en su superclase. Esto permite que un objeto de la subclase se comporte de manera diferente a un objeto de la superclase al llamar al mismo método.

```java
class Animal {
    void hacerSonido() {
        System.out.println("Animal haciendo sonido");
    }
}

class Perro extends Animal {
    @Override
    void hacerSonido() {
        System.out.println("Guau Guau");
    }
}
```

## Beneficios del Polimorfismo

- **Reutilización de código:** Permite utilizar una interfaz común para varios tipos de objetos.

- **Flexibilidad:** Facilita la extensión del código sin modificar las clases existentes.

- **Modularidad:** Facilita el diseño modular y la organización del código en jerarquías de clases.
