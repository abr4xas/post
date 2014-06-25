Title: Xanadu Linux
Date: 2014-04-12 10:20
Category: Linux
Tags: OS,xanadu
Slug: xanadu-linux
Author: abr4xas
Summary: Es un derivado de Debian que utiliza SID como base y LXDE como entorno de escritorio, pensada para ser ligera y a la vez útil, contiene herramientas para rescate de sistemas, análisis forense y navegación anónima, además de todo lo necesario para su uso en el escritorio.
image: http://xanadulinux.files.wordpress.com/2014/05/500x5001.png

Es un derivado de Debian que utiliza SID como base y LXDE como entorno de escritorio, pensada para ser ligera y a la vez útil, contiene herramientas para rescate de sistemas, análisis forense y navegación anónima, además de todo lo necesario para su uso en el escritorio.

El nombre xanadu se ha considerado como sinónimo de opulencia y misterio, sobre todo gracias al poema Kubla Khan de Samuel Taylor Coleridge, también era la capital de verano del imperio Mongol de Kublai Jan y además fue el nombre seleccionado por Theodore Holm Nelson (Ted Nelson) para su idea de "concebir un documento global y único (docuverse), que cubra todo lo escrito en el mundo, mediante una gran cantidad de ordenadores interconectados, que contenga todo el conocimiento existente o, mejor dicho, información en forma de hipertexto."

Se construye usando Live-build, la imagen .ISO y sus configuraciones para crearla se encuentran disponibles bajo licencia GPL v2 (GNU GENERAL PUBLIC LICENSE, Version 2, June 1991) y pueden ser descargadas desde: (link: http://www.mediafire.com/download/8ply6722azd77ih/xanadu-0.4.4-i386.zip text: aquí popup: yes)

Para copiar el contenido de la imagen ISO a una memoria USB puede utilizar unetbootin o el comando bb de la siguiente forma: 

     dd if=nombre.iso of=/dev/sdx oflag=direct bs=1048576

# Características 
___

El usuario es:      user

La clave de user es:     xanadu

La clave de ROOT es:     enfilade

Requerimientos mínimos:

     * 384 Mb RAM (1 Gb RAM para tor)
     * CPU a 800 Mhz o superior (1.0 Ghz para tor)
     * Tarjeta de video a 800x600, 16 Mb vídeo RAM
     * BIOS con capacidad de arranque por USB o CDROM
     * 5 Gb de capacidad de disco para instalar

Desarrolladores:

     * Jesús Palencia
     * Héctor Mantellini

Colaboradores:

     * Alvaro Hernandez  
     * David Rondon


Dudas, consultas y/o sugerencias por favor enviarlas a: sinfallas@gmail.com

Contiene material realizado por:

* Configuraciones realizadas por Jesús Lara para arepalinux-script (https://github.com/phenobarbital/)

Paquetes incluidos:

* Kernel

3.13.1.686-pae

* Escritorio

LXDE

* Ofimatica

Libreoffice

* Gestor de Archivos

Thunar
PCManFM

* Accesorios

gCalculator

* Editor de Textos

Leafpad
Nano 

* Visor - Editor de Imágenes

Gimp
GPicView
Xsane

* Visor PDF

Evince

* Internet 

IceWeasel
Flashplugin-nonfree
FileZilla
Pidgin

* Herramientas del Sistema

Htop
Iotop
Orphaner

* Sonido y Vídeo

Brasero
Qjackctl
Vlc

* Gestor de Software

Synaptic 

* Antivirus

ClamAV 

* Seguridad y Testeo

Autopsy
Sleuthkit
Chkrootkit
Fail2ban
Nmap
Psad
Rkhunter
Shorewall
Wireshark

* Herramientas de Discos

Extundelete
Disk-manager
Dmraid
Magicrescue
GParted
Secure-delete
Foremost
Drbl

* Anonimato

Tor
I2p

* Compresores

Unrar
Unzip
P7zip-full
Xarchiver

* Otras

Btrfs-tools
Cmospwd
Fuse
Fish
Gvfs
Lvm2
Ntfs-3g
Xfsprogs
Tmux
Zsync

# Más info:
___

Pueden ir al repo del proyecto que es (link: https://github.com/sinfallas/xanadu-linux text: este popup: yes).