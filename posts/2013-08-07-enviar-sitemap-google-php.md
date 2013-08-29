---
layout: post
title: Nano – Error reading ~/.nano_history: Permission denied
tagline: "Cosas del d&iacute;a a d&iacute;a... "
tags : [nano, editor, linux]
---

Ciertamente me gusta nano como editor de texto, hoy... De pronto:



{% highlight bash linenos %}
	Error reading ~/.nano_history: Permission denied
    Press Enter to continue starting nano.
{% highlight bash %}

Entonces, toco usar google y encontrar la soluci&oacute;n que es la siguiente:

Hay que editar el archivo /etc/nanorc, es decir


{% highlight bash linenos %}
		sudo nano /etc/nanorc
{% highlight bash %}

Luego buscar la siguiente linea set historylog y comentarla, debe quedar de la siguiente forma:

{% highlight bash linenos %}
		#set historylog
{% highlight bash %}

Cerramos nuestro editor y en la misma consola:

{% highlight bash linenos %}
		sudo rm ~/.nano_history
{% highlight bash %}


[Fuente de la informaci&oacute;n](http://pricklytech.wordpress.com/2010/12/12/ubuntu-nano-error-reading-home-nano_history-permission-denied/ "Fuente de la informaci&oacute;n")