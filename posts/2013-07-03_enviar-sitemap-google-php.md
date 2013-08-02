# Nano – Error reading ~/.nano_history: Permission denied

Ciertamente me gusta nano como editor de texto, hoy... De pronto:



<pre class="prettyprint">
	Error reading ~/.nano_history: Permission denied
    Press Enter to continue starting nano.
</pre>

Entonces, toco usar google y encontrar la soluci&oacute;n que es la siguiente:

Hay que editar el archivo /etc/nanorc, es decir


<pre class="prettyprint">
		sudo nano /etc/nanorc
</pre>

Luego buscar la siguiente linea set historylog y comentarla, debe quedar de la siguiente forma:

<pre class="prettyprint">
		#set historylog
</pre>

Cerramos nuestro editor y en la misma consola:

<pre class="prettyprint">
		sudo rm ~/.nano_history
</pre>


[Fuente de la informaci&oacute;n](http://pricklytech.wordpress.com/2010/12/12/ubuntu-nano-error-reading-home-nano_history-permission-denied/ "Fuente de la informaci&oacute;n")