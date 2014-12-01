Title: Firefox 6 en debian
Date: 2011-08-24 18:35
Category: Web
Slug: firefox6-debian
Author: abr4xas
twitter: abr4xas
Summary: Como todos sabemos, firefox va por su version 6 y muy pronto saldra a la luz
la 7 :D bueno, para quienes usamos debian y estemos acostumbrado a la
personalización que podemos darle a este explorador pues, aqui hay un
truco para tener siempre la ultima version del navegador...
image: 

Como todos sabemos, firefox va por su version 6 y muy pronto saldra a la luz
la 7 :D bueno, para quienes usamos debian y estemos acostumbrado a la
personalización que podemos darle a este explorador pues, aqui hay un
truco para tener siempre la ultima version del navegador...

Debemos ir a este
[enlace](http://www.mozilla.com/es-ES/download/?product=firefox-6.0&os=linux&lang=es-ES "http://www.mozilla.com/es-ES/firefox/")
y bajarnos el paquete tar.bz2

Listo eso debemos copiar el archivo que bajamos a la carpeta /opt en
este caso en la cosola (como root, obvio) debemos hacer algo asi:

```bash
root@Genius:/home/abr4xas/Escritorio# cp firefox-6.0.tar.bz2 /opt/
```

luego de eso, pasamos a la carpeta en cuestion (/opt) cambiando el
directorio:

```bash
cd /opt
```

Si, listamos lo que tenemos en esa carpeta deberia salir (más o menos)
algo asi:  

```bash
root@Genius:/opt# ls Adobe Adobe AIR firefox-6.0.tar.bz2 google TweetDeck
```
Bueno, debemos descomprimir el tar.bz2 con:  
```bash
tar xvjf firefox-6.0.tar.bz2
```

luego de eso tendremos nuestra flamante carpeta "firefox" en el
directorio lista para ser usada :) pero, debemos hacer un enlace
simbolico de la forma:  
```bash
ln -s /opt/firefox/firefox /usr/bin/firefox6
```
(recuerden cambiar, el ultimo numero donde dice firefox por la version
que esten usando)  
listo eso, lo unico que nos queda es hacer un lanzador en la interfaz,
usando el editor de menu agregamos la siguiente linea:  
```bash
/usr/bin/firefox
```
Y listo, ya contamos con nuestro firefox actualizado!!

[Basado en
esto](http://debiansick.wordpress.com/2011/03/23/firefox-4-en-debian-lennysqueezewhezzy/ "Firefox 4 en Debian Lenny/Squeeze/Wheezy").

Btw, esto tambien aplica si queremos usar la version beta del navegador.

Tambien hay una forma mucho más facil y es
[esta](http://ubuntu308.wordpress.com/2010/11/27/instalar-firefox-en-debian-squeeze-forma-facil/ "http://ubuntu308.wordpress.com/2010/11/27/instalar-firefox-en-debian-squeeze-forma-facil/")
pero hasta los momentos solo esta disponible la version 5. Igual, si
prefieren pueden seguir los pasos que les indican ahi ya que son
totalmente validos. :D
