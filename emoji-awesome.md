Title: Twemoji Awesome
Date: 2016-05-11 22:00
Category: Web
Tags: web
Slug: emoji-awesome
Author: abr4xas
twitter: abr4xas
Summary: Es como Font Awesome pero con los Emojis de Twitter.
image: //catherinecgilmore.com/wp-content/uploads/2015/10/Twitter-emogie-wink-300x300.png
header_image: https://camo.githubusercontent.com/018d8e8aa89e4f7660b1e14b9f7eb65556c619b7/687474703a2f2f692e696d6775722e636f6d2f353656486e4d362e706e67

Los estilos emoji se definen en `twemoji-awesome.css`. Como los de font awesome que utiliza `fa-*`, Twemoji awesome utiliza `twa- *` de nombres de clase.

Como font awesome, puede cambiar los tamaños del emoji usando `TWA-lg`, `TWA-2x`, `3x-TWA`, `TWA-4x` y `5x-TWA`.

Twemoji Awesome utiliza imágenes SVG como imágenes de fondo, y algunos navegadores no soportan esto. 
Las imágenes son servidas desde MaxCDN (muchas gracias) <i class="twa twa-1f62c"></i>

Código bajo licencia de MIT. Gráficos autorizado debajo CC-BY.

Es un trabajo original del: [Elle Kasai](http://twitter.com/ellekasai).


Seguro se preguntan la razón de hacer un fork y la respuesta es muy sencilla no usaba todos los emojis que ofrece twitter y este fork contempla todos esos emojis faltantes como el uso de la versión 2.

## Como instalarlo

### bower

```bash
$ bower install twemoji-awesome --save
```
Despues agregamos: 


```html
<link rel="stylesheet" href="/node_modules/twemoji-awesome/twemoji-awesome.min.css">
```

### npm

```bash
$ npm install twemoji-awesome
```
Despues agregamos: 

```html
<link rel="stylesheet" href="/node_modules/twemoji-awesome/twemoji-awesome.min.css">
```

## Como usar

Muy facil, hay que incluir los nombres de clases correspondiente al emoji que queremos usar por ejemplo:

<i class="twa twa-2665"></i> se genera con `<i class="twa twa-2665"></i>`

### más info

* Repo: <a href="http://abr4xas.github.io/twemoji-awesome" target="_blank">aquí</a>
* Demo: <a href="http://abr4xas.github.io/twemoji-awesome/demo.html" target="_blank">aquí</a>