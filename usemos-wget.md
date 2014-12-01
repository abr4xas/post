Title: Usemos #wget 
Date: 2011-09-28 08:45
Author:  
Slug: usemos-wget

**GNU Wget** es una herramienta
[libre](http://es.wikipedia.org/wiki/Software_libre "Software libre")
que permite la descarga de contenidos desde [servidores
web](http://es.wikipedia.org/wiki/Servidor_web "Servidor web") de una
forma simple. Su nombre deriva de [World Wide
Web](http://es.wikipedia.org/wiki/World_Wide_Web "World Wide Web") (w),
y de «obtener» (en
[inglés](http://es.wikipedia.org/wiki/Idioma_ingl%C3%A9s "Idioma inglés")
*get*), esto quiere decir: obtener desde la WWW.

Actualmente soporta descargas mediante los protocolos
[HTTP](http://es.wikipedia.org/wiki/HTTP "HTTP"),
[HTTPS](http://es.wikipedia.org/wiki/HTTPS "HTTPS") y
[FTP](http://es.wikipedia.org/wiki/File_Transfer_Protocol "File Transfer Protocol").
[0]

En este caso vamos aprender unos pequeños pero utiles comandos para el
uso de esta herramienta:  
`wget http://www.ejemplo.com/`  
Con ese comando bajariamos el index.html/htm/php de la pagina llamada
"ejemplo.com"

-   `wget ftp://ftp.gnu.org/pub/gnu/wget/wget-1.10.2.tar.gz`

Y con eso nos bajamos el codigo fuente de wget...

Ok, pero que pasa cuando nos estamos bajando una .ISO (por ejemplo) y se
va la luz (algo tipico en venezuela) y estamos usando wget  
Bueno, simplemente debemos colocar la opcion ` -c` Ejemplo

-   `wget -c ftp://ftp.gnu.org/pub/gnu/wget/wget-1.10.2.tar.gz`

Eso es lo que debemos hacer :D

Tambien pueden ver este enlace[1] y saber un poco más...

 

[0]
[http://es.wikipedia.org/wiki/GNU\_Wget](http://es.wikipedia.org/wiki/GNU_Wget "http://es.wikipedia.org/wiki/GNU_Wget")

[1]
[http://www.linuxtotal.com.mx/index.php?cont=info\_admon\_017](http://www.linuxtotal.com.mx/index.php?cont=info_admon_017 "http://www.linuxtotal.com.mx/index.php?cont=info_admon_017")

 
