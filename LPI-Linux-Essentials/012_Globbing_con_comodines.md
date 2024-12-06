## Globbing con comodines.
El globbing viene de glob que es una abreviatura de global command, una libreria escrita en C y muy utilizada en entornos Unix y GNU/Linux.  
Se utilza par hacer referencia a cosas genericas, o dicho de otro modo, a elementos que tienen un patron en comun.  

### Asterisco (\*)
Con el asterisco podemos sustituir cualquier cadena de texto de cualquier longitud, se puede utilizar solo para hacer referencia a la totalidad de los ficheros o acompañado con el patron que varios ficheros tienen en comun.  
En vez de hacer esto:
~~~
donsilver@debian:~/ficheros$ cd fotos/
donsilver@debian:~/ficheros/fotos$ ls
escritorio-ubuntu.jpeg  logo-ubuntu.gif  personales  shell-commands.gif  tux-clasico.jpeg  tux-moderno.png
donsilver@debian:~/ficheros/fotos$ mkdir seleccion
donsilver@debian:~/ficheros/fotos$ cp escritorio-ubuntu.jpeg logo-ubuntu.gif shell-commands.gif tux-clasico.jpeg tux-moderno.png seleccion/
~~~
Hariamos esto, aqui estamos haciendo referencia a todos los ficheron que terminan con extension de imagen:
~~~
donsilver@debian:~/ficheros$ cd fotos/
donsilver@debian:~/ficheros/fotos$ ls
escritorio-ubuntu.jpeg  logo-ubuntu.gif  personales  shell-commands.gif  tux-clasico.jpeg  tux-moderno.png
donsilver@debian:~/ficheros/fotos$ mkdir seleccion
donsilver@debian:~/ficheros/fotos$ cp *.gif *.jpeg *.png seleccion/
~~~

### Interrogación (?)
Con la interrogación sustitiuye cualquier caracter, pero solamente uno.
~~~
donsilver@debian:~$ cd ficheros/
donsilver@debian:~/ficheros$ ls
casa.doc  cesa.doc  cosa.doc  cosa.txr  cosa.txt  csa  documentos  fotos  musica
donsilver@debian:~/ficheros$ ls c*sa*
casa.doc  cesa.doc  cosa.doc  cosa.txr  cosa.txt  csa
donsilver@debian:~/ficheros$ ls c?sa*
casa.doc  cesa.doc  cosa.doc  cosa.txr  cosa.txt
donsilver@debian:~/ficheros$ ls c?sa?
ls: no se puede acceder a 'c?sa?': No existe el fichero o el directorio
donsilver@debian:~/ficheros$ ls c?sa?*
casa.doc  cesa.doc  cosa.doc  cosa.txr  cosa.txt
~~~
~~~
donsilver@debian:~/ficheros$ cd documentos/informes/
donsilver@debian:~/ficheros/documentos/informes$ ls -l
total 12
drwxr-xr-x 2 donsilver donsilver 4096 nov 26  2009 estadisticas
-rw-r--r-- 1 donsilver donsilver   13 nov 26  2009 informe-2008.txt
-rw-r--r-- 2 donsilver donsilver   13 nov 26  2009 informe-2009.txt
donsilver@debian:~/ficheros/documentos/informes$ ls informe-200?.txt
informe-2008.txt  informe-2009.txt
~~~

### Corchetes (\[]) y Clases de Caracteres
Cualquier caracter dentro de los que se incluyen en los corchetes
- Rangos: se indica el inicio y el final separados por un guion
- Negacion: se pone un acento circunflejo (^) al inicio e indica los caracteres que no son validos
- Clases: Grupos de caracteres predefinidos.
	- \[:alnum:] = Letras y numeros.
	- \[:alpha:] = Letras mayusculas y minusculas.
	- \[:blank:] = Espacios y tabulaciones.
	- \[:digit:] = Numeros(0123456789).
	- \[:lower:] = Letras minusculas (a-z).
	- \[:upper:] = Letras mayusculas (A-Z).

~~~
donsilver@debian:~/backups$ ls -l
total 0
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:46 backup_1999-08-25_usuario1.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:46 backup_1999-08-25_usuario20.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:46 backup_1999-08-25_usuario2.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:46 backup_2019-02-12_usuario1.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:47 backup_2019-02-12_usuario2.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:46 backup_2019-02-12_usuario3.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:47 backup_2019-02-12_usuario50.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:47 backup_2019-02-12_usuario5.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:47 backup_2019-02-12_usuario8.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:47 backup_2019-02-12_usuario9.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:47 backup_2019-11-25_usuario1.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:48 backup_2019-11-26_usuario1.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:48 backup_2019-11-27_usuario1.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:48 backup_2019-11-30_usuario1.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:48 backup_2019-12-30_usuario1.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:49 backup_2020-02-03_usuario1.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:49 backup_2020-05-03_usuario1.tar.gz
donsilver@debian:~/backups$ ls -l backup_20??-??-?[24680]*
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:46 backup_2019-02-12_usuario1.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:47 backup_2019-02-12_usuario2.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:46 backup_2019-02-12_usuario3.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:47 backup_2019-02-12_usuario50.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:47 backup_2019-02-12_usuario5.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:47 backup_2019-02-12_usuario8.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:47 backup_2019-02-12_usuario9.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:48 backup_2019-11-26_usuario1.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:48 backup_2019-11-30_usuario1.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:48 backup_2019-12-30_usuario1.tar.gz
donsilver@debian:~/backups$ ls -l *[[:digit:]]?.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:46 backup_1999-08-25_usuario20.tar.gz
-rw-r--r-- 1 donsilver donsilver 0 sep 18 09:47 backup_2019-02-12_usuario50.tar.gz
donsilver@debian:~/backups$ ls -l *[0-5],tar.gz
ls: no se puede acceder a '*[0-5],tar.gz': No existe el fichero o el directorio
~~~