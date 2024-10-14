<h1 align="center">Tipos de Algoritmos</h1>

<h2>📑 Contenido</h2>

- [Tipos de Algoritmos](#tipos-de-algoritmos)
- [Algoritmos de clasificación](#algoritmos-de-clasificación)
  - [Bubble Sort](#bubble-sort)
  - [Insertion Sort](#insertion-sort)
  - [Selection Sort](#selection-sort)
  - [Merge Sort](#merge-sort)
  - [Quick Sort](#quick-sort)
  - [Heap Sort](#heap-sort)
  - [Radix Sort](#radix-sort)
- [Algoritmos de búsqueda](#algoritmos-de-búsqueda)
  - [Búsqueda lineal (Sequential Search)](#búsqueda-lineal-sequential-search)
  - [Búsqueda binaria (Binary Search)](#búsqueda-binaria-binary-search)
  - [Búsqueda de salto (Jump Search)](#búsqueda-de-salto-jump-search)
  - [Búsqueda por interpolación (Interpolation Search)](#búsqueda-por-interpolación-interpolation-search)
  - [Búsqueda por hash (Hash Search)](#búsqueda-por-hash-hash-search)
- [Algoritmos de Ordenamiento](#algoritmos-de-ordenamiento)
  - [Algoritmos de Ordenamiento Eficientes](#algoritmos-de-ordenamiento-eficientes)
  - [Algoritmos de Ordenamiento Externo](#algoritmos-de-ordenamiento-externo)
- [Algoritmos de Grafos](#algoritmos-de-grafos)
  - [Algoritmos de Recorrido de Grafos](#algoritmos-de-recorrido-de-grafos)
  - [Algoritmos de Flujo Máximo](#algoritmos-de-flujo-máximo)
- [Algoritmos de Combinatoria](#algoritmos-de-combinatoria)
  - [Algoritmos de Generación de Permutaciones y Combinaciones](#algoritmos-de-generación-de-permutaciones-y-combinaciones)
  - [Algoritmos de Ramificación y Poda](#algoritmos-de-ramificación-y-poda)
- [Algoritmos de Optimización](#algoritmos-de-optimización)
  - [Algoritmos Genéticos](#algoritmos-genéticos)
  - [Algoritmos de Recocido Simulado](#algoritmos-de-recocido-simulado)
- [Algoritmos de Criptografía](#algoritmos-de-criptografía)
  - [Algoritmos de Cifrado](#algoritmos-de-cifrado)
  - [Algoritmos de Hashing](#algoritmos-de-hashing)

## Tipos de Algoritmos

Hay una amplia variedad de algoritmos en el campo de la informática, cada uno diseñado para resolver diferentes tipos de problemas.

## Algoritmos de clasificación

Los algoritmos de clasificación son algoritmos que organizan un conjunto de elementos en un orden específico, generalmente en orden ascendente o descendente según un criterio definido.

### Bubble Sort

Este algoritmo compara pares de elementos adyacentes y los intercambia si están en el orden incorrecto. Continúa este proceso hasta que la lista esté ordenada. Es sencillo pero no eficiente para grandes conjuntos de datos.

### Insertion Sort

En este algoritmo, se construye una lista ordenada de elementos uno a uno, insertando cada uno en su lugar correcto en la lista ordenada anteriormente.

### Selection Sort

Este algoritmo divide la lista en dos partes: una parte ordenada y una parte desordenada. Encuentra repetidamente el elemento mínimo de la parte desordenada y lo coloca al final de la parte ordenada.

### Merge Sort

Es un algoritmo de tipo divide y vencerás. Divide repetidamente la lista en mitades hasta que cada mitad tenga un solo elemento. Luego fusiona las mitades de manera ordenada.

### Quick Sort

También es un algoritmo de tipo divide y vencerás. Elige un elemento como pivote y organiza los otros elementos alrededor del pivote, de manera que los elementos menores que el pivote estén a su izquierda y los elementos mayores estén a su derecha. Luego, aplica recursivamente el mismo proceso a las sublistas generadas por el pivote.

### Heap Sort

Utiliza una estructura de datos llamada heap para organizar los elementos. Construye un heap a partir de la lista de elementos y luego extrae repetidamente el elemento máximo (en un heap máximo) o el elemento mínimo (en un heap mínimo) hasta que la lista esté vacía.

### Radix Sort

Este algoritmo clasifica los elementos basándose en dígitos individuales. Comienza ordenando los elementos por su dígito menos significativo y luego repite este proceso para dígitos más significativos hasta que todos los dígitos hayan sido considerados.

## Algoritmos de búsqueda

Los algoritmos de búsqueda son utilizados para encontrar un elemento particular dentro de un conjunto de datos.

### Búsqueda lineal (Sequential Search)

Este es el método más simple de búsqueda. Consiste en recorrer secuencialmente todos los elementos del conjunto de datos hasta encontrar el elemento buscado o hasta que se recorre toda la lista sin encontrarlo. La complejidad temporal de este algoritmo es O(n), donde n es el número de elementos en la lista.

### Búsqueda binaria (Binary Search)

Este algoritmo solo funciona en listas ordenadas. Compara el elemento buscado con el elemento central de la lista y descarta la mitad de la lista en la que el elemento buscado no puede estar presente. Repite este proceso hasta encontrar el elemento o hasta que la lista se reduzca a cero. La complejidad temporal de este algoritmo es O(log n), donde n es el número de elementos en la lista.

### Búsqueda de salto (Jump Search)

Similar a la búsqueda binaria, pero en lugar de dividir la lista por la mitad, este algoritmo salta de manera uniforme a través de los elementos de la lista, reduciendo gradualmente la cantidad de elementos a revisar. La complejidad temporal de este algoritmo es también O(sqrt(n)).

### Búsqueda por interpolación (Interpolation Search)

Funciona mejor en listas uniformemente distribuidas. Estima la posición del elemento buscado en función de su valor y luego realiza una búsqueda binaria ajustada en esa ubicación estimada. La complejidad temporal promedio de este algoritmo es O(log log n), pero en el peor caso puede ser O(n).

### Búsqueda por hash (Hash Search)

Este método utiliza una función de hash para mapear claves de búsqueda a índices de una tabla hash. La búsqueda se realiza calculando el hash de la clave de búsqueda y accediendo directamente al índice correspondiente en la tabla hash. La complejidad temporal de este algoritmo depende en gran medida de la calidad de la función de hash y del factor de carga de la tabla hash.

## Algoritmos de Ordenamiento

### Algoritmos de Ordenamiento Eficientes

Además de los algoritmos de clasificación básicos (como el de inserción, selección y burbuja), existen algoritmos más eficientes como Quicksort, Mergesort, Heapsort, entre otros.

### Algoritmos de Ordenamiento Externo

Estos algoritmos están diseñados para ordenar grandes conjuntos de datos almacenados fuera de la memoria principal, como Merge sort externo.

## Algoritmos de Grafos

### Algoritmos de Recorrido de Grafos

Además de DFS y BFS, hay otros algoritmos como Dijkstra (para encontrar el camino más corto en un grafo ponderado), A\* (para búsqueda de caminos en un grafo) y Floyd-Warshall (para encontrar todos los caminos más cortos entre todos los pares de nodos en un grafo).

### Algoritmos de Flujo Máximo

Algoritmos como Ford-Fulkerson y Edmonds-Karp, utilizados para encontrar el flujo máximo en una red de flujo.

## Algoritmos de Combinatoria

### Algoritmos de Generación de Permutaciones y Combinaciones

Estos algoritmos generan todas las posibles combinaciones y permutaciones de un conjunto dado de elementos.

### Algoritmos de Ramificación y Poda

Utilizados para encontrar soluciones óptimas a problemas de búsqueda exhaustiva, como el problema del viajante de comercio.

## Algoritmos de Optimización

### Algoritmos Genéticos

Inspirados en la evolución biológica, se utilizan para encontrar soluciones óptimas a problemas de optimización.

### Algoritmos de Recocido Simulado

Un método probabilístico para encontrar soluciones aproximadas a problemas de optimización.

## Algoritmos de Criptografía

### Algoritmos de Cifrado

Como AES (Estándar de Cifrado Avanzado) y RSA (Criptografía de Clave Pública), utilizados para cifrar y proteger datos.

### Algoritmos de Hashing

Como SHA-256, utilizados para generar resúmenes de datos que representan de manera única una entrada de datos.
