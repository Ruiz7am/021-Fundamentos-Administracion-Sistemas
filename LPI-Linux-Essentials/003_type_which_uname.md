## Tipos de comandos.

### Comando Type
El interprete BASH tiene comandos que son internos y otros que son externos, escribiendo el comando type y el comando que deseamos consultar en sus argumentos, nos dirá si es interno o externo.
~~~
type cd
type find 
~~~


### Comando Which
El comando which muestra la ruta absoluta del programa que le indiquemos, es decir donde se encuentra.
~~~
which ls
which man
~~~


### Comando Uname
uname muestra informacion sobre el SO, tiene diferentes parametros que podemos usar para mostrar una u otra cosa, o incluso toda la informacion
uname
~~~
uname -a
uname -s
~~~


Otra forma de obtener informacion del sistema es viendo el contenido de los archivos /etc/issue y /etc/os-release, esto lo podemos hacer mediante el comando cat
~~~
cat /etc/issue
cat /etc/os-release
~~~
