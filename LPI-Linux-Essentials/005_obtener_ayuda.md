## Obtener ayuda en la terminal
Hay muchas maneras de obtener ayuda, el que ya hemos visto es el de man.  

*man \'comando\'*. 

Tambien esta un comando mas moderno el cual es info. 

*info \'comando\'*. 

Para encontrar en donde esta un fichero o directorio es locate. 

*locate "archvo a buscar"*. 

Los programas tienen su documentacion mas extensa ubicada en /usr/share/doc. 

Los comandos regularmente tienen un parametro de ayuda que es -h  o --help, esta es una ayuda rapida para poder utlizar el programa. 

*comando -h. 
comando --help*. 

Otros comandos tambien pueden ser whatis, apropos, whereis. 

El comando man tiene:
- Secciones
- Categorias
- Navegar por la info
- Opciones mas importantes como:
    - \-f: equivalente a whatis
    - \-k: equivalente a apropos. 

### Estructura de una pagina de manual. 

|Seccion          |Descripcion                                 |
|------------------|---------------------------------------------|
|NAME              |Nombre del comando y breve descripcion       |
|SYNOPSIS          |Descripcion de la sintaxis del comando       |
|DESCRIPTION       |Descripcion de los efectos del comando       |
|OPTIONS           |Opciones disponibles                         |
|ARGUMENTS         |Argumentos disponibles                       |
|FILES             |Archivos auxiliares                          |
|EXAMPLES          |Una muestra de la linea de comando           |
|SEE ALSO          |Referencias cruzadas a los temas relacionados|
|DIAGNOSTICS       |Mensajes de advertencia y error              |
|COPYRIGHT         |Autor(es) del comando                        |
|BUGS              |Cualquier limitacion conocida del comando    |

 Categorias
 Categoria           # Descripcion
    1                Comando generales
    2                Llamadas del sistema
    3                Llamadas a librerias
    4                Ficheros especiales (normalmente dispositivos en /dev)
    5                Formatos de fichero y convenciones
    6                Juegos
    7                Miscelanea
    8                Comandos de administracion de sistema y demonios
    9                Rutinas de kernel

 info
 Muestra una gran cantidad de informacion que incluyen hiperenlaces que podremos usar para naegar por distintos lugares. Con el caracter ? obtendremos mas ayuda sobre la manera de movernos por la informacion

 updatedb && locate 
 Utiliza una base de datos para localizar elementos en el disco. Podemos usar comodines o expresiones regulares para encontrar varias posibilidades. Su base de datos se actualiza automaticamente, pero lo podemos hacer manualmente con el comando updatedb
update
locate passwd
 Dentro de las paginas man es posible buscar informacion mediante patrones de cadena 
comenzando a escribir slash (/) seguido de el patron que deseamos encontrar
 tambien es posible encontrar todas las opciones de busqueda escribiendo (h) la cual nos dara muchas opciones que no son mas que las que nos proporciona el comando less.
 para ver la primera linea de las paginas man se utiliza el flag -f
man -f ls
 para hacer una busqueda generica mediante un patron o keyword utilizamos el parametro -k, aqui dependiendo el idioma en el que busquemos es la informacion que nos aparecera.
man -k usuarios 
 si hacemos man -f es lo mismo que whatis, igual que si hacemos man -k es lo mismo que apropos
 find
find / -iname "apach2.conf"
