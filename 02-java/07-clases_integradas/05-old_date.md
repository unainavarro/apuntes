<h1 align="center">Date(Obsoleto)</h1>

<h2>📑 Contenido</h2>

- [Date](#date)
- [Métodos importantes (obsoletos)](#métodos-importantes-obsoletos)

## Date

En Java, la clase Date proporciona un medio para trabajar con fechas y horas.

> [!CAUTION]
>
> Esta clase ha sido marcada como obsoleta en Java 8 debido a limitaciones en su diseño y funcionalidad. Se recomienda utilizar las clases del paquete java.time introducidas en Java 8 para trabajar con fechas y horas de una manera más robusta y flexible.

**Aun así, aquí tienes información sobre la clase Date por si la encuentras en un proyecto antiguo.**

- La clase Date representa una instantánea específica en el tiempo, con una precisión de milisegundos.

- Aunque la clase Date es útil para representar instantes de tiempo, tiene limitaciones significativas, como la falta de manejo de zona horaria y operaciones inmutables.

- La mayoría de los métodos en la clase Date están marcados como obsoletos y se recomienda evitar su uso en nuevos desarrollos.

## Métodos importantes (obsoletos)

- **Date():** Constructor que inicializa un objeto Date con la fecha y hora actual.

- **getTime():** Devuelve el número de milisegundos desde el 1 de enero de 1970 (Epoch).

- **setTime(long time):** Establece el tiempo representado por este objeto Date.

- **toString():** Devuelve una representación de cadena de este objeto Date.

- **getYear(), getMonth(), getDate():** Métodos para obtener el año, mes y día del objeto Date.

- **setYear(int year), setMonth(int month), setDate(int date):** Métodos para establecer el año, mes y día del objeto Date.

- **after(Date when), before(Date when):** Métodos para comparar si esta fecha es posterior o anterior a otra fecha.

```java
import java.util.Date;

public class Main {
    public static void main(String[] args) {
        Date currentDate = new Date(); // Crea un objeto Date con la fecha y hora actuales
        System.out.println(currentDate);

        long timestamp = currentDate.getTime(); // Obtiene el número de milisegundos desde Epoch
        System.out.println("Timestamp: " + timestamp);

        Date futureDate = new Date(timestamp + 86400000); // Añade un día (86400000 milisegundos) al timestamp
        System.out.println(futureDate);

        boolean isAfter = futureDate.after(currentDate); // Comprueba si futureDate es después de currentDate
        System.out.println("Is futureDate after currentDate? " + isAfter);
    }
}
```
