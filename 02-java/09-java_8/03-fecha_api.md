<h1 align="center">Fechas</h1>

<h2>📑 Contenido</h2>

- [Fechas](#fechas)
- [LocalDate](#localdate)
- [LocalTime](#localtime)
- [LocalDateTime](#localdatetime)
- [ZonedDateTime](#zoneddatetime)
- [Duration y Period](#duration-y-period)
- [Formateo y Análisis](#formateo-y-análisis)

## Fechas

En Java 8, se introdujo un nuevo API de fecha y hora en el paquete java.time, que proporciona clases para manejar fechas, horas, períodos y duraciones. Este nuevo API reemplaza a las clases Date, Calendar y SimpleDateFormat, que eran propensas a errores y difíciles de usar.

## LocalDate

La clase LocalDate representa una fecha sin referencia a una zona horaria específica. Puedes crear instancias de LocalDate para representar fechas como "2024-05-09".

```java
LocalDate fechaActual = LocalDate.now();
LocalDate fechaEspecifica = LocalDate.of(2024, 5, 9);
```

## LocalTime

La clase LocalTime representa una hora sin referencia a una fecha específica ni a una zona horaria. Puedes crear instancias de LocalTime para representar horas como "10:15:30".

```java
LocalTime horaActual = LocalTime.now();
LocalTime horaEspecifica = LocalTime.of(10, 15, 30);
```

## LocalDateTime

La clase LocalDateTime combina una fecha y una hora, sin referencia a una zona horaria específica. Puedes crear instancias de LocalDateTime para representar fechas y horas como "2024-05-09T10:15:30".

```java
LocalDateTime fechaHoraActual = LocalDateTime.now();
LocalDateTime fechaHoraEspecifica = LocalDateTime.of(2024, 5, 9, 10, 15, 30);
```

## ZonedDateTime

La clase ZonedDateTime representa una fecha y hora con referencia a una zona horaria específica. Puedes crear instancias de ZonedDateTime para representar fechas y horas con información de zona horaria.

```java
ZoneId zonaHoraria = ZoneId.of("Europe/Madrid");
ZonedDateTime fechaHoraZona = ZonedDateTime.of(2024, 5, 9, 10, 15, 30, 0, zonaHoraria);
```

## Duration y Period

Las clases Duration y Period representan duraciones y períodos respectivamente. Duration se utiliza para representar una cantidad de tiempo en términos de segundos y fracciones de segundo, mientras que Period se utiliza para representar una cantidad de tiempo en términos de años, meses y días.

```java
Duration duracion = Duration.ofMinutes(30);
Period periodo = Period.ofDays(7);
```

## Formateo y Análisis

Puedes formatear y analizar fechas y horas utilizando la clase DateTimeFormatter. Esto te permite convertir objetos LocalDate, LocalTime o LocalDateTime en cadenas de texto y viceversa

```java
DateTimeFormatter formateador = DateTimeFormatter.ofPattern("dd/MM/yyyy");
String fechaFormateada = fechaActual.format(formateador);
LocalDate fechaAnalizada = LocalDate.parse("09/05/2024", formateador);
```
