Title: Solucion a un pequeño error al usar youtube-dl
Date: 2011-10-07 00:57
Author:  
Slug: solucion-error-youtubedl

> **youtube-dl** is a small command-line program to download videos from
> YouTube.com and a few more sites. It requires the Python interpreter,
> version 2.x (x being at least 5), and it is not platform specific. It
> should work in your Unix box, in Windows or in Mac OS X. It is
> released to the public domain, which means you can modify it,
> redistribute it or use it however you like.[0]

Bueno, el problema al usarlo fue el siguiente:  
`ERROR: no fmt_url_map or conn information found in video info`  
googleando un poco me tope con esto [1] donde mucha gente indicaba que
presentaba el mismo problema y revisando un poco me tope con este
[comentario](https://github.com/rg3/youtube-dl/issues/108#issuecomment-1730675 "https://github.com/rg3/youtube-dl/issues/108#issuecomment-1730675")
diciendo que hay una nueva version validando la que yo instale  
` youtube-dl --version`  
decia que tenia la version de fecha 2011.01.30 y por eso era el error
solo me toco hacer en consola el update del paquete de la siguiente
forma:  
` youtube-dl --update `  
y tengo la del 2011.09.30 ahora si puedo bajar los videos sin ningun
problema...

Btw, les comento que para bajar los videos de mejor calidad debe usar
esto:

`--max-quality=.mp4` y luego la url del video  
Bueno, espero que les sea util!!

 

[0]
[https://github.com/rg3/youtube-dl](https://github.com/rg3/youtube-dl "https://github.com/rg3/youtube-dl")
