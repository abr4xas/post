Title: Cómo crear una tarjeta de Twitter para nuestro sitio web
Date: 2014-11-17 10:20
Category: Web
Tags: twitter
Slug: twitter-card
Author: abr4xas
twitter: abr4xas
Summary: Twitter, desde su nacimiento se convirtió en una de las redes sociales más importantes e influyentes para cualquier evento, es usado por muchas empresas, periódicos, agencias de noticias para dar a conocer lo que ocurre actualmente. Se han presentado muchos cambios, desde su aspecto visual a la forma en que usamos esta herramienta.
image: http://rincondelatecnologia.com/wp-content/uploads/2014/10/2013-07-Original-Logo-Twitter-Cover-Pictures-HD.png

Se han presentado muchos cambios, desde su aspecto visual a la forma en que usamos esta herramienta. Uno de esos grandes cambios fue la implementación de “Twitter Cards” que no es más que una opción que nos permite poder brindarle al usuario una experiencia multimedia directamente en los “Tweets” para así llamar la atención de nuestros seguidores y que visiten nuestro sitio web.
Como tal, no es nuevo este tipo de técnica, también la ha adoptado Facebook con el uso de Open Graph, solamente con agregar unas pocas etiquetas META en cada página también nos permite agregar contenido multimedia como pueden ver en la siguiente imagen:

![Ejemplo de cómo crear una tarjeta de Twitter para nuestro sitio web](http://rincondelatecnologia.com/wp-content/uploads/2014/10/851569_1406614399603193_975159646_n.png)

## Pasemos a lo que venimos…
### ¿Como implementar las tarjetas de Twitter en nuestro sitio web?

Debemos saber que es lo que queremos mostrar en nuestra tarjeta, debemos seleccionar entre:

* Tarjeta de Resumen: La tarjeta por defecto, incluye el título, descripción, miniatura y cuenta atribución Twitter.
* Tarjeta de Resumen con Ampliación de imagen: Similar a una tarjeta de resumen, pero con una imagen de un lugar destacado.
* Foto Tarjeta: Una tarjeta con sólo una foto.
* Tarjeta de galería: Una tarjeta que destaca una colección de cuatro fotos.
* Tarjeta App: Una tarjeta a los detalles de una aplicación móvil con descarga directa.
* Card Player: Una tarjeta para proporcionar vídeo / audio / media.
* Ficha de Producto: Una tarjeta optimizado para información del producto.

Imaginemos que, vamos a usar la tarjeta de resumen que se puede utilizar para muchos tipos de contenido de la web, de blogs y artículos de noticias, de productos y restaurantes. Está diseñado para dar al lector una vista previa del contenido antes de hacer clic  y visitar nuestra web.

## Codigo de ejemplo

```html
<meta name="twitter:card" content="summary" />
<meta name="twitter:site" content="@flickr" />
<meta name="twitter:title" content="Small Island Developing States Photo Submission" />
<meta name="twitter:description" content="View the album on Flickr." />
<meta name="twitter:image" content="https://farm6.staticflickr.com/5510/14338202952_93595258ff_z.jpg" />
<meta name="twitter:url" content="https://www.flickr.com/photos/unicphoto/sets/72157645001703785/" />
```

Solamente, con colocar esas meta etiquetas vamos a obtener algo como esto:

![Ejemplo de cómo crear una tarjeta de Twitter para nuestro sitio web](http://rincondelatecnologia.com/wp-content/uploads/2014/10/twitter-card.png)

De esta forma se ve en el “time line” de la persona que publica el enlace:

![Ejemplo de cómo crear una tarjeta de Twitter para nuestro sitio web](http://rincondelatecnologia.com/wp-content/uploads/2014/10/twitter-card2.png)

¿Se ve interesante verdad?

## Pero esto no es todo…

Aja, a que no pensaron que hay que validar lo que hicimos para saber si lo hicimos bien verdad? Bueno, esto no es nada del otro mundo, solo debemos ir a esta dirección Card validator y colocar la url de nuestra web (o la pagina donde implementamos la tarjeta) y listo.

Si presentas algún inconveniente puedes usar el sistema de comentarios, que con gusto voy ayudarte!!


[Fuente original](http://rincondelatecnologia.com/como-crear-una-tarjeta-de-twitter-para-nuestro-sitio-web/).


