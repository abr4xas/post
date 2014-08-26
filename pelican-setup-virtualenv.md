Title: Instalando pelican en virtualenv
Date: 2014-07-21 10:21
Category: Linux
Tags: Linux, Dev, Web, Pelican
Slug: pelican-setup-virtualenv
Author: abr4xas
twitter: abr4xas
Summary: Pelican es un generador estático de contenido, al estilo de Jekyll. Por si fuera necesario, en [Static Site Generators](http://staticsitegenerators.net/) hay una recopilación de proyectos similares.
image: https://raw.githubusercontent.com/abr4xas/post/master/images/2043492.png

### Paso 1

En consola escribimos lo siguiente: (Como root/sudo)

```
aptitude install python-virtualenv
```

Luego

```
aptitude install python-pip
```
Nos movemos a nuestra carpeta de trabajo:

```bash
cd ~/virtualenv # La carpeta la pueden llamar como quieran ;)
```
Creamos un directorio de trabajo con ```virtualenv``` para nuestro pelican:

```bash
virtualenv pelican
New python executable in pelican/bin/python
Installing setuptools, pip...done.

```

Ahora, entramos en el directorio llamado pelican y escribimos
```bash
. bin/activate
```

Y veremos en la terminal, algo como esto:
```bash
(pelican)abr4xas@hp ~/virtualenv/pelican $
```

Escribimos:
```bash
pip install pelican Markdown
```

Ya con esto, tenemos -hasta los momentos- lo necesario para trabajar con pelican :D
