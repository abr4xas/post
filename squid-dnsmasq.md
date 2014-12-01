Title: Configuración de Squid+DNSmasq
Date: 2012-01-30 07:29
Author:  
Slug: squid-dnsmasq

[@sinfallas](http://twitter.com/sinfallas "Sigue a sinfallas en twitter!!") paso
un rato configurando un Squid y DNSmasq y como a él no le gusta
documentar yo me encargue de eso y esto fue todo lo que se hizo en un
rato, esto también lo publique recientemente en
[VaSlibre](http://vaslibre.org.ve "VaSlibre") ..

![Squid+DNSMasq](http://i43.tinypic.com/qq3lhu.jpg)

<!--more-->

**Squid+DNSMasq=WIFI**

PROBLEM?

Para poder usar el Squid obviamente lo instalamos, en cualquier distro
basada en Debian:

***sudo apt-get install squid***

Ahora el DNSMasq:

***sudo apt-get install dnsmasq***

Ok bueno,

Imaginemos lo siguiente...

Tenemos la nube, que ira conectada a nuestra tarjeta wifi y la salida
(*bridge*) de esa conexión será por *eth0* hacia nuestro router y de ahi
tendremos wifi.

Ok, *eth0* tendra la IP (*en nuestro caso*) ***192.168.0.10/24*** el
router (***TP-Link***) tendrá la IP ***192.168.0.11/24*** a partir de
aquí los rangos de IP serán:

**192.168.1.100 ---\> 149**

192.168.1.150 ---\> gateway

***192.168.0.10 ---\> DNS 1***

8.8.8.8 ---\> DNS 2

8.8.4.4 ---\> DNS 3

*\*\*\* Que podemos usar OpenDNS (208.67.222.222) o los de COMODO
(8.26.56.26), para una "mayor seguridad".* Los rangos de IP pueden
cambiar según nuestras necesidades. \*\*\*

**PROXY (*Squid*)**

El proxy tendrá la IP ***192.168.0.10*** (***si, la de eth0***) con el
puerto ***3128*** (***default squid***) y por DNS:

**192.168.0.10**

8.8.8.8

8.8.4.4

Ver la configuración del squid.conf en este
[enlace](http://vaslibre.org.ve/publicaciones/squid.conf "Enlace de descarga para el squid.conf")
o editalo usando:

***sudo gedit /etc/squid/squid.conf***

Ahora, las reglas para la IPTables:

Esto en la consola, claro!! ;)

***iptables -t nat -A POSTROUTING -s 192.168.0.0/24 -o wlan0 -j
MASQUERADE***

echo 1 \> /proc/sys/net/ipv4/ip\_forward

iptable-save

Despúes, levantamos el squid:

***/etc/init.d/squid start***

A medida de que vayas navegando se notará el cambio de velocidad en las
páginas que más visitas, debido a que estaran "cacheadas" en dos
directorios del disco duro se puede cambiar la configuración del squid
para que use un pendrive de 2gb para acelerar el tiempo de respuesta del
proxy.

Luego les digo como cambiar eso ;)

Y chan, chan!! :D

Más información:

[http://www.squid-cache.org/](http://www.squid-cache.org/ "Sitio oficial de Squid")

[http://www.thekelleys.org.uk/](http://www.thekelleys.org.uk/ "Sitio oficial de DNSMasq")

[http://es.wikipedia.org/wiki/Netfilter/iptables](http://es.wikipedia.org/wiki/Netfilter/iptables "Que es IPTables")

***\*\* Nota:***

Si eres nuevo en esto quizás existan algunas cosas (por no decir todo
xD) que no entiendas pero en este caso te explicaré algo que es más
notorio que otra cosa:

**192.168.0.10/24** \<-- Seguro quedaste con cara de ***o\_O***

Bueno, esto quiere decir que la mascara de red será de la siguiente
forma:

**255.255.255.0**

Es decir, la IP del router tendrá la misma mascara de red de eth0.

**Cualquier otra duda, google con eso *xD***

Gracias a
@[Sinfallas](http://twitter.com/sinfallas "Sigue a Sinfallas en twitter")
por ayudarnos a configurar todo esto y a
@[xombra](http://twitter.com/xombra "Sigue a xombra en twitter") por
ponerlo puyuo!! Y obvio, me tienes que seguir a mi!! ¬¬"
@[abr4xas](http://twitter.com/abr4xas "Sigue a abr4xas en twitter")

Ahora bien, si sacan cuentas tendremos:

*1 modem CANTV*

1 tarjeta de red.

1 tarjeta wifi

1 router

4 mascaras que haran entretenida la noche a cualquiera que quiera entrar
sin permiso a su red!!
