Title: Pequeños tips para tu Mac
Date: 2014-11-27 10:20
Category: Apple
Tags: mac, apple, osx
Slug: tips-mac-os
Author: abr4xas
twitter: abr4xas
Summary: Algunas pequeñas mejoras y tips para nuestro mac. 
image: /images/apple-8-bit-logo.png

![Mac Logo](http://www.brandsoftheworld.com/sites/default/files/styles/logo-thumbnail/public/0004/3277/brand.gif)

Desde hace algun tiempo poseeo un MacBook, no es un Pro pero, vamos, sigue siendo un Mac xD

Leyendo el blog de @Bucio encontre un par de post bien interesantes:

## WireLurker: Cómo saber si mi Mac esta infectada.

WireLurker es un malware que afecta a equipos Mac y dispositivos iPhone e iPad, el cual proviene de China y fue lanzado para el mercado chino. Se han identificado un total de 467 aplicaciones infectadas con el malware, El cual ha sido descargado más de 356.000 veces. 

Para saber si nuestro Mac esta infectado solo debemos hacer lo siguiente 

```bash
curl -O https://raw.githubusercontent.com/PaloAltoNetworks-BD/WireLurkerDetector/master/WireLurkerDetectorOSX.py

python WireLurkerDetectorOSX.py

```
De estar todo bien, debemos tener un mensaje como el siguiente:

```
Your OS X system isn't infected by the WireLurker. Thank you!
```
El otro post que me fue muy util es el siguiente:

## Cambiar en el Hostname en OS X

En la consola debemos escribir

```bash
sudo scutil --set HostName Nuevo-Nombre.local
```
Donde, ```Nuevo-Nombre``` sera el nombre que le vamos a dar al equipo. Es necesario reiniciar para aplicar los cambios.

Para mas informacion, les invito a leer el [blog de bucio](http://bucio.mx "Blog de Bucio").
