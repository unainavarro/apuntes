<h1 align="center">Expresiones Lambda</h1>

<h2>📑 Contenido</h2>

- [Expresiones Lambda](#expresiones-lambda)
- [Sintaxis](#sintaxis)
- [Interfaces Funcionales](#interfaces-funcionales)
- [Contexto de Tipos](#contexto-de-tipos)
- [Variables Capturadas](#variables-capturadas)
- [Referencias a Métodos](#referencias-a-métodos)

## Expresiones Lambda

Las expresiones lambda en Java 8 son una de las características más destacadas Permiten tratar las funciones como objetos, lo que hace que el código sea más conciso y legible.

## Sintaxis

La sintaxis básica de una expresión lambda se compone de parámetros, una flecha -> y un cuerpo de expresión o un bloque de código

```java
// Expresión lambda sin parámetros y sin retorno
() -> System.out.println("Hola Mundo");

// Expresión lambda con un parámetro y un retorno
(int x) -> x * x;

// Expresión lambda con múltiples parámetros y un retorno
(int x, int y) -> x + y;

// Expresión lambda con un cuerpo de bloque
(String s) -> {
    System.out.println("Hola " + s);
    return s.length();
};
```

## Interfaces Funcionales

Las expresiones lambda se utilizan principalmente en contextos donde se espera una interfaz funcional. Una interfaz funcional es una interfaz que tiene exactamente un método abstracto

```java
// Interfaz funcional con un método abstracto
interface OperacionMatematica {
    int operar(int x, int y);
}

// Uso de una expresión lambda con la interfaz funcional
OperacionMatematica suma = (int x, int y) -> x + y;
System.out.println(suma.operar(5, 3)); // Imprime: 8
```

## Contexto de Tipos

En muchos casos, el compilador de Java puede inferir el tipo de los parámetros de la expresión lambda en función del contexto en el que se utiliza. Por lo tanto, no siempre es necesario especificar explícitamente los tipos de parámetros.

```java
// Interfaz funcional con un método abstracto
interface Saludador {
    String saludar(String nombre);
}

// Uso de una expresión lambda con el tipo de parámetro inferido
Saludador saludo = (nombre) -> "Hola, " + nombre;
System.out.println(saludo.saludar("Juan")); // Imprime: Hola, Juan
```

## Variables Capturadas

Las expresiones lambda pueden acceder a variables locales y parámetros de los métodos que las contienen. Sin embargo, estas variables deben ser efectivamente finales o efectivamente finales (es decir, no deben cambiar su valor después de ser capturadas por la expresión lambda).

```java
String saludo = "Hola";
Saludador saludador = (nombre) -> System.out.println(saludo + ", " + nombre);
```

## Referencias a Métodos

Las expresiones lambda pueden reemplazarse por referencias a métodos cuando la expresión lambda simplemente invoca un método existente.

```java
// Expresión lambda que simplemente invoca el método length() de String
(String s) -> s.length();

// Referencia a método que hace lo mismo
String::length;
```
