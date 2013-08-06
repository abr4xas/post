# Minando usando CPU con cgminer

Debemos tener claro que es [bitcoin](http://bitcoin.org/es/ "Una moneda digital P2P de c&oacute;digo abierto"). 

Descargamos las fuentes de cgminer

Iniciamos creando el directorio de trabajo para esta instalación, ingresamos y ahí descargamos el archivo conteniendo el código fuente del cgminer:

(En consola como root o su)

Instalamos 

 <pre class="prettyprint">
~# aptitude install libcurl4-gnutls-dev
 </pre>

 Y luego: 

 <pre class="prettyprint">
~# mkdir cgminer
~# cd cgminer/
~# wget http://ck.kolivas.org/apps/cgminer/2.10/cgminer-2.10.4.tar.bz2
</pre>

 <pre class="prettyprint">
~# tar -xvjf cgminer-2.10.4.tar.bz2
~# cd cd cgminer-2.10.4/
~# ./configure --enable-cpumining
</pre>

Para conectarnos simplemente debemos:
 <pre class="prettyprint">
~# cgminer --algo auto -o http://pool.bitclockers.com:8332 -u Gram01Test -p test123
</pre>

Yo uso [mining.bitcoin.cz](http://mining.bitcoin.cz "mining.bitcoin.cz"). 

[Fuente de la informaci&oacute;n](http://www.guatewireless.org/tecnologia/bitcoins/como-instalar-cgminer-en-linux-debian-ubuntu-mint.html "Fuente de la informaci&oacute;n").