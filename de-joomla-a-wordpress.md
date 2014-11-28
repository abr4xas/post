Title: Migrar de Joomla a WordPress y no morir en el intento!!
Date: 2014-11-21 10:20
Category: Wordpress
Tags: wordpress, web, plugins, dev
Slug: de-joomla-a-wordpress
Author: abr4xas
twitter: abr4xas
Summary: Bueno, una amiga me pidió que la ayudara a pasar todo el contenido de su sitio web en Joomla a WordPress la aventura de migrar TODA esa información inicia con averiguar la forma de migrar toda esa data...
image: /images/banner-772x250.png

![Alt Text](/images/banner-772x250.png)

Bueno, una amiga me pidió que la ayudara a pasar todo el contenido de su sitio web en Joomla a WordPress la aventura de migrar TODA esa información inicia con averiguar la forma de migrar toda esa data...

Un amigo, @lestat00 me comento que usara el plugin FG Joomla to WordPress pero, que es FG Joomla to WordPress?

>Un plugin para migrar categorías, mensajes, etiquetas, imágenes y otros archivos multimedia de Joomla a WordPress. Se ha probado con las versiones de Joomla 1.5, 1.6, 1.7, 2.5, 3.0, 3.1, 3.2 y 3.3 y WordPress 4.0 en bases de datos grandes (000+ 72 mensajes). Es compatible con las instalaciones de múltiples sitios.

## Instalación:

* Instalar el plugin desde el panel de administración => Plugins menu => Add New => Upload => Seleccionar el archivo zip => Instalar ahora
O simplemente usar el formulario de busqueda y colocar: FG Joomla to WordPress => Instalar ahora
* Activar el plugin
* Iniciar la herramienta de importación > Import > Joomla (FG)
* Hay que configurar los ajustes del plugin para que podamos importar lo que necesitamos, estos datos los podemos encontrar en el archivo configuration.php de Joomla donde, vamos a necesitar los siguientes valores

```php
Hostname = $host
Port = 3306 (standard MySQL port)
Database = $db
Username = $user
Password = $password
Joomla Table Prefix = $dbprefix
```

## Caracteristicas del plugin:

* Requires: 3.0 or higher 
* Compatible up to: WP 4.0.0
* Last Updated: 2014-11-15 
* Downloads: 108,553

Para obtener más informacion, visita esta pagina: https://wordpress.org/plugins/fg-joomla-to-wordpress/
