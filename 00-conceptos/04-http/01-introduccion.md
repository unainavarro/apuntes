<h1 align="center">Protocolo HTTP</h1>

<h2>📑 Contenido</h2>

- [Protocolo HTTP](#protocolo-http)
- [Estructura del Mensaje:](#estructura-del-mensaje)
- [HTTP vs. HTTPS](#http-vs-https)
  - [HTTP (HyperText Transfer Protocol)](#http-hypertext-transfer-protocol)
  - [HTTPS (HyperText Transfer Protocol Secure)](#https-hypertext-transfer-protocol-secure)
- [Uso de HTTP en Aplicaciones Web](#uso-de-http-en-aplicaciones-web)
  - [Navegadores Web](#navegadores-web)
  - [APIs Web](#apis-web)
  - [Caché](#caché)
  - [Autenticación y Sesiones](#autenticación-y-sesiones)
- [Evolución o Versiones](#evolución-o-versiones)

## Protocolo HTTP

HTTP, o Protocolo de Transferencia de Hipertexto, es el protocolo subyacente que permite la comunicación en la World Wide Web. Es un protocolo basado en el modelo cliente-servidor, donde los navegadores web actúan como clientes y los servidores web almacenan y sirven el contenido web.

## Estructura del Mensaje:

Los mensajes HTTP consisten en una línea de inicio, encabezados y un cuerpo opcional.

- **Solicitud:** Línea de solicitud (método, URI, versión del protocolo), encabezados de solicitud, cuerpo opcional.
- **Respuesta:** Línea de estado (versión del protocolo, código de estado, mensaje de estado), encabezados de respuesta, cuerpo opcional.

## HTTP vs. HTTPS

### HTTP (HyperText Transfer Protocol)

No cifra los datos, lo que significa que la información intercambiada entre el cliente y el servidor puede ser interceptada por terceros.

### HTTPS (HyperText Transfer Protocol Secure)

Cifra los datos utilizando SSL/TLS, proporcionando una capa adicional de seguridad que protege la integridad y confidencialidad de los datos durante la transferencia.

## Uso de HTTP en Aplicaciones Web

### Navegadores Web

Los navegadores envían solicitudes HTTP para recuperar páginas web y otros recursos (imágenes, scripts, etc.) desde los servidores.

### APIs Web

Las APIs RESTful utilizan HTTP como protocolo de comunicación para operaciones CRUD (Create, Read, Update, Delete).

### Caché

HTTP permite el uso de mecanismos de caché para mejorar el rendimiento al almacenar copias de recursos solicitados frecuentemente.

### Autenticación y Sesiones

HTTP puede gestionar autenticación mediante encabezados y mantener sesiones de usuario utilizando cookies.

## Evolución o Versiones

- **HTTP/0.9:** La primera versión del protocolo, muy simple y sin encabezados ni métodos distintos de GET.
- **HTTP/1.0:** Introdujo encabezados de solicitud/respuesta, códigos de estado y métodos adicionales.
- **HTTP/1.1:** Mejora significativa sobre HTTP/1.0, con soporte para conexiones persistentes, pipelining, y nuevos métodos como OPTIONS, PUT y DELETE.
- **HTTP/2:** Introducido para mejorar el rendimiento. Utiliza multiplexación de solicitudes, compresión de encabezados y mejor manejo de conexiones.
- **HTTP/3:** Basado en QUIC (Quick UDP Internet Connections), un protocolo de transporte rápido y confiable basado en UDP, diseñado para mejorar la velocidad y la eficiencia de las conexiones.
