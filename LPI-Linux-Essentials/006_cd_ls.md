#### Comando cd (Change Directory)
El comando cd sirve para cambiar el directorio actual o de trabajo, desde el que voy a ejecutar comandos.  

- Directorio "home"
- cd se puede usar con o sin parametros
- Uso de virgulilla (~)
- Uso del guion (-)
- Uso de los dos puntos seguidos (..)

---
descarga de ficheros con ejemplos:
wget sanchezcorbalan.es/ficheros.tar.gz
---

cambia al directorio raiz:
```console
cd /
```
cambia al directorio home del usuario:
~~~
cd ~
~~~ 
cambia al directorio contenedor del actual:
~~~		
cd ../
~~~	
regresa al directorio anterior	
~~~
cd -
~~~
#### Comando ls (List)
Opciones:  
`ls -l` :Nos muestra el contenido en modo vertical, con informacion mas extendida como el dueño del directorio/fichero, la fecha de creacion, los permisos, el tamaño de ficheros en bytes:
~~~
ls -l
total 356
-rw-r--r-- 1 donsilver donsilver   2172 nov 26  2009 escritorio-ubuntu.jpeg
-rw-r--r-- 1 donsilver donsilver   3250 nov 26  2009 logo-ubuntu.gif
drwxr-xr-x 2 donsilver donsilver   4096 nov 26  2009 personales
drwxr-xr-x 2 donsilver donsilver   4096 sep 17 11:36 seleccion
-rw-r--r-- 1 donsilver donsilver 291968 nov 26  2009 shell-commands.gif
-rw-r--r-- 1 donsilver donsilver   3820 nov 26  2009 tux-clasico.jpeg
-rw-r--r-- 1 donsilver donsilver  49105 nov 26  2009 tux-moderno.png
~~~
`ls -lh` :Nos muestra el tamaño en una forma mas entendible para el humano, en kilo, mega, giga, etc.:
~~~
ls -lh
total 356K
-rw-r--r-- 1 donsilver donsilver 2.2K nov 26  2009 escritorio-ubuntu.jpeg
-rw-r--r-- 1 donsilver donsilver 3.2K nov 26  2009 logo-ubuntu.gif
drwxr-xr-x 2 donsilver donsilver 4.0K nov 26  2009 personales
drwxr-xr-x 2 donsilver donsilver 4.0K sep 17 11:36 seleccion
-rw-r--r-- 1 donsilver donsilver 286K nov 26  2009 shell-commands.gif
-rw-r--r-- 1 donsilver donsilver 3.8K nov 26  2009 tux-clasico.jpeg
-rw-r--r-- 1 donsilver donsilver  48K nov 26  2009 tux-moderno.png
~~~
`ls -S` :Ordena el contenido dependiendo el tamaño, del mas grande al mas pequeño (size):
~~~
ls -S
shell-commands.gif  tux-moderno.png  personales  seleccion  tux-clasico.jpeg  logo-ubuntu.gif  escritorio-ubuntu.jpeg
~~~
`ls -r` Ordena el contenido de manera inversa (reverse):
~~~
ls -r
tux-moderno.png  tux-clasico.jpeg  shell-commands.gif  seleccion  personales  logo-ubuntu.gif  escritorio-ubuntu.jpeg
~~~
`ls -t` :Ordena el contenido dependiendo de la fecha, del mas reciente al mas antiguo:
~~~
ls -t
seleccion  personales  shell-commands.gif  logo-ubuntu.gif  escritorio-ubuntu.jpeg  tux-moderno.png  tux-clasico.jpeg
~~~
`ls -R` :Lista la contenido recursivamente, es decir que lista el contenido de un directorio y el contenido de todos los sub-directorios contenidos dentro de el.
~~~
ls -R
.:
escritorio-ubuntu.jpeg  logo-ubuntu.gif  personales  seleccion  shell-commands.gif  tux-clasico.jpeg  tux-moderno.png

./personales:
'con mi portatil.jpg'   en-el-monte.jpg   mi_movil.jpg   pescando.jpg   torre-de-pisa.jpg

./seleccion:
~~~
`ls -a` :Muestra todos los elementos tanto regulares como ocultos, los ficheros/directorios ocultos comienzan con un punto (.), y tambien el directorio actual como un punto y el directorio padre como dos puntos.
~~~
ls -a
.   escritorio-ubuntu.jpeg  logo-ubuntu.gif  seleccion           tux-clasico.jpeg
..  .fichero-oculto.txt     personales       shell-commands.gif  tux-moderno.png
~~~
