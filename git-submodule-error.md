Title: git submodule: “already exists in the index”
Date: 2014-08-21 11:00
Category: Git
Tags: dev, git
Slug: git-submodule-error
Author: abr4xas
twitter: abr4xas
Summary: Los submódulos en git permiten insertar uno o más repositorios externos dentro de otro repositorio. Es decir, permiten manejar uno o varios subproyectos dentro de un gran proyecto versionado con git. Esta característica puede ser útil, por ejemplo, para referenciar archivos que estén en proyectos complementarios, pero administrados por diferentes grupos o personas.
image: https://raw.githubusercontent.com/abr4xas/post/master/images/git.png


![Alt Text](http://blog.x-aeon.com/wp-content/uploads/2011/11/Git-Logo-2Color-910x198.png)

Los submódulos en git permiten insertar uno o más repositorios externos dentro de otro repositorio. Es decir, permiten manejar uno o varios subproyectos dentro de un gran proyecto versionado con git. Esta característica puede ser útil, por ejemplo, para referenciar archivos que estén en proyectos complementarios, pero administrados por diferentes grupos o personas.

Para resumir, [los submódulos en git permiten dividir o combinar un proyecto en varios repositorios separados](http://huntingbears.com.ve/trabajando-con-submodulos-en-git.html).

Entremos a la razón de ser de este post:

Que pasa cuando estamos agregando un submodulo y obtenemos:

```
'NombreCarpeta' already exists in the index
```

Eso nos indica que ```NombreCarpeta``` ya se encuentra en nuestro directorio de trabajo.

## Como podemos solucionar:

Podemos hacer lo siguiente:

```
git ls-files --stage NombreCarpeta
```
Y vamos a tener una salida más o menos a esta:

```
160000 d023657a21c1bf05d0eeaac6218eb5cca8520d16 0	NombreCarpeta
```

Entonces, para eliminar la carpeta del index hacemos:

```
git rm -r --cached NombreCarpeta
```

Y ya con esto podemos agregar nuevamente el submodulo sin problemas :D

Espero les sea de ayuda :D  

