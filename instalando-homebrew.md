Title: Instalando Homebrew
Date: 2014-12-13 19:20
Category: Apple
Tags: mac, apple, os
Slug: instalando-homebrew
Author: abr4xas
twitter: abr4xas
Summary: Instalando homebrew en la mac, para tener todo lo que Apple no quiere que tenga xD 
image: /images/brew.png

![Instalando Homebrew](images/brew.png)

Este será un post sencillo y directo... Así que vamos a ello!!

Para instalar homebrew solo debemos colocar en la terminal:

```bash
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
le damos enter y vamos a obtener una salida parecida esta:

```bash
==> This script will install:
/usr/local/bin/brew
/usr/local/Library/...
/usr/local/share/man/man1/brew.1

Press RETURN to continue or any other key to abort # le damos a enter para continuar
==> /usr/bin/sudo /bin/mkdir /usr/local
Password:
==> /usr/bin/sudo /bin/chmod g+rwx /usr/local
==> /usr/bin/sudo /usr/bin/chgrp admin /usr/local
==> /usr/bin/sudo /bin/mkdir /Library/Caches/Homebrew
==> /usr/bin/sudo /bin/chmod g+rwx /Library/Caches/Homebrew
==> Downloading and installing Homebrew...
==> Installation successful!
==> Next steps
Install the Command Line Tools for Xcode: https://developer.apple.com/downloads
Run `brew doctor` before you install anything
Run `brew help` to get started
TMA:/ abr4xas$ brew doctor
Please note that these warnings are just used to help the Homebrew maintainers
with debugging if you file an issue. If everything you use Homebrew for is
working fine: please don't worry and just ignore them. Thanks!

Warning: Git could not be found in your PATH.
Homebrew uses Git for several internal functions, and some formulae use Git
checkouts instead of stable tarballs. You may want to install Git:
  brew install git

Warning: No developer tools installed.
You should install the Command Line Tools.
The standalone package can be obtained from
  https://developer.apple.com/downloads
or it can be installed via Xcode's preferences.
```
Luego de eso, nos toca instalar ```Xcode command line tools```

Puedes instalar el instalador desde esta pagina de  
[descargas](https://github.com/kennethreitz/osx-gcc-installer/downloads) o puedes usar los siguentes links:

* OS X 10.8 Mountain Lion: [GCC-10.7.pkg](https://github.com/downloads/kennethreitz/osx-gcc-installer/GCC-10.7-v2.pkg) (Includes 10.7 Headers, so use with caution).
* OS X 10.7 Lion: [GCC-10.7.pkg](https://github.com/downloads/kennethreitz/osx-gcc-installer/GCC-10.7-v2.pkg)
* OS X 10.6 Snow Leopard: [GCC-10.6.pkg](https://github.com/downloads/kennethreitz/osx-gcc-installer/GCC-10.6.pkg)

Ahora, para revisar si todo esta bien probamos instalando ```wget``` para eso, escribimos en la terminal:

```bash
$ brew install wget
```
Y debemos tener un mensaje parecido a este (despues de instalar sus dependencias que son: ```xz```, ```makedepend```, ```openssl```):

```bash
==> Installing wget
==> Downloading http://ftpmirror.gnu.org/wget/wget-1.16.tar.xz
🍺  /usr/local/Cellar/wget/1.16: 9 files, 956K, built in 115 seconds
```
Listo!! Ya tenemos ```brew```, ```Xcode command line tools``` y ```wget``` instalados en el MAC :D

## Concideraciones:

Es recomendable hacer:

* ```brew update```
* ```brew doctor```

## ACTUALIZADO 

Luego de instalar las ```Xcode command line tools``` me dio "ciertos" problemas al instalar git, abri este ticket [#34960](https://github.com/Homebrew/homebrew/issues/34960#issuecomment-66895313) y la respuesta de @[jacknagel](https://github.com/Homebrew/homebrew/issues/34960#issuecomment-66895313) fue muy "directa" debido a esto, realice lo siguiente:

* Desinstalar ```osx-gcc-installer```
* Reiniciar
* Instalar Xcode 4.3 
* Correr nuevamente ```brew doctor```
* Listo

### Como desinstalar ```osx-gcc-installer```

Facil!!

En la terminal como root escribimos ```/Library/Developer/4.1/uninstall-devtools -mode=all``` esperamos unos momentos y listo, ya eliminamos ```osx-gcc-installer```.

Continuamos con los otros pasos.

## Instalando ```Xcode 4.3```

Vamos a [developer.apple.com](https://developer.apple.com/downloads) buscamos ```Xcode 4.3``` lo bajamos (pesa 137 mb) lo instalamos y listo. 

## Que paso con git?

Bueno, facil... En la terminal:

```bash
$ brew install git
```
Dejamos que haga lo que tenga que hacer y...

```bash
$ brew info git
git: stable 2.2.0, HEAD
http://git-scm.com
/usr/local/Cellar/git/2.2.0 (1351 files, 32M) *
  Built from source
From: https://github.com/Homebrew/homebrew/blob/master/Library/Formula/git.rb
```

Escribimos nuevamente: ```echo 'export PATH="/usr/local/bin:/usr/local/sbin:~/bin:$PATH"' >> ~/.bash_profile```, reiniciamos la terminal (la cerramos) escribimos ```git --version``` y debemos tener un resultado como este: ```git version 2.2.0```

## Y que dice el doctor?

Bueno, ```brew doctor``` sigue diciendo:

```bash
$ brew doctor
Please note that these warnings are just used to help the Homebrew maintainers
with debugging if you file an issue. If everything you use Homebrew for is
working fine: please don't worry and just ignore them. Thanks!

Warning: A newer Command Line Tools release is available.
The standalone package can be obtained from
  https://developer.apple.com/downloads
or it can be installed via Xcode's preferences.
```
Claro, sigue notificando que hay una nueva version de las ```Command Line Tools``` pero vamos, estoy usando (aun) Lion asi que no puedo hacer mas nada. :)

Espero que les sea util este post!!
