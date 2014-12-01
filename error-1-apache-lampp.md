Title: #XAMPP: Error 1! Couldn't start Apache!
Date: 2011-11-12 21:07
Author:  
Slug: error-1-apache-lampp

 

[![xampp-objectdock](http://abr4xas.org/wp-content/uploads/2011/11/xampp-objectdock.png "xampp-objectdock")](http://abr4xas.org/wp-content/uploads/2011/11/xampp-objectdock.png)

Bueno, el problema radica en que de un momento a otro al iniciar el
xampp obtenía un error como este:  

` XAMPP: Error 1! Couldn't start Apache! XAMPP: Starting diagnose... XAMPP: Sorry, I've no idea what's going wrong.`

Entonces, al intentar eliminarlo, o instalar apache directamente desde
los repos me daba error... Hasta que hoy encontré la forma de como
solucionarlo... xD...

` sudo update-rc.d -f apache2 remove`

Y con eso listo, pude configurar el xampp sin problemas :)

Bueno, chao...

[Fuente](http://tuamigotetieneganas.blogspot.com/2011/03/como-desinstalar-apache-completamente.html "http://tuamigotetieneganas.blogspot.com/2011/03/como-desinstalar-apache-completamente.html")
