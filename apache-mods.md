Title: #Apache, sus mods y algo más
Date: 2012-03-13 02:35
Author:  
Slug: apache-mods


Title: #Apache, sus mods y algo más
Date: 2012-03-13 02:35
Category: Linux
Tags: apache, web server
Slug: apache-mods
Author: abr4xas
twitter: abr4xas
Summary: El servidor apache tiene muchas funcionalidades y "*mods*" que se emplean en el servidor para sacarle un mayor provecho al mismo.
image: 

Todos sabemos que es y de que trata el servidor apache y el que no lo sepa pues, pueden dar [clic aquí](http://es.wikipedia.org/wiki/Servidor_HTTP_Apache "Servidor HTTP Apache") en este enlace para conocer un poco sobre el.

El servidor apache tiene muchas funcionalidades y "*mods*" que se
emplean en el servidor para sacarle un mayor provecho al mismo.



Entre ellos les comento sobre:

-   [mod\_ssl](http://httpd.apache.org/docs/2.2/mod/mod_ssl.html)  -
    Comunicaciones Seguras
    vía [TLS](http://es.wikipedia.org/wiki/TLS "TLS").
-   [mod\_rewrite](http://httpd.apache.org/docs/2.2/mod/mod_rewrite.html)  -
    reescritura de direcciones (generalmente utilizado para transformar
    páginas dinámicas como php en páginas estáticas html para así
    engañar a los navegantes o a los motores de búsqueda en cuanto a
    cómo fueron desarrolladas estas páginas).
-   [mod\_dav](http://httpd.apache.org/docs/2.2/mod/mod_dav.html)  -
    Soporte del
    protocolo [WebDAV](http://es.wikipedia.org/wiki/WebDAV "WebDAV") ([RFC
    2518](http://tools.ietf.org/html/rfc2518)).
-   [mod\_deflate](http://httpd.apache.org/docs/2.2/mod/mod_deflate.html) -
    Compresión transparente con el
    algoritmo [deflate](http://es.wikipedia.org/wiki/Deflaci%C3%B3n_(algoritmo) "Deflación (algoritmo)") del
    contenido enviado al cliente.
-   [mod\_auth\_ldap](http://httpd.apache.org/docs/2.2/mod/mod_auth_ldap.html) -
    Permite autentificar usuarios contra un
    servidor [LDAP](http://es.wikipedia.org/wiki/LDAP "LDAP").
-   [mod\_proxy\_ajp](http://httpd.apache.org/docs/2.2/mod/mod_proxy_ajp.html)  -
    Conector para enlazar con el servidor [Jakarta
    Tomcat](http://es.wikipedia.org/wiki/Jakarta_Tomcat "Jakarta Tomcat") de
    páginas dinámicas
    en [Java](http://es.wikipedia.org/wiki/Java_(lenguaje_de_programaci%C3%B3n) "Java (lenguaje de programación)") ([servlets](http://es.wikipedia.org/wiki/Servlet "Servlet") y [JSP](http://es.wikipedia.org/wiki/JSP "JSP")).

El servidor de base puede ser extendido con la inclusión de módulos
externos entre los cuales se encuentran:

-   [mod\_cband](http://www.howtoforge.com/mod_cband_apache2_bandwidth_quota_throttling) -
    Control de tráfico y limitador de ancho de banda.
-   [mod\_perl](http://perl.apache.org/)- Páginas dinámicas
    en [Perl](http://es.wikipedia.org/wiki/Perl "Perl").
-   [mod\_php](http://www.php.net/manual/es/security.apache.php)-
    Páginas dinámicas en [PHP](http://es.wikipedia.org/wiki/PHP "PHP").
-   [mod\_python](http://www.modpython.org/)- Páginas dinámicas
    en [Python](http://es.wikipedia.org/wiki/Python "Python").
-   [mod\_rexx](http://sourceforge.net/projects/modrexx/)- Páginas
    dinámicas
    en [REXX](http://es.wikipedia.org/wiki/REXX "REXX") y [Object
    REXX](http://es.wikipedia.org/wiki/Object_REXX "Object REXX").
-   [mod\_ruby](http://www.modruby.net/en/) - Páginas dinámicas
    en [Ruby](http://es.wikipedia.org/wiki/Ruby "Ruby").
-   [mod\_aspdotnet](http://httpd.apache.org/cli/) - Páginas dinámicas
    en [.NET de
    Microsoft](http://es.wikipedia.org/wiki/.NET_de_Microsoft ".NET de Microsoft")**(Módulo
    retirado)**.
-   [mod\_mono](http://www.mono-project.com/ASP.NET) - Páginas dinámicas
    en [Mono](http://es.wikipedia.org/wiki/Proyecto_Mono "Proyecto Mono")
-   [mod\_security](http://es.wikipedia.org/wiki/Mod_Security "Mod Security") -
    Filtrado a nivel de aplicación, para seguridad.

Bueno, ya conociendo un poco sobre los módulos que se pueden activar en
apache para sacarle un mayor provecho al servidor hoy les diré un
"viejo" truco para facilitarnos la vida al momento de usar apache como
servidor local para nuestros proyectos o cualquier cosa que estemos
haciendo xD

Luego de instalar apache para poder usarlo todo nuestros scripts deben
ir en /var/www para que al entrar a 127.0.0.1/pruyecto
localhost/proyecto se ejecute todo lo que estemos haciendo cierto? Pero,
eso de estar en consola a cada rato haciendo un  

```
cp /home/tu_usuario/proyecto /var/www/
```
es algo tedioso si eres una de esas personas que no les gusta usar
consola o para los efectos trabajar con nautilus en modo root para poder
acceder a esa carpeta ya que root tiene permisos sobre ella...

Si, es valido aplicar la de hacerse propietario de esa carpeta y eso...
Pero vamos, hay quienes no les gusta mucho hacer eso y para esas
personas va este post... :D

Bueno, existe una opción para cambiar el DocumentRoot de apache y que
sea cualquier carpeta en nuestro sistema... ¿Como se hace? Pues,
sencillo... En consola debemos escribir (o copiar según el caso xD)  

```
sudo gedit /etc/apache2/sites-available/default
```

Colocamos nuestra clave y vamos a ver un archivo con la siguiente
información:  
```
<VirtualHost *:80> ServerAdmin webmaster@localhost
DocumentRoot /home/abr4xas/Documentos/www 
<Directory /> Options FollowSymLinks AllowOverride None </Directory> 
<Directory /home/abr4xas/Documentos/www> Options Indexes FollowSymLinks MultiViews AllowOverride None Order allow,deny allow from all </Directory>
ScriptAlias /cgi-bin/ /usr/lib/cgi-bin/ usr/lib/cgi-bin"> AllowOverride None Options +ExecCGI -MultiViews +SymLinksIfOwnerMatch Order allow,deny Allow from all </Directory>  
ErrorLog ${APACHE_LOG_DIR}/error.log
# Possible values include: debug, info, notice, warn, error, crit, # alert, emerg. LogLevel warn
CustomLog ${APACHE_LOG_DIR}/access.log combinedAlias /doc/ "/usr/share/doc/" usr/share/doc/"> Options Indexes MultiViews FollowSymLinks AllowOverride None Order deny,allow Deny from all Allow from 127.0.0.0/255.0.0.0 ::1/128 </Directory>
</VirtualHost>
```
Lo que esta resaltado debemos cambiarlo por la ruta de nuestra carpeta
que va a trabajar como DocumentRoot en mi caso es: 

```
/home/abr4xas/Documentos/www
```

Al cambiar esa ruta por la carpeta que quieren usar solo resta iniciar
nuevamente el apache  

```
sudo /etc/init.d/apache2 stop 
sudo /etc/init.d/apache2 start
```
Y listo, ya tenemos una carpeta de "*facil*" acceso para todo lo que
vamos hacer!! :D
