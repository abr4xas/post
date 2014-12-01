Title: Cambiar el background del LightDM
Date: 2011-10-09 05:41
Author:  
Slug: cambiar-background-lightdm

Bueno, buscando información de como cambiar el background que trae por
defecto el LightDM (btw, [para saber que es el ligthDM clic
aqui](http://es.wikipedia.org/wiki/LightDM "http://es.wikipedia.org/wiki/LightDM"))
el cual dure un rato buscando y comparando los métodos para cambiarlo
decidí quedarme con el que sale en
[OMGubuntu](http://www.omgubuntu.co.uk/2011/09/tool-change-lightdm-wallpaper-ubuntu-11-10/ "http://www.omgubuntu.co.uk/2011/09/tool-change-lightdm-wallpaper-ubuntu-11-10/")
el cual es el siguiente:

Abrimos consola y colocamos:<!--more-->

`gksu gedit /etc/lightdm/unity-greeter.conf`  
Lo que vamos a editar esta después de la linea que dice:  
`[greeter]`  
Y "SOLO" debemos poner el nombre de la imagen que queremos que sea el
fondo vean la imagen de abajo para que tengan una idea :D

[caption id="" align="alignnone" width="500" caption="Imagen de
OMGUbuntu"]![cambiar backgroud
LightDM](http://cdn.omgubuntu.co.uk/wp-content/uploads/2011/09/Screenshot-at-2011-09-30-15-45-54-500x412.png "cambiar backgroud LightDM")[/caption]

[[Clic aqui para ver el background por
defecto](http://es.wikipedia.org/wiki/Archivo:Lightdm-screenshot.jpg "http://es.wikipedia.org/wiki/Archivo:Lightdm-screenshot.jpg")]

 
