Title: Minando usando CPU con cgminer
Date: 2013-08-06 10:20
Category: Bitcoin
Tags: bitcoin, mineria, linux
Slug: cgminer-bitcoin
Author: abr4xas
Summary: Debemos tener claro que es [bitcoin](http://bitcoin.org/es/ "Una moneda digital P2P de c&oacute;digo abierto"). Bitcoin es una moneda digital, un protocolo y un software que permite...
image:https://ip.bitcointalk.org/?u=http%3A%2F%2F1.bp.blogspot.com%2F-yjNJCUvRTR8%2FUVEijuSP7XI%2FAAAAAAAAAUw%2Fr43k5i4117M%2Fs1600%2Fminer.png&t=541&c=rqFLUfdwujto3g

Debemos tener claro que es [bitcoin](http://bitcoin.org/es/ "Una moneda digital P2P de c&oacute;digo abierto"). Bitcoin es una moneda digital, un protocolo y un software que permite...

 * Transacciones instantáneas punto a punto
 * Pagos en todo el mundo
 * Bajos o cero costos de procesamiento
 * Y mucho más

Bitcoin utiliza tecnología punto a punto para operar sin una autoridad central; gestionando las transacciones y la emisión de Bitcoins que se llevan a cabo conjuntamente por la red. A través de muchas de sus propiedades únicas, Bitcoin permite usos interesantes que no pueden ser cubiertos por otros sistemas de pago.

El software es un proyecto libre de código abierto, impulsado por la comunidad y liberado bajo la licencia MIT.

Descargamos las fuentes de cgminer

Iniciamos creando el directorio de trabajo para esta instalación, ingresamos y ahí descargamos el archivo conteniendo el código fuente del cgminer:

(En consola como root o su)

Instalamos 

{% highlight bash linenos %}
~# aptitude install libcurl4-gnutls-dev
{% endhighlight %}

 Y luego: 

{% highlight bash linenos %}
~# mkdir cgminer
~# cd cgminer/
~# wget http://ck.kolivas.org/apps/cgminer/2.10/cgminer-2.10.4.tar.bz2
{% endhighlight %}

{% highlight bash linenos %}
~# tar -xvjf cgminer-2.10.4.tar.bz2
~# cd cd cgminer-2.10.4/
~# ./configure --enable-cpumining
{% endhighlight %}

Para conectarnos simplemente debemos:

{% highlight bash linenos %}
~# cgminer --algo auto -o http://pool.bitclockers.com:8332 -u Gram01Test -p test123
{% endhighlight %}

Yo uso [mining.bitcoin.cz](http://mining.bitcoin.cz "mining.bitcoin.cz"). 

[Fuente de la informaci&oacute;n](http://www.guatewireless.org/tecnologia/bitcoins/como-instalar-cgminer-en-linux-debian-ubuntu-mint.html "Fuente de la informaci&oacute;n").