### Comando Echo
echo : imprime cadenas de texto en pantalla
~~~
donsilver@debian:~$ echo Hola Mundo
Hola Mundo
donsilver@debian:~$ echo "Hola Mundo"
Hola Mundo
~~~
echo -e : el parametro (o conocido tambien en ingles como flag) -e le indica a echo que interpretara los caracteres especiales, como salto de linea '\n' o tabulador '\t' 
~~~
donsilver@debian:~$ echo -e "Hola \n Mundo"
Hola
Mundo
echo -e "Hola \t Mundo"
Hola    Mundo
~~~

Uso de comillas simples y dobles  
En este ejemplo vemos como pueden ser utilizadas segun el caso, aqui las comillas dobles interpretan la variable de entorno como es, una variable, y muestra su contenido.
~~~
donsilver@debian:~$ echo "$USER"
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
~~~
al utilizar las comillas simples interpreta todo lo que hay dentro como una cadena de texto.
~~~
donsilver@debian:~$ echo '$PATH'
$PATH
~~~
~~~
donsilver@debian:~$ echo "rutas ==> $PATH"
rutas ==> /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
donsilver@debian:~$ echo 'rutas ==> $PATH'
rutas ==> $PATH
~~~
