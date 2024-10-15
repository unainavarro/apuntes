<h1 align="center">Pruebas Funcionales (Functional Testing)</h1>

<h2>📑 Contenido</h2>

- [Pruebas Funcionales (Functional Testing)](#pruebas-funcionales-functional-testing)
- [Objetivos de las Pruebas Funcionales](#objetivos-de-las-pruebas-funcionales)
- [Tipos de Pruebas Funcionales](#tipos-de-pruebas-funcionales)
- [Ventajas](#ventajas)
- [Prácticas Recomendadas](#prácticas-recomendadas)
- [Ejemplo Conceptual (sin código)](#ejemplo-conceptual-sin-código)

## Pruebas Funcionales (Functional Testing)

Las pruebas funcionales (Functional Testing) son un tipo de prueba de software que se enfoca en verificar que el sistema cumpla con los requisitos funcionales especificados. Estas pruebas evalúan si el software hace lo que se supone que debe hacer según los requisitos y especificaciones del usuario, sin preocuparse por los detalles de la implementación interna. En otras palabras, se centran en el "qué" hace el sistema en lugar del "cómo" lo hace.

## Objetivos de las Pruebas Funcionales

**Validar requisitos funcionales:** Asegurarse de que el software cumple con todos los requisitos y especificaciones funcionales definidas en los documentos de requisitos.

**Verificar el comportamiento del sistema:** Comprobar que todas las funcionalidades del sistema funcionan como se espera en diferentes escenarios.

**Garantizar la correcta interacción del usuario:** Asegurarse de que el sistema interactúa correctamente con los usuarios y que la interfaz de usuario es funcional y fácil de usar.

**Identificar defectos y errores:** Detectar cualquier defecto o error en las funcionalidades del sistema para corregirlos antes de la entrega final.

## Tipos de Pruebas Funcionales

**Pruebas de caja negra:** Evaluar la funcionalidad del sistema sin conocer su estructura interna. Los casos de prueba se basan en los requisitos y especificaciones del software.

**Pruebas de regresión:** Asegurarse de que las nuevas funcionalidades o cambios en el software no introduzcan errores en las funcionalidades existentes.

**Pruebas de aceptación del usuario (UAT):** Validar que el sistema cumple con los requisitos del usuario y que está listo para su implementación en producción.

**Pruebas de sistema:** Evaluar el sistema completo para asegurar que todas las partes del software funcionen correctamente juntas.

**Pruebas de integración:** Verificar que diferentes módulos o componentes del sistema funcionen correctamente juntos.

## Ventajas

Alineación con los requisitos del usuario: Aseguran que el software cumple con las expectativas y necesidades del usuario.

Detección temprana de errores: Identifican errores y defectos en las etapas iniciales del desarrollo, lo que facilita su corrección.

Mejora de la calidad del software: Al validar todas las funcionalidades, se garantiza un producto final más robusto y confiable.

Aseguran la usabilidad: Verifican que la interfaz de usuario sea funcional y fácil de usar.

## Prácticas Recomendadas

**Revisión exhaustiva de los requisitos:** Comprender a fondo los requisitos y especificaciones del software antes de diseñar los casos de prueba.

**Diseño de casos de prueba basados en escenarios:** Crear casos de prueba que cubran diferentes escenarios de uso, incluyendo casos normales, casos límite y casos de error.

**Automatización de pruebas:** Utilizar herramientas de automatización para ejecutar pruebas repetibles y consistentes, lo que mejora la eficiencia y la cobertura de las pruebas.

**Ejecución de pruebas de regresión:** Realizar pruebas de regresión después de cualquier cambio en el software para asegurar que las funcionalidades existentes no se vean afectadas.

**Documentación clara:** Mantener una documentación clara y detallada de los casos de prueba, resultados de las pruebas y cualquier defecto encontrado.

## Ejemplo Conceptual (sin código)

Supongamos que estamos desarrollando una aplicación bancaria con funcionalidades como iniciar sesión, transferir dinero y consultar el saldo. Las pruebas funcionales podrían incluir los siguientes casos:

**Inicio de sesión:**

- **Caso positivo:** Verificar que los usuarios puedan iniciar sesión con credenciales válidas.
- **Caso negativo:** Verificar que los usuarios no puedan iniciar sesión con credenciales inválidas y que reciban un mensaje de error apropiado.

**Transferencia de dinero:**

- **Caso positivo:** Verificar que los usuarios puedan transferir dinero a otra cuenta y que el saldo se actualice correctamente en ambas cuentas.
- **Caso límite:** Verificar que no se pueda transferir más dinero del disponible en la cuenta.
- **Caso de error:** Verificar que se muestre un mensaje de error si la transferencia falla por problemas técnicos.

**Consulta de saldo:**

- **Caso positivo:** Verificar que los usuarios puedan consultar su saldo actual.
- **Caso negativo:** Verificar que se muestre un mensaje de error si hay un problema al recuperar la información del saldo.

En cada uno de estos casos, las pruebas funcionales validarían que las funcionalidades del sistema funcionan según lo especificado y cumplen con los requisitos del usuario.
