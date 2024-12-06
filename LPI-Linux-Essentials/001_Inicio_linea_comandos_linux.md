# INTRODUCCION A LA LINEA DE COMANDOS EN LINUX (BASH)
(del curso Udemy.com: Certificación LPI Linux Essentials: Temario oficial Completo, de Antonio Sanchez Corbalan)
---

Los comando, en general, se ejecutan con la siguiente sintaxis:  

**comando \[parametros\] argumentos**  

por ejemplo listamos el contenido de un directorio:  

```console
donsilver@debian:~ $ ls -l Descargas/
```  

Existen rutas absolutas y relativas, las absolutas son las que se muestran o ejecutan desde el directorio raiz, por ejemplo:
~~~
donsilver@debian:~$ ls -l /home/donsilver/Descargas
~~~

Las rutas relativas serian indicando la ruta a partir del directorio actual o con unos "comodines" que veremos mas adelante:
~~~
donsilver@debian:~$ ls -l Descargas
~~~

la virgulilla \[\~\] nos indica que estamos en nuestro directorio de Home
~~~
donsilver@debian:~$ en este caso nuestro directorio seria /home/donsilver
~~~

Los comodines que mencione anteriormente son el punto (.) y el doble-punto (..), el punto hace referencia al mismo directorio actual en el que se encuentra el prompt, el doble-punto hace referencia al directorio "Padre", es decir al directorio que esta sobre el directorio actual en la jerarquia o dicho mas simple el directorio que contiene al directorio actual.

Algunos comandos basicos que debemos aprender:  

pwd : que signfifica print work directory imprime el directorio actual en el que esta el prompt
~~~
donsilver@debian:~$ pwd
/home/donsilver
~~~

ls : lista los ficheros y directorios contenidos en el directorio especificado de manera horizontal, en este caso si argumentos muestra el contenido del directorio actual
~~~
donsilver@debian:~$ ls
~~~

ls -l : nos lista el contenido de manera vertical, con mas detalles como el tipo de archivo, los permisos, el dueño del fichero/directorio, el tamaño en bytes, la fecha y la hora de creación.
~~~
donsilver@debian:~$ ls -l
~~~

ls -lh : nos muestra lo mismo que ls -l pero en vez de mostrarnos el peso del archivo/directorio en bytes nos muestra en una forma mas "humana", es decir que el usuario pueda interpretar mejor el tamaño.
~~~
donsilver@debian:~$ ls -lh
~~~

ls -a : nos muestra el contenido absoluto, es decir que nos muestra los archivios visibles y los que estan ocultos
~~~
donsilver@debian:~$ ls -a
~~~

ls -lt : lista contenido con orden por fecha
~~~
donsilver@debian:~$ ls -lt
~~~

ls -r : lista contenido en reversa
~~~
donsilver@debian:~$ ls -r
~~~

cd : change directory cambia al directorio especificado en argumentos
~~~
donsilver@debian:~$ cd ~
~~~

man : comando manual, acompañado con un comando especifico en argumentos nos muestra las paginas de manual de ese comando
~~~
donsilver@debian:~$ man pwd
~~~

clear : borra todo en pantalla dejando solo el prompt como al principio
~~~
donsilver@debian:~$ clear
~~~
