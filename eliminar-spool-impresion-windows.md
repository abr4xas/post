Title: Eliminar el spool de impresión de windows
Date: 2015-03-28 17:38
Category: Blog
Tags: 
Slug: eliminar-spool-impresion-windows
Author: abr4xas
twitter: abr4xas
Summary: A veces cuando estamos imprimiendo un documento puede aparecer un mensaje diciéndonos que hay un problema con la impresora o con el servicio de cola de impresión.
image: http://winblog.blob.core.windows.net/win/sites/2/2012/02/6874.5_5F00_01C91EBC.png

A veces cuando estamos imprimiendo un documento puede aparecer un mensaje diciéndonos que hay un problema con la impresora o con el servicio de cola de impresión.

Para solventar este inconveniente podemos crear un archivo .bat con lo siguiente:

```
net stop spooler
del %systemroot%\system32\spool\printers\*.shd
del %systemroot%\system32\spool\printers\*.spl
Net start spooler
```

Lo que hace este archivo es eliminar todo lo que se encuentre en la cola de impresión y nos permite trabajar nuevamente sin problemas.

Espero que este post les ayude si presentan este mismo problema.