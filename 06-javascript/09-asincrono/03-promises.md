<h1 align="center">Promises</h1>

<h2>📑 Contenido</h2>

- [Promises](#promises)
- [Argumentos](#argumentos)
- [Valores](#valores)
- [Ejemplo](#ejemplo)

## Promises

Una promesa(Promise) en JavaScript es un objeto que representa la eventual finalización o el fracaso de una operación asíncrona.

## Argumentos

- **resolve:** cuando el promise se cumple.
- **reject:** cunado no se cumple.

```js
const promesa = new Promise((resolve, reject) => {
  promesa
    .then((valor) => {
      // hacer algo con el valor
    })
    .catch((error) => {
      // manejar el error
    })
    .finally(() => {
      // hacer algo al final
    });
});
```

## Valores

- **Pending:** En espera.
- **Fulfiled:** Se cumplió.
- **Reject:** Rechazado no se cumple.

## Ejemplo

```js
const authUser = new Promise((resolve, reject) => {
  const auth = true;

  if (auth) {
    resolve("Usuario Autenticado");
  } else {
    reject("No se puede conectar");
  }
});

console.log(authUser);

authUser
  .then(function (respuesta) {
    console.log(respuesta);
  })
  .catch(function (error) {
    console.log(error);
  });
```
