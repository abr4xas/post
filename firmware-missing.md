Title: UPDATE: Posible perdida de firmware para el módulo r8169.
Date: 2011-08-24 19:18
Category: Linux
Tags: linux, firmware
Slug: firmware-missing
Author: abr4xas
twitter: abr4xas
Summary: Bueno, desde hace unos dias estoy usando la version testing de debian (fue un
proceso largo para hacer el cambio que despues les dire) entre una de
las cosas que me dieron "cierto" problema fue un error con el kernel.
image: 

Bueno, desde hace unos dias estoy usando la version testing de debian (fue un
proceso largo para hacer el cambio que despues les dire) entre una de
las cosas que me dieron "cierto" problema fue un error con el kernel.
Para el momento estaba usando la 2.6.39 y pues, al momento de hacer la
actualización completa me salio esto:

```bash
Possible missing firmware /lib/firmware/rtl_nic/rtl8105e-1.fw for module r8169 with 2.6.39 kernel
```

ciertamente, un gran problema no? Pero lo bueno es que tiene una
solucion facil y es la siguiente:  
En consola debemos escribir:  

```bash
git clone git://git.kernel.org/pub/scm/linux/kernel/git/romieu/linux-firmware.git
```
esperamos a que baje todo el git y por ultimo ahi mismo en la consola:  
```bash
cp -r linux-firmware/rtl_nic/ /lib/firmware/
```
(cabe destacar que ese ultimo comando debe ser en mode root o para los
efectos usar sudo ;) )  
Y bueno, ya... Eso es todo lo que hay que hacer para solventar el
problemita...

Fuente:
[http://www.davidgis.fr/blog/index.php?2011/05/06/800--resolu-solved-w-possible-missing-firmware-lib-firmware-rtl\_nic-rtl8105e-1fw-for-module-r8169](http://www.davidgis.fr/blog/index.php?2011/05/06/800--resolu-solved-w-possible-missing-firmware-lib-firmware-rtl_nic-rtl8105e-1fw-for-module-r8169 "http://www.davidgis.fr/blog/index.php?2011/05/06/800--resolu-solved-w-possible-missing-firmware-lib-firmware-rtl_nic-rtl8105e-1fw-for-module-r8169")


UPDATE: Ya el git no se encuentra

Not Found
=========

The requested URL /pub/scm/linux/kernel/git/romieu/linux-firmware.git
was not found on this server.
