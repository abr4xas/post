Title: twig-slug una micro extensión para twig
Date: 2017-07-11 17:11
Category: dev
Tags: php, laravel,twig
Slug: my-php-packages-twig-slug
Author: abr4xas
twitter: abr4xas
Summary: Esta extensión de twig nació por la idea de solventar un pequeño inconveniente con un proyecto donde estaba trabajando...
image:
header_image: https://dab1nmslvvntp.cloudfront.net/wp-content/uploads/2015/05/1432540034Screenshot-2015-05-25-09.46.24-1024x336.png


Pues si, estaba trabajando en un proyecto donde se hizo una migración de un código anticuado a algo un poco más actualizado. Se necesitaba trabajar con url amigables entre otros requerimientos...

## Twig Slug Generator


A [Twig](http://twig.sensiolabs.org/) extension for [abr4xas/twig-slug](https://github.com/abr4xas/twig-slug).

## how to install

```bash
$ composer require abr4xas/twig-slug
$ composer dumpautoload -o // optional
```
or add this to your `composer.json`

```json
    "require": {
        "abr4xas/twig-slug": "dev-master"
    }
```
and

```bash
$ composer update
$ composer dumpautoload -o // optional
```

## usage

First register the extension with Twig:

```php
$twig = new Twig_Environment($loader);
$twig->addExtension(new \SeoUrl\SeoUrl());
```

then use it in your templates:

```
{{ This is an awesome string | seourl }} // output: this-is-an-awesome-string
```

in `SomeController` like this:

```php
<?php

namespace SomeNameSpace;

use SeoUrl\SeoUrl;

class SomeController
{
    public function someFunction()
    {
        $str = 'This is an awesome string';

        $seoUrl = SeoUrl::generateSlug($str); // output: this-is-an-awesome-string

    }
}
```