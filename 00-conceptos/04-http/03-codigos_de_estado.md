<h1 align="center">Códigos de estado</h1>

<h2>📑 Contenido</h2>

- [Códigos de estado](#códigos-de-estado)
- [Algunos códigos](#algunos-códigos)
  - [Respuestas informativas (100–199)](#respuestas-informativas-100199)
  - [Respuestas satisfactorias (200–299)](#respuestas-satisfactorias-200299)
  - [Redirecciones (300–399)](#redirecciones-300399)
  - [Errores de los clientes (400–499)](#errores-de-los-clientes-400499)
  - [Errores de los servidores (500–599)](#errores-de-los-servidores-500599)

## Códigos de estado

Los códigos de estado HTTP son respuestas estandarizadas que un servidor web devuelve al cliente para indicar el resultado de una solicitud HTTP. Estos códigos se dividen en cinco categorías principales, cada una representada por un número de tres dígitos donde el primer dígito indica la categoría.

## Algunos códigos

### Respuestas informativas (100–199)

- **100 Continue:** El cliente debe continuar con su solicitud.
- **101 Switching Protocols:** El servidor acepta el cambio de protocolo solicitado por el cliente.

### Respuestas satisfactorias (200–299)

- **200 OK:** La solicitud ha tenido éxito.
- **201 Created:** La solicitud ha sido cumplida y ha resultado en la creación de un nuevo recurso.
- **204 No Content:** La solicitud ha sido procesada con éxito, pero no hay contenido que devolver.

### Redirecciones (300–399)

- **301 Moved Permanently:** El recurso solicitado ha sido movido de forma permanente a una nueva URI.
- **302 Found:** El recurso solicitado reside temporalmente en una URI diferente.
- **304 Not Modified:** El recurso no ha sido modificado desde la última solicitud.

### Errores de los clientes (400–499)

- **400 Bad Request:** El servidor no puede procesar la solicitud debido a un error del cliente.
- **401 Unauthorized:** La solicitud requiere autenticación.
- **403 Forbidden:** El servidor comprende la solicitud, pero se niega a autorizarla.
- **404 Not Found:** El servidor no puede encontrar el recurso solicitado.

- **405 Method Not Allowed:** El método especificado en la solicitud no está permitido para el recurso.

### Errores de los servidores (500–599)

- **500 Internal Server Error:** El servidor encontró una condición inesperada que le impidió cumplir con la solicitud.
- **502 Bad Gateway:** El servidor, actuando como puerta de enlace o proxy, recibió una respuesta inválida del servidor ascendente.
- **503 Service Unavailable:** El servidor no está disponible temporalmente debido a sobrecarga o mantenimiento.
- **504 Gateway Timeout:** El servidor, actuando como puerta de enlace o proxy, no recibió una respuesta a tiempo del servidor ascendente.
