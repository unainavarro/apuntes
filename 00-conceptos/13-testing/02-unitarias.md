<h1 align="center">Pruebas Unitarias (Unit Testing)</h1>

<h2>📑 Contenido</h2>

- [Pruebas Unitarias (Unit Testing)](#pruebas-unitarias-unit-testing)
- [Objetivos de las Pruebas Unitarias](#objetivos-de-las-pruebas-unitarias)
- [Características](#características)
- [Ventajas](#ventajas)
- [Prácticas recomendadas](#prácticas-recomendadas)
- [Ejemplo Conceptual (sin código)](#ejemplo-conceptual-sin-código)

## Pruebas Unitarias (Unit Testing)

Las pruebas unitarias (Unit Testing) son un tipo de prueba de software que se centra en verificar la funcionalidad de las unidades más pequeñas del código, como funciones, métodos o clases. El objetivo principal de las pruebas unitarias es asegurarse de que cada unidad individual funcione correctamente de manera aislada.

## Objetivos de las Pruebas Unitarias

**Validar la funcionalidad de cada unidad:** Asegurarse de que cada unidad de código produzca el resultado esperado para una variedad de entradas.

**Detectar y corregir errores temprano:** Identificar errores en las primeras etapas del desarrollo, lo que facilita su corrección antes de que se integren con otras partes del sistema.

**Facilitar el refactorizado:** Proporcionar una red de seguridad que permita refactorizar el código con confianza, asegurando que las funcionalidades existentes no se vean afectadas.

**Documentar el comportamiento del código:** Actuar como documentación viva que describe cómo se espera que funcione cada unidad del sistema.

## Características

**Aisladas:** Las pruebas unitarias deben probar solo una unidad de código a la vez, sin depender de otras partes del sistema. Esto se logra utilizando mocks, stubs o fakes para simular dependencias.

**Rápidas:** Las pruebas unitarias deben ser rápidas de ejecutar para que puedan integrarse en el ciclo de desarrollo continuo y ejecutarse con frecuencia.

**Automatizadas:** Las pruebas unitarias deben ser fácilmente automatizables para que puedan ejecutarse de manera consistente y repetible, idealmente como parte de una integración continua.

**Determinísticas:** Deben producir el mismo resultado cada vez que se ejecuten con las mismas entradas, lo que significa que no deben depender de factores externos como la red o el sistema de archivos.

## Ventajas

**Mejora de la calidad del código:** Detectar y corregir errores tempranos ayuda a mejorar la calidad general del código.

**Facilita el mantenimiento:** Proporcionan confianza al hacer cambios o refactorizar el código, ya que cualquier problema será detectado rápidamente.

**Reducción de costos:** Corregir errores en una etapa temprana del desarrollo es menos costoso que hacerlo en etapas posteriores.

**Documentación:** Sirven como documentación adicional para el código, ayudando a otros desarrolladores a entender cómo debería funcionar cada unidad.

## Prácticas recomendadas

**Desarrollo Guiado por Pruebas (TDD):** Escribir las pruebas antes del código de producción. Esto ayuda a enfocar el desarrollo en los requisitos y garantiza una cobertura de pruebas completa.

**Nombrado claro:** Utilizar nombres descriptivos para las pruebas que expliquen claramente qué se está probando y cuáles son las expectativas.

**Cobertura de casos borde:** Asegurarse de que las pruebas cubran una variedad de casos, incluyendo casos normales, casos extremos y casos de error.

**Ejecución frecuente:** Integrar las pruebas unitarias en el ciclo de desarrollo continuo, ejecutándolas con cada cambio de código para detectar problemas rápidamente.

**Aislamiento de pruebas:** Utilizar técnicas como mocks y stubs para aislar las unidades de código que se están probando, eliminando dependencias externas.

## Ejemplo Conceptual (sin código)

Supongamos que tenemos una función calcularSuma(a, b) que debe devolver la suma de dos números. Una prueba unitaria para esta función podría incluir varios casos:

- **Caso estándar:** Verificar que calcularSuma(2, 3) devuelve 5.

- **Caso límite:** Verificar que calcularSuma(0, 0) devuelve 0.

- **Caso negativo:** Verificar que calcularSuma(-1, -1) devuelve -2.

En cada uno de estos casos, la prueba unitaria verificaría que el resultado de calcularSuma es el esperado.
