Title: Como usar bower
Date: 2014-08-11 10:20
Category: Web Linux
Tags: bower, npm, web
Slug: how-to-use-bower
Author: abr4xas
twitter: abr4xas
Summary: Bower es un gestor de paquetes para las tecnologías del lado del cliente. Se puede utilizar para buscar, instalar, desinstalar activos web como JavaScript, HTML y CSS.
image: https://raw.githubusercontent.com/abr4xas/post/master/images/RS5MKSa.png


![Bower.io](https://raw.githubusercontent.com/abr4xas/post/master/images/bower.png)

Bower es un gestor de paquetes para las tecnologías del lado del cliente. Se puede utilizar para buscar, instalar, desinstalar activos web como JavaScript, HTML y CSS.

Se puede instalar fácilmente así:

```
npm install -g bower
```

## ¿¡¡AYUDA!!?

Simplemente debemos escribir en consola ```bower help``` y vamos a obtener lo siguiente:

```bash
$ bower help

Usage:

    bower <command> [<args>] [<options>]

Commands:

    cache                   Manage bower cache
    help                    Display help information about Bower
    home                    Opens a package homepage into your favorite browser
    info                    Info of a particular package
    init                    Interactively create a bower.json file
    install                 Install a package locally
    link                    Symlink a package folder
    list                    List local packages
    lookup                  Look up a package URL by name
    prune                   Removes local extraneous packages
    register                Register a package
    search                  Search for a package by name
    update                  Update a local package
    uninstall               Remove a local package
    version                 Bump a package version

Options:

    -f, --force             Makes various commands more forceful
    -j, --json              Output consumable JSON
    -l, --log-level         What level of logs to report
    -o, --offline           Do not hit the network
    -q, --quiet             Only output important information
    -s, --silent            Do not output anything, besides errors
    -V, --verbose           Makes output more verbose
    --allow-root            Allows running commands as root
    --version               Output Bower version

See 'bower help <command>' for more information on a specific command.
```

## Como instalar un paquete?

Pues, facil simplemente escribiendo en consola:

```
bower install nombre_paquete
```

donde ```nombre_paquete``` es el paquete que queremos instalar... Por ejemplo:

```
bower install bootstrap
```

## Usando el paquetes

Pues, simplemente debemos hacer la referencia de donde se encuentra nuestro paquete en el archivo que estamos trabajando.

Siguiendo el ejemplo de instalar bootstrap nuestro documento html puede quedar de la siguiente forma:

```html
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge, chrome=1">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <meta name="description" content="">
        <meta name="author" content="">
        <link rel="shortcut icon" href="">
        <title>Template for Bootstrap</title>
        <!-- Bootstrap core CSS -->
        <link href="bower_components/bootstrap/dist/css/bootstrap.min.css" rel="stylesheet">
    </head>
```
## Algo más...

Realmente, no queda mucho por decir... Solo trabajar con ```bower``` para comprenderlo y poder sacarle el provecho.