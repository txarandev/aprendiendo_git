# Git & GitHub

## Fundamentos Git 📂

### Los tres estados de Git

- **Confirmado (committed)**: Significa que los datos están almacenados de manera segura en tu base de datos local.

- **Modificado (modified)**: Significa que has modificado el archivo pero todavía no lo has confirmado a tu base de datos.

- **Preparado (staged)**: Significa que has marcado un archivo modificado en su versión actual para que vaya en tu próxima confirmación.

### Las tres secciones del proyecto Git

- Directorio de Git **(Git directory)**.

- Directorio de trabajo **(working directory)**.

- Area de preparación **(staging area)**.

## CONFIGURACIÓN DE GIT ⚙️

```git
git config --global user.name "name"

git config --global user.email email@email.com

git config --global core.editor code

git config --global init.defaultBranch main
```

### Otros comandos de interes

- `git config --list` = Muestra una lista de las configuraciones
- `git help config` = Muestra una guia sobre comandos de 'config'.

## INICIALIZANDO UN REPOSITORIO 🗃️

- `git init` = Inicia un repositorio en la carpeta actual.

## MOSTRANDO y ADMINISTRANDO DATOS 📝

- `git status` = Se usa para determinar que archivos estan en que estado.

- `git status -s` = Muestra los archivos de una forma mas simplificada. Los archivos nuevos que no están rastreados tienen un **'??'** a su lado, los archivos que están preparados tienen una **'A'** y los modificados una **'M'**.

- `git diff` = Muestra mas detalladamente los cambios que todavia no se han subido a 'stage'.

- `git diff --staged` = Se usa para ver lo que se preparo y se subira en la proxima confirmación.  (--staged y --cached son sinónimos).

- `git add .` = Sube todos los archivos a stage.

- `git add <nombrearchivo>` = Sube a stage solo el archivo nombrado.

- `git rm <nombrearchivo>` = Para eliminar archivos de Git, debes eliminarlos de tus archivos rastreados (o mejor dicho, **eliminarlos del área de preparación**) y luego confirmar. Si modificaste el archivo y ya lo habías añadido al índice, tendrás que forzar su eliminación con la opción **'-f'**.

- `git mv <arch1.txt> <arch2.txt>` = con este comando podemos renombrar archivos en GIT.

## HISTORIAL DE CONFIRMACIONES 📚️

- `git log` = muestra el historial de confirmaciones.

## CONFIRMANDO CAMBIOS 💾

- `git commit` = confirma los cambios y abre un editor de texto para poner info sobre los cambios.

- `git commit -m "mensaje"` = esta es la opción mas usada añade el mensaje del cambio directamente.
