Title: Defer a la carga de javascript
Date: 2014-04-29 10:20
Category: Web
Tags: javascript, web
Slug: defer-loadind-javascript
Author: abr4xas
Summary: Hagamos un verdadero defer a la carga del javascript
image: http://ocpsoft.org/wp-content/uploads/2013/01/javascript_logo_unofficial-300x300.png

Hacer defer el javascript es uno de esos temas que preocupan a quienes tienen una pagina web en cuanto al tema de la optimización de la misma.

Hay gente que hace esto: 
```javascript
<script  type="text/javascript" defer="defer">
     ...
</script>
```     
O también te encuentras con quienes dicen que uses async o que lo pongas al final de la pagina para todos ellos les tengo noticias:

# ESO NO FUNCIONA
Google, en su gran sabiduría nos deja este script:
```javascript
<script type="text/javascript">
    function downloadJSAtOnload() {
    var element = document.createElement("script");
    element.src = "deferredfunctions.js";
    document.body.appendChild(element);
    }
    if (window.addEventListener)
    window.addEventListener("load", downloadJSAtOnload, false);
    else if (window.attachEvent)
    window.attachEvent("onload", downloadJSAtOnload);
    else window.onload = downloadJSAtOnload;
</script>
```

Creo que no tiene explicación ¿cierto? Por si mismo se explica pero, de igual manera acá les dejo este (link: https://developers.google.com/speed/docs/best-practices/payload#DeferLoadingJS text: enlace popup: yes) para que lean un poco más :)

Update:

Bueno si, creo que debo explicarlo un poco xD

Lo que debemos cambiar del script es lo siguiente:

```javascript
element.src = "deferredfunctions.js";
```

donde: deferredfunctions.js es nuestro script.