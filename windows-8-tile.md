Title: Creando tiles de Windows 8.1 para nuestro sitio web
Date: 2014-12-28 10:20
Category: web
Tags: web
Slug: windows-8-tile
Author: abr4xas
twitter: abr4xas
Summary: Como crear las famosas tiles de windows 8.1 para nuestro sitio web
image: http://www.technologytell.com/gadgets/files/2013/11/Windows-8_1_3.jpg

Las tiles son pequeños recuadros que conforman una pantalla de inicio bastante dinámica mostrando en llamativos 
colores la información necesaria para mostrar lo que sucede en nuestras aplicaciones instaladas.

En esta oportunidad, vamos a aprender como crear unas tiles personalizadas para nuestro sitio web:

## Facil

No es cosa del otro mundo ni complicada hacer solo debemos ir a este sitio [web](http://www.buildmypinnedsite.com) y seguir
los pasos que nos piden.

* Title
  * Que es el titulo de nuestro sitio web
* Background color 
  * Que no es mas que el color de fondo del "tile"
* Subir una imagen
 * Esta imagen puede ser el logo de nuestra web
* Notificaciones
 * En este apartado debemos colocar la URL de nuestro feed
* Obtenemos el codigo
 * Hay varias formas de usarlo
  * Subiendo los archivos que nos proporcionan en la pagina web
  * Agregando una meta etiqueta
  
## Agregando estos cambios al blog

Este blog usa pelican, un generador de contenidos estatico que funciona con python si tambien usas pelican y quieres
agregar una tile a tu blog debes incluir esto en tu ```pelicanconf.py```

```python
STATIC_PATHS = ['static/browserconfig.xml',
		'static/large.png',
		'static/square.png',
		'static/tiny.png',
		'static/wide.png',]

EXTRA_PATH_METADATA = {
    'static/browserconfig.xml': {'path': 'browserconfig.xml'},
    'static/large.png': {'path': 'large.png'},
    'static/square.png': {'path': 'square.png'},
    'static/tiny.png': {'path': 'tiny.png'}, 
    'static/wide.png': {'path':'wide.png'},
}
```

Yo tengo el contenido dentro de una carpeta llamada static.

Esto es todo, espero que les guste!!

Saludos
