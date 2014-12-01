Title: apt-get vs aptitude
Date: 2012-05-23 17:25
Author:  
Slug: apt-aptitude

APT se utiliza básicamente para la instalación y desinstalación de
paquetes en sistemas GNU/Linux basados en Debian desde los repositorios
(sources.list). Su uso mas común es apt-get.

Los cuatro comandos más usados son: install, remove, update y upgrade.
Aquí tienes una explicación detallada de todos los comandos de apt-get:

 

<!--more-->

-   **apt-get update** - Descarga nuevas listas de paquetes
-   **apt-get upgrade** - Realiza una actualización
-   **apt-get install** - Instala nuevos paquetes
-   **apt-get remove** - Elimina paquetes
-   **apt-get source** - Descarga archivos fuente
-   **apt-get build-dep** - Configura las dependencias de construcción
    para paquetes fuente
-   **apt-get dist-upgrade** - Actualiza la distribución
-   **apt-get dselect-upgrade** - Sigue las selecciones de dselect
-   **apt-get clean** - Elimina los archivos descargados
-   **apt-get autoclean** - Elimina los archivos descargados antiguos
-   **apt-get check** - Verifica que no haya dependencias incumplidas

pt-get trabaja muy bien identificando qué dependencias necesitan ser
instaladas para que funcione un paquete determinado, pero falla
miserablemente a la hora de eliminar dicho paquete.

Aptitude es una herramienta mejor para instalar, eliminar, actualizar, y
administrar de otras formas los paquetes en tu sistema que apt. Para
empezar, desde sus comienzos, aptitude ha sido capaz de resolver el
problema de las dependencias huérfanas. En segundo lugar, tiene una
interfaz basada encurses que supera totalmente a la de dselect.
Finalmente, y no menos importante, usa una sola herramienta con muchas
funciones. Veamos:

-   **aptitude**: Al ejecutarlo sin argumentos muestra una interfaz para
    buscar, navegar, instalar, actualizar y realizar otras tareas de
    administración de paquetes.
-   **aptitude install**: Instala software en tu sistema, junto con las
    dependencias necesarias.
-   **aptitude remove**: Elimina paquetes junto con las dependencias que
    queden huérfanas.
-   **aptitude purge**: Elimina paquetes y dependencias huérfanas junto
    con los ficheros de configuración.
-   **aptitude search**: Busca paquetes en las listas de paquetes
    locales de apt.
-   **aptitude update**: Actualiza las listas de paquetes locales.
-   **aptitude upgrade**: Actualiza los paquetes disponibles.
-   **aptitude clean**: Elimina los ficheros que fué necesario descargar
    para instalar software en tu sistema.
-   **aptitude dist-upgrade**: Actualiza paquetes, incluso si eso
    significa que debe desinstalar otros.
-   **aptitude show**: Muestra detalles acerca del paquete nombrado.
-   **aptitude autoclean**: Elimina los paquetes deb obsoletos.
-   **aptitude hold**: Fuerza a que un paquete permanezca en su versión
    actual, y no se actualice.

<div>
Pero aptitude tiene otras ventajas respecto a su predecesor, apt:Al
buscar un paquete con aptitude, los resultados aparecen ordenados
alfabéticamente y justificados por columnas; también te dirá cuales
están instalados en tu sistema, en lugar de darte un listado de paquetes
en un formato desordenado e ilegible, como hace apt-cache.

</p>
Y eso no es todo: los paquetes que apt-get te recomendaba y
sugería, aptitude los instala directamente, siempre avisándote,
obviamente.

</div>
<div>
</div>
<div>
[fuente](http://usandocanaima.blogspot.com/2011/06/gestionando-paquetes-apt-get-o-aptitude.html "Gestionando paquetes ¿apt-get o aptitude?")

</div>

