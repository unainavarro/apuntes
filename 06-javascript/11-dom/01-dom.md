<h1 align="center">DOM</h1>

<h2>📑 Contenido</h2>

- [DOM](#dom)
- [Acceso a los nodos](#acceso-a-los-nodos)
- [Atajos](#atajos)
- [Acceder a nodos a partir de otros:](#acceder-a-nodos-a-partir-de-otros)
- [Ejemplos](#ejemplos)
- [HTML](#html)

## DOM

> El DOM es una estructura en árbol que representa todos los elementos HTML de la página y sus atributos.
> Todo lo que contiene la página se representa como nodos del árbol
> y mediante el DOM podemos acceder a cada nodo, modificarlo, eliminarlo o añadir nuevos nodos
> de forma que cambiamos dinámicamente la página mostrada al usuario.
> La raíz del árbol DOM es document y de este nodo cuelgan el resto de elementos HTML.
>
> Cada etiqueta HTML suele originar 2 nodos:
>
> **Element:** correspondiente a la etiqueta
>
> **Text:** correspondiente a su contenido (lo que hay entre la etiqueta y su par de cierre)

## Acceso a los nodos

- **.getElementById(id):** devuelve el nodo con la id pasada.
- **.getElementsByClassName(clase)** Devuelve una colección con todos los nodos de la clase indicada.
- **.getElementsByTagName(etiqueta)** Devuelve una colección con todos los nodos de la etiqueta.
- **.querySelector(selector)** Devuelve el primer nodo seleccionad por el selector CSS indicado.
- **.querySelectorAll(selector)** Devuelve una colección con todos los nodos seleccionados por el selector CSS indicado.

## Atajos

- **document.documentElement:** devuelve el nodo del elemento `<html>`
- **document.head:** devuelve el nodo del elemento `<head>`
- **document.body:** devuelve el nodo del elemento `<body>`
- **document.title:** devuelve el nodo del elemento `<title>`
- **document.link:** devuelve una colección con todos los hiperenlaces del documento
- **document.anchor:** devuelve una colección con todas las anclas del documento
- **document.forms:** devuelve una colección con todos los formularios del documento
- **document.images:** devuelve una colección con todas las imágenes del documento
- **document.scripts:** devuelve una colección con todos los scripts del documento

## Acceder a nodos a partir de otros:

- **elemento.parentElement:** devuelve el elemento padre de elemento
- **elemento.children:** devuelve la colección con todos los elementos hijo de elemento (sólo elementos HTML, no comentarios ni nodos de tipo texto)
- **elemento.childNodes:** devuelve la colección con todos los hijos de elemento, incluyendo comentarios y nodos de tipo texto por lo que no suele utilizarse
- **elemento.firstElementChild:** devuelve el elemento HTML que es el primer hijo de elemento
- **elemento.firstChild:** devuelve el nodo que es el primer hijo de elemento (incluyendo nodos de tipo texto o comentarios)
- **elemento.lastElementChild, elemento.lastChild:** igual pero con el último hijo
- **elemento.nextElementSibling:** devuelve el elemento HTML que es el siguiente hermano de elemento
- **elemento.nextSibling:** devuelve el nodo que es el siguiente hermano de elemento (incluyendo nodos de tipo texto o comentarios)
- **elemento.previousElementSibling, elemento.previousSibling:** igual pero con el hermano anterior
- **elemento.hasChildNodes:** indica si elemento tiene o no nodos hijos
- **elemento.childElementCount:** devuelve el nº de nodos hijo de elemento

## Ejemplos

```js
window.addEventListener("load", inicio);

function inicio() {
  document.getElementById("texto").addEventListener("click", cambiarTexto);
  document.getElementById("clase").addEventListener("click", cambiarClase);
  document
    .getElementById("eliminarClase")
    .addEventListener("click", eliminarClase);
  document.getElementById("lista").addEventListener("click", cambiarLista);

  function cambiarTexto() {
    document.getElementById("parrafo1").innerHTML = "Texto modificado";
    document.getElementsByTagName("p")[1].style.color = "pink";
    document.getElementsByClassName("parrafo3")[0].style.fontSize = "2rem";
  }

  function cambiarClase() {
    document.getElementById("parrafo1").setAttribute("class", "nuevaClase");
    //document.getElementById("parrafo2").className("nuevaClase");
    //document.getElementsByClassName("parrafo3")[0].setAttribute("title","Parrafo3");
  }

  function eliminarClase() {
    document.getElementById("parrafo1").setAttribute("class", "");
  }

  function cambiarLista() {
    let lista = document.getElementsByTagName("li");

    for (i = 0; i < lista.length; i++) {
      lista[i].innerHTML = "item: " + i;
    }
  }

  //Crear y eliminar elementos

  document
    .getElementById("crearParrafo")
    .addEventListener("click", crearParrafo);
  document.getElementById("eliminar").addEventListener("click", eliminar);

  function crearParrafo() {
    let parrafo = document.createElement("p");
    let texto = document.createTextNode("Texto desde Js");
    parrafo.appendChild(texto);

    document.body.appendChild(parrafo);
  }

  function eliminar() {
    document.body.lastChild.remove();
  }
}
```

## HTML

```html
<div id="wrapper">
  <p id="parrafo1">Texto prueba</p>
  <p id="parrafo2">Texto prueba</p>
  <p class="parrafo3">Texto prueba</p>
</div>

<ul>
  <li>Melón</li>
  <li>Manzana</li>
  <li>Pera</li>
  <li>Piña</li>
</ul>

<hr />

<button id="texto">texto</button>
<button id="clase">clase</button>
<button id="lista">lista</button>
<button id="crearParrafo">crear parrafo</button>
<button id="eliminar">eliminar parrafo</button>
<button id="eliminarClase">eliminar clase</button>
```
