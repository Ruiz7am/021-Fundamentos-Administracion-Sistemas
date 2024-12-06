# Rutas Relativas y Rutas Absolutas

<br>

Una ruta absoluta hace referencia a un fichero o directorio desde la **raiz del sistea** de archivos

<br>

~~~
donsilver@debian:~$ ls /home/donsilver/peliculas/terror/2024/donsilver
~~~

<br>
<br>

Una ruta relativa es la que hace referencia a un fichero o directorio a partir de otra locacion dentro del sistema de archivos

<br>

~~~
donsilver@debian:~$ cd peliculas/terror/2024/donsilver
~~~

<br>
<br>

Se pueden utilizar el comodin .. para poder hacer referencia a una ruta que esta sobre del wd

<br>

~~~
donsilver@debian:~/peliculas/terror/2024/donsilver$ ls ../../../terror
2024
~~~
