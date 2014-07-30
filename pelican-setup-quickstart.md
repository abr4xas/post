Title: Instalando pelican: pelican-quickstart
Date: 2014-07-29 10:30
Category: Linux
Tags: Linux, Dev, Web, Pelican, Markdown
Slug: pelican-setup-quickstart
Author: abr4xas
twitter: abr4xas
Summary: Vamos a usar ```pelican-quickstart``` para generar nuestro blog y otras cosas...
image: images/2043492.png

Dentro de nuestro directorio ```~/virtualenv/pelican``` escribimos ```pelican-quickstart``` y seguimos todas las preguntas que nos hace el script


```
(pelican)abr4xas@hp ~/virtualenv/pelican $ pelican-quickstart
Welcome to pelican-quickstart v3.4.0.

This script will help you create a new Pelican-based website.

Please answer the following questions so this script can generate the files
needed by Pelican.

    
> Where do you want to create your new web site? [.] 
> What will be the title of this web site? My title
> Who will be the author of this web site? author
> What will be the default language of this web site? [en] en
> Do you want to specify a URL prefix? e.g., http://example.com   (Y/n) y
> What is your URL prefix? (see above example; no trailing slash) http://localhost
> Do you want to enable article pagination? (Y/n) y
> How many articles per page do you want? [10] 2
> Do you want to generate a Fabfile/Makefile to automate generation and publishing? (Y/n) y
> Do you want an auto-reload & simpleHTTP script to assist with theme and site development? (Y/n) y
> Do you want to upload your website using FTP? (y/N) n
> Do you want to upload your website using SSH? (y/N) n
> Do you want to upload your website using Dropbox? (y/N) n
> Do you want to upload your website using S3? (y/N) n
> Do you want to upload your website using Rackspace Cloud Files? (y/N) n
> Do you want to upload your website using GitHub Pages? (y/N) n
Done. Your new project is available at /home/abr4xas/virtualenv/pelican
```
Para iniciar pelican debemos escribir ```make devserver``` y luego debemos ir a ```http://localhost:8000``` y veremos algo parecido a esto:

![Alt Text]({filename}/images/pelican1.png)

## Escribir un post

La estructura de un post con [markdown](http://blog.abr4xas.org/markdown-syntax.html) es la siguiente:

```
Title: My super title
Date: 2010-12-03 10:20
Category: Python
Tags: pelican, publishing
Slug: my-super-post
Author: 
Summary: Una descripción corta de lo que trata el post... 
image: http://url/de/imagen/destacada

A partir de aquí, el contenido del post... 

![Alt Text]({filename}/images/nombre-de-la-imagen.png)

```

Para guardar el archivo podemos hacerlo tomando el slug (my-super-post) con la extension ```.md``` ejemplo: ```my-super-post.md``` y esto va en la carpeta ```content``` 


## Como dato:
Si vamos a incluir imagenes en nuestras publicaciones seamos ordenados, por lo tanto vamos a crear una carpeta llamada ```images``` y ahi metemos todas las imagenes que necesitemos. ;)

## Escribir una pagina:

Dentro de la carpeta ```content``` podemos crear otra carpeta llamada ```pages``` y ahi podemos incluir todas las paginas necesarias por ejemplo la de ```about```.


Hasta la proxima entrada :D
