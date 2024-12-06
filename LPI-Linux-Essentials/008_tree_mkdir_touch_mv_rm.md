
# Crear y borrar ficheros y directorios 

<br>

## Crear directorios directamente en el pwd o con ruta especifica

~~~
donsilver@debian:~$ mkdir fotos	# se crea el directorio fotos
donsilver@debian:~$ mkdir mis_imagenes
donsilver@debian:~$ cd fotos
donsilver@debian:~/fotos$ mkdir vacaciones # se crea el directorio vacaciones dentro del directorio vacaciones
donsilver@debian:~/fotos$ mkdir navidad # se crea el directorio navidad dentro de directorio fotos
donsilver@debian:~$ cd .. # regresamos al directorio home/donsilver
donsilver@debian:~$ mkdir peliculas/terror # nos manda un mensaje de error porque el 
#mkdir: nos e puede crear el directorio <<peliculas/terror>>: No existe el fichero o directorio # directorio peliculas no existe
donsilver@debian:~$ mkdir -p peliculas/terror # para poder crear directorio sobre rutas que no existen es necesario aplicar el parametro -p (parents) para poder crearlo, aqui ya nos crea tanto el directorio padre como el hijo
donsilver@debian:~$ mkdir -p peliculas/comedia/2024/donsilver/ # crea una ruta de 4 directorios
donsilver@debian:~$ cd peliculas/comedia/2024/donsilver/ 
donsilver@debian:~$ cd ~
~~~

<br>

## Crear ficheros

~~~
donsilver@debian:~$ touch fichero # todos estos ejemplos crean ficheros
donsilver@debian:~$ touch mi_fichero
donsilver@debian:~$ > mi_fichero2
~~~

<br>

## Mover y renombrar

~~~
donsilver@debian:~$ mv mi_fichero mi-carta   # se utiliza para mover o cambiar de nombre
donsilver@debian:~$ mv fotos mis_imagenes
donsilver@debian:~$ mv mi-carta mis_imagenes/
donsilver@debian:~$ mv mi_fichero2 mis_imagenes/mi-carta2 # o las 2 cosas al mismo tiempo
~~~

<br>

## Remover

~~~
rm fichero # remueve un fichero
rm -r mis_imagenes/  # para remover directorios es necesario aplicar el parametro -r (recursive)
~~~

<br>

## Comando tree

~~~
donsilver@debian:~$ tree # muestra el contenido del pwd en modo de arbol tanto directorios como su contenido. funciona como ls, se puede introducir una ruta de directorio como argumento para listar su contenido.
~~~