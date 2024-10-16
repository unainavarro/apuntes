<h1 align="center">Anotaciones</h1>

<h2>📑 Contenido</h2>

- [Anotaciones](#anotaciones)
- [Definición de Anotaciones](#definición-de-anotaciones)
- [Uso de Anotaciones](#uso-de-anotaciones)
- [Anotaciones de Retención y Objetivo](#anotaciones-de-retención-y-objetivo)
- [Anotaciones Predefinidas](#anotaciones-predefinidas)
- [Reflexión](#reflexión)

## Anotaciones

En Java 8, no se introdujeron nuevas anotaciones específicas en el lenguaje, pero se realizaron mejoras en el uso de las anotaciones existentes. Las anotaciones en Java son metadatos que proporcionan información adicional sobre clases, métodos u otros elementos en el código fuente.

## Definición de Anotaciones

Puedes definir tus propias anotaciones en Java utilizando la palabra clave @interface.

```java
import java.lang.annotation.ElementType;
import java.lang.annotation.Retention;
import java.lang.annotation.RetentionPolicy;
import java.lang.annotation.Target;

@Retention(RetentionPolicy.RUNTIME)
@Target(ElementType.METHOD)
public @interface MiAnotacion {
    String valor() default "default";
}
```

## Uso de Anotaciones

Puedes aplicar anotaciones a clases, métodos, campos u otros elementos en tu código utilizando la sintaxis @NombreDeAnotacion.

```java
public class MiClase {

    @MiAnotacion
    public void miMetodo() {
        // Código del método
    }
}
```

## Anotaciones de Retención y Objetivo

Las anotaciones pueden tener políticas de retención y objetivos específicos. La política de retención determina en qué momentos la anotación estará disponible (por ejemplo, en tiempo de ejecución o solo en tiempo de compilación), mientras que el objetivo especifica los elementos a los que se puede aplicar la anotación (por ejemplo, clases, métodos, campos, etc.).

## Anotaciones Predefinidas

Java proporciona varias anotaciones predefinidas en el paquete java.lang.annotation, como @Deprecated, @Override, @SuppressWarnings, etc. Estas anotaciones se utilizan comúnmente para proporcionar información adicional sobre el código y ayudar en la verificación y documentación del mismo.

## Reflexión

Las anotaciones se pueden acceder en tiempo de ejecución utilizando reflexión. Esto permite que las aplicaciones inspeccionen y respondan dinámicamente a las anotaciones presentes en las clases y métodos.

```java
MiAnotacion anotacion = MiClase.class.getMethod("miMetodo").getAnnotation(MiAnotacion.class);
String valor = anotacion.valor();
```
