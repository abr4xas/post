Title: Plantilla para Pelican
Date: 2014-07-11 10:20
Category: Web
Tags: pelican, python, web
Slug: pelican-template
Author: abr4xas
twitter: abr4xas
Summary: Una plantilla para pelican usando bootstrap, aun con cosas por mejorar pero puede ser usada sin problemas :D
image: images/2043492.png

Ok, todo bien pero... ¿Que diablos es Pelican? Bueno, acá la respuesta:

> Open-source static site publishing tool. Supports Markdown and reST-formatted content. Powered by Python. And lots of fish.

El repo de la plantilla es [este](https://github.com/abr4xas/ptemplate "Repo de plantilla").


<div class="alert alert-danger" role="alert">POR FAVOR, NO AGREGARLO COMO UN SUBMODULO... SE RECOMIENDA HACER UN <code>FORK</code> Y A PARTIR DE AHÍ HACER LO CONVENIENTE</div>



## Las razones para usar pelican

 * Porque es fácilisimo de instalar (incluso yo he podido hacerlo :P) con tan solo instalar pip (administrador de paquetes de python) y clonar (git clone) unos cuantos repositorios está todo listo.
 * Porque con tan solo editar el archivo pelicanconf.py podemos sacarle muchísimo partido a Pelican, co solo indicar una ruta ya tenemos un nuevo theme, además todos los plugin se configuran desde este archivo.
 * Porque tiene muchos [themes](https://github.com/getpelican/pelican-themes "pelican-themes") distintos con los podemos dar un look and feel más personalizado a la página.
 * Porque tiene cantidad de [plugins](https://github.com/getpelican/pelican-plugins "plugins") con los que poder añadir nuevas funcionalidades a Pelican. Por ejemplo, construir un sitemap de manera sencilla.

-------

## Configuraciones 

```python
THEME = 'abr4xas' # pueden llamarlo como quieran
FEED_RSS = 'feed'
DISQUS_SITENAME = ''
TWITTER_USERNAME = ''
USE_PAGER = 'True'
CC_LICENSE = ""
OPEN_GRAPH_FB_APP_ID = ''
```

 * Sobre ```CC_LICENSE``` pueden seguir este [enlace](http://github.com/hlapp/cc-tools "cc-tools").
 * Sobre los iconos, deben editarlos y colocarlos con el tamaño que se indica claro, eso es si quieren... ;) para más informacion revisar la carpeta ```static/images```
 * Revisar el contenido de ```templates/base.html``` y editar lo necesario (boton de paypal, suscripción por email).
 * Revisar el contenido de ```templates/index.html``` y de ```templates/article.html``` para cambiar el codigo de adsense por el propio. En este ultimo tambien se encuentra la suscripción por email y publicidad.

Enlaces de interes:

 * [http://getpelican.com](http://getpelican.com "http://getpelican.com")
 * [Las razones para usar pelican](http://jesuslc.com/2014/02/27/primeros-pasos-con-pelican-en-windows/ "¿Por qué elegir Pelican para crear html estático?")

Si te gusta esta plantilla, y quieres dar las gracias por las horas que pase haciendolo por favor:

 * Puedes realizar una pequeña donacion usando paypal.
 * Incluir un enlace desde tu blog al mio.

De verdad, muchas gracias por usarlo.

## Screenshots

### v0.2 de la plantilla
Descarga: [aquí](https://github.com/abr4xas/ptemplate/archive/v0.2.zip "Descargar")
![Alt Text]({filename}/images/blog2.png)

### v0.1 de la plantilla
Descarga: [aquí](https://github.com/abr4xas/ptemplate/archive/v0.1.zip "Descargar")
![Alt Text]({filename}/images/blog.png)