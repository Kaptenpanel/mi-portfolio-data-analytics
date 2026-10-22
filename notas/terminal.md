# Chuleta de comandos

## Comandos básicos del terminal

Pwd --> la carpeta donde estoy

Ls --> listar el contenido de la carpeta

Ls -a --> incluir ficheros escondidos

Ls -la --> incluir ficheros escondidos y mostrar sus permisos

Cd --> va a home

Cd "" --> va a ""

Cd / --> va a la carpeta raíz

Cd .. --> sube un nivel en el orden de carpetas

Mkdir "" --> crea la carpeta ""

Touch "".'' --> Crea el archivo "".''

Cat "__" --> muestra el contenido de "__"

Cp origen destino copia el archivo en origen al destino

Mv origen destino MUEVE el archivo (no guarda una copia en el origen)

Rm archivo --> borra x archivo

Rm -r carpeta --> borra x carpeta

Open -e archivo --> abre un archivo en el editor de texto por defecto

Open . --> abre la carpeta actual en el explorador.

Podemos decir que open / abrirá la carpeta raíz.. etc.
Clear / ctrl+L --> limpia el terminal.

History --> muestra la historia de comandos

## Comandos esenciales de git

git --version --> comprobar versión de git

git config --global --list --> Ver configuración global de git en el sistema

git init --> inicializar un repositorio

git status --> ver el estado del repositorio

git add --> añade un archivo o directorio al repositorio

git commit -m --> añade un commit con un comentario.

git log --oneline --> ver el log de git.

git switch -c nombre-rama --> crear una nueva rama con el nombre de rama

git clone <url> --> descarga un repositorio entero con todo su historial.

### otros comandos importantes de git

git diff                       # qué ha cambiado y no está en staging

git diff --staged              # qué está en staging y entrará en el commit

git restore archivo.sql        # descartar cambios no guardados de un archivo

git restore --staged archivo   # sacar un archivo de staging sin perder los cambios

git revert <hash>              # crear un commit que deshace otro commit

### flujo para volver a rama principal y borrar rama anterior

git switch master

git pull git branch -d nombre_rama

### flujo para trabajo diario

```
git switch main
git pull                                  # 1. partir de la última versión
git switch -c practica-2-1-3              # 2. rama para el trabajo nuevo
# ... trabajamos, editamos archivos ...
git status                                # 3. qué ha cambiado
git add .                                 # 4. preparar
git commit -m "Completar práctica 2.1.3"  # 5. guardar la foto
git push -u origin practica-2-1-3         # 6. subir la rama
# 7. abrir el pull request en GitHub, revisar y fusionar
# 8. volver a main y hacer git pull
```

## Venv de python

Cada vez que se entra en la carpeta hay que ejecutar:
```source .venv/bin/activate```
para activar el entorno virtual de python.

### jupyter labs

Como Zed tiene problemas con los notebooks de jupyter
(hay que usar repl y es un rollo), es mejor utilizar
jupyter labs por si: ```python -m jupyter lab```

## postgresql

Para iniciar el servicio:

```sudo launchctl load /Library/LaunchDaemons/postgresql-18.plist```

Y se comprueba con:

```sudo launchctl list | grep postgresql```

```/Library/PostgreSQL/18/bin/pg_isready -h localhost -p 5432```

Debe responder que está aceptando conexiones.

### para habilitar el servicio

```sudo launchctl enable system/postgresql-18```

Y para comprobar que está habilitado:

```sudo launchctl print-disabled system | grep postgresql-18```
