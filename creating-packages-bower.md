Title: Crear un paquete con bower
Date: 2014-08-07 10:20
Category: Web
Tags: bower, npm, web
Slug: creating-packages-bower
Author: abr4xas
twitter: abr4xas
Summary: Bower, un simple y fácil gestor de paquetes para la web. Depende de Node y de NPM y funciona a través de consola
image: images/bower-logo.png


![Bower.io]({filename}/images/bower.png)

Bower, un simple y fácil gestor de paquetes para la web. Depende de Node y de NPM y funciona a través de consola, se puede instalar fácilmente así:

```
npm install -g bower
```

## bower.json

Los paquetes son definidos por el archivo manifiesto ```bower.json``` que es muy similar  al ```package.json``` de node o al ```Gemfile``` de Ruby.

## Creando nuestro plugin/paquete

Necesitamos:

* Una cuenta en github.
* Lo que vamos a publicar.

Asumiendo que cumplimos esos requisitos, y que estamos en nuestro directorio de trabajo desde consola escribimos:

```
 bower init
```

Ese comando define muchas opciones para saber más sobre ellas, clic [aquí](https://github.com/bower/bower.json-spec).

## Ejemplo

Veamos un ejemplo de como seria el manifiesto ```bower.json```
```
{
  "name": "custom.css",
  "version": "0.1",
  "main": "path/to/main.css",
  "ignore": [
    ".jshintrc",
    "**/*.txt",
    "**/.*",
    "node_modules",
    "bower_components",
    "test",
    "tests"
  ],
  "dependencies": {
    "<name>": "<folder>",
    "<name>": "<package>"
  },
  "homepage": "",
  "authors": [
    "name <mail@domain>"
  ],
  "description": "Lorem Ipsum",
  "keywords": [
    "custom",
    "bootstrap"
  ],
  "license": "GPL2"
}
```
## Registro

Registrar nuesto paquete/plugin permite instalarlo de la siguiente forma: ```bower install <nombre-paquete>```.

Entonces, para registrar lo que hicimos debemos escribir en consola

```
bower register example git://github.com/user/example.git
```
donde: 

 * example es el nombre de nuestro plugin/paquete
 * ```git://github.com/user/example.git``` debemos cambiar los valores correspondientes a nuestro usuario y repo en github

Esto es todo :D
Gracias por la visita!!