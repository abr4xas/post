Title: Netflix en Linux
Date: 2014-05-29 10:20
Category: Linux
Tags: linux
Slug: netflix-linux
Author: abr4xas
Summary: Como activar de forma facil Silverlight para ver Netflix en linux
image: images/Netflix-App-Logo.jpg


Si, hay muchos tutoriales de como poder activar de forma facil Silverlight para ver Netflix en linux pero no todos funcionan de verdad...

Bueno, por lo menos no a mi... ;)

Desde hace un par de semanas tengo Netflix y pues, no hay como tal un cliente para Linux hay muchas formas de como poder usarlo una de ellas es instalando un tal: "Netflix-Desktop" que a mi, NO ME FUNCIONABA entonces me di a la tarea de buscar algo más facil y lo que encontre fue: 

     add-apt-repository ppa:pipelight/stable
     apt-get update && sudo apt-get install pipelight-multi

Luego hacemos:

     pipelight-plugin --enable silverlight

Obviamente, para activar el plugin

## Getting Netflix to Work

Luego de todo eso, seguimos teniendo problemas asi como lo muestra la imagen

![Alt Text](http://main.makeuseoflimited.netdna-cdn.com/wp-content/uploads/2014/02/pipelight_netflix_error.jpg)

debemos hacer otro pequeño cambio y es usar: "(link: https://addons.mozilla.org/en-US/firefox/addon/user-agent-switcher/ text: User Agent Switcher popup: yes) para Firefox" y "(link: https://chrome.google.com/webstore/detail/user-agent-switcher-for-c/djflhoibgkdhkhhcedjiklpkjnoahfmg text: User Agent Switcher popup: yes) para Chrome"

En las configuraciones del plugin debemos tener lo siguiente:

![Alt Text]({filename}/images/config_netflix_ua.png)

     Mozilla/5.0 (Windows NT 6.1; WOW64; rv:15.0) Gecko/20120427 Firefox/15.0a1

Y es todo, ya estamos disfrutando de Netflix!!

![Alt Text](http://main.makeuseoflimited.netdna-cdn.com/wp-content/uploads/2014/02/pipelight_netflix_running.jpg)

(link: http://www.makeuseof.com/tag/easily-enable-silverlight-watch-netflix-linux/ text: Fuente de la información popup: yes)