---
layout: post
title: Debian nos pertenece
tagline: "Hablando sobre el proyecto Debian"
tags : [debian, linux]
---

[Debsources](http://anonscm.debian.org/gitweb/?p=qa/debsources.git "Debsources - all Debian source are belong to us") es una sencilla aplicación web que permite publicar una réplica de código fuente Debian desempaquetado en la Web.

Puede implementar Debsources donde quieras, pero no hay una instancia principal en [http://sources.debian.net](http://sources.debian.net) (*sources.dn para abreviar*) que es probable que encuentre interesante. sources.dn sigue de cerca el archivo de Debian de dos maneras:

 * se actualiza 4 veces al día para reflejar el contenido del archivo de Debian  
 * contiene las fuentes procedentes de suites oficiales de Debian: los habituales (de antigua estable al experimental), *-updates (ex volátil), *-proposed-updates y *-backports de Wheezy (on) 


Via sources.dn que por lo tanto, puede navegar por el contenido de los paquetes fuente de Debian con funciones de visualización de código habituales, como resaltado de sintaxis. Más interesante aún, usted puede buscar en el código fuente (de sólo inestable, sin embargo) a través de la integración con [http://codesearch.debian.net](http://codesearch.debian.net). También puede utilizar sources.dn programación para consultar versiones ni enlaces a líneas específicas disponibles, con la posibilidad de añadir mensajes emergentes contextuales (ejemplo).

De hecho, es posible que se han topado con sources.dn ya en los últimos días, a través de otros servicios de Debian populares en los que ya se ha integrado. En particular: codesearch.dn ahora por defecto para mostrar los resultados a través sources.dn y el PTS ha crecido de nuevo "código fuente Browse" hipervínculos que apuntan a la misma. Si tienes ideas de otros servicios de Debian, donde sources.dn debe integrarse, por favor hágamelo saber.

Me parece Debsources y sources.dn ya bastante útil, pero, como sucede a menudo, todavía hay un montón TODO. Obviamente, todo es Software Libre (publicada bajo licencia GNU AGPLv3). No dude en reportar nuevos bugs y, mejor, para enviar parches para los más destacados.


 * [Fuente de la informaci&oacute;n](http://bits.debian.org/2013/07/introducing_sources.debian.net.html "all Debian source are belong to us")
 * [Debsources provides access to the source code of the Debian operating system.](http://sources.debian.net/ "Debsources provides access to the source code of the Debian operating system.")