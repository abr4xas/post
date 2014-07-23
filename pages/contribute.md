Title: Contribuir
Date: 2014-06-24 10:20
Category: contribute
Tags: contribute
Slug: contribute
Author: abr4xas
Summary: Linux, un poco de python, bash, php, ruby, wordpress, bootstrap, css y otras cosas que no caben acá...
image: https://octodex.github.com/images/socialite.jpg

**abr4xas.org** usa *[Pelican](http://blog.getpelican.com/)* un generador de sitios web estático y esta alojado en github.

Lo unico necesario para ayudar es:

* conocimientos sobre ```git```
* una cuenta en github para poder hacer ```fork``` y enviar los Pull Request.

## Repo: *[Post](https://github.com/abr4xas/post)*

Este repo cuenta con las siguientes caracteristicas:

La estructura del post:

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

La estructura de directorios ```content/``` es:

```
content/
├── extra
│   └── CNAME
├── images
│   ├── nombre-de-la-imagen.png
├── pages
│   ├── about.md
│   └── contribute.md
```        

Obviamente, los post deben ser escritos con markdown puedes leer esta *[guia](https://github.com/circa75/dropplets/wiki/Markdown-Syntax-Guide)* para tener mayor información de como hacerlo.

Las imagenes deben tener las siguientes caracteristicas:

* Ancho: 200px
* Alto: 200px

## Temas y normas para la publicación

Hay una gran variedad de temas que sería genial leer en **abr4xas.org** podemos tener publicaciones sobre sus opiniones personales acerca de cualquier cosa, pero estos temas:

* No deben violar ningun derecho de ```copyright```.
* No deben ser sobre racismo.
* Ni hablar de **POLITICA**.
* Pornografia.

Cualquier publicación que viole estas normativas será eliminado.

## Ya envie mi post, ¿cuando será publicado?

El post pasa a estar publicado luego que sea aceptado el pull request. Este proceso es de aproximadamente 10 minutos.

## Licencia

Todos los post estan disponible bajo *[CC 4.0 (by-nc-sa)](http://creativecommons.org/licenses/by-nc-sa/4.0)* a menos que, el autor decida incluir una licencia diferente..


### NOTA

* Por favor, no editar el contenido de ```CNAME ``` en ```content/extra``` ¡Gracias!
* Si se necesita crear otra pagina, crear un ticket *[aquí](https://github.com/abr4xas/post/issues)*.
