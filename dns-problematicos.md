Title: Y que paso con los DNS?
Date: 2014-08-26 11:00
Category: Blog
Tags: blog, web, dns
Slug: dns-problematicos
Author: abr4xas
twitter: abr4xas
Summary: Hace un par de semanas de forma "misteriosa" no podia ingresar al blog y varias personas me habian notificado este inconveniente y me puse a investigar que pasaba...
image: /images/1375758_1378127522423533_1335788860_n.jpg

Hace un par de semanas de forma "misteriosa" no podia ingresar al blog y varias personas me habian notificado este inconveniente y me puse a investigar que pasaba...

Lo que más me llamo la atencion a esto es que si hubieran bloqueado la ip del servidor donde estoy alojado TODOS los dominios no serian accesibles pero no era el caso, solamente mi dominio era el problema. TT__TT

### Ping

```
 $ ping abr4xas.org
ping: unknown host abr4xas.org
```

### dig

```
 $ dig abr4xas.org

; <<>> DiG 9.9.5-3-Ubuntu <<>> abr4xas.org
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: SERVFAIL, id: 46967
;; flags: qr rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 512
;; QUESTION SECTION:
;abr4xas.org.            IN    A 

;; Query time: 632 msec
;; SERVER: 8.8.8.8#53(8.8.8.8)
;; WHEN: Tue Aug 19 14:00:52 VET 2014
;; MSG SIZE  rcvd: 40
```


### El problema:

Despues de mucho leer, preguntar (gracias a todos los que me dieron una respuesta) llegue a:

Las DNS de Google

* 8.8.8.8
* 8.8.4.4

Como pueden ver al ejecutar: ``` $ host abr4xas.org 8.8.8.8 ``` esto es lo que obtengo:

```
$ host abr4xas.org 8.8.8.8
Using domain server:
Name: 8.8.8.8
Address: 8.8.8.8#53
Aliases: 

Host abr4xas.org not found: 2(SERVFAIL)
```


### Solución:

Instale TOR en mi pc, para verificar que pasaba con mi dominio y podia entrar sin ningun problema entonces, debido a eso tome la siguiente decision:

Cambiar las DNS por las de Open DNS:

* 208.67.222.222
* 208.67.220.220

Y problema resuelto :D ya las personas que tenian las DNS de google cambiaron y pueden entrar sin problemas.
