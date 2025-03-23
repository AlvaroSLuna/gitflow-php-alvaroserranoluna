# Documentación del Flujo de Trabajo con Git Flow

Este documento describe los pasos seguidos en el desarrollo de un proyecto utilizando Git Flow.

---
## Parte 1: Configuración Inicial

1. Se ha creado el repositorio en GitHub.
2. Se ha clonado el repositorio con el comando:
   ```sh
   git clone <URL_DEL_REPOSITORIO>
   ```
3. Se ha creado este archivo `README.md` y se ha subido a la rama `main`.
4. Se han utilizado los comandos:
   ```sh
   git add .
   git commit -m "Añadiendo README.md"
   git push origin main
   ```
5. Se ha creado la rama `develop`.
6. Se ha inicializado Git Flow con:
   ```sh
   git flow init
   ```

---
## Parte 2: Creación de una Nueva Funcionalidad

1. Se ha creado la nueva funcionalidad con el comando:
   ```sh
   git flow feature start crear-mi-archivo
   ```
2. Se ha creado una carpeta `alumnos/` y dentro de ella un archivo `alumno.php`.
3. Se han agregado los cambios y confirmado en la rama `develop`:
   ```sh
   git add .
   git commit -m "Añadiendo alumno.php"
   git push origin feature/crear-mi-archivo
   ```

---
## Parte 3: Modificación del Index

1. Se ha creado una nueva funcionalidad en Git Flow con el comando:
   ```sh
   git flow feature start modificar-index
   ```
2. Se ha creado un archivo `index.php` y se ha agregado contenido.
3. Se han confirmado los cambios y la funcionalidad se ha subido a `develop`:
   ```sh
   git add .
   git commit -m "Añadiendo index.php"
   git push origin feature/modificar-index
   ```

---
## Parte 4: Resolución de Conflictos

1. Para generar un conflicto, se ha creado una nueva rama `develop2`.
2. Se ha escrito una línea distinta en cada rama.
3. Al intentar hacer merge, se ha generado un conflicto.
4. Se ha resuelto eliminando la línea desactualizada y manteniendo la correcta.
5. Se han confirmado los cambios después de resolver el conflicto.

---
## Parte 5: Eliminación de un Archivo

1. Se ha eliminado un archivo con el comando:
   ```sh
   git rm alumnos/alvaro.php
   ```
2. Se han agregado los cambios y se han confirmado:
   ```sh
   git add .
   git commit -m "Eliminando archivo alumnos/alvaro.php"
   git push origin develop
   ```

---
## Parte 6: Publicación de una Versión Estable

Para subir una versión estable, se han ejecutado los siguientes comandos:
```sh
git push origin main
git push origin develop
git push origin --tags
```

De esta manera, la versión estable se ha publicado correctamente en el repositorio remoto.

