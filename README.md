# Comandos básicos de Linux (spanish)

Este repositorio contiene una lista de comandos útiles de Linux y sus posibles combinaciones.

##  indice de la lista de comandos y un breve resumen:

| Comando | Descripción |
|---------|-------------|
| [man](#man) | Muestra el manual de un comando |
| [cd](#cd) | Cambia el directorio actual al que se indica como argumento |
| [ls](#ls) | Lista los archivos y directorios |
| [pwd](#pwd) | Muestra el directorio actual en el que se encuentra el usuario |
| [less](#less) | Muestra el contenido de un archivo de texto en la terminal |
| [cat](#cat) | Muestra el contenido de uno o más archivos de texto en la terminal |
| [file](#file) | Determina el tipo de un archivo examinando su contenido |
| [ln](#ln) | Crea enlaces entre archivos |
| [cp](#cp) | Copia uno o más archivos o directorios a otro destino |
| [mv](#mv) | Mueve o renombra uno o más archivos o directorios |
| [rm](#rm) | Elimina uno o más archivos o directorios |
| [mkdir](#mkdir) | Crea uno o más directorios con el nombre que se indica como argumento |
| [type](#type) | Muestra cómo se interpretaría un comando o palabra clave por el shell |
| [which](#which) | Muestra la ruta completa de los comandos ejecutables |
| [help](#help) | Muestra información sobre los comandos integrados del shell |
| [man](#man) | Muestra el manual de un comando |
| [find](#find) | Busca archivos o directorios que cumplan con ciertos criterios |
| [chmod](#chmod) | Cambia los permisos de acceso a los archivos o directorios |
| [chown](#chown) | Cambia el propietario y/o el grupo de los archivos o directorios |
| [head](#head) | Muestra las primeras líneas de un archivo o de la entrada estándar |
| [tail](#tail) | Muestra las últimas líneas de un archivo o de la entrada estándar |
| [grep](#grep) | Busca patrones en archivos o en la entrada estándar |
| [ps](#ps) | Muestra los procesos en ejecución |
| [top](#top) | Muestra la lista de procesos en ejecución en tiempo real |
| [du](#du) | Muestra el espacio utilizado por archivos y directorios |
| [df](#df) | Muestra el espacio utilizado y disponible en los sistemas de archivos |
| [ssh](#ssh) | Inicia una sesión remota segura en un servidor |
| [scp](#scp) | Copia archivos entre un sistema local y un sistema remoto a través de SSH |
| [tar](#tar) | Crea o extrae archivos comprimidos en formato tar |
| [gzip](#gzip) | Comprime o descomprime archivos en formato gzip |
| [unzip](#unzip) | Descomprime archivos en formato zip |
| [wget](#wget) | Descarga archivos desde la web |
| [history](#history) | Muestra el historial de comandos ejecutados anteriormente |
| [su](#su) | Cambia al usuario superusuario o a otro usuario |
| [sudo](#sudo) | Ejecuta un comando con privilegios de superusuario |


## man

El comando **man** muestra el manual de un comando, es decir, su descripción, opciones, argumentos y ejemplos. Se usa de la siguiente manera:

```bash
man [comando]
```
Por ejemplo, para ver el manual del comando **ls**, se escribe:

```bash
man ls
```
## pwd

El comando **pwd** muestra el directorio actual en el que se encuentra el usuario. No necesita ningún argumento. Se usa así:

```bash
pwd
```

## ls

El comando **ls** lista los archivos y directorios que hay en el directorio actual o en uno especificado. Se puede usar con diferentes opciones para modificar el formato o el contenido de la salida. Algunas opciones comunes son:

- `-a`: muestra todos los archivos, incluyendo los ocultos (que empiezan con un punto).
- `-l`: muestra la salida en formato largo, con información adicional como los permisos, el tamaño, el dueño y la fecha de modificación.
- `-h`: muestra el tamaño de los archivos en un formato legible para humanos (por ejemplo, KB, MB, GB).
- `-r`: invierte el orden de la salida (por defecto es alfabético ascendente).
- `-S`: ordena la salida por tamaño de archivo, de mayor a menor.
- `-t`: ordena la salida por fecha de modificación, de más reciente a más antiguo.

Se usa de la siguiente forma:

```bash
ls [opciones] [directorio]
```

Por ejemplo, para listar los archivos del directorio `/home` en formato largo y ordenados por tamaño, se escribe:

```bash
ls -lhS /home
```

## cd

El comando **cd** cambia el directorio actual al que se indica como argumento. Se usa así:

```bash
cd [directorio]
```

Por ejemplo, para cambiar al directorio `/usr/bin`, se escribe:

```bash
cd /usr/bin
```

Si no se especifica ningún argumento, el comando **cd** cambia al directorio personal del usuario (`/home/[usuario]`). También se puede usar el símbolo `~` para referirse al directorio personal.

Para volver al directorio anterior, se puede usar el argumento `-`. Por ejemplo:

```bash
cd -
```
## less

El comando **less** muestra el contenido de un archivo de texto en la terminal, permitiendo desplazarse por él con las teclas de dirección o la barra espaciadora. Se usa así:

```bash
less [archivo]
```

Por ejemplo, para ver el contenido del archivo `/etc/passwd`, se escribe:

```bash
less /etc/passwd
```

Para salir del comando **less**, se presiona la tecla `q`.

## cat

El comando **cat** muestra el contenido de uno o más archivos de texto en la terminal, sin permitir desplazarse por él. También se puede usar para concatenar o crear archivos. Se usa de la siguiente manera:

```bash
cat [opciones] [archivos]
```

Por ejemplo, para mostrar el contenido de los archivos `file1.txt` y `file2.txt`, se escribe:

```bash
cat file1.txt file2.txt
```

Para crear un archivo llamado `file3.txt` con el contenido de los dos anteriores, se usa el operador `>` para redirigir la salida. Por ejemplo:

```bash
cat file1.txt file2.txt > file3.txt
```

## touch

El comando **touch** crea un archivo vacío con el nombre que se indica como argumento. Si el archivo ya existe, actualiza su fecha de modificación. Se usa así:

```bash
touch [archivo]
```

Por ejemplo, para crear un archivo llamado `test.txt`, se escribe:

```bash
touch test.txt
```

## cp

El comando **cp** copia uno o más archivos o directorios a otro destino. Se puede usar con diferentes opciones para modificar el comportamiento del comando. Algunas opciones comunes son:

- `-i`: pregunta antes de sobrescribir un archivo existente.
- `-r`: copia recursivamente los directorios y su contenido.
- `-v`: muestra el progreso de la copia.

Se usa de la siguiente forma:

```bash
cp [opciones] [origen] [destino]
```

Por ejemplo, para copiar el archivo `test.txt` al directorio `/home`, se escribe:

```bash
cp test.txt /home
```

Para copiar el directorio `docs` y todo su contenido al directorio `/home`, se usa la opción `-r`. Por ejemplo:

```bash
cp -r docs /home
```

## mv

El comando **mv** mueve o renombra uno o más archivos o directorios. Se puede usar con las mismas opciones que el comando **cp**. Se usa así:

```bash
mv [opciones] [origen] [destino]
```

Por ejemplo, para renombrar el archivo `test.txt` a `test2.txt`, se escribe:

```bash
mv test.txt test2.txt
```

Para mover el archivo `test2.txt` al directorio `/home`, se escribe:

```bash
mv test2.txt /home
```

## rm

El comando **rm** elimina uno o más archivos o directorios. Se puede usar con las mismas opciones que el comando **cp**, además de las siguientes:

- `-f`: fuerza la eliminación sin preguntar.
- `-d`: elimina un directorio vacío.

Se usa de la siguiente manera:

```bash
rm [opciones] [archivos o directorios]
```

Por ejemplo, para eliminar el archivo `test2.txt`, se escribe:

```bash
rm test2.txt
```

Para eliminar el directorio `docs` y todo su contenido, se usa la opción `-r`. Por ejemplo:

```bash
rm -r docs
```

## mkdir

El comando **mkdir** crea uno o más directorios con el nombre que se indica como argumento. Se puede usar con las siguientes opciones:

- `-p`: crea los directorios intermedios necesarios si no existen.
- `-v`: muestra el progreso de la creación.

Se usa así:

```bash
mkdir [opciones] [directorios]
```

Por ejemplo, para crear un directorio llamado `proyecto`, se escribe:

```bash
mkdir proyecto
```

Para crear una estructura de directorios como `proyecto/src/main`, se usa la opción `-p`. Por ejemplo:

```bash
mkdir -p proyecto/src/main
```

## rmdir

El comando **rmdir** elimina uno o más directorios vacíos. Se puede usar con las mismas opciones que el comando **mkdir**. Se usa así:

```bash
rmdir [opciones] [directorios]
```

Por ejemplo, para eliminar el directorio `proyecto/src/main`, se escribe:

```bash
rmdir proyecto/src/main
```

## file

El comando **file** determina el tipo de un archivo examinando su contenido. Se puede usar con las siguientes opciones:

- `-b`: no muestra el nombre del archivo al imprimir el tipo.
- `-i`: muestra el tipo MIME del archivo en lugar del tipo humano.
- `-z`: intenta examinar el contenido de los archivos comprimidos.

Se usa así:

```bash
file [opciones] [archivos]
```

Por ejemplo, para saber el tipo de un archivo llamado `readme.md`, se escribe:

```bash
file readme.md
```

Para mostrar el tipo MIME de un archivo llamado `imagen.jpg`, se usa la opción `-i`. Por ejemplo:

```bash
file -i imagen.jpg
```

## type

El comando **type** muestra cómo se interpretaría un comando o palabra clave por el shell. Se puede usar con las siguientes opciones:

- `-a`: muestra todas las ubicaciones que contienen un ejecutable con el nombre dado.
- `-p`: muestra la ruta del ejecutable si el nombre es un comando.
- `-t`: muestra una palabra que indica el tipo de comando: alias, keyword, function, builtin o file.

Se usa así:

```bash
type [opciones] [nombre]
```

Por ejemplo, para saber cómo se interpreta el comando `ls`, se escribe:

```bash
type ls
```

Para mostrar todas las ubicaciones que contienen un ejecutable llamado `python`, se usa la opción `-a`. Por ejemplo:

```bash
type -a python
```

## which

El comando **which** muestra la ruta completa de los comandos ejecutables. Se puede usar con las siguientes opciones:

- `-a`: muestra todas las coincidencias en lugar de solo la primera.
- `-s`: no muestra nada, solo devuelve un código de salida que indica si el comando existe o no.

Se usa así:

```bash
which [opciones] [comandos]
```

Por ejemplo, para saber dónde está el comando `git`, se escribe:

```bash
which git
```

Para mostrar todas las coincidencias del comando `python`, se usa la opción `-a`. Por ejemplo:

```bash
which -a python
```

## help

El comando **help** muestra información sobre los comandos integrados del shell. Se puede usar con las siguientes opciones:

- `-d`: muestra una breve descripción de cada comando.
- `-m`: muestra la información en formato de manual.

Se usa así:

```bash
help [opciones] [comando]
```

Por ejemplo, para ver la información sobre el comando `cd`, se escribe:

```bash
help cd
```

Para ver la información en formato de manual sobre el comando `echo`, se usa la opción `-m`. Por ejemplo:

```bash
help -m echo
```


## find

El comando **find** busca archivos o directorios que cumplan con ciertos criterios. Se puede usar con las siguientes opciones:

- `-name`: busca por el nombre del archivo o directorio.
- `-type`: busca por el tipo de archivo o directorio (f para archivos, d para directorios, l para enlaces simbólicos, etc.).
- `-size`: busca por el tamaño del archivo o directorio.
- `-exec`: ejecuta un comando sobre los archivos o directorios encontrados.

Se usa así:

```bash
find [opciones] [ruta] [expresión]
```

Por ejemplo, para buscar todos los archivos con extensión `.txt` en el directorio actual, se escribe:

```bash
find . -name "*.txt"
```

Para buscar todos los directorios vacíos en el directorio `/home`, se usa la opción `-type` y la expresión `-empty`. Por ejemplo:

```bash
find /home -type d -empty
```

Para buscar todos los archivos mayores de 1 MB y cambiar sus permisos a solo lectura, se usa la opción `-size` y la opción `-exec` con el comando `chmod`. Por ejemplo:

```bash
find . -size +1M -exec chmod 444 {} \;
```

## chmod

El comando **chmod** cambia los permisos de acceso a los archivos o directorios. Se puede usar con las siguientes opciones:

- `-R`: aplica el cambio de permisos de forma recursiva a todos los archivos y directorios dentro del directorio especificado.
- `-v`: muestra el progreso del cambio de permisos.

Se usa así:

```bash
chmod [opciones] [modo] [archivo o directorio]
```

El modo puede ser numérico o simbólico. El modo numérico se basa en una combinación de tres dígitos que representan los permisos de lectura (r), escritura (w) y ejecución (x) para el propietario (u), el grupo (g) y los demás usuarios (o). Por ejemplo, 644 significa que el propietario tiene permiso de lectura y escritura, el grupo tiene permiso de lectura y los demás usuarios tienen permiso de lectura. El modo simbólico se basa en los símbolos +, - y = para añadir, quitar o asignar permisos a cada categoría de usuarios. Por ejemplo, u+x significa que se añade el permiso de ejecución al propietario.

Por ejemplo, para cambiar los permisos de un archivo llamado `script.sh` a solo lectura para todos los usuarios, se puede usar el modo numérico o el modo simbólico. Por ejemplo:

```bash
chmod 444 script.sh
```

o

```bash
chmod a=r script.sh
```

Para cambiar los permisos de todos los archivos y directorios dentro del directorio `proyecto` a lectura y escritura para el propietario y lectura para el grupo y los demás usuarios, se usa la opción `-R`. Por ejemplo:

```bash
chmod -R 644 proyecto
```

## chown

El comando **chown** cambia el propietario y/o el grupo de los archivos o directorios. Se puede usar con las siguientes opciones:

- `-R`: aplica el cambio de propietario y/o grupo de forma recursiva a todos los archivos y directorios dentro del directorio especificado.
- `-v`: muestra el progreso del cambio de propietario y/o grupo.

Se usa así:

```bash
chown [opciones] [usuario]:[grupo] [archivo o directorio]
```

Por ejemplo, para cambiar el propietario y el grupo de un archivo llamado `informe.pdf` a `juan:ventas`, se escribe:

```bash
chown juan:ventas informe.pdf
```

Para cambiar solo el propietario, se omite el grupo. Por ejemplo:

```bash
chown juan informe.pdf
```

Para cambiar solo el grupo, se omite el usuario. Por ejemplo:

```bash
chown :ventas informe.pdf
```

Para cambiar el propietario y el grupo de todos los archivos y directorios dentro del directorio `proyecto` a `ana:desarrollo`, se usa la opción `-R`. Por ejemplo:

```bash
chown -R ana:desarrollo proyecto
```
## head

El comando **head** muestra las primeras líneas de un archivo o de la entrada estándar. Se puede usar con las siguientes opciones:

- `-n`: especifica el número de líneas a mostrar. Por defecto son 10.
- `-c`: especifica el número de bytes a mostrar.
- `-q`: no muestra los nombres de los archivos.
- `-v`: muestra los nombres de los archivos.

Se usa así:

```bash
head [opciones] [archivos]
```

Por ejemplo, para mostrar las primeras 5 líneas del archivo `readme.md`, se escribe:

```bash
head -n 5 readme.md
```

Para mostrar los primeros 20 bytes del archivo `readme.md`, se escribe:

```bash
head -c 20 readme.md
```

## tail

El comando **tail** muestra las últimas líneas de un archivo o de la entrada estándar. Se puede usar con las mismas opciones que el comando `head`, además de:

- `-f`: sigue mostrando las nuevas líneas que se añaden al final del archivo.
- `+n`: muestra las líneas a partir de la n-ésima.

Se usa así:

```bash
tail [opciones] [archivos]
```

Por ejemplo, para mostrar las últimas 10 líneas del archivo `readme.md`, se escribe:

```bash
tail readme.md
```

Para mostrar las líneas desde la 15 hasta el final del archivo `readme.md`, se escribe:

```bash
tail +15 readme.md
```

## grep

El comando **grep** busca una cadena de texto en uno o más archivos y muestra las líneas que la contienen. Se puede usar con las siguientes opciones:

- `-i`: ignora las diferencias entre mayúsculas y minúsculas.
- `-n`: muestra el número de línea de cada coincidencia.
- `-v`: muestra las líneas que no contienen la cadena buscada.
- `-r`: busca recursivamente en todos los archivos de un directorio y sus subdirectorios.

Se usa así:

```bash
grep [opciones] [cadena] [archivo(s)]
```

Por ejemplo, para buscar la palabra `hola` en el archivo `saludo.txt`, se escribe:

```bash
grep hola saludo.txt
```

Para buscar la palabra `hola` en todos los archivos del directorio actual, se usa la opción `-r`. Por ejemplo:

```bash
grep -r hola .
```

## ps

El comando **ps** muestra información sobre los procesos que se están ejecutando en el sistema. Se puede usar con las siguientes opciones:

- `-a`: muestra todos los procesos de todos los usuarios.
- `-u`: muestra el nombre del usuario que inició el proceso y el uso de CPU y memoria.
- `-x`: muestra los procesos que no están asociados a una terminal.
- `-e`: muestra todos los procesos del sistema, incluyendo los del kernel.

Se usa así:

```bash
ps [opciones]
```

Por ejemplo, para ver los procesos del usuario actual, se escribe:

```bash
ps -u
```

Para ver todos los procesos del sistema con información detallada, se usa la opción `-e`. Por ejemplo:

```bash
ps -e
```

## top

El comando **top** muestra información en tiempo real sobre los procesos que se están ejecutando en el sistema, ordenados por el uso de CPU o memoria. Se puede usar con las siguientes opciones:

- `-d`: especifica el intervalo de tiempo entre cada actualización, en segundos.
- `-p`: muestra solo los procesos con los identificadores (PID) indicados.
- `-u`: muestra solo los procesos del usuario indicado.
- `-o`: ordena los procesos por el campo indicado, como `CPU`, `MEM`, `TIME`, etc.

Se usa así:

```bash
top [opciones]
```

Por ejemplo, para ver los procesos que más CPU consumen, se escribe:

```bash
top -o CPU
```

Para ver solo los procesos del usuario `root`, se usa la opción `-u`. Por ejemplo:

```bash
top -u root
```

## du

El comando **du** muestra el espacio ocupado por uno o más archivos o directorios. Se puede usar con las siguientes opciones:

- `-h`: muestra el tamaño en unidades legibles por humanos, como `K`, `M`, `G`, etc.
- `-s`: muestra solo el tamaño total de cada argumento, sin desglosar por subdirectorios.
- `-a`: muestra el tamaño de todos los archivos, no solo de los directorios.
- `-c`: muestra el tamaño total de todos los argumentos.

Se usa así:

```bash
du [opciones] [archivo(s) o directorio(s)]
```

Por ejemplo, para ver el espacio ocupado por el directorio `proyecto`, se escribe:

```bash
du proyecto
```

Para ver el espacio ocupado por el directorio `proyecto` y sus subdirectorios, se usa la opción `-h`. Por ejemplo:

```bash
du -h proyecto
```

## df

El comando **df** muestra el espacio disponible y ocupado por las particiones del disco. Se puede usar con las siguientes opciones:

- `-h`: muestra el tamaño en unidades legibles por humanos, como `K`, `M`, `G`, etc.
- `-T`: muestra el tipo de sistema de archivos de cada partición.
- `-a`: muestra todas las particiones, incluyendo las que no tienen punto de montaje.
- `-i`: muestra el número de inodos disponibles y usados por cada partición.

Se usa así:

```bash
df [opciones]
```

Por ejemplo, para ver el espacio disponible y ocupado por las particiones del disco, se escribe:

```bash
df
```

Para ver el tipo de sistema de archivos y el número de inodos de cada partición, se usan las opciones `-T` y `-i`. Por ejemplo:

```bash
df -Ti
```
## ssh

El comando **ssh** permite establecer una conexión segura con un servidor remoto usando el protocolo Secure Shell. Se puede usar para acceder a un repositorio de GitHub o para ejecutar comandos en el servidor. Se puede usar con las siguientes opciones:

- `-i`: especifica el archivo que contiene la clave privada para la autenticación.
- `-p`: especifica el puerto al que se quiere conectar.
- `-v`: muestra información detallada sobre la conexión.

Se usa así:


```bash
ssh [opciones] [usuario@]host
```

Por ejemplo, para conectarse al servidor de GitHub usando la clave privada `id_rsa`, se escribe:

```bash
ssh -i id_rsa git@github.com
```

## scp

El comando **scp** permite copiar archivos o directorios entre un servidor remoto y la máquina local usando el protocolo Secure Shell. Se puede usar para subir o descargar archivos de un repositorio de GitHub. Se puede usar con las siguientes opciones:

- `-i`: especifica el archivo que contiene la clave privada para la autenticación.
- `-p`: preserva los atributos de los archivos copiados.
- `-r`: copia recursivamente los directorios y sus contenidos.
- `-v`: muestra información detallada sobre la copia.

Se usa así:

```bash
scp [opciones] origen destino
```

Por ejemplo, para copiar el archivo `readme.md` desde el repositorio local al servidor de GitHub, se escribe:

```bash
scp -i id_rsa readme.md git@github.com:usuario/repositorio.git
```

Para copiar el directorio `proyecto` desde el servidor de GitHub al directorio local `~/Documentos`, se usa la opción `-r`. Por ejemplo:

```bash
scp -r -i id_rsa git@github.com:usuario/proyecto.git ~/Documentos
```

## tar

El comando **tar** permite crear o extraer archivos comprimidos en formato tar. Se puede usar para empaquetar varios archivos o directorios en uno solo, lo que facilita su transporte o almacenamiento. Se puede usar con las siguientes opciones:

- `-c`: crea un archivo tar.
- `-x`: extrae un archivo tar.
- `-f`: especifica el nombre del archivo tar.
- `-v`: muestra los nombres de los archivos procesados.
- `-z`: comprime o descomprime el archivo tar usando gzip.

Se usa así:

```bash
tar [opciones] [archivo]
```

Por ejemplo, para crear un archivo tar llamado `proyecto.tar.gz` que contenga el directorio `proyecto` y sus subdirectorios, se usan las opciones `-c`, `-f` y `-z`. Por ejemplo:

```bash
tar -czf proyecto.tar.gz proyecto
```

Para extraer el contenido del archivo tar `proyecto.tar.gz` en el directorio actual, se usan las opciones `-x`, `-f` y `-z`. Por ejemplo:

```bash
tar -xzf proyecto.tar.gz
```

## gzip

El comando **gzip** permite comprimir o descomprimir archivos usando el algoritmo de compresión gzip. Se puede usar para reducir el tamaño de los archivos y ahorrar espacio en disco o en la red. Se puede usar con las siguientes opciones:

- `-d`: descomprime el archivo.
- `-k`: conserva el archivo original sin comprimir.
- `-l`: muestra información sobre el archivo comprimido.
- `-v`: muestra el nombre y el porcentaje de compresión del archivo.

Se usa así:

```bash
gzip [opciones] [archivo]
```

Por ejemplo, para comprimir el archivo `readme.md` y reemplazarlo por `readme.md.gz`, se escribe:

```bash
gzip readme.md
```

Para descomprimir el archivo `readme.md.gz` y conservar el original, se usa la opción `-k`. Por ejemplo:

```bash
gzip -dk readme.md.gz
```

## unzip

El comando **unzip** permite extraer archivos comprimidos en formato zip. Se puede usar para descomprimir archivos descargados de Internet o enviados por correo electrónico. Se puede usar con las siguientes opciones:

- `-d`: especifica el directorio donde se extraerán los archivos.
- `-l`: muestra el contenido del archivo zip sin extraerlo.
- `-v`: muestra información detallada sobre el archivo zip y los archivos extraídos.

Se usa así:

```bash
unzip [opciones] [archivo]
```

Por ejemplo, para extraer el contenido del archivo zip `proyecto.zip` en el directorio actual, se escribe:

```bash
unzip proyecto.zip
```

Para extraer el contenido del archivo zip `proyecto.zip` en el directorio `~/Documentos`, se usa la opción `-d`. Por ejemplo:

```bash
unzip -d ~/Documentos proyecto.zip
```

## wget

El comando **wget** permite descargar archivos o páginas web desde Internet. Se puede usar para obtener recursos de GitHub o de otras fuentes. Se puede usar con las siguientes opciones:

- `-O`: especifica el nombre del archivo de salida.
- `-P`: especifica el directorio donde se guardará el archivo descargado.
- `-q`: no muestra mensajes ni indicadores de progreso.
- `-v`: muestra información detallada sobre la descarga.

Se usa así:

```bash
wget [opciones] [url]
```

Por ejemplo, para descargar el archivo `readme.md` desde el repositorio de GitHub `usuario/proyecto.git` y guardarlo como `proyecto_readme.md` en el directorio actual, se usan las opciones `-O` y `-q`. Por ejemplo:

```bash
wget -O proyecto_readme.md -q https://raw.githubusercontent.com/usuario/proyecto.git/master/readme.md
```

## history

El comando **history** permite mostrar o manipular el historial de comandos ejecutados en la terminal. Se puede usar para revisar o repetir los comandos anteriores. Se puede usar con las siguientes opciones:

- `-c`: borra el historial de comandos.
- `-d`: elimina una entrada del historial especificando su número.
- `-r`: lee el historial de comandos desde un archivo.
- `-w`: escribe el historial de comandos a un archivo.

Se usa así:

```bash
history [opciones] [número]
```

Por ejemplo, para mostrar los últimos 10 comandos ejecutados, se escribe:

```bash
history 10
```

Para repetir el comando número 5 del historial, se usa el signo de exclamación. Por ejemplo:

```bash
!5
```

## su

El comando **su** permite cambiar de usuario en la terminal. Se puede usar para ejecutar comandos con los privilegios de otro usuario. Se puede usar con las siguientes opciones:

- `-`: inicia una sesión de inicio para el nuevo usuario.
- `-c`: ejecuta un comando como el nuevo usuario y luego vuelve al usuario anterior.
- `-l`: muestra información sobre el nuevo usuario.

Se usa así:

```bash
su [opciones] [usuario]
```

Por ejemplo, para cambiar al usuario `root`, se escribe:

```bash
su root
```

Para ejecutar el comando `ls` como el usuario `root` y luego volver al usuario actual, se usa la opción `-c`. Por ejemplo:

```bash
su -c ls root
```

## sudo

El comando **sudo** permite ejecutar un comando como otro usuario, normalmente como el superusuario o administrador. Se puede usar para realizar tareas que requieren permisos especiales. Se puede usar con las siguientes opciones:

- `-u`: especifica el usuario como el que se quiere ejecutar el comando.
- `-l`: muestra los comandos que se pueden ejecutar con sudo.
- `-k`: invalida la contraseña almacenada en caché y solicita una nueva.
- `-v`: verifica la contraseña almacenada en caché y la actualiza.

Se usa así:

```bash
sudo [opciones] [comando]
```

Por ejemplo, para ejecutar el comando `apt update` como el superusuario, se escribe:

```bash
sudo apt update
```

Para ejecutar el comando `ls` como el usuario `juan`, se usa la opción `-u`. Por ejemplo:

```bash
sudo -u juan ls
```

:)









