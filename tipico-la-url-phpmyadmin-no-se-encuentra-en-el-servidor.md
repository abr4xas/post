Title: Tipico, la url /phpmyadmin/ no se encuentra en el servidor
Date: 2011-10-13 03:46
Author:  
Slug: tipico-la-url-phpmyadmin-no-se-encuentra-en-el-servidor

Bueno, tratando de instalar el phpmyadmin para hacer unas pruebas para
un sistema que estoy haciendo sale el siguiente error:

“Not Found The requested URL /phpmyadmin/ was not found on this server“
=======================================================================

buscando información encontré en
[http://sliceoflinux.com](http://sliceoflinux.com/2009/06/19/instalar-phpmyadmin-en-ubuntu-9-04-server-paso-a-paso/ "http://sliceoflinux.com/2009/06/19/instalar-phpmyadmin-en-ubuntu-9-04-server-paso-a-paso/")
la solución al problemita y es el siguiente:

`echo "Include /etc/phpmyadmin/apache.conf" | sudo tee -a /etc/apache2/apache2.conf`

despues de hacer eso solo debemos reiniciar el apache con:  
`/etc/init.d/apache2 restart`

Actualizamos la pagina y WIIIINNN... Ya tenemos el phpmyadmin
funcionando...
