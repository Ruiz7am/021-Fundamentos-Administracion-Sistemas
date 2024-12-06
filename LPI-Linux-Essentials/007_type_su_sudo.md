### Comando Type
El comando type nos permite determinar que tipo de comando es, si es un ejecutable, un comando interno (builtin) o si es externo o un alias.
cd es un comando interno de la shell
~~~
donsilver@lubuntu:~$ type cd
cd es una orden interna del intérprete de ordenes 		
~~~
El comando whereis no nos muestra ningun fichero relacionado con cd porque los comandos internos se encunetran incluidos dentro del propio shell:
~~~
 donsilver@lubuntu:~$ whereis cd
 cd:
~~~
El comando ls es un fichero ejecutable
~~~
donsilver@lubuntu:~$ whereis ls
ls: /usr/bin/ls /usr/share/man/man1/ls.1.gz    
~~~
 donsilver@lubuntu:~$ type ls                               	# ademas el comando ls tiene un alias que hacer
 #ls es un alias de `ls --color=auto' 					        # que hace referencia al mismo comando pero con
																# un parametro de salida de color

 No todos los usuarios del sistema pueden ejecutar los mismos comandos, por ejemplo
 ejecutando el comando adduser desde una cuenta de usuario estandar obtendriamos la siguiente salida:
 donsilver@lubuntu:~$ adduser
 adduser: Sólo root puede añadir un usuario o un grupo al sistema.    # nos indica que nuestro usuario no tiene
																	  # los permisos necesarios para ejecutar el
																	  # el comando

 Para poder ejecutar comandos con permisos de administrador, se necesita aplicar otro comando antes, dependiendo de la distro, puede variar el comando. 
La variable de entorno $PATH contiene los directorios en donde el interprete buscará los comandos solicitados
 por el usuario, dependiendo el usuario la variable $PATH tendrá unos u otros directorios.
 En este ejemplo el usuario estandar donsilver tendrá los siguientes directorios:
 donsilver@debian:~$ echo $PATH                                    
 /usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games      

 El comando por ejemplo en debian seria asi:
 donsilver@debian:~$ su  								       # se aplica el comando su	
 Contraseña:   										           # se ingresa la contraseña de root
 root@debian:/home/donsilver# echo $PATH			           # el usuario cambia a root pero con los mismos
 /usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games      # directorios de la variable $PATH

  Para poder ingresar totalmente a los permisos de administrador el comando en debian seria:
 donsilver@debian:~$ su -     								   # el mismo comando su pero con un guion el cual
 Contraseña:   												   # nos envia al directorio de root y nos muestra
 root@debian:~# pwd  										   # el contenido de la variable $PATH diferente
 /root   													   # al del usuario estandar.
 root@debian:~# echo $PATH
 /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin  

  Existe tambien un comando para ejecutar comandos con permisos de root desde usuarios estandar sin tener que
  logearse en la cuenta de root o elevar los permisos. El comando en cuestion es sudo:
 donsilver@debian:~$ cat /etc/shadow					# al ejecutar el cat sobre este fichero que tiene solo
 cat: /etc/shadow: Permiso denegado						# permisos de root, nos muestra que no tenemos acceso al
 donsilver@debian:~$ sudo cat /etc/shadow               # como usuario estandar, pero aplicando el comando sudo
														# al inicio nos pedirá la contraseña de usuario y 
														# podremos ejecutarlo, siempre y cuando el usuario
														# estandar se encuentre en el grupo sudoers.

Tambien podemos aplicar sudo para ingresar a la cuenta de root
donsilverio@debian:~$ sudo -i
Contraseña:
root@debian:~# whoami
root
