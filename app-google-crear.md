Title: Como crear una APP para #google chrome web store.
Date: 2011-11-07 23:56
Category: Dev
Tags: google, app
Slug: app-google-crear
Author: abr4xas
twitter: abr4xas
Summary: Bueno, este post es muy interesante ya que nos enseña una forma rápida y muuuuy sencilla de crear una pequeña app para la web store de google chrome, que funciona para nuestro blog o pagina web.
image: 

Bueno, este post es muy interesante ya que nos enseña una forma rápida y muuuuy sencilla de crear una pequeña app para la web store de google chrome, que funciona para nuestro blog o pagina web.

Este post es original de **Hamedullah Khan** para
[http://technorious.com](http://technorious.com/how-to-create-a-google-chrome-web-store-app-for-your-blog.html "How to Create a Google Chrome Web Store App for Your Blog").

La idea de esto es que las personas que visitan nuestro blog/pagina y
usen google chrome tengan una forma más rápida de entrar a nuestro blog.

Bueno, aquí vamos:

Principalmente debemos tener en cuenta:

-   Que nuestro blog/pagina web este registrado debidamente en [Google
    Webmaster
    Tools.](https://www.google.com/webmasters/tools/home?hl=es "Herramientas para webmasters de Google ")
-   Tener una TDC y pagar \$5 para poder publicar nuestras app.

Ok, independientemente de que tengamos o no, una TDC podemos hacer
nuestra app ya que la misma quedara guardada como un borrador en nuestro
"***Developer Dashboard***" :)

-   De tener una TDC debemos ir directamente a "**[Pay this fee
    now](https://chrome.google.com/webstore/developer/purchase_signup_fee?hl=en-US&continue=https://chrome.google.com/webstore/developer/dashboard?hl%3Den-US "A one-time developer registration fee of US$5.00 is required to verify your account and publish items.")**"
    y pagar los \$5 xD..
-   Debemos crear una carpeta, en mi caso la llame "*abr4xas*" en esa
    carpeta debemos tener 2 archivos el primero de ellos es un archivo
    de texto llamado: "***manifest.json***" en el cual debemos incluir:

```
{ 
    "name": "El blog de abr4xas", 
    "description": "Un blog de tecnologia, linux y cualquier otra cosa interesante", 
    "version": "0.1", 
    "icons": { "128": "icon_128.png" }, 
    "app": { 
        "urls": [ "http://abr4xas.org/" ], 
        "launch": { 
        "web_url": "http://abr4xas.org/" 
        } 
    } 
}
```
¿vieron los \_ÚNICOS\_ campos que hay que cambiar verdad? Si, son:
"name, description, urls, web\_url"

-   Debemos crear un icono de nuestro blog o web de 128\*128 en formato
    png y el mismo debe ser llamado "***icon\_128.png***"
-   Hacemos unos screenshot y los mismos deben ser de 400×275 y de igual
    forma en formato png.
-   Ahora, a comprimir esa carpeta que hicimos a un .zip, en mi caso
    quedo abr4xas.zip
-   Hacemos el upload, luego de eso llenamos todo el formulario que nos
    aparece posterior a la subida de nuestro archivo.
-   Y si pagaron la cuota única de \$5 pues publican su app :)

 

Aqui, como se vería nuestra app en la chrome web store:
