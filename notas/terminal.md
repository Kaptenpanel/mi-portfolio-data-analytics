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
Open . --> abre la carpeta actual en el explorador. Podemos decir que open / abrirá la carpeta raíz.. etc.
Clear / ctrl+L --> limpia el terminal.
History --> muestra la historia de comandos

##### En GIT

git --version --> comprobar versión de git
git config --global --list --> Ver configuración global de git en el sistema
git init --> inicializar un repositorio
git status --> ver el estado del repositorio
git add --> añade un archivo o directorio al repositorio
git commit -m --> añade un commit con un comentario.
git log --oneline --> ver el log de git.