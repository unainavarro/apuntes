<h1 align="center">Ajax</h1>

<h2>📑 Contenido</h2>

- [Introducción](#introducción)
  - [Ejemplo](#ejemplo)
  - [Peticiones Web](#peticiones-web)
  - [Peticiones archivo txt](#peticiones-archivo-txt)

## Introducción

AJAX es un acrónimo de Asynchronous JavaScript And XML, que significa JavaScript y XML asíncronos. AJAX no es un lenguaje de programación, sino una técnica que permite crear aplicaciones web dinámicas e interactivas, usando una combinación de tecnologías existentes.

Con AJAX, puedes enviar y recibir datos del servidor sin tener que recargar la página completa, lo que mejora la velocidad y la experiencia de usuario. También puedes actualizar partes de la página según los datos recibidos, creando interfaces más ricas y responsivas.

Para usar AJAX, necesitas crear un objeto XMLHttpRequest, que es una API integrada en el navegador que permite hacer peticiones HTTP al servidor. Con este objeto, puedes especificar el método, la URL, los datos y las funciones de devolución de llamada que se ejecutarán cuando la petición tenga éxito o falle.

### Ejemplo

```js
// Creamos un objeto XMLHttpRequest
const xhr = new XMLHttpRequest();

// Definimos una función que se ejecutará cuando la petición se complete
xhr.onload = function () {
  // Si el estado de la petición es 200 (OK)
  if (xhr.status === 200) {
    // Mostramos la respuesta del servidor por consola
    console.log(xhr.responseText);
  }
};

// Abrimos la petición con el método GET y la URL del recurso
xhr.open("GET", "datos.txt");

// Enviamos la petición al servidor
xhr.send();
```

### Peticiones Web

```js
let peticion = new XMLHttpRequest();
console.log("Estado inicial de la petición: " + peticion.readyState);

peticion.open("GET", "https://jsonplaceholder.typicode.com/users");
console.log("Estado de la petición tras el 'open': " + peticion.readyState);

peticion.send();
console.log("Petición hecha");

peticion.addEventListener("readystatechange", function () {
  console.log("Estado de la petición: " + peticion.readyState);
  if (peticion.readyState === 4) {
    if (peticion.status === 200) {
      console.log("Datos recibidos:");
      let usuarios = JSON.parse(peticion.responseText); // Convertirmos los datos JSON a un objeto
      console.log(usuarios);
      //Mostrar datos
      document.getElementById("mostrar").addEventListener("click", function () {
        for (usuario of usuarios) {
          let template = `
            <ul>
                <li>-Nombre: ${usuario.name}</li>
                <li>-Alias: ${usuario.username}</li>
                <li>-E-mail ${usuario.email}</li>
                <li>-Web ${usuario.website}</li>
            </ul>
            `;
          document.getElementById("ver").innerHTML += template;
        }
      });
    } else {
      console.log(
        "Error " +
          peticion.status +
          " (" +
          peticion.statusText +
          ") en la petición"
      );
    }
  }
});
console.log("Petición acabada");

//
```

### Peticiones archivo txt

```html
<!-- HTML -->
<button id="cambiar">Cargar</button>
```

```js
//JavaScript

document.getElementById("cambiar").addEventListener("click", cambiarContenido);

function cambiarContenido() {
  const http = new XMLHttpRequest();

  //Comprobar solicitud
  http.onreadystatechange = function () {
    if (this.readyState == 4 && this.status == 200) {
      console.log(this);
      document.getElementById("response").innerHTML = this.responseText;
    }
  };
  //Método, nombre archivo, true/false(Asyn)
  http.open("GET", "Documento de texto.txt", true);
  http.send();
}
```
