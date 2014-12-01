Title: Cambiar el "ServerName" en Apache.
Date: 2011-09-01 23:51
Author:  
Slug: cambiar-el-servername-en-apache

Cuando estamos trabajando con Apache, como nuestro servidor de pruebas
al momento de realizar alguna actualización o cuando lo instalamos si
verificamos todo lo que dice la consola al momento de hacer alguna de
esas cosas mecionadas podemos apreciar que nos dice:

`Starting web server: apache2apache2: Could not reliably determine the server's fully qualified domain name, using 127.0.1.1 for ServerName.`  
En este caso, eso tiene una solucion facil y rapida:

primero debemos editar el archivo httpd.conf:

`gedit /etc/apache2/httpd.conf`

y colocar:

`ServerName localhost`  
Reiniciamos el servicio con:  
`service apache2 restart`  
Y listo.  
Bueno, chao... Eso es todo!!  
Y listo, ahora revisamos
