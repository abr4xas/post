Title: #VirtualBox... Los DKMS no funcionan. 
Date: 2012-02-27 19:53
Author:  
Slug: virtualbox-los-dkms-no-funcionan

Antes de contarles que paso con los DKMS les hablare un poco sobre
ellos...  
![Logo
VirtualBox](http://abr4xas.org/wp-content/uploads/2012/02/vbox_logo2_gradient.png "vbox_logo2_gradient")

Dynamic Kernel Module Support (DKMS) es un framework usado para generar
módulos del núcleo Linux cuyas fuentes no suelen residir en el árbol
fuente del núcleo Linux. DKMS habilita controladores de núcleo para ser
automáticamente reconstruidos cuando un nuevo núcleo es instalado lo que
hace posible usar un nuevo núcleo inmediatamente, en lugar de esperar
que módulos compatibles de terceras partes para ser liberado.  
DKMS fue escrito por el Equipo de Ingenieros de Linux en Dell en 2003.

Ya está incluido en muchas distribuciones del sistema operativo Linux,
como Ubuntu 8.10 [1]

<span style="color: #ff0000;">[adsenseyu2]</span>

<!--more-->Bueno, como ya saben que son los dkms les diré que paso:

Como he sabido por todos, los dkms es un modulo para VirtualBox para que
funcione sin problemas pero en este caso yo tenia
la versión 3.2.6-030206-generic-pae (i686) del kernel y de ahi radica el
problema...

Al iniciar el virtualbox salia una ventana de error como la siguiente:

![VirtualBox Kernel
Error](http://www.tecnoretales.com/wp-content/uploads/2009/05/errorvirtualbox.gif)

<span style="color: #ff0000;">[adsenseyu1]</span>

Después de pasar un buuuen rato averiguando el porque me percate de que
se trataba de un problema del kernel (obvio no? xD)

Bueno, la unica solución viable era:

-   Cambiar el kernel y probar nuevamente

De no ser esa la solución pues, seguiría buscando en google :)

Efectivo, al cambiar el kernel e iniciar virtualbox no hubo ningun error
:D FTW!!

<span style="color: #ff0000;">[adsenseyu4]</span>

Actualmente esto es lo que tengo:

`abr4xas@dx2400:~$ uname -a Linux dx2400 3.1.0-030100-generic #201110241006 SMP Mon Oct 24 14:20:44 UTC 2011 i686 i686 i386 GNU/Linux`

Y fino, despues de un buen rato ya tango mis maquinas virtuales
funcionando sin problemas!!

<span style="color: #ff0000;">[adsenseyu3]</span>

[1] [http://es.wikipedia.org/wiki/Dynamic\_Kernel\_Module\_Support](http://es.wikipedia.org/wiki/Dynamic_Kernel_Module_Support)

La imagen gracias
a [tecnoretales.com](http://www.tecnoretales.com/linux/kernel-driver-not-installed-rc-1908-error-virtualbox/ "http://www.tecnoretales.com/linux/kernel-driver-not-installed-rc-1908-error-virtualbox/")

 
