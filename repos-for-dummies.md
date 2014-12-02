Title: Configurar repos en #debian. (For Dummies)
Date: 2011-09-15 04:24
Category: Linux
Tags: debian
Slug: repos-for-dummies
Author: abr4xas
twitter: abr4xas
Summary: Unas de las cosas que me han dicho ultimamente es que: "*No se como tu usas
debian, yo lo instale pero nunca pude instalar nada*" de seguro estaras
pensando en que si actualizo la lista de los repos y casualmente ese es
el problema... 
image: 

Unas de las cosas que me han dicho ultimamente es que: "*No se como tu usas
debian, yo lo instale pero nunca pude instalar nada*" de seguro estaras
pensando en que si actualizo la lista de los repos y casualmente ese es
el problema...

Este post va directamente a esa personas que por no preguntar o quizas,
por no saber buscar en google, "[*Que hacer despues de instalar
debian*](http://www.google.co.ve/search?q=que+hacer+despues+de+instalar+debian&ie=utf-8&oe=utf-8&aq=t&rls=org.mozilla:es-MX:official&client=firefox-a "Que hacer despues de instalar debian")"

Primero que nada, debemos entender lo siguiente:

Debian se distribuye (mediante *réplicas*) a través de cientos de
servidores en Internet. Usar un servidor cercano ayuda a acelerar la
descarga a la vez que se reduce la carga en nuestros servidores
centrales así como en la propia Internet en general.[0]

Las réplicas de Debian pueden ser primarias o secundarias, según las
siguientes definiciones:

-   Una **réplica primaria** posee un ancho de banda considerable, está
    disponible 24 horas al día y tiene un nombre fácil de recordar, del
    tipo ftp..debian.org.

Las réplicas primarias se actualizan automáticamente cada vez que hay
cambios en el repositorio de Debian.

-   Una **réplica secundaria** puede restringir qué es lo que replica
    (por posibles problemas de espacio). Aunque una réplica sea
    secundario eso no significa necesariamente que tenga que ser más
    lenta o estar menos actualizada que una primaria.

Y por si aun no se entiende que es un repositorio aqui les dejo este
enlace[1]

OK, ahora vamos con esto:

La lista de los repos se encuentra en el siguiente ruta
```/etc/apt/sources.list```: en este caso vamos a consola y escribimos:

```bash
cat /etc/apt/sources.list
```

Esto para ver que hay dentro del archivo sources.list

A eso lo que esta ahi debemos incluir los repositorios *contrib* y
*non-free*.
```bash
\#  
\# deb cdrom:[Debian GNU/Linux 6.0.0 \_Squeeze\_ - Official amd64
NETINST Binary-1 20110205-14:31]/ squeeze main \*\*  
\#deb cdrom:[Debian GNU/Linux 6.0.0 \_Squeeze\_ - Official amd64
NETINST Binary-1 20110205-14:31]/ squeeze main \*\*

deb http://ftp.pt.debian.org/debian/ squeeze main contrib non-free  
\#deb-src http://ftp.pt.debian.org/debian/ squeeze main

deb http://security.debian.org/ squeeze/updates main contrib non-free  
\#deb-src http://security.debian.org/ squeeze/updates main

deb http://ftp.pt.debian.org/debian/ squeeze-updates main contrib
non-free  
\#deb-src http://ftp.pt.debian.org/debian/ squeeze-updates main

```
Por favor, no le presten atencion a las lineas que tienen los 2 \*\* ya
que esas lineas varian cuando uds hacen la instalacion del sistema.

Bueno, en el enlace [0] estan las direcciones de las réplicas primarias
de Debian. Ahi pueden jugar con eso para seleccionar el repo más cercano
a uds para que la descarga sea mucho más rapida.

Finalmente, para actualizar el equipo lo que debemos hacer es (en la
consola):

```bash
aptitude update
```

Y luego un:

```bash
aptitude full-upgrade
```

Listo, nuestro sistema actualizado!!

Enjoy!!!!!!!!!

Fuente:  
[0]
[http://www.debian.org/mirror/list](http://www.debian.org/mirror/list "Réplicas de Debian en todo el mundo")

[1]
[http://es.wikipedia.org/wiki/Repositorio](http://es.wikipedia.org/wiki/Repositorio "Repositorio")

[http://servidordebian.wikidot.com/squeeze-es:config](http://servidordebian.wikidot.com/squeeze-es:config "http://servidordebian.wikidot.com/squeeze-es:config")
