<h1 align="center">Math</h1>

<h2>📑 Contenido</h2>

- [Math](#math)
- [Propiedades y Métodos](#propiedades-y-métodos)
  - [PI](#pi)
  - [Números random(pseudoaleatorio) entre 1-10](#números-randompseudoaleatorio-entre-1-10)
  - [Max y Min](#max-y-min)
  - [Redondear](#redondear)
  - [Redondear al alza](#redondear-al-alza)
  - [Redondear a la baja](#redondear-a-la-baja)
  - [Potencia](#potencia)
  - [Valor absoluto](#valor-absoluto)
  - [Devolver la parte entera](#devolver-la-parte-entera)
  - [Devolver el signo del número](#devolver-el-signo-del-número)

## Math

El objeto incorporado Math en JavaScript proporciona un conjunto de constantes y métodos estáticos para realizar operaciones matemáticas comunes. Estas operaciones incluyen funciones trigonométricas, funciones exponenciales, redondeo de números, generación de números aleatorios, entre otras.

## Propiedades y Métodos

### PI

Math.PI: Representa la constante matemática Pi, aproximadamente igual a 3.14159.

```JS
//Pi E LN2 LN10, SQRT1_2 SQRT2
console.log(Math.PI);
```

### Números random(pseudoaleatorio) entre 1-10

Math.random(): Devuelve un número pseudoaleatorio en el rango [0, 1).

```JS
console.log(parseInt(Math.random() * 10 + 1));
```

### Max y Min

Devuelve el número más alto o más bajo.

```JS
console.log(Math.max(2, 3, 1, 5, 10));
console.log(Math.min(2, 3, 1, 5, 10));
```

### Redondear

Math.round(x): Redondea x al número entero más cercano.

```JS
console.log(Math.round(5.78));
```

### Redondear al alza

Math.ceil(x): Redondea x al entero más pequeño mayor o igual que x.

```JS
console.log(Math.ceil(5.78));
```

### Redondear a la baja

Math.floor(x): Redondea x al entero más grande menor o igual que x.

```JS
console.log(Math.floor(5.78));
```

### Potencia

Math.pow(base, exponente): Devuelve la base elevada al exponente.

```JS
console.log(Math.pow(2, 2));
```

### Valor absoluto

Math.abs() se utiliza para devolver el valor absoluto de un número, es decir, su valor numérico sin el signo.

```JS
console.log(Math.abs(-4));
```

### Devolver la parte entera

Math.trunc() se utiliza para eliminar la parte decimal de un número, devolviendo solo la parte entera.

```JS
console.log(Math.trunc(13.745));
```

### Devolver el signo del número

Math.sign() se utiliza para devolver el signo de un número, indicando si el número es positivo, negativo o cero.

Devuelve 1 si el número es positivo, -1 si es negativo, y 0 si es cero.

```JS
console.log("-----Signo----");

console.log(Math.sign(-8));
console.log(Math.sign(0));
console.log(Math.sign(NaN));
console.log(Math.sign(45));
```
