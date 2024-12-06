### Mostrar texto: comandos cat, more y less.

#### Comando cat.

`cat` : Puede concatenar ficheros de texto. Se suele usar para mostrar su contenido en pantalla.  
Con el parámetro `-n` muestra el número de línea.

```console
debian:~/ficheros/fotos$ cat /etc/issue
Debian GNU/Linux 12 \n \l

```
```console
debian:~/ficheros/fotos$ cat -n /etc/issue
     1  Debian GNU/Linux 12 \n \l
     2
```
```console
debian:~/ficheros/fotos$ cat -n /etc/network/interfaces
     1  # This file describes the network interfaces available on your system
     2  # and how to activate them. For more information, see interfaces(5).
     3
     4  source /etc/network/interfaces.d/*
     5
     6  # The loopback network interface
     7  auto lo
     8  iface lo inet loopback
```

Este comando originariamente se utiliza para concatenar elementos. Pero se puede utilizar también para mostrar el contenido de un fichero. Pero tiene un inconveniente, los ficheros que tienen muchas líneas son mas incomodos de leer por que no caben en la pantalla o si buscamos una líena en concreto.

#### Comando more.

Para poder leer mejor el contenido de un fichero tenemos otros comando como `more`:

```console
debian:~/ficheros/fotos$ sudo more /var/log/boot.log
[sudo] contraseña para donsilver:
[  OK  ] Started NetworkManager.service - Network Manager.
[  OK  ] Reached target network.target - Network.
         Starting NetworkManager-wait-online.service - Network Manager Wait Online...
         Starting cups.service - CUPS Scheduler...
         Starting ssh.service - OpenBSD Secure Shell server...
         Starting systemd-user-sessions.service - Permit User Sessions...
[  OK  ] Finished systemd-user-sessions.service - Permit User Sessions.
         Starting plymouth-quit-wait.service - Hold until boot process finishes up...
         Starting systemd-hostnamed.service - Hostname Service...
[  OK  ] Started cups.service - CUPS Scheduler.
[  OK  ] Started ModemManager.service - Modem Manager.
[  OK  ] Started udisks2.service - Disk Manager.
[  OK  ] Started ssh.service - OpenBSD Secure Shell server.
[  OK  ] Started systemd-hostnamed.service - Hostname Service.
[  OK  ] Finished e2scrub_reap.service - Remove Stale Online ext4 Metadata Check Snapshots.
[  OK  ] Listening on systemd-rfkill.socket - Load/Save RF Kill Switch Status /dev/rfkill Watch.
         Starting NetworkManager-dispatcher.service - Network Manager Script Dispatcher Service...
         Stopping cups.service - CUPS Scheduler...
[  OK  ] Stopped cups.service - CUPS Scheduler.
[  OK  ] Stopped cups.path - CUPS Scheduler.
         Stopping cups.path - CUPS Scheduler...
[  OK  ] Started cups.path - CUPS Scheduler.
[  OK  ] Closed cups.socket - CUPS Scheduler.
         Stopping cups.socket - CUPS Scheduler...
[  OK  ] Listening on cups.socket - CUPS Scheduler.
         Starting cups.service - CUPS Scheduler...
[  OK  ] Started NetworkManager-dispatcher.service - Network Manager Script Dispatcher Service.
[  OK  ] Started cups.service - CUPS Scheduler.
[  OK  ] Finished logrotate.service - Rotate log files.
--Más--(79%)
```

El cual nos dará la opción de movernos por pantalla, utilizando la tecla `enter` para avanzar **línea por línea** o con la tecla  `space-bar` para movernos **varias líneas**.  
También nos muestra el porcentaje del fichero que se a alcanzado a mostrar.  
Para **salir** solamente presionamos la tecla `q`.  
Con la tecla `h` nos muestra opciones que podemos utilizar dentro del fichero.

#### Comando less

El comando `less` hace lo mismo que more pero con mucho mas opciones, adicional a eso tenemos que nos interna en, por decirlo de una manera, "en otra pantalla", dentro de la misma terminal en donde no podemos ver el prompt y podemos utlizar las mismas teclas de navegación y de ayuda que more **(enter, space-bar, q y h)**

