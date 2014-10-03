Title: Xanadu GNU / Linux
Date: 2014-09-21 10:20
Category: Linux
Tags: OS,xanadu
Slug: xanadu-linux-update
Author: xanadulinux
twitter: xanadulinux
Summary: Ha salido una nueva version de est derivado de Debian que utiliza SID como base y LXDE como entorno de escritorio, pensada para...
image: /images/xanadu-linux.png

![Alt Text](/images/xanadu-linux.png)

Es un derivado de Debian que utiliza SID como base y LXDE como entorno de escritorio, pensada para ser ligera y a la vez útil, contiene herramientas para rescate de sistemas, análisis forense y navegación anónima, además de todo lo necesario para su uso en el escritorio.

El grupo de desarrollo de Xanadu GNU/Linux se complace en anunciar la versión 0.6.0 de nuestra distribución. Esta versión viene llena de muchos cambios importantes, entre los que podemos mencionar:

 * Se sustituye el kernel original por el kernel liquorix.
 * Se sustituye BASH por FISH como shell por defecto.
 * Se agrega soporte para XFS y BTRFS además de EXT4 en el instalador.
 * Si se instala usando XFS se agregan parámetros dedicados al sysctl.conf.
 * Se incorpora apparmor.
 * El script “entorno” ahora nos da mas información.
 * Los valores “shmmax” y “shmall” se calculan durante el arranque.
 * Se agrega “tcp_mtu_probing” al sysctl.conf.
 * Se activa el soporte para IPv6.
 * La opción “activar seguridad” fue movida desde el script adicionales al script post-instalador y se crea la opción “desactivar seguridad”.
 * Se agrega la opción para instalar hplip-gui desde el post-instalador.
 * Se agrega la opción para desactivar compton en adicionales.
 * Se agrega el paquete florence (teclado en pantalla)
 * Se agregan los siguientes paquetes: joystick, x11-touchscreen-calibrator, xinput-calibrator, xserver-xorg-input-elographics, xserver-xorg-input-multitouch.
 * Se eliminan los paquetes plymouth, usbview y lxlauncher.
 * Se desactiva la búsqueda automática de la partición de persistencia para acelerar el arranque.

En el caso de la imagen ISO llamada minimal se elimina debido a su poca popularidad y para simplificar el proceso de creación de las ISO, en su lugar se utilizara el script “modo-server” que se encarga de realizar limpieza sobre un xanadu ya instalado dejando solo los componentes incluidos originalmente en la imagen minimal.

También se cambiara la frecuencia de publicación de nuevas versiones de la distribución que a partir de ahora se harán trimestralmente, estando programada la publicación de la próxima versión para principios del mes de diciembre, como siempre en la sección de descarga se encuentran los nuevos enlaces:

[https://xanadulinux.wordpress.com/descarga/](https://xanadulinux.wordpress.com/descarga/)

NOTA: Hay un error SIGSEGV en brasero en la imagen i386 que impide su ejecución, este error ya fue reportado a sus desarrolladores y esta a la espera de una solución. Después de instalar Xanadu i386 solo deberá realizar una actualización para corregir el problema.


