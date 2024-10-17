<h1 align="center">Listas</h1>

<h2>📑 Contenido</h2>

- [Listas Ordenadas](#listas-ordenadas)
  - [Cambiar número de inicio](#cambiar-número-de-inicio)
  - [Cambiar el valor](#cambiar-el-valor)
  - [Invertir orden](#invertir-orden)
  - [Cambiar Tipo](#cambiar-tipo)
- [Listas No Ordenadas(Desordenadas)](#listas-no-ordenadasdesordenadas)
  - [Cambiar el símbolo](#cambiar-el-símbolo)
- [Listas de Definiciones](#listas-de-definiciones)
- [Listas Anidadas](#listas-anidadas)
- [Listas de Enlaces](#listas-de-enlaces)

## Listas Ordenadas

Para mostrar listas ordenadas en HTML se utiliza las etiquetas: <br>
`<ol> <li>Elementos<li> </ol>`

```HTML
Ejemplo:
    <ol>
      <li>Elemento-1</li>
      <li>Elemento-2</li>
      <li>Elemento-3</li>
    </ol>

Resultado:
    1.Elemento-1
    2.Elemento-2
    3.Elemento-3
```

### Cambiar número de inicio

Se puede cambiar el número de inicio de las listas ordenadas con el atributo `start="numero"`

```HTML
Ejemplo:
    <ol start="4">
      <li>Elemento-1</li>
      <li>Elemento-2</li>
      <li>Elemento-3</li>
    </ol>

Resultado:
    4.Elemento-1
    5.Elemento-2
    6.Elemento-3
```

### Cambiar el valor

Se puede cambiar el valor concreto de un número en las listas ordenadas con el atributo `value="numero"`

> [!IMPORTANT]
>
> También cambia los números que van después del valor cambiado.

```HTML
Ejemplo:
    <ol>
      <li>Elemento-1</li>
      <li value="44">Elemento-2</li>
      <li>Elemento-3</li>
      <li>Elemento-4</li>
      <li>Elemento-5</li>
    </ol>

Resultado:
    1.Elemento-1
    44.Elemento-2
    45.Elemento-3
    46.Elemento-4
    47.Elemento-5
```

### Invertir orden

Para invertir el orden de las listas(No cambia el orden del contenido) `<ol reversed>`

```HTML
Ejemplo:
    <ol reversed>
      <li>Elemento-1</li>
      <li>Elemento-2</li>
      <li>Elemento-3</li>
    </ol>

Resultado:
    3.Elemento-1
    2.Elemento-2
    1.Elemento-3
```

### Cambiar Tipo

Para cambiar el tipo de orden de una lita ordenada:

- Lista decimales(Por defecto).
- Listas alfabéticas en minúsculas-mayúsculas(a-A).
- Listas de números romanos en minúsculas-mayúsculas(i-I).
- Mediante CSS se puede cambiar más tipos: `list-style-type`
- Mejor asignar el tipo de lista mediante CSS.

```HTML
Ejemplo:
    <ol type="a">
      <li>Elemento-1</li>
      <li>Elemento-2</li>
      <li>Elemento-3</li>
    </ol>

Resultado:
    a.Elemento-1
    b.Elemento-2
    c.Elemento-3
```

## Listas No Ordenadas(Desordenadas)

Para mostrar listas no ordenadas en HTML se utiliza las etiquetas:<br>
`<ul> <li>Elementos<li> </ul>`

```HTML
Ejemplo:
    <ul>
      <li>Elemento-1</li>
      <li>Elemento-2</li>
      <li>Elemento-3</li>
    </ul>

Resultado:
    • Elemento-1
    • Elemento-2
    • Elemento-3
```

### Cambiar el símbolo

Se puede cambiar el símbolo de la lista desordenada:
<br> > `<ul type="square">`

- Por defecto las listas desordenas usan el símbolo de •
- Los 4 tipos mas comunes son:
  - **dist:** Para poner el símbolo por defecto.
  - **circle:** Para poner un símbolo circular.
  - **square:** Para poner un símbolo cuadrado.
  - **none:** Para eliminar la marca.
- Mejor asignar el tipo de lista mediante CSS.

```HTML
Ejemplo:
    <ul type="circle">
      <li>Elemento-1</li>
      <li>Elemento-2</li>
      <li>Elemento-3</li>
    </ul>

Resultado:
    ◌ Elemento-1
    ◌ Elemento-2
    ◌ Elemento-3
```

## Listas de Definiciones

Para mostrar listas de definiciones en HTML se utiliza las etiquetas: <br>
`<dl> <dt>Término<dt> <dd>Definición<dd> </dl>`

```HTML
Ejemplo:
<dl>
  <dt>Término1</dt>
  <dd>Definición 1</dd>

  <dt>Término 2</dt>
  <dd>Definición 2</dd>
</dl>

Resultado:
    Término1
        Definición 1
    Término 2
        Definición 2
```

## Listas Anidadas

Se pueden anidar los diferentes tipos de listas para formar una lista que contenga: listas ordenadas, desordenadas, de definición, con enlaces, imágenes...

```HTML
Ejemplo:
  <ul>
      <li>Elemento 1</li>
      <li>Elemento 2</li>
      <li>
        <ol>
          <li>Elemento 2.1</li>
          <li>Elemento 2.2</li>
        </ol>
      </li>
      <li>Elemento 3</li>
      <dd>
        <dt>Término1</dt>
        <dd>Definición 1</dd>
        <dt>Término 2</dt>
        <dd>Definición 2</dd>
      </dd>
      <li>Elemento 4</li>
    </ul>

Resultado:
    • Elemento 1
    • Elemento 2
        1. Elemento 2.1
        2. Elemento 2.2
    • Elemento 3
    Término1
        Definición 1
    Término 2
        Definición 2
    • Elemento 4
```

## Listas de Enlaces

Este tipo de listas son muy comunes a la hora de crear una navegación para una página web.

```HTML
Ejemplo:
     <ul>
      <li><a href="ruta_del_enlace">Enlace 1</a></li>
      <li><a href="ruta_del_enlace">Enlace 2</a></li>
      <li><a href="ruta_del_enlace">Enlace 3</a></li>
    </ul>
```

Resultado:

- <u>Enlace 1</u>
- <u>Enlace 2</u>
- <u>Enlace 3</u>
