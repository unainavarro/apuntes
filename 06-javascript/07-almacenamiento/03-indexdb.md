<h1 align="center">IndexDB</h1>

<h2>📑 Contenido</h2>

- [IndexDB](#indexdb)
- [Operaciones básicas](#operaciones-básicas)
  - [Crear base de datos](#crear-base-de-datos)
  - [Crear almacenes de objetos](#crear-almacenes-de-objetos)
  - [Agregar datos](#agregar-datos)
  - [Recuperar datos](#recuperar-datos)

## IndexDB

IndexDB es una API de JavaScript para almacenar y recuperar grandes cantidades de datos estructurados en el navegador del usuario. Proporciona una forma poderosa y eficiente de almacenar datos del lado del cliente, lo que permite a las aplicaciones web trabajar con grandes cantidades de datos de manera eficiente, incluso cuando no hay conexión a Internet.

IndexedDB utiliza una base de datos de tipo NoSQL que almacena pares clave-valor, donde la clave y el valor pueden ser objetos JavaScript complejos. IndexedDB utiliza transacciones para realizar operaciones de lectura y escritura, lo que garantiza la consistencia de los datos.

## Operaciones básicas

### Crear base de datos

```js
const request = window.indexedDB.open("miBaseDeDatos", 1);

request.onerror = function (event) {
  console.error("Error al abrir la base de datos:", event.target.error);
};

request.onsuccess = function (event) {
  const db = event.target.result;
  console.log("Base de datos abierta correctamente:", db);
};
```

### Crear almacenes de objetos

```js
request.onupgradeneeded = function (event) {
  const db = event.target.result;
  const objectStore = db.createObjectStore("miAlmacen", { keyPath: "id" });
  console.log("Almacen de objetos creado:", objectStore);
};
```

### Agregar datos

```js
request.onsuccess = function (event) {
  const db = event.target.result;
  const transaction = db.transaction(["miAlmacen"], "readwrite");
  const objectStore = transaction.objectStore("miAlmacen");
  const data = { id: 1, nombre: "Juan", edad: 30 };
  const request = objectStore.add(data);

  request.onsuccess = function (event) {
    console.log("Datos agregados correctamente:", data);
  };
};
```

### Recuperar datos

```js
request.onsuccess = function (event) {
  const db = event.target.result;
  const transaction = db.transaction(["miAlmacen"], "readonly");
  const objectStore = transaction.objectStore("miAlmacen");
  const request = objectStore.get(1);

  request.onsuccess = function (event) {
    const data = event.target.result;
    console.log("Datos recuperados:", data);
  };
};
```
