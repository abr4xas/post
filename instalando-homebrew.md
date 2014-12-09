Title: Instalando Homebrew
Date: 2014-12-08 19:20
Category: Apple
Tags: mac, apple, os
Slug: instalando-homebrew
Author: abr4xas
twitter: abr4xas
Summary: Instalando homebrew en la mac, para tener todo lo que Apple no quiere que tenga xD 
image: http://url/de/imagen/destacada

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
