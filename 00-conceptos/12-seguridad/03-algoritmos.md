<h1 align="center">Algoritmos Criptográficos</h1>

<h2>📑 Contenido</h2>

- [Algoritmos Criptográficos](#algoritmos-criptográficos)
- [Algoritmos de Cifrado Simétrico](#algoritmos-de-cifrado-simétrico)
- [Algoritmos de Cifrado Asimétrico](#algoritmos-de-cifrado-asimétrico)
- [Algoritmos de Funciones Hash](#algoritmos-de-funciones-hash)
- [Algoritmos de Derivación de Claves](#algoritmos-de-derivación-de-claves)
- [Algoritmos de Firmas Digitales](#algoritmos-de-firmas-digitales)

## Algoritmos Criptográficos

Los algoritmos criptográficos son fundamentales para asegurar la confidencialidad, integridad y autenticidad de la información en sistemas digitales.

La elección del algoritmo criptográfico adecuado depende del contexto y los requisitos específicos de seguridad, rendimiento y recursos disponibles. Es importante mantenerse actualizado sobre las vulnerabilidades y mejores prácticas en criptografía para asegurar que los algoritmos y las implementaciones sean robustos y eficaces contra las amenazas actuales.

## Algoritmos de Cifrado Simétrico

**AES (Advanced Encryption Standard)**

AES es el estándar de cifrado simétrico más utilizado hoy en día. Utiliza bloques de 128 bits y soporta claves de 128, 192 y 256 bits.

- **Uso Común:** Protección de datos en reposo y en tránsito, VPNs, cifrado de disco, HTTPS.
- **Ventajas:** Seguro, eficiente y ampliamente adoptado.
- **Desventajas:** La seguridad depende de la gestión adecuada de las claves.

**DES (Data Encryption Standard)**

Un algoritmo de cifrado simétrico de 56 bits. Considerado obsoleto y reemplazado por AES debido a su vulnerabilidad a ataques de fuerza bruta.

- **Uso Común:** Históricamente usado en sistemas financieros y administrativos.
- **Ventajas:** Fácil de implementar.
- **Desventajas:** Inseguro debido a su corta longitud de clave.

**3DES (Triple DES)**

Una variante más segura de DES que aplica el algoritmo tres veces a cada bloque de datos.

- **Uso Común:** Sistemas financieros y aplicaciones que heredaron DES.
- **Ventajas:** Más seguro que DES.
- **Desventajas:** Más lento y menos eficiente que AES.

## Algoritmos de Cifrado Asimétrico

**RSA (Rivest-Shamir-Adleman)**

Un algoritmo de cifrado asimétrico basado en la factorización de grandes números primos. Utiliza claves públicas y privadas.

- **Uso Común:** Cifrado de datos, firmas digitales, intercambio de claves.
- **Ventajas:** Seguridad comprobada y ampliamente utilizado.
- **Desventajas:** Requiere claves largas para una alta seguridad, lo que lo hace computacionalmente intensivo.

**ECC (Elliptic Curve Cryptography)**

Un enfoque de criptografía asimétrica basado en las propiedades algebraicas de las curvas elípticas.

- **Uso Común:** Cifrado de datos, firmas digitales, intercambio de claves.
- **Ventajas:** Seguridad equivalente a RSA con claves mucho más cortas, lo que lo hace más eficiente.
- **Desventajas:** Más complejo de implementar y entender.

## Algoritmos de Funciones Hash

**SHA (Secure Hash Algorithm)**

- **SHA-1:** Produce un hash de 160 bits. Vulnerable a ataques de colisión.
- **SHA-2:** Incluye variantes como SHA-224, SHA-256, SHA-384 y SHA-512, que producen hashes de diferentes tamaños. Considerado seguro.
- **SHA-3:** Basado en el algoritmo Keccak, proporciona una alternativa a SHA-2 con opciones de hash de diferentes tamaños.
- **Uso Común:** Verificación de integridad de datos, firmas digitales, almacenamiento de contraseñas.

**MD5 (Message Digest Algorithm 5)**

- **Descripción:** Produce un hash de 128 bits.
- **Uso Común:** Verificación de integridad de archivos.
- **Ventajas:** Rápido y eficiente.
- **Desventajas:** Vulnerable a colisiones y ataques de preimagen. No recomendado para aplicaciones de seguridad.

## Algoritmos de Derivación de Claves

**PBKDF2 (Password-Based Key Derivation Function 2)**

- **Descripción:** Una función de derivación de claves que aplica una función hash junto con una sal y múltiples iteraciones.
- **Uso Común:** Almacenamiento seguro de contraseñas.
- **Ventajas:** Configurable en términos de tiempo de computación.
- **Desventajas:** Puede ser vulnerable a ataques de hardware especializado.

**bcrypt**

- **Descripción:** Basado en el algoritmo Blowfish, incluye una sal y es adaptable en términos de costo computacional.
- **Uso Común:** Almacenamiento seguro de contraseñas.
- **Ventajas**: Resistente a ataques de fuerza bruta, incorpora una sal y permite ajustar el costo computacional.
- **Desventajas:** Más lento que otras funciones de derivación de claves, lo cual es intencional para aumentar la seguridad.

**scrypt**

- **Descripción:** Diseñado para ser intensivo tanto en memoria como en CPU, lo que lo hace resistente a ataques en hardware especializado.
- **Uso Común:** Almacenamiento seguro de contraseñas, criptomonedas.
- **Ventajas:** Alta resistencia a ataques de hardware especializado.
- **Desventajas:** Más complejo y consume más recursos que bcrypt.

## Algoritmos de Firmas Digitales

**DSA (Digital Signature Algorithm)**

- **Descripción:** Un estándar para firmas digitales basado en problemas matemáticos de logaritmos discretos.
- **Uso Común:** Firmas digitales, autenticación.
- **Ventajas:** Firmas pequeñas y verificables.
- **Desventajas:** Requiere más tiempo de generación de claves.

**ECDSA (Elliptic Curve Digital Signature Algorithm)**

- **Descripción:** Una variante de DSA que utiliza criptografía de curva elíptica.
- **Uso Común:** Firmas digitales, autenticación.
- **Ventajas:** Seguridad equivalente con claves más cortas y eficientes que DSA.
- **Desventajas:** Más complejo de implementar.
