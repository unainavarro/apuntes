<h1 align="center">Math</h1>

<h2>📑 Contenido</h2>

- [Math](#math)
- [Métodos importantes](#métodos-importantes)

## Math

La clase Math en Java proporciona un conjunto de métodos estáticos para realizar operaciones matemáticas comunes. **Estos métodos no requieren que se cree una instancia de la clase Math, ya que son métodos estáticos.**

## Métodos importantes

- **abs(x):** Devuelve el valor absoluto de x.

- **ceil(x):** Devuelve el entero más pequeño mayor o igual que x.

- **floor(x):** Devuelve el entero más grande menor o igual que x.

- **round(x):** Devuelve el valor de x redondeado al entero más cercano.

- **max(x, y):** Devuelve el valor más grande de x e y.

- **min(x, y):** Devuelve el valor más pequeño de x e y.

- **sqrt(x):** Devuelve la raíz cuadrada de x.

- **pow(x, y):** Devuelve x elevado a la potencia de y.

- **exp(x):** Devuelve el valor de e elevado a la potencia de x.

- **log(x):** Devuelve el logaritmo natural (base e) de x.

- **sin(x), cos(x), tan(x):** Devuelve el seno, coseno y tangente de x, respectivamente, donde - x está en radianes.

- **asin(x), acos(x), atan(x):** Devuelve el arcoseno, arcocoseno y arcotangente de x, respectivamente, en radianes.

- **toDegrees(x):** Convierte el ángulo x de radianes a grados.

- **toRadians(x):** Convierte el ángulo x de grados a radianes.

```java
double x = 10.5;
double y = -7.3;

double absoluteValue = Math.abs(y); // Devuelve 7.3
double roundedValue = Math.round(x); // Devuelve 11
double squareRoot = Math.sqrt(x); // Devuelve 3.24037034920393
double power = Math.pow(x, 2); // Devuelve 110.25
double sine = Math.sin(Math.toRadians(30)); // Devuelve 0.5 (seno de 30 grados)

System.out.println(absoluteValue);
System.out.println(roundedValue);
System.out.println(squareRoot);
System.out.println(power);
System.out.println(sine);
```
