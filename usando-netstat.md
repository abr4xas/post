Title: Usando #netstat
Date: 2012-04-26 10:53
Author:  
Slug: usando-netstat

Netstat (network statistics) es una herramienta de línea de comandos que
muestra un listado de las conexiones activas de una computadora, tanto
entrantes como salientes. Existen versiones de este comando en varios
sistemas como Unix, GNU/Linux, Mac OS X, Windows y BeOS.  
La información que resulta del uso del comando incluye el protocolo en
uso, las tablas de ruteo, las estadísticas de las interfaces y el estado
de la conexión. Existen, además de la versión para línea de comandos,
herramientas con interfaz gráfica (GUI) en casi todos los sistemas
operativos desarrollados por terceros. [1]

<!--more-->

[1] [http://es.wikipedia.org/wiki/Netstat](http://es.wikipedia.org/wiki/Netstat "http://es.wikipedia.org/wiki/Netstat")

`abr4xas@dx2400:~$ netstat --help usage: netstat [-vWeenNcCF] [<Af>] -r netstat {-V|--version|-h|--help} netstat [-vWnNcaeol] [<Socket> ...] netstat { [-vWeenNac] -i | [-cWnNe] -M | -s } -r, --route muestra la tabla de ruteado -i, --interfaces muestra la tabla de interfaz -g, --groups muestra la pertenencia a grupos multicast -s, --statistics muestra las estadísticas de la red (como SNMP) -M, --masquerade muestra las conexiones enmascaradas -v, --verbose descripción amplia -W, --wide don't truncate IP addresses -n, --numeric no se resolverán nombres --numeric-hosts no resuelve nombres de anfitrión --numeric-ports no resuelve por nombres de puerto --numeric-users no resuelve por nombres de usuario -N, --symbolic resuelve nombres hardware -e, --extend muestra otra/más información -p, --programs muestra el nombre PID/Programa para los zócalos -c, --continuous listado continuo -l, --listening muestra los zócalos a la escucha de servidores -a, --all, --listening muestra todos los zócalos (predeterminado: conectado) -o, --timers muestra temporizadores -F, --fib muestra la base de información hacia adelante (predeterminado) -C, --cache muestra la caché de ruteado en vez de la FIB`

Una forma comun de usar esta herramienta es:  
`abr4xas@dx2400:~$ netstat -a`  
Con eso podemos ver todas las conexiones activas... En mi caso salio
esto:

[![NetStat](http://abr4xas.org/wp-content/uploads/nasa-1024x608.jpg "NetStat")](http://abr4xas.org/wp-content/uploads/nasa.jpg)

Como ven, hay una IP que siempre se repite 192.203.230.10 le hice un
whois para ver a donde me conectaba y resulto esto:

[![netstat](http://abr4xas.org/wp-content/uploads/nasa_whois-1024x819.jpg "netstat")](http://abr4xas.org/wp-content/uploads/nasa_whois.jpg)

Como pueden ver, netstat es una herramienta muy importante
para así validar que escuchamos y que nos escucha...

También podemos usar:`abr4xas@dx2400:~$ netstat -a -n`  
Nos aparecerá un listado, que nos indicará el protocolo, dirección
remota (IP), puerto de escucha y estado.  
Esta orden tambien te sirve para saber si eres vulnerable. Si te
aparecen cualquiera de estos puertos abiertos :139, :137, :138,
"<span style="color: #ff0000;">**Preocupate**</span>".[2]

[2] [http://www.xombra.com/go\_articulo.php?nota=34](http://www.xombra.com/go_articulo.php?nota=34 "http://www.xombra.com/go_articulo.php?nota=34")

 
