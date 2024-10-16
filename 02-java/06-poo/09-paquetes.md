<h1 align="center">Paquetes</h1>

<h2>📑 Contenido</h2>

- [Paquetes](#paquetes)
- [Creación de paquetes](#creación-de-paquetes)
- [Estructura de directorios](#estructura-de-directorios)
- [Importación de paquetes:](#importación-de-paquetes)
- [Beneficios de los paquetes](#beneficios-de-los-paquetes)

## Paquetes

En Java, los paquetes son mecanismos de organización y agrupación de clases y otros elementos relacionados en una jerarquía. Proporcionan un espacio de nombres único para evitar conflictos de nombres entre clases y mejorar la organización del código.

## Creación de paquetes

Para crear un paquete en Java, debes incluir una declaración package al principio de tu archivo fuente Java. Esta declaración especifica el nombre del paquete al que pertenece la clase.

Por ejemplo, si tienes una clase llamada MiClase que pertenece al paquete com.ejemplo, la declaración de paquete se vería así:

```java
package com.ejemplo;

public class MiClase {
    // Código de la clase
}
```

## Estructura de directorios

La estructura de directorios en el sistema de archivos refleja la estructura de los paquetes en Java. Por ejemplo, si el paquete de la clase MiClase es com.ejemplo, entonces el archivo fuente MiClase.java debe estar ubicado en un directorio llamado com/ejemplo.

```
src/
└── com/
    └── ejemplo/
        └── MiClase.java
```

## Importación de paquetes:

Para utilizar clases de otros paquetes en tu código, puedes importar el paquete o clases específicas dentro del paquete utilizando la declaración import. Esto permite acceder a las clases del paquete sin necesidad de usar el nombre completo de la clase cada vez.

```java
import com.ejemplo.MiClase;

public class OtraClase {
    public static void main(String[] args) {
        MiClase objeto = new MiClase();
        // Código que utiliza la clase MiClase
    }
}
```

## Beneficios de los paquetes

- **Organización del código:** Facilitan la organización y la estructura del código fuente en proyectos grandes.

- **Prevención de conflictos de nombres:** Proporcionan un espacio de nombres único para evitar conflictos de nombres entre clases.

- **Reutilización de código:** Permiten reutilizar y compartir clases en diferentes proyectos o partes del mismo proyecto.

- **Control de acceso:** Facilitan el control de acceso a clases y otros elementos mediante la especificación de modificadores de acceso como public, protected, private, etc.
