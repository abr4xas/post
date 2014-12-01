Title: #lcf: script para cambiar los nombres de archivos.
Date: 2011-09-26 16:41
Author:  
Slug: lcf-script-para-cambiar-los-nombres-de-archivos

Bueno, hace unos dias un amigo me pregunto si habia una forma de cambiar
los nombres de archivos a minusculas ya que se mudaron a un servidor
Gnu/Linux y tenian ese inconveniente...

Haciendo la respectiva busqueda me tope con:

[Linux for Newbies, Part 16: Shell Scripting](http://northernjourney.com/opensource/newbies/newb016.html "http://northernjourney.com/opensource/newbies/newb016.html")
======================================================================================================================================================================

y dejan el siguiente script:  

``  #!/bin/sh # lowercase any filenames with uppercase chars for file in $* do if [ -f $file ] then lcfile=`echo $file | tr [:upper:] [:lower:]` if [ $file != $lcfile ] then mv -i $file $lcfile fi fi done ``  
Para hacerlo funcional solo debemos escribir: "chmod a + x lcf" y
listo.

 
