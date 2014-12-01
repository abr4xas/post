Title: #VirtualBox Guest Additions
Date: 2012-02-25 01:34
Author:  
Slug: virtualbox-guest-additions

![Logo
VirtualBox](http://abr4xas.org/wp-content/uploads/2012/02/vbox_logo2_gradient.png "vbox_logo2_gradient")

VirtualBox Guest Additions es un paquete especial de software que forma
parte de [VirtualBox](http://virtualbox.org "http://virtualbox.org") y
que debe instalarse en cada una de las máquinas virtuales para mejorar
el rendimiento y añadir nuevas funciones. Consisten en una serie de
controladores (drivers) y aplicaciones para el sistema virtualizado que
lo optimizan para un mejor rendimiento y usabilidad.

Las Guest Additions (aplicaciones del huesped) se encuentran disponibles
en una imagen de CD-ROM con el nombre VBoxGuestAdditions.iso. que
debemos montar en nuestra máquina virtual como una unidad de CD e
instalarlas desde ella. [1]

 

<span style="color: #ff0000;">[adsenseyu3]</span>

Ok, teniendo claro eso de "***Guest Additions***" les voy a contar lo
que me paso tratando de instalarlas...

<!--more-->Como todos sabemos, directamente desde la aplicación de
VirtualBox podemos bajarlas y al hacerlo me dio un error como veremos en
la siguiente imagen:

![VirtualBox Guest
Additions](http://abr4xas.org/wp-content/uploads/2012/02/virtualbox.jpg "VirtualBox Guest Additions")

<span style="color: #ff0000;">[adsenseyu2]</span>

El error radica en que, la URL que esta ahi esta incorrecta y por eso el
problema al bajarla la .iso me puse a revisar y la ruta correcta es
[esta](http://dlc.sun.com.edgesuite.net/virtualbox/4.1.2/ "Ruta correcta para VirtualBox Guest Additions") ahí
encontraran muchos paquetes (rpm, deb y exe) de virtual box y el
necesario [VBoxGuestAdditions\_4.1.2.iso](http://dlc.sun.com.edgesuite.net/virtualbox/4.1.2/VBoxGuestAdditions_4.1.2.iso "VBoxGuestAdditions_4.1.2.iso").

Fuente
[1] [sliceoflinux.com/2009/05/04/¿que-son-las-virtualbox-guest-additions/](http://sliceoflinux.com/2009/05/04/¿que-son-las-virtualbox-guest-additions/ "http://sliceoflinux.com/2009/05/04/¿que-son-las-virtualbox-guest-additions/")
