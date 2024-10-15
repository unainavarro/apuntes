<h1 align="center">RESTful </h1>

<h2>📑 Contenido</h2>

- [RESTful](#restful)
- [Principios de REST](#principios-de-rest)
- [Características de una API RESTful](#características-de-una-api-restful)
- [Beneficios de las APIs RESTful](#beneficios-de-las-apis-restful)

## RESTful

RESTful es un término que se refiere a un estilo arquitectónico para el diseño de servicios web que se basa en los principios de REST (Transferencia de Estado Representacional). REST, desarrollado por Roy Fielding en su tesis doctoral en 2000, propone un conjunto de restricciones y principios para crear servicios web que sean escalables, flexibles y eficientes.

## Principios de REST

**Recursos:** Todo en un sistema REST es considerado como un recurso, que puede ser un objeto, una imagen, un archivo, o cualquier otra cosa.

**Identificadores Únicos:** Cada recurso debe tener un identificador único (URL) que lo identifique de manera unívoca.

**Representaciones:** Los recursos pueden tener múltiples representaciones, como JSON, XML, HTML, etc., que se utilizan para interactuar con el recurso.

**Operaciones sin Estado:** Cada solicitud de cliente al servidor debe contener toda la información necesaria para comprender y procesar la solicitud, lo que significa que el servidor no debe mantener el estado de la sesión del cliente entre solicitudes.

**Interfaz Uniforme:** Define un conjunto uniforme de operaciones (GET, POST, PUT, DELETE) para manipular recursos.

**Sistema Cliente-Servidor:** La arquitectura es cliente-servidor, lo que significa que el cliente y el servidor son independientes entre sí y pueden evolucionar de forma independiente.

**Sin Acoplamiento entre Cliente y Servidor:** El cliente y el servidor son independientes entre sí y no deben conocer detalles de la implementación del otro.

## Características de una API RESTful

**Uso de Métodos HTTP:** Las operaciones CRUD (Crear, Leer, Actualizar, Eliminar) se mapean a los métodos HTTP (GET, POST, PUT, DELETE).

**Nombres de Recursos Significativos:** Los recursos deben tener nombres significativos y representar entidades del dominio de aplicación.

**Utilización de URI (Identificadores de Recursos Uniformes):** Cada recurso debe tener una URI única para identificarlo.

**Formatos de Representación:** Se utilizan formatos de representación estándar, como JSON o XML, para intercambiar datos.

**Estado de la Sesión en el Cliente:** El estado de la sesión, si es necesario, se mantiene en el cliente, no en el servidor.

**Cacheabilidad:** Las respuestas de la API pueden ser cacheadas para mejorar el rendimiento.

## Beneficios de las APIs RESTful

**Simplicidad y Elegancia:** El diseño basado en recursos y la utilización de métodos HTTP simplifican la interacción entre el cliente y el servidor.

**Escalabilidad:** La arquitectura sin estado y la separación entre cliente y servidor facilitan la escalabilidad horizontal.

**Interoperabilidad:** Al utilizar estándares abiertos como HTTP y JSON, las APIs RESTful son interoperables entre diferentes sistemas y plataformas.

**Flexibilidad:** Los clientes pueden interactuar con la API de manera flexible, utilizando diferentes representaciones y formatos de datos.
