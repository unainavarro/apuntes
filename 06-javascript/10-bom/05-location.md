<h1 align="center">Location</h1>

<h2>📑 Contenido</h2>

- [Location](#location)
  - [Propiedades y Métodos](#propiedades-y-métodos)
  - [Ejemplos](#ejemplos)

## Location

La propiedad location te permite obtener o modificar la URL de la página actual, así como redirigir el navegador a una nueva página.

### Propiedades y Métodos

- **location.href:** devuelve o cambia el href (URL) de la página actual.
- **location.hostname:** devuelve el nombre de dominio del servidor web.
- **location.pathname:** devuelve la ruta y el nombre de archivo de la página actual.
- **location.protocol:** devuelve el protocolo web utilizado (http: o https:).
- **location.assign():** carga un nuevo documento con la URL especificada.
- **location.reload():** recarga la página actual desde el servidor o desde la caché.
- **location.replace():** reemplaza la página actual por una nueva con la URL especificada.

### Ejemplos

```JS
// Obtener la URL completa de la página actual
console.log(location.href); // por ejemplo, "https://www.bing.com/"

// Cambiar la URL de la página actual
location.href = "https://www.google.com/"; // redirige a Google

// Obtener el nombre de dominio del servidor web
console.log(location.hostname); // por ejemplo, "www.bing.com"

// Obtener la ruta y el nombre de archivo de la página actual
console.log(location.pathname); // por ejemplo, "/search"

// Obtener el protocolo web utilizado
console.log(location.protocol); // por ejemplo, "https:"

// Cargar un nuevo documento con la URL especificada
location.assign("https://www.wikipedia.org/"); // redirige a Wikipedia

// Recargar la página actual desde el servidor
location.reload(true); // fuerza una recarga desde el servidor

// Reemplazar la página actual por una nueva con la URL especificada
location.replace("https://www.youtube.com/"); // redirige a YouTube sin guardar el historial

```
