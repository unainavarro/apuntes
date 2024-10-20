<h1 align="center">Cookies</h1>

<h2>📑 Contenido</h2>

- [Cookies](#cookies)
  - [Ejemplo](#ejemplo)
  - [Opciones adicionales](#opciones-adicionales)

## Cookies

Las cookies son pequeños fragmentos de datos que los sitios web pueden almacenar en el navegador del usuario. Estos datos se envían entre el navegador y el servidor web en cada solicitud y respuesta HTTP, lo que permite que los sitios web almacenen información sobre la actividad del usuario, como preferencias, estado de la sesión, datos de inicio de sesión, entre otros.

En JavaScript, puedes trabajar con cookies utilizando el objeto document.cookie. Este objeto proporciona métodos para leer, escribir y eliminar cookies.

> [!IMPORTANT]
>
> Es importante tener en cuenta que el objeto document.cookie almacena todas las cookies como una sola cadena separada por punto y coma (;). Cada cookie está representada por un par clave-valor, y las cookies individuales están separadas por punto y coma.

Las cookies tienen limitaciones, como un tamaño máximo y restricciones de privacidad. Por ejemplo, las cookies solo pueden almacenar hasta 4 KB de datos y los navegadores pueden tener configuraciones que limiten el uso de cookies de terceros por razones de privacidad y seguridad. Además, el acceso a cookies está sujeto a las políticas de privacidad del navegador y del usuario.

### Ejemplo

```js
// Crear Cookies
document.cookie =
  "nombre=valor; expires=fecha; path=path; domain=dominio; secure";
document.cookie = "usuario=juan";

// Obtener Valor
const cookies = document.cookie.split("; ");
for (const cookie of cookies) {
  const [nombre, valor] = cookie.split("=");
  if (nombre === "usuario") {
    console.log("El valor de la cookie 'usuario' es:", valor);
    break;
  }
}

// Eliminar Cookies
document.cookie = "usuario=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";
```

### Opciones adicionales

Además del nombre y el valor de la cookie, las cookies pueden tener varias opciones adicionales que controlan su comportamiento.

- **Expires (Caducidad):** Esta opción indica cuándo la cookie expirará y dejará de ser válida. Puedes establecerla usando una fecha y hora en formato UTC.

  ```js
  document.cookie = "nombre=valor; expires=Thu, 01 Jan 2023 00:00:00 UTC";
  ```

- **Max-Age:** Esta opción especifica la vida útil de la cookie en segundos desde el momento en que se crea (en lugar de una fecha de expiración específica).

  ```js
  document.cookie = "nombre=valor; max-age=3600"; // La cookie expirará después de una hora
  ```

- **Path:** Esta opción indica el alcance de la cookie dentro de la ruta del URL especificado. Por defecto, la cookie es válida para el directorio actual del documento que la ha configurado y para todos los subdirectorios. Puedes especificar una ruta diferente para limitar el alcance de la cookie.

  ```js
  document.cookie = "nombre=valor; path=/ruta";
  ```

- **Domain:** Esta opción especifica el dominio al que se enviará la cookie. Por defecto, la cookie se envía solo al dominio del sitio que la ha configurado. Puedes usar esta opción para permitir que la cookie se envíe a subdominios o dominios específicos.

  ```js
  document.cookie = "nombre=valor; domain=.tusitio.com";
  ```

- **Secure:** Esta opción indica que la cookie solo se enviará a través de una conexión HTTPS segura. Por defecto, las cookies se envían tanto a través de conexiones seguras como no seguras (HTTP). Puedes usar esta opción para asegurar que la cookie solo se envíe a través de conexiones seguras.

  ```js
  document.cookie = "nombre=valor; secure";
  ```

> [!CAUTION]
>
> No todas las opciones de las cookies son compatibles con todos los navegadores, y algunas opciones pueden ser ignoradas o ajustadas automáticamente por el navegador. Además, las opciones de las cookies pueden tener implicaciones importantes en la privacidad y seguridad del usuario, así que asegúrate de entender cómo y cuándo utilizarlas de manera apropiada.
