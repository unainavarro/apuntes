<h1 align="center">Entrada Principal</h1> 

<h2>📑 Contenido</h2> 

- [Entrada Principal](#entrada-principal)
- [Ejecutar sin este método](#ejecutar-sin-este-método)
- [Publico y Estático](#publico-y-estático)

## Entrada Principal

El método ``public static void main(String[] args)`` es el punto de entrada principal para las aplicaciones Java. Cuando se ejecuta un programa Java, la JVM busca este método y lo invoca automáticamente para comenzar la ejecución del programa. Los argumentos pasados al programa desde la línea de comandos se pueden acceder a través del parámetro args.

Breve explicación de cada parte de este método:

1. **public:** Es un modificador de acceso que indica que el método main es accesible desde cualquier parte de la aplicación. Esto significa que puede ser llamado desde otras clases o paquetes.

2. **static:** Es una palabra clave que indica que el método main pertenece a la clase en sí misma, no a instancias individuales de la clase. Esto significa que el método main puede ser invocado sin necesidad de crear un objeto de la clase que lo contiene.

3. **void:** Es el tipo de retorno del método main. Indica que el método no devuelve ningún valor.

4. **main:** Es el nombre del método. Java busca este método específico cuando se ejecuta un programa Java.

5. **String[] args:** Es el parámetro del método main. Representa un array de cadenas de texto (String) que pueden ser pasadas al programa cuando se ejecuta desde la línea de comandos. El nombre args es una convención, pero podría ser cualquier otro nombre válido.

## Ejecutar sin este método

En teoría, puedes compilar un programa Java sin un método main, pero no podrás ejecutarlo como una aplicación independiente. El método main es el punto de entrada principal para la ejecución de una aplicación Java, por lo que si no lo tienes, no habrá un punto de inicio claro para la ejecución del programa.

Sin el método main, aún puedes tener clases y métodos en tu programa, pero necesitarás otro mecanismo para ejecutarlos. Por ejemplo, podrías tener una clase con un método específico para realizar una acción particular, y luego llamar a ese método desde otro programa Java que tenga un método main. De esta manera, el programa que tiene el método main actuaría como un punto de entrada para ejecutar el código en tu programa.

Sin embargo, para fines prácticos y para ejecutar una aplicación Java de manera independiente, es necesario tener un método main. Es la convención estándar y el punto de entrada esperado por la JVM cuando se inicia una aplicación Java. Por lo tanto, aunque técnicamente podrías crear un programa Java sin un método main, no sería utilizable como una aplicación independiente y no podrías ejecutarlo directamente.

## Publico y Estático

De acuerdo con la especificación del lenguaje, el método main debe ser público y estático para que la JVM pueda encontrar y ejecutar el programa.

Razones clave por las que el método main tiene que ser publico:

- **Accesibilidad:** La JVM necesita poder acceder al método main para iniciar la ejecución del programa. Si el método main fuera privado, la JVM no tendría acceso a él y no podría ejecutar el programa.

- **Punto de entrada público:** El método main sirve como el punto de entrada público para la ejecución de la aplicación Java. Debe ser accesible desde fuera de la clase para que la JVM pueda encontrarlo y comenzar la ejecución del programa.

Razones clave por las que el método main tiene que ser estático:

- **Acceso sin instancia:** Cuando se ejecuta un programa Java, la JVM no crea una instancia de la clase principal que contiene el método main. En su lugar, la JVM invoca directamente el método main desde la clase misma. Para permitir que la JVM llame a un método sin necesidad de una instancia de la clase, el método debe ser estático.

- **Punto de entrada estático:** El método main es el punto de entrada principal para la ejecución de una aplicación Java. Debe estar disponible para su invocación sin necesidad de crear objetos de la clase que lo contiene. Al marcar el método main como estático, se garantiza que pueda ser llamado directamente desde la clase, sin necesidad de crear instancias de la misma.

- **Convención y especificación del lenguaje:** La especificación del lenguaje Java establece que el método main debe ser estático. Esto se debe a la forma en que la JVM está diseñada para buscar y ejecutar el método main como punto de entrada de un programa Java.