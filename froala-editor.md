Title: Froala WYSIWYG Editor
Date: 2014-08-21 10:20
Category: Web
Tags: dev, web
Slug: froala-editor
Author: abr4xas
twitter: abr4xas
Summary: Froala WYSIWYG Editor se basa en las últimas tecnologías y de acuerdo a las últimas tendencias.
image: images/editorfroala.png

![Alt Text]({filename}/images/froalalogo.png)


Froala WYSIWYG Editor se basa en las últimas tecnologías y de acuerdo a las últimas tendencias.

Caracteristicas:

* Cross-browser
* Cross-platform
* Complete Functionality
* Autosave
* Retina Ready
* High Performance

## Integrando Froala 

Version actual: 1.1.7

## Requerimientos: 

* jQuery 1.10.2 o superiror.
* Font Awesome 4.1.0.

Con el fin de integrar froala es necesario incluir: 

* ```froala_editor.min.js```
* ```froala_editor.min.css``` 

Eso dentro de ```<head> </ head>```.

Un ejemplo practico de lo que debemos incluir:

```html
// Include Font Awesome
<link href="../css/font-awesome.min.css" rel="stylesheet" type="text/css">

// Include editor style file
<link href="../css/froala_editor.min.css" rel="stylesheet" type="text/css">

// Include jQuery library
<script src="http://code.jquery.com/jquery-1.10.2.js"></script>

// Include editor javascript file
<script src="../js/froala_editor.min.js"></script>
```

Y lo más importante:


```javascript
<script>
    $(function(){
        $('#edit').editable({inlineMode: false})
    });
</script>
```  

## Donde va el editor?

Pues, sencillo va dentro de:

```html
<section id="editor">

</section>
```

Veamos este ejemplo:

imaginando que tenemos un formulario para realizar una publicación y si ese form usa frolala el mismo quedaria de la siguiente forma:

```html
<section id="editor">
    <form action="" method="post" role="form">
        <div class="form-group">
            <input class="form-control" type="text" id="title" name="title" placeholder="Title..." value="Titulo">
        </div>
        <div class="form-group">
            <textarea class="form-control" rows="10" placeholder="Enter text ..." id="edit" name="content">

            </textarea>
        </div>
        <br>
        <button type="submit" class="btn btn-primary">Post</button>
    </form>
</section>
```



## Resultado final

![Alt Text]({filename}/images/ejemplofroala.png)


## Enlaces de interes:

* [http://editor.froala.com](http://editor.froala.com).
* [http://editor.froala.com/docs](http://editor.froala.com/docs).


Gracias a @echevemaster por recomendarme este editor :D 