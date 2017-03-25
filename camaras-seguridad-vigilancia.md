Title: ZoneMinder una excelente alternativa para el monitoreo de cámaras de seguridad y vigilancia bajo linux
Date: 2017-03-25 13:00
Category: tools
Tags: tools
Slug:camaras-seguridad-linux-zoneminder
Author: abr4xas
twitter: abr4xas
Summary: ZoneMinder es un conjunto de aplicaciones, herramientas que nos permiten controlar, monitorear nuestras cámaras de seguridad, de vigilancia.
image: https://i.ebayimg.com/00/s/MTAwMFgxMDAw/z/i8cAAOSwi0RXyMpI/$_35.JPG
header_image: images/control-room.jpg

ZoneMinder es un sistema de código abierto y de última generación para <a href="http://www.eviterobos.es" target="_blank">cámaras de vigilancia</a> de última generación que nos permite monitorear nuestro hogar, oficina o donde lo necesitemos usando cualquier hardware que tengamos en nuestras manos.


> Es importante aclarar que existen normativas y reglas en diversos países que prohíben la grabación con cámaras de vigilancia en la calle o mucho menos si la visión de la cámara llega a alcanzar la propiedad de algún vecino o domicilios ajenos a tu propiedad.


Las <a href="http://www.eviterobos.es" target="_blank">Cámaras de Seguridad</a> son una medida extra al vigilar nuestro hogar, oficina sin importar qué tan paranoico pueda parecer ya que nuestra seguridad la de nuestras familias y bienes son primero.

### Caracteristicas importantes a tomar en cuenta para usar un sistema CCTV

* Reducir y/o documentar pérdidas.
* Supervisión y control.
* Mejorar la calidad y efectividad del desempeño de empleados.
* Apoyo para el personal de seguridad ya que puede supervisar muchas áreas simultáneamente.
* Disuasión.
* Evidenciar ante terceros de forma correcta los eventos ocurridos (ejm: autoridades, empresas de seguro).


![ZoneMinder](https://wiki.contribs.org/images/thumb/c/c6/Zoneminder.png/250px-Zoneminder.png)

### Y que hace de ZoneMinder la mejor opción?

* Es de código abierto y gratuito.
* Usted está en control de sus datos.
* Funciona con una enorme lista de cámaras.
* Fácil de instalar - desde el paquete o la fuente.
* Las API permiten la integración con terceros.
* ZmNinja - Nueva aplicación para móviles.

### Antes de instalar 

Revisen la lista del hardware compatible con ZoneMinder en su <a href="http://www.zoneminder.com/wiki/index.php/Supported_hardware" target="_blank">wiki</a>

### Instalación

* Necesitamos un entorno LAMP
Ya debes saber como hacer esto xD

Despues de la instalación debemos hacer unas modificaciones:

```
nano /etc/mysql/my.cnf

# Al final del archivo colocar lo siguiente:
innodb_file_per_table
```
Reinicias el servicio:

`service mysql restart`

Hay que activar el módulo CGI de apache y el módulo rewrite

```
a2enmod cgi
a2enmod rewrite
```

Reinicias el servicio:

`service apache2 restart`

Despues de esto pasamos a instalar como tal la herramienta:

Estoy usando una instalación de Ubuntu 16.04 #YOLO

```
add-apt-repository ppa:iconnor/zoneminder
aptitude update
aptitude install zoneminder
```

Configuramos los permisos de `/etc/zm/zm.conf` a `root:www-data 740`

```
chmod 740 /etc/zm/zm.conf
chown root:www-data /etc/zm/zm.conf
```

Necesitamos crear un nuevo usuario

`adduser www-data video`

Activamos la configuración de Zoneminder

`a2enconf zoneminder`

Y reparamos los permisos

`chown -R www-data:www-data /usr/share/zoneminder/`

Y ya casi para finalizar necesitamos editar este archivo: 
`nano /etc/apache2/conf-available/zoneminder.conf`

E incluir lo siguiente

```
<Directory /usr/share/zoneminder/www>
  Options -Indexes +FollowSymLinks
```

Y 

```
<Directory /usr/share/zoneminder/www/api>
    AllowOverride All
</Directory>
```

Deben editarlo para que queden tal cual como se los indico

Y ya para finalizar

`service apache2 reload`

Activamos e iniciamos Zoneminder

`systemctl enable zoneminder && systemctl enable zoneminder`

