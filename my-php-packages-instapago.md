Title: Librería Instapago para PHP
Date: 2017-07-11 17:11
Category: dev
Tags: php
Slug: my-php-packages-instapago
Author: abr4xas
twitter: abr4xas
Summary: Una pequeña librería para consumir el API de instapago
image:
header_image: https://camo.githubusercontent.com/01ea404aaaf915c565787cceaf98303955d9776b/68747470733a2f2f69302e77702e636f6d2f706c7567696e732e73766e2e776f726470726573732e6f72672f2173766e2f62632f313538333935332f696e7374617061676f2f6173736574732f62616e6e65722d373732783235302e706e67


Como todos saben instapago una solución tecnológica pensada para el mercado de comercio electrónico (eCommerce) en Venezuela y Latinoamérica, con la intención de ofrecer un producto de primera categoría, que permita a las personas y empresas apalancar sus capacidades de expansión, facilitando los mecanismos de pago para sus clientes, con una integración amigable a los sistemas que actualmente utilizan.

Aprovechando la oportunidad, les cuento que hice este [plugin de wordpress](https://wordpress.org/plugins/instapago/) para woocommerce con instapago

### instalación

```
$ composer require instapago/instapago
$ composer dumpautoload -o // opcional
```

#### como usar

creamos un archivo `index.php`

```php
<?php

require 'vendor/autoload.php';

use \Instapago\Api;


$paymentData = [
  'amount' => '200',
  'description' => 'test',
  'card_holder' => 'jon doe',
  'card_holder_id' => '11111111',
  'card_number' => '4111111111111111',
  'cvc' => '123',
  'expiration' => '12/2020',
  'ip' => '127.0.0.1',
];

try{

  $api = new Api('<keyId>','<publicKeyId>');

  $respuesta = $api->directPayment($paymentData);
  // hacer algo con $respuesta
}catch(\Instapago\Exceptions\InstapagoException $e){

  echo $e->getMessage(); // manejar el error

}catch(\Instapago\Exceptions\AuthException $e){

  echo $e->getMessage(); // manejar el error

}catch(\Instapago\Exceptions\BankRejectException $e){

  echo $e->getMessage(); // manejar el error

}catch(\Instapago\Exceptions\InvalidInputException $e){

  echo $e->getMessage(); // manejar el error

}catch(\Instapago\Exceptions\TimeoutException $e){

  echo $e->getMessage(); // manejar el error

}catch(\Instapago\Exceptions\ValidationException $e){

  echo $e->getMessage(); // manejar el error

}
```

Podemos revisar rápidamente si todo funciona correctamente escribiendo:

```bash
$ php -S localhost:8000
```

#### llaves de pruebas

```
* keyId = 74D4A278-C3F8-4D7A-9894-FA0571D7E023
* publicKeyId = e9a5893e047b645fed12c82db877e05a
```

### phpunit

```
$ phpunit --configuration="phpunit.xml.dist"
```

### enlaces

* [Documentación de la librería](https://github.com/abr4xas/php-instapago/blob/master/help/DOCUMENTACION.md)
* [Registro de cambios](https://github.com/abr4xas/php-instapago/blob/master/CHANGELOG.md)
* [Colaboración](https://github.com/abr4xas/php-instapago/blob/master/help/CONTRIBUCION.md)
* [Autores](https://github.com/abr4xas/php-instapago/blob/master/help/AUTORES.md)

### licencia

Licencia [MIT](http://opensource.org/licenses/MIT) :copyright: 2016