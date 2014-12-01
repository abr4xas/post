Title: #Debian, pasando de squeeze a wheezy
Date: 2011-08-26 03:37
Author:  
Slug: de-squeeze-a-wheezy-debian

Bueno, antes de entrar en "*materia*" debemos conocer ciertas cosas
sobre esta distro:

![Debian
Powered](http://abr4xas.org/wp-content/uploads/2011/08/debian_powered1.png "Debian Powered")Debian
siempre mantiene al menos tres versiones en mantenimiento activo:
"estable", "en pruebas" e "inestable" (stable, testing y unstable). Sus
principales características son:

-   **Rama estable**:La distribución "estable" (stable) contiene la
    publicación oficial más reciente de Debian.Esta es la versión de
    producción de Debian, cuyo uso recomendamos principalmente.

 

-   **Rama en pruebas**:La distribución "en pruebas" (testing) es la
    futura "estable", contiene paquetes que aún no han sido aceptados en
    dicha rama pero están a la espera de ello.La principal ventaja de
    usar esta rama es que tiene versiones más recientes del software.

 

-   **Rama inestable**:La distribución "inestable" es donde tiene lugar
    el desarrollo activo de Debian. Generalmente, esta rama es la que
    usan los desarrolladores y otros usuarios que quieren estar a la
    última. La distribución "inestable" se llama y siempre se llamará
    Sid.

Para saber más
[http://www.esdebian.org/wiki/ramas-desarrollo-debian](http://www.esdebian.org/wiki/ramas-desarrollo-debian "http://www.esdebian.org/wiki/ramas-desarrollo-debian")

Ok, a lo que vinimos... Si lo que queremos cambiar de squeeze a wheezy
(estable a testing) en debian lo primero que debemos hacer en una
terminal como root:  
`gedit /etc/apt/sources.list`

para cambiar lo que tenemos ahi por:  
` #Repositorios oficiales`

deb http://ftp.debian.org/debian/ testing main  
deb-src http://ftp.debian.org/debian/ testing main contrib non-free

\#Repositorios de seguridad

deb http://security.debian.org/ testing/updates main  
deb-src http://security.debian.org/ testing/updates main

\#Repositorios multimedia

deb http://www.debian-multimedia.org/ testing main  
deb-src http://www.debian-multimedia.org/ testing main

Luego de eso, debemos hacer un:

` aptitude update aptitude safe-upgrade aptitude full-upgrade`

Si de casualidad tienen un error con algun modulo en el kernel pueden
ver este
[post](http://abr4xas.org/2011/08/firmware-missing/ "http://abr4xas.org/2011/08/firmware-missing/")

Y bueno, listo ya estan usando debian testing :D...

Al menos que, despues de hacer el reboot no puedan entrar de forma
normal a su equipo :( la solucion a eso es muy facil  (por lo menos en
mi caso pero, debe ser igual :))

al momento del reboot el sistema les va a pedir su usuario y contraseña
la cual deben poner luego de eso se loguean como root y escriben:

` aptitude install xserver-xorg`

Y listo, esperan a que bajen todos los paquetes y tendran su flamante
wheezy!!

Bueno, chao!!
