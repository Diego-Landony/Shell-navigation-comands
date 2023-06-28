# Comandos de Linux (spanish)

Este repositorio contiene una lista de comandos útiles de Linux y sus posibles combinaciones.


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
