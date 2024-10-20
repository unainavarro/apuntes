<h1 align="center">LocalStorage</h1>

<h2>📑 Contenido</h2>

- [LocalStorage](#localstorage)
- [Guardar Variable](#guardar-variable)
- [Leer Variables](#leer-variables)
- [Guardar JSON](#guardar-json)
- [Leer JSON](#leer-json)
- [Eliminar Elementos](#eliminar-elementos)

## LocalStorage

LocalStorage es una herramienta que se utiliza vía JavaScript, donde podremos manipular nuestros datos almacenados de la forma que estimemos más conveniente1. LocalStorage te permite acceder al objeto local Storage; los datos persisten almacenados entre de las diferentes sesiones de navegación.

## Guardar Variable

```js
localStorage.setItem("color", "rojo");
```

## Leer Variables

```js
console.log(localStorage.getItem("color"));
```

## Guardar JSON

```js
localStorage.setItem("colores", JSON.stringify(["rojo", "azul", "verde"]));
```

## Leer JSON

```js
const colores = JSON.parse(localStorage.getItem("colores"));
console.log("----Iterar Colores----");
for (const c of colores) {
  console.log(c);
}
```

## Eliminar Elementos

```js
localStorage.removeItem("color");

localStorage.clear();
```
