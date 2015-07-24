Title: Tamaños maximos de almacenamiento de TEXT, TINYTEXT, MEDIUM/LONG TEXT
Date: 2015-07-11 18:00
Category: Web
Tags: mysql, database
Slug: tinytext-text-mediumtext-and-longtext-maximum-storage-sizes
Author: abr4xas
twitter: abr4xas
Summary: Cuales son los tamaños maximos de almacenamiento de TINYTEXT, TEXT, MEDIUMTEXT y LONGTEXT  &#x1F615;
image: http://www.hostingreviewslist.com/wp-content/uploads/2013/04/database-server-web-hosting-icon-flat-green1.png

![MySQL](https://www.rosehosting.com/blog/wp-content/uploads/2014/09/mysql.png)

Cuando estamos diseñando una base de datos siempre nos preguntamos cual sera el tipo de dato que vamos a manejar, pero, que pasa con esos campos en los que necesitamos guardar cierta cantidad de informacion?

Aqui es donde aparece: TINYTEXT, TEXT, MEDIUMTEXT y LONGTEXT

Muy bien, ya sabemos que podemos usar algunos de esos tipos pero, relamente cual es el tamaño maximo de almacenamiento de cada uno de ellos?

En StackOverflow.com el usuario Bridge realizo una respuesta a esta interrogante y es la siguiente:


```
      Type | Maximum length
-----------+-------------------------------------
  TINYTEXT |           255 (2 8−1) bytes
      TEXT |        65,535 (216−1) bytes = 64 KiB
MEDIUMTEXT |    16,777,215 (224−1) bytes = 16 MiB
  LONGTEXT | 4,294,967,295 (232−1) bytes =  4 GiB
```

NOTA: El numero de caracteres que pueden ser alamacenados va a depender de la codificacion que estemos usando.

Ya con esto podemos tener una idea de como hacer nuestras tablas y evitar modificarlas mientras estamos trabajando en algun proyecto web.


Lecturas recomendadas

* [Documentacion de MySQL para mas info](http://dev.mysql.com/doc/refman/5.7/en/string-type-overview.html).
* [TINYTEXT, TEXT, MEDIUMTEXT, and LONGTEXT maximum storage sizes](http://stackoverflow.com/questions/13932750/tinytext-text-mediumtext-and-longtext-maximum-storage-sizes)
