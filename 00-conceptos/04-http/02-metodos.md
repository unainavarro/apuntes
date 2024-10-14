<h1 align="center">Métodos HTTP</h1>

<h2>📑 Contenido</h2>

- [Métodos HTTP](#métodos-http)
- [Importancia de los métodos HTTP](#importancia-de-los-métodos-http)
- [Métodos más comunes](#métodos-más-comunes)
  - [GET](#get)
  - [POST](#post)
  - [PUT](#put)
  - [DELETE](#delete)
  - [PATCH](#patch)
  - [HEAD](#head)
  - [OPTIONS](#options)
  - [CONNECT](#connect)

## Métodos HTTP

Los métodos HTTP, también conocidos como verbos HTTP, son acciones que se pueden realizar sobre los recursos en un servidor web. Cada método tiene un propósito específico y ayuda a definir la intención de la solicitud del cliente.

## Importancia de los métodos HTTP

- **Claridad y Semántica:** Los métodos proporcionan una semántica clara sobre la acción deseada, lo que facilita la comprensión y el mantenimiento del código.
- **Estándares y Convenciones:** Facilitan la interoperabilidad y la conformidad con los estándares web.
- **Seguridad:** Ayudan a definir comportamientos seguros e inseguros, permitiendo una mejor gestión de permisos y accesos.
- **Idempotencia:** Garantiza que ciertas operaciones sean seguras de repetir sin causar efectos no deseados.

> [!NOTE]
>
> La idempotencia significa que siempre se obtiene el mismo resultado cuando se repite todo, o parte, de la serie de peticiones.

## Métodos más comunes

### GET

Solicita un recurso específico del servidor.

- **Usos:** Recuperar datos sin modificar el estado del recurso en el servidor.
- **Idempotente:** Sí (múltiples solicitudes tienen el mismo efecto).
- **Seguro:** Sí (no altera el estado del servidor).
- **Ejemplo:** Solicitar una página web (GET /index.html).

### POST

Envía datos al servidor para crear un nuevo recurso.

- **Usos:** Enviar datos de formularios, subir archivos, crear nuevos registros.
  Idempotente: No (cada solicitud puede crear un nuevo recurso o cambiar el estado del servidor).
- **Seguro:** No.
- **Ejemplo:** Enviar datos de un formulario de registro de usuario (POST /users).

### PUT

Reemplaza un recurso en el servidor con los datos proporcionados.

- **Usos:** Actualizar un recurso existente o crear un recurso si no existe.
- **Idempotente:** Sí (múltiples solicitudes tienen el mismo efecto).
- **Seguro:** No.
- **Ejemplo:** Actualizar un perfil de usuario (PUT /users/123).

### DELETE

Elimina un recurso específico del servidor.

- **Usos:** Borrar un recurso específico.
- **Idempotente:** Sí (múltiples solicitudes tienen el mismo efecto).
- **Seguro:** No.
- **Ejemplo:** Eliminar un artículo (DELETE /articles/123).

### PATCH

Aplica modificaciones parciales a un recurso.

- **Usos:** Actualizar parcialmente un recurso.
- **Idempotente:** Sí (múltiples solicitudes tienen el mismo efecto).
- **Seguro:** No.
- **Ejemplo:** Actualizar parcialmente un perfil de usuario (PATCH /users/123).

### HEAD

Solicita los encabezados de un recurso, sin el cuerpo del recurso.

- **Usos:** Verificar la existencia o la última modificación de un recurso sin descargar el contenido.
- **Idempotente:** Sí (múltiples solicitudes tienen el mismo efecto).
- **Seguro:** Sí (no altera el estado del servidor).
- **Ejemplo:** Obtener encabezados de una página web (HEAD /index.html).

### OPTIONS

Describe las opciones de comunicación disponibles para un recurso.

- **Usos:** Consultar los métodos soportados por un servidor o recurso.
- **Idempotente:** Sí (múltiples solicitudes tienen el mismo efecto).
- **Seguro:** Sí (no altera el estado del servidor).
- **Ejemplo:** Obtener métodos permitidos para un recurso (OPTIONS /users/123).

### CONNECT

Establece un túnel hacia el servidor identificado por el recurso.

- **Usos:** Utilizado principalmente para túneles SSL (HTTPS) a través de proxies HTTP.
- **Idempotente:** No (específico para conexiones de túnel).
- **Seguro:** No.
- **Ejemplo:** Crear un túnel a un servidor (CONNECT example.com:443).
