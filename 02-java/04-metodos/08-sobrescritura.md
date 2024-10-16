<h1 align="center">Sobrescritura de Métodos</h1>

<h2>📑 Contenido</h2>

- [Sobrescritura de Métodos](#sobrescritura-de-métodos)
  - [Características clave de la sobrescritura de métodos:](#características-clave-de-la-sobrescritura-de-métodos)
- [Sobrecarga vs Sobrescritura](#sobrecarga-vs-sobrescritura)

## Sobrescritura de Métodos

La sobrescritura de métodos en Java se refiere a la capacidad de una subclase de proporcionar una implementación específica de un método que ya está definido en su superclase. Esto permite a una subclase proporcionar una implementación específica para un método que ya existe en su superclase, lo que permite modificar o extender el comportamiento de ese método.

### Características clave de la sobrescritura de métodos:

- La subclase debe proporcionar una implementación del método con la misma firma (nombre y lista de parámetros) que el método que se está sobrescribiendo en la superclase.

- La subclase puede modificar o extender el comportamiento del método sobrescrito, pero no puede cambiar su firma.

- La decisión sobre qué versión del método se llama se toma en tiempo de ejecución, basándose en el tipo de objeto en tiempo de ejecución.

```java
public class Animal {
    public void sonido() {
        System.out.println("El animal hace un sonido");
    }
}

public class Perro extends Animal {
    @Override
    public void sonido() {
        System.out.println("El perro ladra");
    }
}
```

## Sobrecarga vs Sobrescritura

la sobrecarga de métodos se refiere a tener varios métodos con el mismo nombre pero diferentes parámetros, mientras que la sobrescritura de métodos se refiere a proporcionar una implementación específica de un método que ya está definido en una superclase. Ambos conceptos son fundamentales en la programación orientada a objetos y son utilizados frecuentemente en el desarrollo de aplicaciones Java.
