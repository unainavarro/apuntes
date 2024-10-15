<h1 align="center">Criptografía</h1>

<h2>📑 Contenido</h2>

- [Criptografía](#criptografía)
- [Conceptos Básicos](#conceptos-básicos)
- [Técnicas de Criptografía](#técnicas-de-criptografía)
- [Protocolos Criptográficos](#protocolos-criptográficos)
- [Aplicaciones de la Criptografía](#aplicaciones-de-la-criptografía)
- [Desafíos y Consideraciones](#desafíos-y-consideraciones)

## Criptografía

La criptografía informática es una rama de la criptografía que se centra en la protección de la información en entornos digitales. Utiliza técnicas matemáticas para asegurar que los datos sean confidenciales, íntegros y auténticos, incluso en presencia de adversarios.

La criptografía informática es un campo dinámico y en constante evolución, crucial para mantener la seguridad y la privacidad en el mundo digital. A medida que las amenazas avanzan, también lo hacen las técnicas y tecnologías criptográficas para contrarrestarlas.

## Conceptos Básicos

**Confidencialidad:** Garantiza que la información solo sea accesible para las partes autorizadas. Se logra mediante el cifrado, que convierte datos legibles en datos ilegibles.

**Integridad:** Asegura que la información no ha sido alterada de manera no autorizada. Se utilizan funciones hash y códigos de autenticación de mensajes (MAC) para verificar la integridad de los datos.

**Autenticación:** Verifica la identidad de las partes que se comunican y asegura que los datos provengan de una fuente legítima.

**No repudio:** Evita que una parte niegue haber enviado o recibido un mensaje. Se logra mediante firmas digitales.

## Técnicas de Criptografía

**Criptografía Simétrica:**

- Utiliza la misma clave para cifrar y descifrar los datos. Ejemplos: AES (Advanced Encryption Standard), DES (Data Encryption Standard).
- **Ventajas:** Rápida y eficiente para grandes volúmenes de datos.
- **Desventajas:** Gestión de claves compleja, ya que ambas partes deben compartir la misma clave de manera segura.

**Criptografía Asimétrica:**

- Utiliza un par de claves: una clave pública y una clave privada. La clave pública cifra los datos y la clave privada los descifra. Ejemplos: RSA, ECC (Elliptic Curve Cryptography).
- **Ventajas:** Facilita la distribución de claves y proporciona autenticación y no repudio.
- **Desventajas:** Es más lenta y menos eficiente para grandes volúmenes de datos.

**Funciones Hash:**

- Generan un valor fijo (hash) a partir de un mensaje de cualquier tamaño. Son utilizadas para verificar la integridad de los datos. Ejemplos: SHA-256, MD5.
- **Propiedades:** Los hash deben ser únicos, rápidos de calcular y resistentes a colisiones (dos mensajes diferentes no deben producir el mismo hash).

**Firmas Digitales:**

Utilizan criptografía asimétrica para proporcionar autenticación y no repudio. Un mensaje se firma con la clave privada del remitente y se verifica con la clave pública del remitente. Ejemplos: DSA (Digital Signature Algorithm), RSA.

**Criptografía de Curva Elíptica (ECC):**

Una forma avanzada de criptografía asimétrica que ofrece un alto nivel de seguridad con claves más cortas y eficientes que RSA.

## Protocolos Criptográficos

**SSL/TLS:** Protocolos para asegurar la comunicación a través de Internet. Utilizan una combinación de criptografía simétrica y asimétrica para proteger la transmisión de datos entre clientes y servidores.

**IPsec:** Protocolo que asegura las comunicaciones a nivel de red, proporcionando autenticación, integridad y confidencialidad de los datos.

**PGP/GPG:** Protocolos para cifrar y firmar correos electrónicos y archivos. Utilizan una combinación de criptografía simétrica y asimétrica.

## Aplicaciones de la Criptografía

**Seguridad en la Web:**

- HTTPS asegura las comunicaciones entre navegadores web y servidores.
- Autenticación de usuarios y gestión de sesiones.

**Seguridad en Redes:**

- VPNs usan criptografía para proteger las conexiones a través de redes no seguras.
- Protección de datos en redes inalámbricas (WPA/WPA2).

**Almacenamiento Seguro:**

Cifrado de discos y sistemas de archivos para proteger datos en reposo.

**Firmas y Certificados Digitales:**

Utilizados para autenticar software, documentos y comunicaciones electrónicas.

## Desafíos y Consideraciones

**Gestión de Claves:** La seguridad de los sistemas criptográficos depende en gran medida de la gestión segura de las claves.

**Ataques Criptográficos:** Los adversarios intentan romper los esquemas criptográficos. Es fundamental utilizar algoritmos seguros y actualizados.

**Rendimiento y Eficiencia:** La criptografía puede introducir sobrecarga computacional. Es crucial equilibrar la seguridad con el rendimiento.

**Cumplimiento Normativo:** Asegurarse de que las prácticas criptográficas cumplan con las regulaciones y estándares aplicables (por ejemplo, GDPR, PCI-DSS).
