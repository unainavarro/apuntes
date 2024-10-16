<h1 align="center">Clase File(Ficheros)</h1>

<h2>📑 Contenido</h2>

- [Ficheros](#ficheros)
- [Creación de archivos](#creación-de-archivos)
- [Lectura de archivos](#lectura-de-archivos)
- [Escritura en archivos](#escritura-en-archivos)
- [Eliminación de archivos](#eliminación-de-archivos)
- [Actualización de archivos](#actualización-de-archivos)
- [CRUD](#crud)

## Ficheros

En Java, puedes manejar archivos utilizando las clases del paquete java.io

## Creación de archivos

Para crear un archivo en Java, puedes utilizar la clase File en conjunto con la clase FileOutputStream o FileWriter

```java
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        try {
            File archivo = new File("archivo.txt");
            if (archivo.createNewFile()) {
                System.out.println("Archivo creado: " + archivo.getName());
            } else {
                System.out.println("El archivo ya existe.");
            }
        } catch (IOException e) {
            System.out.println("Ocurrió un error al crear el archivo.");
            e.printStackTrace();
        }
    }
}
```

## Lectura de archivos

Para leer datos desde un archivo en Java, puedes utilizar la clase FileInputStream o FileReader junto con las clases BufferedReader o Scanner.

```java
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        try (BufferedReader br = new BufferedReader(new FileReader("archivo.txt"))) {
            String linea;
            while ((linea = br.readLine()) != null) {
                System.out.println(linea);
            }
        } catch (IOException e) {
            System.out.println("Ocurrió un error al leer el archivo.");
            e.printStackTrace();
        }
    }
}
```

## Escritura en archivos

Para escribir datos en un archivo en Java, puedes utilizar la clase FileOutputStream o FileWriter junto con las clases BufferedWriter o PrintWriter.

```java
import java.io.BufferedWriter;
import java.io.FileWriter;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        try (BufferedWriter bw = new BufferedWriter(new FileWriter("archivo.txt"))) {
            bw.write("Hola, mundo!");
            bw.newLine();
            bw.write("Este es un archivo de texto.");
            System.out.println("Datos escritos en el archivo.");
        } catch (IOException e) {
            System.out.println("Ocurrió un error al escribir en el archivo.");
            e.printStackTrace();
        }
    }
}

```

## Eliminación de archivos

Para eliminar un archivo en Java, puedes utilizar el método delete() de la clase File

```java
import java.io.File;

public class Main {
    public static void main(String[] args) {
        File archivo = new File("archivo.txt");
        if (archivo.delete()) {
            System.out.println("Archivo eliminado: " + archivo.getName());
        } else {
            System.out.println("No se pudo eliminar el archivo.");
        }
    }
}

```

## Actualización de archivos

Para actualizar un archivo en Java, puedes leer el contenido existente, realizar las modificaciones necesarias y luego escribir el contenido actualizado en el archivo.

```java
import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.FileReader;
import java.io.FileWriter;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        try (BufferedReader br = new BufferedReader(new FileReader("archivo.txt"));
             BufferedWriter bw = new BufferedWriter(new FileWriter("archivo.txt", true))) {
            String linea;
            while ((linea = br.readLine()) != null) {
                // Realizar modificaciones necesarias en cada línea
                // Por ejemplo, agregar una nueva línea al final del archivo
                bw.write("\nNueva línea agregada");
            }
        } catch (IOException e) {
            System.out.println("Ocurrió un error al actualizar el archivo.");
            e.printStackTrace();
        }
    }
}

```

## CRUD

Para implementar un CRUD (Crear, Leer, Actualizar, Eliminar) de un archivo en Java, puedes seguir los pasos que te mencioné anteriormente y combinarlos para cada operación CRUD específica

```java
import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.File;
import java.io.FileReader;
import java.io.FileWriter;
import java.io.IOException;

public class FicheroCRUD {

    // Método para crear un nuevo registro en el archivo
    public static void crearRegistro(String nombreArchivo, String nuevoRegistro) {
        try (BufferedWriter bw = new BufferedWriter(new FileWriter(nombreArchivo, true))) {
            bw.write(nuevoRegistro);
            bw.newLine();
            System.out.println("Registro creado exitosamente.");
        } catch (IOException e) {
            System.out.println("Ocurrió un error al crear el registro.");
            e.printStackTrace();
        }
    }

    // Método para leer todos los registros del archivo
    public static void leerRegistros(String nombreArchivo) {
        try (BufferedReader br = new BufferedReader(new FileReader(nombreArchivo))) {
            String linea;
            System.out.println("Registros en el archivo:");
            while ((linea = br.readLine()) != null) {
                System.out.println(linea);
            }
        } catch (IOException e) {
            System.out.println("Ocurrió un error al leer el archivo.");
            e.printStackTrace();
        }
    }

    // Método para actualizar un registro en el archivo
    public static void actualizarRegistro(String nombreArchivo, String registroExistente, String nuevoRegistro) {
        try (BufferedReader br = new BufferedReader(new FileReader(nombreArchivo));
             BufferedWriter bw = new BufferedWriter(new FileWriter("temp.txt"))) {
            String linea;
            while ((linea = br.readLine()) != null) {
                if (linea.equals(registroExistente)) {
                    bw.write(nuevoRegistro);
                } else {
                    bw.write(linea);
                }
                bw.newLine();
            }
            System.out.println("Registro actualizado exitosamente.");
        } catch (IOException e) {
            System.out.println("Ocurrió un error al actualizar el registro.");
            e.printStackTrace();
        }

        // Renombrar el archivo temporal al nombre original
        File archivoOriginal = new File(nombreArchivo);
        File archivoTemporal = new File("temp.txt");
        archivoTemporal.renameTo(archivoOriginal);
    }

    // Método para eliminar un registro del archivo
    public static void eliminarRegistro(String nombreArchivo, String registroAEliminar) {
        try (BufferedReader br = new BufferedReader(new FileReader(nombreArchivo));
             BufferedWriter bw = new BufferedWriter(new FileWriter("temp.txt"))) {
            String linea;
            while ((linea = br.readLine()) != null) {
                if (!linea.equals(registroAEliminar)) {
                    bw.write(linea);
                    bw.newLine();
                }
            }
            System.out.println("Registro eliminado exitosamente.");
        } catch (IOException e) {
            System.out.println("Ocurrió un error al eliminar el registro.");
            e.printStackTrace();
        }

        // Renombrar el archivo temporal al nombre original
        File archivoOriginal = new File(nombreArchivo);
        File archivoTemporal = new File("temp.txt");
        archivoTemporal.renameTo(archivoOriginal);
    }

    public static void main(String[] args) {
        String nombreArchivo = "datos.txt";

        // Crear un nuevo registro
        String nuevoRegistro = "Nuevo registro";
        crearRegistro(nombreArchivo, nuevoRegistro);

        // Leer todos los registros del archivo
        leerRegistros(nombreArchivo);

        // Actualizar un registro existente
        String registroExistente = "Registro existente";
        String nuevoRegistroActualizado = "Registro actualizado";
        actualizarRegistro(nombreArchivo, registroExistente, nuevoRegistroActualizado);

        // Leer todos los registros del archivo después de la actualización
        leerRegistros(nombreArchivo);

        // Eliminar un registro del archivo
        String registroAEliminar = "Registro a eliminar";
        eliminarRegistro(nombreArchivo, registroAEliminar);

        // Leer todos los registros del archivo después de la eliminación
        leerRegistros(nombreArchivo);
    }
}
```
