Title: Error en maquina virtual en #Debian
Date: 2011-09-18 20:24
Category: Linux
Tags: virtual box
Slug: error-vbox-debian
Author: abr4xas
twitter: abr4xas
Summary: Error en maquina virtual en #Debian
image: 

Kernel driver not installed (rc=-1908)

```bash
root@Genius:/home/abr4xas\# /etc/init.d/vboxdrv setup  
Stopping VirtualBox kernel modules:.  
Uninstalling old VirtualBox DKMS kernel modules:.  
Trying to register the VirtualBox kernel modules using DKMS:  
Failed, trying without DKMS ... failed!  
Recompiling VirtualBox kernel modules:.  
Starting VirtualBox kernel modules:  
modprobe vboxdrv failed. Please use 'dmesg' to find out why ...
failed!
```

-   Por lo visto, lo de hacer:

```bash
/etc/init.d/vboxdrv setup
```
no funciono... :-/ Toca hacer algo y es
instalar los dkms

-   de nuevo en consola:
```bash
apt-get install dkms
```

-   Y bueno, con esto estamos listos no? vamos a nuestra querida consola
    y hacemos:

```bash
root@Genius:/home/abr4xas\# /etc/init.d/vboxdrv setup  
Stopping VirtualBox kernel modules:.  
Uninstalling old VirtualBox DKMS kernel modules:.  
Removing old VirtualBox netadp kernel module:.  
Removing old VirtualBox netflt kernel module:.  
Removing old VirtualBox kernel module:.  
Trying to register the VirtualBox kernel modules using DKMS:Error! Your
kernel headers for kernel 3.0.0-1-686-pae cannot be found.  
Please install the linux-headers-3.0.0-1-686-pae package,  
or use the --kernelsourcedir option to tell DKMS where it's located

Failed, trying without DKMS ... failed!  
Recompiling VirtualBox kernel modules:.  
Starting VirtualBox kernel modules:  
modprobe vboxdrv failed. Please use 'dmesg' to find out why ... failed!
```

Ok, aun no damos solucion al problema :( en este caso, como pueden ver
me dice ahora que los headers para el kernel 3.0.0-1-686-pae no se
encuentran ya saben lo que debemos hacer no?

-   en consola debemos colocar:

```bash
apt-get install linux-headers-`uname -r
```

-   Esperamos a que baje todo lo que necesitamos despues de eso hacemos
    (nuevamente):

```bash
/etc/init.d/vboxdrv setup
```

Y debemos obtener algo asi como:  

```bash
Stopping VirtualBox kernel modules:.  
Uninstalling old VirtualBox DKMS kernel modules:.  
Removing old VirtualBox netadp kernel module:.  
Removing old VirtualBox netflt kernel module:.  
Removing old VirtualBox kernel module:.  
Trying to register the VirtualBox kernel modules using DKMS:.  
Starting VirtualBox kernel modules:.  
```

:D WIN!! Ya tenemos nuestro kernel con los modulos necesarios para
seguir usando nuestro virtual box!!
