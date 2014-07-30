Title: Hello world: Laravel
Date: 2014-05-07 10:20
Category: dev
Tags: php, laravel
Slug: hello-world-laravel
Author: abr4xas
twitter: abr4xas
Summary: Mis experiencias con Laravel 4. Practicamente desde cero... =P
image: images/laravel.png

 > Laravel como tal trabaja especificamente con "Routes with Closures" en lugar de un MVC tradicional con el objetivo de hacer el código más claro. Aun así permite el uso de MVC tradicional.

Este (y posiblemente otros) post serán una pequeña introducción para entender un poco Laravel.

## Puesta en marcha
Requerimientos previos:
```bash
aptitude install php5-cli
```
Luego:
```bash
curl -sS https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer
```
Y ya con esto podemos ejecutar composer en cualquier otro proyecto que lo necesite :)

## Obteniendo Laravel

Existen dos formas de obtener laravel

 * La primera: Un .ZIP desde el repo de github haciendo clic (link: https://github.com/laravel/laravel/archive/master.zip text: aquí popup: yes)
 * La segunda: Clonando el repo https://github.com/laravel/laravel

Yo, seleccione el .ZIP :problem:

## Manos a la obra

Procedemos a obtener todo lo necesario para poder trabajar con laravel usando composer:
```bash
composer install
```
**BTW**...

Si de casualidad presentan algun tipo de error con php5-mcrypt hagan esto:

```bash
     aptitude install mcrypt
     aptitude install php5-mcrypt
```

Y luego:

     sudo ln -s /etc/php5/conf.d/mcrypt.ini /etc/php5/mods-available
     sudo php5enmod mcrypt
     sudo service apache2 restart

update
<strike>NOTA: El primer cambio que hice fue renombrar server.php a index.php </strike>
Escribimos en la terminal: 

```bash
     php artisan serve
```

Y vamos a obtener algo como esto:

```bash
     Laravel development server started on http://localhost:8000
```

Y listo :)

Ajá... Si ya no tenemos ningun tipo de error procedemos:

Usando nuestro editor de texto preferido navegamos hasta:

```
app/controllers/HomeController.php
```

Y vamos a ver algo parecido a esto:

```
public function showWelcome()
{
    return View::make('hello');
}
```     
En este punto, estamos "trabajando" con el controlador pero necesitamos saber a donde va ( o viene sengun como lo quieran ver) los llamados que se hacen para mostrar las paginas que estemos visualizando y es por esto que debemos revisar el siguiente archivo:

```
app/routes.php
```
Donde, vamos a ver algo como esto:

```
     Route::get('/', function()
     {
         return View::make('hello');
     });
```
Ahí esta llamando a una "**vista**" llamada "*hello*" entonces navegamos hasta:

     app/views/hello.php

Y vemos que es el "hello world" de Laravel.

¿Que les parece si cambiamos todo lo que esta ahí por:

     <h1>Hola mamá, estoy usando Laravel</h1>

Guardamos el archivo que modificamos y listo, al ejecutar laravel nuevamente en nuestro web server local vamos a ver los cambios que hicimos.

Si, nada del otro mundo pero, poco a poco iremos haciendo más cosas :D

Dejemos esto por los momentos en este punto, luego seguiremos con esto.