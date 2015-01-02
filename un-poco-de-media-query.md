Title: Hablemos un poco sobre los media query
Date: 2015-01-01 10:20
Category: Web
Tags: web, dev
Slug: media-query
Author: abr4xas
twitter: abr4xas
Summary: En desarrollo web, Media Queries es un módulo CSS3 que permite adaptar la representación del contenido a características del dispositivo como la resolución de pantalla (por ejemplo, un smartphone frente a pantallas de alta definición) o la presencia de características de accesibilidad como el braille. Se convirtió en un estándar recomendado por la W3C en Junio del 2012.1 y es un principio básico de la tecnología de Diseño web adaptativo.
image: https://spinspire.com/sites/spinspire.com/files/field/image/95302236.png


> En desarrollo web, Media Queries es un módulo CSS3 que permite adaptar la representación del contenido a características del dispositivo como la resolución de pantalla (por ejemplo, un smartphone frente a pantallas de alta definición) o la presencia de características de accesibilidad como el braille. Se convirtió en un estándar recomendado por la W3C en Junio del 2012.1 y es un principio básico de la tecnología de Diseño web adaptativo.

wikipedia

## Entrando en materia

Las Media queries consisten de un media type y una o mas expresiones, implicando características del medio, la cual se resuelve como verdadera o falsa. El resultado de la consulta es verdadera si el tipo de medio especificado en el media query concuerda con el tipo de dispositivo que está siendo mostrado y todas las expresiones en el media query son verdaderas.

### Media que?

Los media types permiten indicar una serie de estilos que se aplicaran segun el tipo del medio, en algunas paginas, al ver el codigo fuente,
podemos encontrar algo como esto:

```html
<link rel="stylesheet" type="text/css" media="all" href="style.css">
<link rel="stylesheet" type="text/css" media="print" href="print.css">
```
Los media types más típicos son:

* all: para todo (valor por defecto).
* print: en la vista previa de impresión y a la hora de imprimir.
* screen: para las pantallas de ordenador.
* tv: para televisores.

## Media Query para los dispositivos mas comunes

```css
/* Smartphones (portrait and landscape) ----------- */
@media only screen
and (min-device-width : 320px)
and (max-device-width : 480px) {
/* Styles */
}
 
/* Smartphones (landscape) ----------- */
@media only screen
and (min-width : 321px) {
/* Styles */
}
 
/* Smartphones (portrait) ----------- */
@media only screen
and (max-width : 320px) {
/* Styles */
}
 
/* iPads (portrait and landscape) ----------- */
@media only screen
and (min-device-width : 768px)
and (max-device-width : 1024px) {
/* Styles */
}
 
/* iPads (landscape) ----------- */
@media only screen
and (min-device-width : 768px)
and (max-device-width : 1024px)
and (orientation : landscape) {
/* Styles */
}
 
/* iPads (portrait) ----------- */
@media only screen
and (min-device-width : 768px)
and (max-device-width : 1024px)
and (orientation : portrait) {
/* Styles */
}
 
/* Desktops and laptops ----------- */
@media only screen
and (min-width : 1224px) {
/* Styles */
}
 
/* Large screens ----------- */
@media only screen
and (min-width : 1824px) {
/* Styles */
}
 
/* iPhone 4 ----------- */
@media
only screen and (-webkit-min-device-pixel-ratio : 1.5),
only screen and (min-device-pixel-ratio : 1.5) {
/* Styles */
}
```

Si bien es cierto que existen frameworks css que ayudan en el desarrollo de los sitios web no necesariamente TODO
lo que tiene ese framework lo usamos. Un ejemplo claro de esto es bootstrap, tiene muchas cosas que ayudan al desarrollo
pero nunca llegamos a usar todo el potencial que nos ofrece.

Bootstrap es genial, pero como dije arriba realmente no usamos todo el potencial que nos ofrece, y vamos a tener 
codigo innecesario en nuestras aplicaciones web cuando solamente usamos el 10% del framework.


