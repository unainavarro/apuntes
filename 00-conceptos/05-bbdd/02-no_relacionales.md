<h1 align="center">No Relacionales (NoSQL)</h1>

<h2>📑 Contenido</h2>

- [No Relacionales (NoSQL)](#no-relacionales-nosql)
- [Características](#características)
- [Tipos de bases de datos NoSQL](#tipos-de-bases-de-datos-nosql)
- [Ventajas de las bases de datos NoSQL](#ventajas-de-las-bases-de-datos-nosql)
- [Desventajas](#desventajas)
- [Casos de uso](#casos-de-uso)

## No Relacionales (NoSQL)

Las bases de datos no relacionales, también conocidas como bases de datos NoSQL, son sistemas de gestión de bases de datos que no siguen el modelo relacional tradicional. Fueron diseñadas para abordar las limitaciones de las bases de datos relacionales en cuanto a escalabilidad, flexibilidad y manejo de datos no estructurados o semi-estructurados. NoSQL significa "Not Only SQL", lo que indica que estos sistemas pueden usar SQL junto con otros métodos de consulta.

## Características

- **Flexibilidad de Esquema:** Las bases de datos NoSQL suelen tener esquemas flexibles que permiten cambios dinámicos en la estructura de los datos sin necesidad de reestructurar la base de datos completa.
  Los datos pueden ser semi-estructurados o no estructurados.
- **Escalabilidad Horizontal:** Diseñadas para escalar horizontalmente a través de múltiples servidores.
  Permiten el manejo eficiente de grandes volúmenes de datos y un alto rendimiento de lectura/escritura.
- **Modelos de Datos Diversos:** No siguen un solo modelo de datos, sino que se adaptan a diferentes tipos de necesidades con varios modelos como documentos, clave-valor, columnares y grafos.
- **Alta Disponibilidad y Tolerancia a Fallos:** Implementan mecanismos robustos para la replicación de datos y la tolerancia a fallos, asegurando alta disponibilidad.

## Tipos de bases de datos NoSQL

- **Bases de Datos de Documentos:**

  - **Estructura:** Almacenan datos en documentos (generalmente JSON, BSON o XML).
  - **Uso:** Aplicaciones web, gestión de contenidos.
  - **Ejemplo:** MongoDB, CouchDB.
  - **Ventajas:** Flexibilidad en el esquema, buena para datos jerárquicos.

- **Bases de Datos Clave-Valor:**

  - **Estructura:** Almacenan datos como pares clave-valor.
  - **Uso:** Caches, sesiones, preferencias de usuario.
  - **Ejemplo:** Redis, DynamoDB.
  - **Ventajas:** Simplicidad, muy rápido para operaciones de lectura/escritura.

- **Bases de Datos Columnares:**

  - **Estructura:** Almacenan datos en columnas en lugar de filas.
  - **Uso:** Análisis de big data, aplicaciones analíticas.
  - **Ejemplo:** Apache Cassandra, HBase.
  - **Ventajas:** Optimización para consultas de lectura/escritura de grandes volúmenes de datos.

- **Bases de Datos de Grafos:**
  - **Estructura:** Almacenan datos en nodos y aristas, representando entidades y sus relaciones.
  - **Uso:** Redes sociales, sistemas de recomendación.
  - **Ejemplo:** Neo4j, OrientDB.
  - **Ventajas:** Excelentes para modelar y consultar datos altamente conectados.

## Ventajas de las bases de datos NoSQL

- **Escalabilidad Horizontal:** Capacidad de escalar fácilmente distribuyendo la carga en múltiples servidores.
- **Alto Rendimiento:** Optimización para operaciones de lectura/escritura rápidas.
- **Flexibilidad del Esquema:** Permite cambios en la estructura de los datos sin interrupciones significativas.
- **Manejo de Datos No Estructurados:** Eficiencia en el almacenamiento y consulta de datos no estructurados o semi-estructurados.

## Desventajas

- **Consistencia Eventual:** Algunas bases de datos NoSQL priorizan la disponibilidad y la partición sobre la consistencia (CAP theorem), lo que puede llevar a retrasos en la propagación de cambios.
- **Falta de Estandarización:** La ausencia de un estándar universal puede complicar la migración entre diferentes sistemas NoSQL.
- **Funcionalidades Limitadas:** Pueden carecer de algunas funcionalidades avanzadas de SQL, como las uniones complejas.

## Casos de uso

- **Grandes Volúmenes de Datos:** Aplicaciones que manejan grandes cantidades de datos y requieren escalabilidad.
- **Datos No Estructurados:** Aplicaciones que manejan datos variados y cambiantes.
- **Requerimientos de Alto Rendimiento:** Sistemas que necesitan bajas latencias en operaciones de lectura/escritura.
- **Analítica y Big Data:** Aplicaciones que requieren análisis de datos a gran escala y almacenamiento distribuido.
