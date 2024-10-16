<h1 align="center">Modificadores de acceso</h1>

<h2>📑 Contenido</h2>

- [Modificadores de acceso](#modificadores-de-acceso)

## Modificadores de acceso

Los modificadores de acceso son palabras clave que se utilizan para controlar la visibilidad de los campos, métodos y constructores de una clase. Estos modificadores determinan desde dónde se puede acceder a los miembros de una clase y quién puede acceder a ellos.

Java proporciona cuatro tipos de modificadores de acceso:

- **public:** Los miembros marcados como public son accesibles desde cualquier clase y cualquier paquete. No hay restricciones de acceso.

- **private:** Los miembros marcados como private son accesibles solo dentro de la misma clase. No se pueden acceder desde clases fuera de la clase que los contiene.

- **protected:** Los miembros marcados como protected son accesibles dentro de la misma clase, dentro del mismo paquete y por clases que son subclases de la clase que los contiene (herencia).

- **default** (sin especificador de acceso): Si no se especifica un modificador de acceso (también conocido como "default"), el miembro es accesible solo dentro del mismo paquete. No se puede acceder desde clases fuera del paquete.

**Ejemplo**

```java
package com.ejemplo;

public class Ejemplo {
    public int publico; // Accesible desde cualquier lugar
    private int privado; // Accesible solo dentro de la misma clase
    protected int protegido; // Accesible dentro del mismo paquete y por subclases
    int defaultInt; // Accesible solo dentro del mismo paquete
}
```
