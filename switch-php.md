Title: Haciendo un switch en #PHP
Date: 2012-03-06 08:44
Author:  
Slug: switch-php

![ElePHPant\_-\_Mascot\_PHP-logo](http://abr4xas.org/wp-content/uploads/2012/03/ElePHPant_-_Mascot_PHP-logo-4C78D1AC4E-seeklogo.com_.gif "ElePHPant_-_Mascot_PHP-logo")

 

La sentencia ***switch*** es similar a una serie de sentencias IF en la
misma expresión. En muchas ocasiones, es posible que se quiera comparar
la misma variable (o expresión) con muchos valores diferentes, y
ejecutar una parte de código distinta dependiendo de a que valor es
igual. Para esto es exactamente la expresión *switch*. [1]

<span style="color: #ff0000;">[adsenseyu1]</span>

<!--more-->

Ok, veamos un ejemplo:

    switch ($i) {
     case "manzana":
     echo "i es una manzana";
     break;
     case "barra":
     echo "i es una barra";
     break;
     case "pastel":
     echo "i es un pastel";
     break;
     }
     ?>

 <span style="color: #ff0000;">[adsenseyu2]</span>

Con este ejemplo nos podemos hacernos la idea de como usarlo no? Ahora
bien, les comentare un "viejo truco" como dice
@[xombra](http://twitter.com/xombra "http://twitter.com/xombra") el cual
he aplicado en muchas cosas que he estado haciendo...  
En este caso, se trata de que al seleccionar un enlace y que abra esa
ventana bueno, con el ejemplo que les dare creo que me explicare mejor
xD

<span style="color: #ff0000;">[adsenseyu3]</span>

Bueno, suponiendo que tenemos nuestro index.php dentro de las etiquetas
\<body\> y \</body\> colocamos:

    include 'include/seleccion.php';
     ?>

Donde en ese archivo seleccion.php (al que podemos llamar como queramos)
colocamos:

    if (!isset($_GET["ver"])) { $ver = 'home'; } else { $ver = htmlentities(trim($_GET["ver"])); }
     switch($ver){
     case 'Home':
     include 'include/home.php';
     break;
     case 'About':
     include_once 'include/about.php';
     break;
     case 'Contacto':
     include_once 'include/contacto.php';
     break;
     default:
     include 'include/home.php';
     } ?>

Ok, explico lo que hay:

    if (!isset($_GET["ver"])) { $ver = 'Home'; } else { $ver = htmlentities(trim($_GET["ver"]));

En esa linea estamos diciendo que si no esta vacío  la opción "ver"
obtenida por \$\_GET donde declaramos a \$ver = Home, de lo contrario
limpiamos el valor de \$\_GET["ver"] con las funciones htmlentities[2] y
trim [3]

Por consiguiente, al hacer clic en un enlace de la forma:

    href="index.php?ver=Home" target="_self" title="Clic aquí para ir directamente a la página XXXX" >Ir a la página XXXXX

donde ver=Home se va directo a la pagina llamada home.php que tenemos
dentro de la carpeta include.

Btw, usamos esa carpeta "***include***" para asi colocar todo lo
referente a las paginas que vamos a usar.

<span style="color: #ff0000;">[adsenseyu4]</span>

Bueno, esto es todo por los momentos :D a medida que tenga tiempo
les seguiré colocando cosas útiles como esta!!

Más info, clic en los siguientes enlaces:

[1] [http://www.php.net/manual/es/control-structures.switch.php](http://www.php.net/manual/es/control-structures.switch.php "Estructura de control switch.")

[2] [http://www.php.net/manual/es/function.htmlentities.php](http://www.php.net/manual/es/function.htmlentities.php "Función htmlentities")

[3] [http://www.php.net/manual/es/function.trim.php](http://www.php.net/manual/es/function.trim.php "Función trim")

Btw, le dan un clic a la publicidad? :D ¡GRACIAS!
