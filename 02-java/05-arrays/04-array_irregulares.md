<h1 align="center">Array Irregulares</h1>

<h2>📑 Contenido</h2>

- [Array Irregulares](#array-irregulares)

## Array Irregulares

Un "Jagged Array" (o array irregular) en Java es un tipo de array multidimensional donde las submatrices tienen diferentes longitudes. A diferencia de un array multidimensional regular, donde todas las filas tienen la misma longitud, en un array irregular, cada fila puede tener una longitud diferente.

En un array irregular, cada elemento del array principal es en realidad un array de una dimensión. Estos arrays internos pueden tener diferentes longitudes, lo que los hace "irregulares" en comparación con un array multidimensional regular.

```java
int[][] jaggedArray = {
    {1, 2, 3},
    {4, 5},
    {6, 7, 8, 9}
};
```

> [!NOTE]
>
> Los arrays irregulares son útiles cuando necesitas representar datos que no tienen una estructura regular o cuando las longitudes de las submatrices varían en tu aplicación. Sin embargo, debido a su naturaleza irregular, pueden ser un poco más complicados de manejar en comparación con los arrays multidimensionales regulares.
