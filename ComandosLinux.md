# COMANDOS LINUX

|COMANDO|COMANDOS ADICIONALES|SIGNIFICADO|DESCRIPCIÓN|
|:-:|:-|:-:|:-|
|***pwd***||*"print woking directory"*|**Visualiza la ruta del directorio actual**|
|***cd***||*"change directory"*|**Navegación de archivos y directorios**|
||*\<directorio>*||se dirige al directorio nombrado|
||*\<archivo>*||en el directorio que nos encontremos actualmente se abrirá el archivo nombrado|
||*..*||retrocede un directorio al que nos encontreamos|
||*~*||vuelve al directorio de inicio/personal|
||*/*||vuelve al directorio principal de la unidad|
||*-*||vuelve al directorio que hayamos usado previamente|
|***ls***||*"list"*|**Ver el contenido de un directorio**|
||*(vacío)*||muestra el contenido del directorio actual|
||*\<directorio>*||muestra el contenido del directorio nombrado|
||*\\*||muestra el contenido del directorio de inicio|
||*-R*||lista también todos los archivos de los subdirectorios|
||*-a*||muestra los archivos ocultos|
||*-l*||lista los archivos y directorios con información detallada: permisos, tamaño, propietario, etc|
||*-s*||listar archivos y directorios con sus tamaños|
||*-t*||listar archivos y directorios en orden descendente a la última fecha de modificación|
||*-tr*||listar archivos y directorios en orden ascendente a la última fecha de modificación|
||*-S*||listar archivos y directorios en orden descendente al tamaño|
||*-Sr*||listar archivos y directorios en orden ascendente al tamaño|
|***cat***||*"concatenate"*|**Listar el contenido de un archivo**|
||*nombrearchivo*||lista el contenido del archivo|
||*> nombrearchivo*||crea un nuevo archivo|
||*nombrearchivo1 > nombrearchivo2*||mueve el contenido de 1 a 2 sobrescibiéndolo (si el archivo 2 no existe, se crea)|
||*nombrearchivo1 >> nombrearchivo2*||mueve el contenido de 1 al final del 2 (si el archivo 2 no existe, se crea)|
||*nombrearchivo1 nombrearchivo2 > nombrearchivo3*||une los archivos 1 y 2 almacenándolos en el archivo 3|
||*nombrearchivo \| tr a-z A-Z > salida.txt*||convierte el nombre de un archivo de minúsculas a mayúsculas|
||*nombrearchivo \| more*||separa el archivo por páginas|
||*nombrearchivo \| less*||separa el archivo por páginas y permite moverse a través de ellas con 'AvPág' y 'RePág'|
||*-n*||enumera cada línea del archivo|
||*-e*||escribe un '$' al final de cada línea|
||*-t*||escribe '^I' en cada espacio por tabulador|
|***cp***||*"copy"*|**Copiar archivos de un directorio a otro**|
||*nombrearchivo \<directorio>*||copia el archivo al directorio indicado|
||*nombrearchivo1 \nombrearchivo2*||copia el archivo 1 en un nuevo archivo en el mismo directorio en el que nos encontramos|
|***mv***||*"move"*|**Mover o renombrar archivos**|
||*\<archivo> \<directorio>*||muve el archivo al directorio indicado|
||*\<archivo1> \<archivo2>*||renombra el archivo|
|***mkdir***||*"make directory"*|**Crear un nuevo directorio**|
||*\<directorioactual>/\<directorionuevo>*||crea un subdirectorio en el directorio actual|
||*-p \<directorio1>/\<directorio3>/\<directorio2>*|*"parents"*|se crea un nuevo directorio entre los directorios 1 y 2|
|***rmdir***||*"remove directory"*|**Borra directorios vacíos**|
|***rm***||*"remove"*|**Borra directorios y su contenido**|
||*-r*||elimina unicamente directorios no vacíos|
||*-d*||elimina unicamente directorios vacios|
||*-i*||pregunta por cada archivo antes de borrarlo|
|***touch***|||**Crear un nuevo archivo en blanco**|
||*\<directorio>/nombrearchivo*||crea un archivo nuevo vacío en el directorio especificado|
|***locate***|||**Localizar archivos**|
||*-i*||en la busqueda, no distinque entre mayúsculas y minúsculas|
||*palabra1\*palabra2*||buscará cualquier archivo que contenga las palabras 1 y 2 exactas|
|***find***|||**Busca archivos y directorios**|
||*\<direcotorio> -name nombrearchivo*||busca el archivo indicado dentro del directorio y sus subdirectorios|
||*. -name nombrearhivo*||busca el archivo en el directorio actual y sus subdirectorios|
|***grep***||*"global regular expression print"*|**Busca a través de todo el texto de un archivo**|
||*palabra nombrearchivo*||busca la palabra indicada en el archivo especificado y se mostrarán las líneas que contengan dicha palabra|
|***sudo***||*"superuser do"*|**Permite realizar tareas que requieren permisos administrativos o raíz**|
|***df***||"disk free"|**Obtener información sobre el uso del espacio del disco del sistema**|
||*-m*||ver el informe en MB|
|***du***||*"disk usage"*|**Verificar el espacio de un archivo o directorio**|
|***head***|||**Ver las primeras líneas de un archivo de texto**|
||*-n N nombrearchivo*||muestra las N primeras líneas del archivo (de forma predeterminada muestra 10)|
|***tail***|||**Ver las últimas líneas de un archivo de texto**|
||*-n N nombrearchivo*||muestra las N últimas líneas del archivo (de forma predeterminada muestra 10)|
|***diff***||*"difference"*|**Compara el contenido de dos archivos línea por línea. Después genera las líneas que no coinciden**|
|***tar***||*"tape archive"*|**Guardar archivos en un *tarball* (similar a un *zip* con compresión opcional)**|
|***chmod***||*"change mode"*|**Cambiar los permisos de lectura, escritura y ejecución de archivos y directorios**|
|***chown***||*"change owner"*|**Cambiar/tranferir la propiedad de un archivo a un nuevo usuario**|
|***jobs***|||**Muestra todos los trabajos (procesos) actuales junto con sus estados**|
|***kill***|||**Para cerrar manualmente un programa**|
||*SIGTERM (signal 15)*||solicita que un programa deje de ejecutarse y da algo de tiempo para guardar todo el progreso (señal predeterminada si no se especifica)|
||*SIGKILL (signal 9)*||obliga a los programas a detenerse inmediatamente y el progreso no guardado se perderá|
|***ping***||*"packet internet groper"*|**Verificar el estado de conectividad a un servidor**|
|***wget***||*"non-interactive network downloader"*|**Descargar archivos de Internet**|
|***uname***||*"unix name"*|**Imprime información detallada sobre tu sistema Linux: nombre de la máquina, sistema operativo, núcleo, etc**|
|***sh***||*"command language interpreter"*|**Ejecuta un fichero de comandos**|
|***top***||*"real-time process monitor"*|**Muestra una lista de los procesos en ejecución y la cantidad de CPU que utiliza cada proceso**|
|***history***|||**Revisar comandos ingresados anteriormente**|
|***man***||*"manual"*|**Ayuda/manual sobre los comandos**|
|***echo***|||**Mover algunos datos a un archivo**|
||*texto >> nombrearchivo*||agregar un texto a un archivo determinado|
|***zip, unzip***|||**Para (des)comprimir archivos**|
|***hostname***|||**Conocer el nombre de tu host/red**|
||*-I*||muestra la dirección IP de la red|
|***useradd, userdel***|||**Crear/eliminar usuarios**|
||*passwd*|*"password"*|agregar un contraseña a la cuenta de un nuevo usario|

> *nombrearchivo = nombre + extensión
