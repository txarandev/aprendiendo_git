# Git & GitHub

## Fundamentos Git 📂

### - Los tres estados de Git

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
- `git config --global alias.<nombrealias> 'log -1 HEAD'` = Se utiliza para crear alias **atajos** para hacer mas facil el manejo de git.

### INICIALIZANDO UN REPOSITORIO 🗃️

- `git init` = Inicia un repositorio en la carpeta actual.

### MOSTRANDO y ADMINISTRANDO DATOS 📝

- `git status` = Se usa para determinar que archivos estan en que estado.

- `git status -s` = Muestra los archivos de una forma mas simplificada. Los archivos nuevos que no están rastreados tienen un **'??'** a su lado, los archivos que están preparados tienen una **'A'** y los modificados una **'M'**.

- `git diff` = Muestra mas detalladamente los cambios que todavia no se han subido a 'stage'.

- `git diff --staged` = Se usa para ver lo que se preparo y se subira en la proxima confirmación.  (--staged y --cached son sinónimos).

- `git add .` = Sube todos los archivos a stage.

- `git add <nombrearchivo>` = Sube a stage solo el archivo nombrado.

- `git rm <nombrearchivo>` = Para eliminar archivos de Git, debes eliminarlos de tus archivos rastreados (o mejor dicho, **eliminarlos del área de preparación**) y luego confirmar. Si modificaste el archivo y ya lo habías añadido al índice, tendrás que forzar su eliminación con la opción **'-f'**.

- `git mv <arch1.txt> <arch2.txt>` = con este comando podemos renombrar archivos en GIT.

- `git restore --staged <archi.txt>` = Se usa para sacar los archivos del area de preparacion.

### HISTORIAL DE CONFIRMACIONES 📚️

- `git log` = muestra el historial de confirmaciones.

- `git log -p` = muestra el historial de confirmaciones con los cambios recientes.

- `git log --stat` = Imprime tras cada confirmación una lista de archivos modificados, indicando cuántos han sido modificados y cuántas líneas han sido añadidas y eliminadas para cada uno de ellos, y un resumen de toda esta información.

- `git log --pretty=oneline` = Otras opciones son **short, full y fuller**, que muestran la salida en un formato parecido, pero añadiendo menos o más información, respectivamente.

- `git log --pretty=format` = permite especificar tu propio formato. Algunas de las opciones más útiles aceptadas por **format**:
  - **%H**: Hash de la confirmacion.
  - **%h**: Hash de la confirm abreviado.
  - **%T**: Hash del arbol.
  - **%t**: Hash del arbol abreviado.
  - **%P**: Hashes de las confirmaciones padre.
  - **%p**: Hashes de las confirmaciones padre abreviados
  - **%an**: Nombre del autor.
  - **%ae**: Dirección de correo del autor.
  - **%ad**: Fecha de autoría (el formato respeta la opción –date).
  - **%ar**: Fecha de autoría, relativa.
  - **%cn**: Nombre del confirmador.
  - **%ce**: Dirección de correo del confirmador.
  - **%cd**: Fecha de confirmación.
  - **%cr**: Fecha de confirmación, relativa.
  - **%s**: Asunto.

- `git log --pretty=oneline --graph` = añade un pequeño gráfico **ASCII** mostrando tu historial de ramificaciones y uniones.

### CONFIRMANDO CAMBIOS 💾

- `git commit` = confirma los cambios y abre un editor de texto para poner info sobre los cambios.

- `git commit -m "mensaje"` = esta es la opción mas usada añade el mensaje del cambio directamente.

- `git commit --amend` = Uno de las acciones más comunes a **deshacer** es cuando confirmas un cambio antes de tiempo y olvidas agregar algún archivo, o te equivocas en el mensaje de confirmación. Si quieres rehacer la confirmación, puedes reconfirmar con la opción **--amend**.

### DESHACER un archivo preparado ⚠️

- `git reset HEAD <archivo.txt>` = Deshace la preparación del archivo. `git reset` puede ser un comando peligroso, especialmente si lo llamas con la opción `--hard`. Sin embargo, en el escenario descrito anteriormente, el archivo que está en tu directorio de trabajo no se toca, por lo que es relativamente seguro.

### DESHACER un archivo modificado ⚠️

- `git checkout -- <archi.txt>` = Sirve para descartar los cambios que se hicieron.

## RAMAS 🔗

- `git branch <nombrerama>` = Para crear una rama usamos **branch** seguido del nombre que queremos dar a la rama.

- `git checkout <nombrerama>` = Para cambiar de rama usamos el comando **checkout**.