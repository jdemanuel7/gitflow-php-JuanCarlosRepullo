Proyecto Git Flow en PHP

1. Creación del repositorio y configuración inicial

Pasos realizados:

Creé un repositorio en GitHub con el nombre gitflow-php-[tu_nombre].

Cloné el repositorio en mi equipo local:

git clone <URL_del_repositorio>
cd gitflow-php-[tu_nombre]

Inicialicé Git Flow en el proyecto:

git flow init

Verifiqué la existencia de la rama develop y la creé si era necesario:

git checkout develop

2. Creación de un archivo PHP

Pasos realizados:

Creé una nueva funcionalidad en Git Flow:

git flow feature start crear-mi-archivo

Dentro de la carpeta alumnos/, creé el archivo tu_nombre.php con el siguiente contenido:

<?php
// Archivo: alumnos/tu_nombre.php
echo "Hola, soy [Tu Nombre] y estoy aprendiendo Git Flow!";
?>

Confirmé y subí los cambios a la rama develop:

git add alumnos/tu_nombre.php
git commit -m "Agregado archivo PHP para feature/crear-mi-archivo"
git flow feature finish crear-mi-archivo

3. Modificación de un archivo existente

Pasos realizados:

Creé una nueva funcionalidad en Git Flow:

git flow feature start modificar-index

Modifiqué index.php para incluir el archivo PHP:

<?php
include "alumnos/tu_nombre.php";
?>

Confirmé los cambios y subí la funcionalidad a develop:

git add index.php
git commit -m "Modificado index.php para incluir archivo PHP de alumnos"
git flow feature finish modificar-index

4. Resolución de conflictos

Pasos realizados:

Se modificó index.php en la misma línea que otro compañero.

Se intentó hacer merge de ambas funcionalidades en develop, lo que generó un conflicto.

Para resolver el conflicto:

Ejecuté git status para ver los archivos en conflicto.

Edite manualmente index.php, asegurándome de mantener ambas modificaciones necesarias.

Guardé los cambios y realicé el commit:

git add index.php
git commit -m "Resuelto conflicto en index.php"

Finalicé la funcionalidad:

git flow feature finish modificar-index

5. Eliminación de un archivo

Pasos realizados:

Creé una nueva funcionalidad en Git Flow:

git flow feature start borrar-mi-archivo

Eliminé mi archivo PHP dentro de alumnos/:

git rm alumnos/tu_nombre.php

Confirmé y subí los cambios:

git commit -m "Eliminado archivo PHP de alumnos"
git flow feature finish borrar-mi-archivo

6. Publicación de la versión final

Pasos realizados:

Creé una nueva release:

git flow release start v1.0

Finalicé la versión y la fusioné en main:

git flow release finish v1.0

Creé una etiqueta para la versión final:

git tag v1.0 -m "Versión final v1.0"
git push origin main --tags

Conclusión

Este proyecto permitió poner en práctica el uso de Git Flow en un proyecto PHP, organizando correctamente las funcionalidades y asegurando una correcta gestión de versiones.
