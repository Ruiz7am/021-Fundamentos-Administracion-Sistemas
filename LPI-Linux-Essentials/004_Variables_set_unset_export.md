### Comando Set
Set muestra o modifica la configuracion de nuestro entorno. Sin parametros visualiza variables del sistema y con -o una lista de las opciones y sus estados.
~~~
donsilver@debian:~$ set
~~~

### Comando Export
Export crea o modifica variables de entorno
~~~
donsilver@debian:~$ export NOMBRE=Silverio
donsilver@debian:~$ echo $NOMBRE
Silverio
~~~


Unset elimina una variable de entorno.
~~~
donsilver@debian:~$ unset NOMBRE
~~~


### Comando Env
Env sin parametros muestra las variables de entorno. Lo podemos usar para ejecutar un comando modificando el valor de variables de entorno.
~~~
donsilver@debian:~$ env PATH=/new/path /bin/bash/
~~~


La variable PATH define los directorios donde se buscará el comando que intentaremos ejecutar. Si el fichero esta en cualquier otro lugar tendremos que especificar la ruta. Cuando esta en el directorio actual podemos ejecutarlo con el comodin de directorio actual: ./comando
echo $PATH

History muestra las ultimas ordenes que hemos ejecutado, Al cerrar la sesion se guarda en el directorio de usario en un fichero de nombre .bash_history
~~~
donsilver@debian:~$ history
donsilver@debian:~$ cat /home/donsilver/.bash_history
~~~
