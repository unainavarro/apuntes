<h1 align="center">Forks</h1>

<h2>📑 Contenido</h2>

- [¿Que son los forks?](#que-son-los-forks)
- [Operaciones para trabajar con un fork](#operaciones-para-trabajar-con-un-fork)
  - [Crea un Fork](#crea-un-fork)
  - [Clonar tu Fork](#clonar-tu-fork)
  - [Crea una Rama](#crea-una-rama)
  - [Realiza Cambios y Confirma](#realiza-cambios-y-confirma)
  - [Envía los Cambios a tu Fork](#envía-los-cambios-a-tu-fork)
  - [Crea una Pull Request](#crea-una-pull-request)
  - [Revisión y Fusión](#revisión-y-fusión)
  - [Actualizar tu Fork](#actualizar-tu-fork)

## ¿Que son los forks?

Un "fork" en Git se refiere a la creación de una copia de un repositorio Git en tu propia cuenta de GitHub o en otra plataforma de alojamiento de código. Los forks se utilizan comúnmente en proyectos de código abierto y colaborativo, y permiten a los colaboradores realizar cambios en un proyecto sin tener permisos para modificar directamente el repositorio original.

Este proceso de fork permite a los colaboradores contribuir a proyectos de código abierto sin necesidad de permisos especiales. Es una práctica común en el desarrollo colaborativo de software y es una de las características clave de las plataformas de alojamiento de código como GitHub.

## Operaciones para trabajar con un fork

### Crea un Fork

Si deseas contribuir a un proyecto en GitHub, por ejemplo, puedes navegar al repositorio del proyecto y hacer clic en el botón "Fork" en la esquina superior derecha de la página. Esto creará una copia completa del repositorio en tu propia cuenta de GitHub.

### Clonar tu Fork

Después de crear el fork, puedes clonarlo en tu máquina local utilizando el comando git clone. Esto te dará una copia local de tu fork en tu computadora.

```bash
git clone <URL_de_tu_fork>
```

### Crea una Rama

En tu repositorio local, puedes crear una nueva rama para trabajar en una característica o corrección de errores específica. Esto te permite trabajar en tu propia rama sin afectar la rama principal de tu fork.

```bash
git checkout -b <nombre_de_rama>
```

### Realiza Cambios y Confirma

Haz los cambios necesarios en tu rama y utiliza git commit para confirmar los cambios localmente.

```bash
git add .

git commit -m "Descripción del cambio"
```

### Envía los Cambios a tu Fork

Utiliza git push para enviar tus cambios a tu fork en línea.

```bash
git push origin <nombre_de_rama>
```

### Crea una Pull Request

Después de enviar los cambios a tu fork, puedes crear una Pull Request (solicitud de extracción) desde tu fork hacia el repositorio original. Esto notificará a los dueños del proyecto original sobre tus cambios y permitirá que revisen y, si es necesario, los fusionen en el repositorio principal.

### Revisión y Fusión

Los dueños del proyecto revisarán tus cambios y, si son aceptados, los fusionarán en el repositorio principal. Tu contribución se habrá completado en este punto.

### Actualizar tu Fork

Si el repositorio original ha recibido cambios mientras trabajabas en tu fork, puedes mantener tu fork actualizado utilizando git pull para obtener los cambios del repositorio original en tu fork.

```bash
git pull upstream <nombre_de_rama>
```
