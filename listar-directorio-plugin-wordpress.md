Title: Listado de directorio, una falla algo peculiar.
Date: 2016-04-25 17:30
Category: Wordpress
Tags: Wordpress
Slug: listar-directorio-plugin-wordpress
Author: abr4xas
twitter: abr4xas
Summary: Quien tiene la responsabilidad de la seguridad a la hora de instalar Wordpress para evitar el listado de directorio? Una pequeña anecdota de como llegue al directorio de un plugin y encontre información critica guardada en texto plano.
image: https://levynewsnetwork.files.wordpress.com/2011/06/wordpress-logo.jpg

## Un poco de historia

Google, como sabemos es el buscador mas grande que existe a la hora de econtrar cualquier tipo de info.

Buscando una imagen llegue hasta una ruta muy parecida a esta:

```
http://www.dominio.com/wp-content/plugins/el-plugin/inc/img/nombre-de-la-imagen.png
```
Entonces, se me ocurrio que quizas podia listar el directorio completo y ciertamente fue asi y encontre algo como esto:

![Listado de directorio](/images/print_faill_plugin.png)


Si, realmente no es tan grave que se pueda listar un directorio, lo que si es grave el contenido de ese archivo que ven ahi llamado `data.log`

## La gravedad del asunto.

El archivo `data.log` contiene/contenia informacion delicada sobre las api key del servicio de pago, y especialmente la informacion de una transaccion realizada donde se podia encontrar el num de TDC, la fecha de vencimiento y el cod CCV.

Todo esto me lleva a la siguiente pregunta:

## ¿A quien le corresponde estar pendiente que no se puedan listar los directorios del Wordpress?


Nota: Antes de escribir este post fue notificado al dueño del dominio el problema y ya fue solventado.
