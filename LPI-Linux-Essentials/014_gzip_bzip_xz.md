### Comandos para comprimir y descomprimir.

Hay varios comandos para comprimir y descomprimir, el funcionamiento básico es el mismo en los más conocidos:
- `gzip`
- `bzip`
- `xz`

Si le indicamos uno o varios ficheros los comprimirán. Para conservar el original indicamos la opción `-k`. Para descomprimir podemos usar la opción `-d` o usar un comando que añade `un` al nombre original (gunzip, bunzip, unxz)

Ejemplos:

```console
:~$ gzip fichero
:~$ gunzip fichero.gz
:~$ bzip -k fichero
:~$ bzip -d fichero.bz
```

Lo ponemos en práctica:

```console
debian:~/ficheros/fotos$ gzip logo-ubuntu.gif
debian:~/ficheros/fotos$ ll logo*
-rw-r--r-- 1 donsilver donsilver 3.2K nov 26  2009 logo-ubuntu.gif.gz
debian:~/ficheros/fotos$ gzip -k tux-*
debian:~/ficheros/fotos$ ll tux-*
-rw-r--r-- 1 donsilver donsilver 3.8K nov 26  2009 tux-clasico.jpeg
-rw-r--r-- 1 donsilver donsilver 3.8K nov 26  2009 tux-clasico.jpeg.gz
-rw-r--r-- 1 donsilver donsilver  48K nov 26  2009 tux-moderno.png
-rw-r--r-- 1 donsilver donsilver  48K nov 26  2009 tux-moderno.png.gz
debian:~/ficheros/fotos$ gunzip logo-ubuntu.gif.gz
debian:~/ficheros/fotos$ bzip -k logo-ubuntu.gif
-bash: bzip: orden no encontrada
debian:~/ficheros/fotos$ xz -k logo-ubuntu.gif
debian:~/ficheros/fotos$ xz -d logo-ubuntu.gif.xz
xz: logo-ubuntu.gif: El fichero ya existe
debian:~/ficheros/fotos$ ll
total 420K
drwxr-xr-x 4 donsilver donsilver 4.0K sep 24 10:14 ./
drwxr-xr-x 5 donsilver donsilver 4.0K sep 24 09:55 ../
-rw-r--r-- 1 donsilver donsilver 2.2K nov 26  2009 escritorio-ubuntu.jpeg
-rw-r--r-- 1 donsilver donsilver    0 sep 17 12:08 .fichero-oculto.txt
-rw-r--r-- 1 donsilver donsilver 3.2K nov 26  2009 logo-ubuntu.gif
-rw-r--r-- 1 donsilver donsilver 3.2K nov 26  2009 logo-ubuntu.gif.xz
drwxr-xr-x 2 donsilver donsilver 4.0K nov 26  2009 personales/
drwxr-xr-x 2 donsilver donsilver 4.0K sep 17 11:36 seleccion/
-rw-r--r-- 1 donsilver donsilver 286K nov 26  2009 shell-commands.gif
-rw-r--r-- 1 donsilver donsilver 3.8K nov 26  2009 tux-clasico.jpeg
-rw-r--r-- 1 donsilver donsilver 3.8K nov 26  2009 tux-clasico.jpeg.gz
-rw-r--r-- 1 donsilver donsilver  48K nov 26  2009 tux-moderno.png
-rw-r--r-- 1 donsilver donsilver  48K nov 26  2009 tux-moderno.png.gz
```