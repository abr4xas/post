Title: Fusión de diferentes ramas git
Date: 2014-07-14 10:20
Category: Git
Tags: github, git, terminal
Slug: merge-branches-git-terminal
Author: abr4xas
Summary: Fusión de diferentes ramas git a través de la línea de comandos 
image: https://github.global.ssl.fastly.net/images/modules/logos_page/GitHub-Logo.png

## Paso 1: 

Desde el repositorio del proyecto, revisamos la nueva rama y probamos los cambios

```
git checkout -b spinner-dev-master master
git pull https://github.com/spinner-dev/ptemplate.git master
```

## Paso 2: 

Combinamos los cambios y actualizamos el repo

```
git checkout master
git merge --no-ff spinner-dev-master
git push origin master
```

### NOTA

Realizar los cambios correspondientes, ```spinner-dev-master``` es un repo de ejemplo para este post.