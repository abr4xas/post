Title: Coffeekup, el lenguaje de marcado para Coffeescript 
Date: 2014-10-10 10:35
Category: Web
Tags: Web, Javascript
Slug: coffeekup
Author: abr4xas
twitter: abr4xas
Summary: CoffeeKup es un motor de plantillas para Node.js y navegadores que le permite escribir sus plantillas HTML en 100% CoffeeScript puro. Fue creado en la celebración de whyday, como una aplicación del concepto utilizado en Markaby ("marcado como Ruby", por Tim Fletcher y por qué la dura suerte) a CoffeeScript.
image: images/coffeekup.png

![Coffeekup, el lenguaje de marcado para Coffeescript](http://cdn.codevisually.com/wp-content/uploads/2014/04/coffeekup.jpg)

### CoffeeKup 

Es un motor de plantillas para Node.js y navegadores que le permite escribir sus plantillas HTML en 100% CoffeeScript puro. Fue creado en la celebración de whyday, como una aplicación del concepto utilizado en Markaby ("marcado como Ruby", por Tim Fletcher y por qué la dura suerte) a CoffeeScript.

### Como instalar CoffeeKup


Asumiendo que tenemos node,js y npm instalados en nuestro equipo

```
npm install coffeekup

```
Para instalarlo de forma global solo hay que escribir:

```
npm install coffeekup -g

```
Si queremos usar la ultima version:

```
git clone git@github.com:mauricemach/coffeekup.git && cd coffeekup
cake build
npm link
cd ~/myproject
npm link coffeekup

```

### Necesitas ayuda?

Simplemente escribe en la terminal ```coffeekup -h``` y vas a tener un resultado como este:

```
$ coffeekup -h

Usage:
  coffeekup [options] path/to/template.coffee

      --js           compile template to js function
  -n, --namespace    global object holding the templates (default: "templates")
  -w, --watch        watch templates for changes, and recompile
  -o, --output       set the directory for compiled html
  -p, --print        print the compiled html to stdout
  -f, --format       apply line breaks and indentation to html output
  -u, --utils        add helper locals (currently only "render")
  -v, --version      display CoffeeKup version
  -h, --help         display this help message

```



### Y que es CoffeScript
![Coffescript](http://coffeescript.org/documentation/images/logo.png)
CoffeeScript es un pequeño lenguaje que compila en JavaScript. Por debajo de ese torpe pátina-esque Java, JavaScript siempre ha tenido un corazón precioso. CoffeeScript es un intento de exponer las partes buenas de JavaScript de una manera sencilla.


### CoffeeScript Un pequeño gran libro

Descubre como convertirte en un mejor desarrollador escribiendo JavaScript con CoffeeScript, el lenguaje que ha revolucionado el mundo web y que empresas como AirBnB o Dropbox lo utilizan actualmente en sus productos.
<iframe width="100%" height="400" src="https://leanpub.com/coffeescript/embed?a=1JMUVmdjLCzfZh6oVhu5bb" frameborder="0" allowtransparency="true"></iframe>
**Escrito por**: Javi Jimenez @soyjavi, quien es fundador de Tapquo, empresa especializada en el desarrollo de la movilidad con HTML5, con más de 15 años de experiencia en el mundo del código, los pixeles y la creatividad. Miembro de la W3C, evangelista de los estándares abiertos y de la web como plataforma universal para los desarrolladores. Craftman amante de Javascript y creador de herramientas como LungoJS, QuoJS, Monocle y TukTuk usadas por miles de desarrolladores por todo el mundo.



_____________________

#### Enlaces de interes

* Para saber mas de CoffeeKup, clic [aqui](http://coffeekup.org/)
* Para saber mas de coffescript, clic [aqui](http://coffeescript.org/)
* Para saber mas de Tapquo, clic [aqui](http://tapquo.com/)
