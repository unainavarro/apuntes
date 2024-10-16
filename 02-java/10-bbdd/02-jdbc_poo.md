<h1 align="center">JDBC con POO</h1>

<h2>📑 Contenido</h2>

- [JDBC con POO](#jdbc-con-poo)
- [Ejemplo básico](#ejemplo-básico)

## JDBC con POO

El uso de JDBC (Java Database Connectivity) con Programación Orientada a Objetos (POO) implica organizar y estructurar tu código Java de manera que utilice los principios de la POO para interactuar con la base de datos.

## Ejemplo básico

Supongamos que tienes una clase llamada DatabaseManager que se encarga de gestionar la conexión a la base de datos y ejecutar consultas. Esta clase podría tener métodos para conectar, desconectar y ejecutar consultas SQL.

```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

public class DatabaseManager {
    private Connection connection;

    // Método para conectar a la base de datos
    public void connect(String url, String user, String password) throws SQLException {
        connection = DriverManager.getConnection(url, user, password);
    }

    // Método para desconectar de la base de datos
    public void disconnect() throws SQLException {
        if (connection != null && !connection.isClosed()) {
            connection.close();
        }
    }

    // Método para ejecutar una consulta SQL
    public ResultSet executeQuery(String sql) throws SQLException {
        Statement statement = connection.createStatement();
        return statement.executeQuery(sql);
    }

    // Otros métodos para ejecutar actualizaciones, inserciones, etc.
}
```

Luego, puedes tener otras clases que representen entidades en tu base de datos, como User, Product, etc. Estas clases pueden tener métodos para manipular los datos de esas entidades.

```java
public class User {
    private int id;
    private String username;
    private String password;

    // Constructor, getters y setters
}
```

Finalmente, puedes tener una clase Main donde creas una instancia de DatabaseManager y utilizas sus métodos junto con los objetos de tus entidades para interactuar con la base de datos.

```java
import java.sql.SQLException;

public class Main {
    public static void main(String[] args) {
        DatabaseManager dbManager = new DatabaseManager();

        try {
            // Conectar a la base de datos
            dbManager.connect("jdbc:mysql://localhost:3306/mydatabase", "username", "password");

            // Ejemplo de consulta SQL
            ResultSet resultSet = dbManager.executeQuery("SELECT * FROM users");

            // Procesar los resultados
            while (resultSet.next()) {
                int id = resultSet.getInt("id");
                String username = resultSet.getString("username");
                String password = resultSet.getString("password");

                // Crear objeto User con los datos obtenidos
                User user = new User();
                user.setId(id);
                user.setUsername(username);
                user.setPassword(password);

                // Hacer algo con el objeto User (por ejemplo, imprimirlo)
                System.out.println(user);
            }

            // Desconectar de la base de datos
            dbManager.disconnect();
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
}
```
