Title: Compilar ROM Firefox OS
Date: 2014-03-27 10:20
Category: Linux
Tags: firefox os
Slug: cocinar-rom-firefoxos-zte-open
Author: abr4xas
twitter: abr4xas
Summary: Preparando todo para compilar una ROM Firefox OS para el ZTE Open y otras cosas...
image: images/Firefox-OS.png

Luego de (link: actualizando-zte-open-de-firefox-os text: actualizar el ZTE Open popup: yes) me di la tarea de buscar información de como "cocinar" (*compilar/instalar*) una ROM para mi ZTE Open aquí les resumo un poco lo que encontré y lo que hice: 

# No encontré nada 

Si bueno, pase varios días y no encontré mucha información hasta que me tope con: (link: http://rowehl.com/blog/2013/10/24/firefoxos-1-dot-2-on-zte-open/ text: esto popup: yes) y (link: http://gnulinuxvagos.es/topic/2090-compilandoinstalando-la-%C3%BAltima-versi%C3%B3n-de-firefox-os-para-el-zte-open/#entry11912 text: esto popup: yes) y basándome en eso hice este (link: https://github.com/abr4xas/workbench text: script en bash popup: yes).

# Aja... Y ahora?

Bueno, si bien podemos seguir completamente este (link: http://gnulinuxvagos.es/topic/2090-compilandoinstalando-la-%C3%BAltima-versi%C3%B3n-de-firefox-os-para-el-zte-open/#entry11912 text: tutorial popup: yes) también podemos ejecutar el (link: https://github.com/abr4xas/workbench text: script en bash popup: yes) que nos adelanta un poco el trabajo.

# Efectos secundarios? 

Si, absolutamente... Si compilamos para la v1.3 luego de aplicar el ./flash.sh notamos:

 * La imagen del logo de Firefox OS no funciona es decir, no se le mueve la cola al zorro.
 * Luego de unos días de usar la ROM perdí la opción del vibra call (no se la razón de esto).

Y por lo que entiendo todo es al momento de compilar si no queremos tener las herramientas de desarrolladores aplicamos:

```bash
    BRANCH=v1.3 VARIANT=user ./config.sh inari
```    
Pero al hacerlo e instalar la ROM me instala todas las herramientas de desarrolladores.

Entonces, no se como modificar eso... Si sabes algo escríbeme al twitter @abr4xas :)