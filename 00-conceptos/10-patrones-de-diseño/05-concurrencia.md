<h1 align="center">Patrones de Concurrencia</h1>

<h2>📑 Contenido</h2>

- [Patrones de Concurrencia](#patrones-de-concurrencia)

## Patrones de Concurrencia

Los patrones de concurrencia son patrones de diseño que se utilizan para manejar la concurrencia y la sincronización en aplicaciones multi-hilo. Estos patrones proporcionan soluciones a problemas comunes que surgen al diseñar sistemas concurrentes.

## Bloqueo Múltiple (Multiple Locks)

Divide un objeto grande o complejo en varios objetos más pequeños y utiliza un bloqueo diferente para cada uno. Esto reduce la contención en el acceso a los recursos compartidos y mejora el rendimiento en sistemas multi-hilo.

## Bloqueo Jerárquico (Hierarchical Locking)

Establece un orden jerárquico en los bloqueos para evitar la aparición de condiciones de carrera y bloqueos mutuos. Este patrón ayuda a prevenir la inversión de prioridades y la inanición.

## Semáforo (Semaphore)

Controla el acceso a un recurso compartido utilizando un contador entero que se incrementa o decrementa. Los semáforos se utilizan comúnmente para controlar el acceso a recursos limitados y para coordinar actividades entre varios hilos.

## Monitor (Monitor)

Utiliza un bloqueo exclusivo asociado a un recurso compartido para garantizar la exclusión mutua y la sincronización entre los hilos. Los monitores permiten a los hilos esperar y notificar eventos relacionados con el recurso compartido.

## Productor-Consumidor (Producer-Consumer)

Coordina la producción y el consumo de datos entre hilos separados. Utiliza una cola o un buffer compartido para enviar datos desde los productores a los consumidores, garantizando la sincronización entre ellos.

## Barrera (Barrier)

Sincroniza un grupo de hilos para que esperen hasta que todos los hilos alcancen un punto de sincronización común antes de continuar. Esto se utiliza comúnmente para dividir un proceso en varias etapas y sincronizar la ejecución entre ellas.

## Pool de Hilos (Thread Pool)

Gestiona un conjunto predefinido de hilos reutilizables para ejecutar tareas en paralelo. Los pools de hilos reducen el costo de la creación y destrucción de hilos y controlan el número máximo de hilos activos para evitar la sobrecarga del sistema.

## Barrera Cíclica (Cyclic Barrier)

Es similar a la barrera estándar, pero permite que un grupo de hilos se sincronice en puntos de sincronización múltiples a lo largo de la ejecución. Esto se utiliza comúnmente en aplicaciones donde se realizan varias iteraciones de un cálculo complejo.
