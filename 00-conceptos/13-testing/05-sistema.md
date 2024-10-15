<h1 align="center">Pruebas de Sistema (System Testing)</h1>

<h2>📑 Contenido</h2>

- [Pruebas de Sistema (System Testing)](#pruebas-de-sistema-system-testing)
- [Objetivos de las Pruebas de Sistema](#objetivos-de-las-pruebas-de-sistema)
- [Tipos de Pruebas de Sistema](#tipos-de-pruebas-de-sistema)
- [Ventajas de las Pruebas de Sistema](#ventajas-de-las-pruebas-de-sistema)
- [Prácticas Recomendadas para las Pruebas de Sistema](#prácticas-recomendadas-para-las-pruebas-de-sistema)
- [Ejemplo Conceptual (sin código)](#ejemplo-conceptual-sin-código)

## Pruebas de Sistema (System Testing)

Las pruebas de sistema (System Testing) son un tipo de prueba de software que se centra en verificar el sistema completo y validarlo contra los requisitos especificados. Estas pruebas se llevan a cabo después de que todos los componentes o módulos del sistema se han integrado correctamente y se aseguran de que el sistema en su conjunto funcione como se espera. Las pruebas de sistema abarcan una amplia gama de pruebas funcionales y no funcionales.

## Objetivos de las Pruebas de Sistema

**Verificar la funcionalidad del sistema completo:** Asegurar que todas las funcionalidades del sistema funcionen correctamente cuando se combinan e integran todas las partes.

**Validar los requisitos:** Comprobar que el sistema cumple con los requisitos y especificaciones del usuario o cliente.

**Identificar defectos y problemas:** Detectar cualquier defecto o problema en el sistema completo antes de que sea desplegado en producción.

**Evaluar la interacción entre componentes:** Asegurar que los diferentes componentes del sistema interactúen correctamente entre sí.

## Tipos de Pruebas de Sistema

**Pruebas funcionales:** Verifican que las funcionalidades del sistema cumplan con los requisitos especificados.

**Pruebas de rendimiento:** Evalúan la capacidad del sistema para funcionar bajo carga, su capacidad de respuesta y su eficiencia.

**Pruebas de seguridad:** Aseguran que el sistema protege adecuadamente los datos y previene accesos no autorizados.

**Pruebas de usabilidad:** Evalúan la facilidad de uso de la interfaz del sistema y la experiencia del usuario.

**Pruebas de compatibilidad:** Verifican que el sistema funcione correctamente en diferentes entornos, configuraciones de hardware y software, y con otros sistemas.

**Pruebas de recuperación:** Aseguran que el sistema pueda recuperarse adecuadamente de fallos, errores o interrupciones.

**Pruebas de migración:** Verifican que los datos y funcionalidades se trasladen correctamente de un sistema antiguo a uno nuevo.

**Pruebas de instalación:** Aseguran que el sistema se instale correctamente en todos los entornos necesarios.

## Ventajas de las Pruebas de Sistema

**Verificación completa:** Proporcionan una verificación completa del sistema, asegurando que todas las partes funcionen correctamente juntas.

**Detección de defectos:** Identifican defectos y problemas en un contexto que simula más fielmente el entorno de producción.

**Validación de requisitos:** Aseguran que el sistema cumpla con todos los requisitos y especificaciones antes de su despliegue.

**Mejora de la calidad:** Ayudan a entregar un producto final de alta calidad y confiabilidad.

## Prácticas Recomendadas para las Pruebas de Sistema

**Planificación detallada:** Desarrollar un plan de pruebas de sistema detallado que cubra todos los aspectos funcionales y no funcionales del sistema.

**Casos de prueba exhaustivos:** Crear casos de prueba exhaustivos basados en los requisitos y especificaciones del sistema.

**Ambiente de prueba adecuado:** Utilizar un entorno de prueba que replique el entorno de producción lo más fielmente posible.

**Automatización de pruebas:** Automatizar las pruebas de sistema siempre que sea posible para mejorar la eficiencia y cobertura de las pruebas.

**Ejecución de pruebas de regresión:** Realizar pruebas de regresión para asegurar que los cambios en el sistema no introduzcan nuevos defectos.

**Revisión y actualización continua:** Revisar y actualizar los casos de prueba y el plan de pruebas según sea necesario para mantener su relevancia y efectividad.

## Ejemplo Conceptual (sin código)

Supongamos que estamos desarrollando una aplicación de comercio electrónico. Las pruebas de sistema podrían incluir los siguientes casos:

**Proceso de compra:**

- Caso funcional: Verificar que un usuario pueda buscar productos, agregar productos al carrito, realizar el pago y recibir una confirmación de pedido.
- Caso de rendimiento: Evaluar cómo se comporta el sistema cuando 1000 usuarios realizan compras simultáneamente.
- Caso de seguridad: Asegurar que la información de pago se maneje de manera segura y que los datos del usuario estén protegidos.

**Gestión de usuarios:**

- Caso funcional: Verificar que los usuarios puedan registrarse, iniciar sesión, actualizar su perfil y cerrar sesión.
- Caso de usabilidad: Evaluar la facilidad de uso de la interfaz de usuario para registrarse y gestionar la cuenta.

**Interacción con otros sistemas:**

- Caso de integración: Verificar que la aplicación de comercio electrónico se integre correctamente con el sistema de inventario y el sistema de envíos.
- Caso de compatibilidad: Asegurar que la aplicación funcione correctamente en diferentes navegadores web y dispositivos móviles.

En cada uno de estos casos, las pruebas de sistema validarían que el sistema completo funciona según lo especificado, que las interacciones entre componentes son correctas y que el sistema cumple con todos los requisitos y expectativas del usuario.
