# Git & GitHub

## Fundamentos Git

### Los tres estados de Git

- **Confirmado (committed)**: significa que los datos están almacenados de manera segura en tu base de datos local.

- **Modificado (modified)**: significa que has modificado el archivo pero todavía no lo has confirmado a tu base de datos.

- **Preparado (staged)**: significa que has marcado un archivo modificado en su versión actual para que vaya en tu próxima confirmación.

### Las tres secciones del proyecto Git

- directorio de Git (Git directory).

- directorio de trabajo (working directory).

- área de preparación (staging area).

## CONFIGURACIÓN DE GIT

```git
git config --global user.name "name"

git config --global user.email email@email.com

git config --global core.editor code
```

### Otros comandos de interes

- `git config --list` = Muestra una lista de las configuraciones
- `git help config` = Muestra una guia sobre comandos de 'config'.
