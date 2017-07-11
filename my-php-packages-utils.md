Title: Pequeño paquete de composer para php con algunas cosas útiles 
Date: 2017-07-11 17:11
Category: dev
Tags: php, laravel
Slug: my-php-packages-utils
Author: abr4xas
twitter: abr4xas
Summary: Este *composer package* fue creado con la idea de agilizar un poco las cosas que uso día a día...
image:
header_image: https://buddy.works/data/blog/_thumbnails/cover-php-logo.png


Un simple *composer package* que puede servir de utilidad a cualquiera. Esta compuesto por:

* Gravatar
* Simple generador de url amigable
* Hash de password
* Formateo de moneda
* Debug

### instalación

Muy facil, con composer:

```bash
$ composer require abr4xas/utils
$ composer dumpautoload -o // optional
```

### componentes


```php
use Abr4xas\Utils\SeoUrl;
use Abr4xas\Utils\Hash;
use Abr4xas\Utils\Debug;
use Abr4xas\Utils\Money;
use Abr4xas\Utils\Gravatar;
```

### como usuarlo

```php

<?php

require 'vendor/autoload.php';

use Abr4xas\Utils\SeoUrl;

SeoUrl::generateSlug('this is an awesome string'); // this-is-an-awesome-string


use Abr4xas\Utils\Hash;
// read the docs :smile:

use Abr4xas\Utils\Debug;

Debug::dieDump($var);

use Abr4xas\Utils\Money;

Money::generaFormato(200, ['s' => 'USD$']); // USD$ 200.00
Money::generaFormato(200, ['s' => 'USD$', 'd' => 4]); // USD$ 200.0000

Money::quitarFormato('USD$ 200',  ['s' => 'USD$']); // 200.00
Money::quitarFormato('USD$ 200',  ['s' => 'USD$', 'd' => 4]); // 200.0000

use Abr4xas\Utils\Gravatar;

Gravatar::getAvatarUrl('email@domain.tld', ['s'=> 80, 'd'=>'mm', 'secure' => true]);

```

Recomiendo que leean la documentación dentro de cada archivo para que tengan una mejor idea de como usar esto y sacarle mayor rendimiento.