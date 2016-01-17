Title: Hashing Passwords con php
Date: 2016-01-17 16:20
Category: php
Tags: php
Slug: hash-password-php
Author: abr4xas
twitter: abr4xas
Summary: Pequeña implementacion de php para hacer un hash de contraseñas.
image: https://camo.githubusercontent.com/ffa7f25498b6130088f019f6cfce7255fd50406a/687474703a2f2f692e696d6775722e636f6d2f6d7563734c2e6a7067

![Y U NO HASH PASSWORD?](https://camo.githubusercontent.com/ffa7f25498b6130088f019f6cfce7255fd50406a/687474703a2f2f692e696d6775722e636f6d2f6d7563734c2e6a7067)

Una de las formas mas faciles de crear un hash para las contraseñas usando php es `md5` podemos ver en este ejemplo como implementarlo:

```php
md5('password');
```

Esto nos dara como resultado algo asi: `5f4dcc3b5aa765d61d8327deb882cf99`

Pero, realmente esto no es muy efectivo.

## Usando `password_hash`

Usando la documentacion de php nos dice que para usar esta funcion debemos hacer lo siguiente:

```php
string password_hash ( string $password , integer $algo [, array $options ] )
```

### Algoritmos soportados

* PASSWORD_DEFAULT
* PASSWORD_BCRYPT

### Opciones soportadas:

* Salt
* Cost

## Como usar `password_hash`

### Usando `PASSWORD_DEFAULT`

```php
password_hash('password', PASSWORD_DEFAULT);
```
Esto nos dara como resultado algo asi: `$2y$10$hdbF9lyKu5sWphXMtDB46eAO0RNYYlSTufwqIvmC6AC7xhC27s2w.`

### Usando `PASSWORD_BCRYPT`

```php
echo password_hash('password', PASSWORD_BCRYPT);
```
Esto nos dara como resultado algo asi: `$2y$10$U4cpa/joKALEIIZT72K.Ze7s4S2eXTxee4NpnoOgZEZuqwCo1ZCQK`


Vamos un poco mas alla...

Tomando en cuenta lo que nos dice la documentacion aun podemos pasarle un tercer parametro que sera un `array` con ciertas caracteristicas:

```php

$options = [
    'cost' => 11,
    'salt' => mcrypt_create_iv(22, MCRYPT_DEV_URANDOM),
];
```

Y nuestra pequeña funcion pasa a ser esto:

```php
echo password_hash('password', PASSWORD_BCRYPT, $options);
```
Esto nos dara como resultado algo asi: `$2y$11$7.RPImGZC4gN/Tf5sInLGeOkqtUirnway.gOEacAdmlOFk.ipPL4m`

> Hay que tener en cuenta que la opcion `salt` ya se encuentra `deprecated` en la version 7.0.0 de php por lo cual, recomiendan usar el `salt` que se genera por defecto.


Como podemos ver en los resultados de cada ejemplo hay ciertas cosas que siempre van a ser iguales (en el caso que no cambiemos el valor de `cost`) y esto lo podemos ver en la siguiente imagen:

![Ejemplo de hash password con php](http://php.net/manual/en/images/2a34c7f2e658f6ae74f3869f2aa5886f-crypt-text-rendered.svg)



Espero que esto les sea de utilidad.

Lecturas recomendadas:

[http://php.net/manual/en/function.password-hash.php](http://php.net/manual/en/function.password-hash.php).
