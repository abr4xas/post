Title: Hablando de XEN y otras yerbas...
Date: 2012-05-24 08:13
Author:  
Slug: xen-y-otras-yerbas

**Xen** es un [monitor de máquina
virtual](http://es.wikipedia.org/wiki/Monitor_de_m%C3%A1quina_virtual "Monitor de máquina virtual") de [código
abierto](http://es.wikipedia.org/wiki/C%C3%B3digo_abierto "Código abierto") desarrollado
por la [Universidad de
Cambridge](http://es.wikipedia.org/wiki/Universidad_de_Cambridge "Universidad de Cambridge").

La meta del diseño es poder ejecutar instancias de [sistemas
operativos](http://es.wikipedia.org/wiki/Sistema_Operativo "Sistema Operativo") con
todas sus características, de forma completamente funcional en un equipo
sencillo. Xen proporciona aislamiento seguro, control de recursos,
garantías de calidad de servicio y migración de máquinas virtuales en
caliente. Los sistemas operativos pueden ser modificados explícitamente
para correr Xen (aunque manteniendo la compatibilidad con aplicaciones
de usuario). Esto permite a Xen alcanzar virtualización de alto
rendimiento sin un soporte especial de hardware. Intel ha realizado
diversas contribuciones a Xen que han permitido añadir soporte para sus
extensiones de arquitectura VT-X Vanderpool. Esta tecnología permite que
sistemas operativos sin modificar actúen como hosts dentro de las
máquinas virtuales de Xen, siempre y cuando el servidor físico soporte
las extensiones VT
de [Intel](http://es.wikipedia.org/wiki/Intel "Intel") o Pacifica
de [AMD](http://es.wikipedia.org/wiki/AMD "AMD"). [0]

[0] [http://es.wikipedia.org/wiki/Xen](http://es.wikipedia.org/wiki/Xen)

<!--more-->

\# Instalando xen  
`aptitude install xen-linux-system`

\# En consola:  

`root@dx2400:/# aptitude install xen-linux-system-amd64 Se instalarán los siguiente paquetes NUEVOS: bridge-utils{a} gawk{a} libxenstore3.0{a} linux-image-3.2.0-0.bpo.2-amd64{ab} python2.5{a} python2.5-minimal{a} xen-hypervisor-4.0-amd64{a} xen-linux-system-3.2.0-0.bpo.2-amd64{a} xen-linux-system-amd64 xen-utils-4.0{a} xen-utils-common{a} xenstore-utils{a} 0 paquetes actualizados, 12 nuevos instalados, 0 para eliminar y 0 sin actualizar. Necesito descargar 30,6 MB de ficheros. Después de desempaquetar se usarán 140 MB. No se satisfacen las dependencias de los siguientes paquetes: linux-image-3.2.0-0.bpo.2-amd64: Depende: linux-base (>= 3~) pero está instalado 2.6.32-45. Rompe: initramfs-tools (< 0.99~) pero está instalado 0.98.8. Las acciones siguientes resolverán estas dependencias`  

` Mantener los paquetes siguientes en la versión actual: 1) linux-image-3.2.0-0.bpo.2-amd64 [Sin instalar] 2) xen-linux-system-3.2.0-0.bpo.2-amd64 [Sin instalar] 3) xen-linux-system-amd64 [Sin instalar]`  

` ¿Acepta esta solución? [Y/n/q/?]q Abandonando todos los esfuerzos por resolver estas dependencias Cancela.`  
Como ven, esa solución no seria la apropiada porque romperia
dependencias... Asi que decidi hacer lo siguiente:

\# Instalar xen-linux-system  

` root@dx2400:/home/abr4xas# aptitude install xen-linux-system "xen-linux-system" es un paquete virtual proporcionado por: xen-linux-system-amd64 xen-linux-system-2.6-xen-amd64 Debe elegir uno para instalar. No se instalará, actualizará o eliminará ningún paquete. 0 paquetes actualizados, 0 nuevos instalados, 0 para eliminar y 0 sin actualizar. Necesito descargar 0 B de ficheros. Después de desempaquetar se usarán 0 B.`

En este caso, yo seleccione xen-linux-system-amd64

Entonces tenemos algo asi como:  

` root@dx2400:/home/abr4xas# aptitude install xen-linux-system-amd64 Se instalarán los siguiente paquetes NUEVOS: bridge-utils{a} gawk{a} libxenstore3.0{a} linux-image-3.2.0-0.bpo.2-amd64{a} python2.5{a} python2.5-minimal{a} xen-hypervisor-4.0-amd64{a} xen-linux-system-3.2.0-0.bpo.2-amd64{a} xen-linux-system-amd64 xen-utils-4.0{a} xen-utils-common{a} xenstore-utils{a} 0 paquetes actualizados, 12 nuevos instalados, 0 para eliminar y 0 sin actualizar. Necesito descargar 30,6 MB de ficheros. Después de desempaquetar se usarán 140 MB. ¿Quiere continuar? [Y/n/?]`  
\# Instalar virt-manager  
` aptitude install virt-manager`  
luego, debemos seguir lo que dice @Phenobarbital en este enlace:  

[http://phenobarbital.wordpress.com/2012/05/04/xen-4-y-debian-corrigiendo-algunos-detalles](http://phenobarbital.wordpress.com/2012/05/04/xen-4-y-debian-corrigiendo-algunos-detalles "http://phenobarbital.wordpress.com/2012/05/04/xen-4-y-debian-corrigiendo-algunos-detalles")

 

Gracias a @Phenobarbital por sus consejos a la hora de la instalación y
configuración!! :D
