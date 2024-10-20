<h1 align="center">Continue y Break</h1>

<h2>📑 Contenido</h2>

- [Continue y Break](#continue-y-break)
  - [Continue](#continue)
  - [Break](#break)
- [Etiquetas Label](#etiquetas-label)

## Continue y Break

`continue` y `break` son palabras clave utilizadas en estructuras de control de flujo en varios lenguajes de programación, incluyendo JavaScript. Se utilizan para controlar el flujo de ejecución dentro de bucles, como for, while y do...while.

### Continue

La instrucción continue finaliza la ejecución de las instrucciones en la iteración actual del bucle actual o etiquetado, y continúa la ejecución del bucle con la siguiente iteración.

```js
//Iterar del 0-4 saltándose el dos
for (let i = 0; i < 5; i++) {
  if (i === 2) {
    continue; // Omite la iteración actual cuando i es igual a 2
  }
  console.log(i);
}
```

### Break

La instrucción break termina la instrucción current loop o switch y transfiere el control del programa a la instrucción después de la instrucción terminada. También se puede usar para saltar más allá de una declaración etiquetada cuando se usa dentro de esa instrucción etiquetada.

```js
// Itera del 0-4 y se sale si encuentra un 3
for (let i = 0; i < 5; i++) {
  if (i === 3) {
    break; // Sale del bucle cuando i es igual a 3
  }
  console.log(i);
}
//Resultado: 0,1,2  (No imprime el 3)
```

## Etiquetas Label

Las etiquetas se utilizan para identificar un bloque de código y se pueden asociar con las declaraciones break y continue. Permiten especificar a qué bucle o bloque se aplica la declaración break o continue.

```js
//Ejemplo con break
loopExterior: for (let i = 0; i < 3; i++) {
  loopInterior: for (let j = 0; j < 3; j++) {
    if (i === 1 && j === 1) {
      break loopExterior; // Sale del bucle exterior cuando i es igual a 1 y j es igual a 1
    }
    console.log(i, j);
  }
}
/*
Resultado:
0 0
0 1
0 2
1 0
*/

//Ejemplo con continue
loopExterior: for (let i = 0; i < 3; i++) {
  loopInterior: for (let j = 0; j < 3; j++) {
    if (i === 1 && j === 1) {
      continue loopExterior; // Sale del bucle exterior cuando i es igual a 1 y j es igual a 1
    }
    console.log(i, j);
  }
}
/*
Resultado:
0 0
0 1
0 2
1 0
2 0
2 1
2 2
*/
```

> [!NOTE]
>
> El uso de etiquetas es opcional y no es necesario en la mayoría de las situaciones. Sin embargo, pueden ser útiles en casos específicos donde tienes bucles anidados y necesitas controlar el flujo de ejecución de manera más granular.
