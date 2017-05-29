Title: Instalar impresoras en Linux
Date: 2017-05-29 22:10
Category:
Tags:
Slug: impresoras-hp-linux
Author: abr4xas
twitter: abr4xas
Summary: Cada versión de Linux es diferente, y configurar correctamente la impresora dependerá de si estamos usando Fedora, CentOS, Red Hat o cualquier otra distribución. En los casos más hardcore puede que tengamos que tirar únicamente de consola de comandos. 
image:
header_image: http://cdn.makeuseof.com/wp-content/uploads/2014/07/printing-linux-670x335.jpg

Cada versión de Linux es diferente, y configurar correctamente la impresora dependerá de si estamos usando Fedora, CentOS, Red Hat o cualquier otra distribución. En los casos más hardcore puede que tengamos que tirar únicamente de consola de comandos. 

En Linux la mayoría de las impresoras están disponibles desde el momento en que la conectas. Pero, ¿Que pasa si deseas hacer tareas más específicas como alinear los cartuchos o ver los niveles de tinta?. Tu solución es  HP Linux Imaging Printing.

### HPLIP to the rescue


HP Linux Imaging Printing es una aplicación Open Source por parte de HP, para dar soporte a las impresoras HP en las diferentes distribuciones Linux. Actualmente el Kernel de Linux ya contiene todos los controladores de HPLIP, es por ello que sólo basta con conectarla, esperar a que la reconozca y mandar a imprimir todo lo que deseas.

Ahora bien, si deseas realizar tareas como alinear los cartuchos, ver niveles de tinta, imprimir página de prueba o limpiar los cartuchos, lo único que tienes que hacer es instalar la interfaz gráfica para poder acceder a todas estas características.

Por Terminal instalas la interfaz gráfica con:

```
sudo aptitude install hplip-gui 
```

### Sobre el cartucho y toner de las impresoras


* Los <a href="https://www.astinta.es/3-toner-brother" target="_blank" rel="follow">toner brother</a> son compatibles con la gran mayoria de las impresoras equipos multifuncionales y fax HP.

* Los <a href="https://www.astinta.es/7-cartuchos-tinta-hp" target="_blank" rel="follow">cartuchos para hp</a> no tienen que ser originales ya que actualmente los precios son muy altos, existen una gran variedad de cartuchos que son compatibles que trabajan muy bien y la calidad es superior.


### HPLIP ToolBox

Esta herramienta no sirve solo para administrar impresoras HP, sino que también sirve para instalarlas.


![HPLIP ToolBox](http://3.bp.blogspot.com/-Xv4a4nLojfw/U-JytI8An6I/AAAAAAAACME/zUZUXcaPcBM/s1600/hp-actions.png)

Muchas de las cosas que se pueden hacer desde HPLip-Toolbox se pueden hacer también desde otras partes, sobre todo  configuración de las opciones de impresión:

- Desde la página correspondiente a la Dirección ip de la impresora
- A partir de la dirección http://localhost:631/printers en el navegador web
- Desde el programa que abre un archivo que vayamos a imprimir
- Desde Configuración del Sistema-Impresoras 
  
La comprobación del estado de los distintos cartuchos de tinta solo la puedo hacer desde:

- la herramienta HPLip-Toolbox->Pestaña Supplies
- el navegador web con la dirección ip correspondiente a la impresora.
- fuera del pc, desde el panel de la impresora.


Todas las opciones que nos presenta HPLIP ToolBox son importantes pero hay una en la que debemos prestarle atención de vez en cuando y es la pestaña Supplies:

### Pestaña Supplies:

Nos indica como están los distintos cartuchos de tinta. Herramienta muy útil para que no nos quedemos por sorpresa sin tinta de algún color, sobre todo del negro, y que nos permite comprar el cartucho de tinta que este apunto de acabarse antes de que eso suceda, y evitar así que en algún momento nos quedemos sin poder imprimir.
La comprobación del estado de los distintos cartuchos de tinta solo la puedo hacer desde la herramienta HPLip-Toolbox->Pestaña Supplies y desde la dirección ip correspondiente a la impresora, y no he visto que se pueda hacer desde ningún otro sitio del sistema operativo.También se puede comprobar desde fuera del pc, desde el panel de la impresora.


![HPLIP ToolBox](http://2.bp.blogspot.com/-YcoYKSDtCPQ/U_9HugiD9GI/AAAAAAAACRA/MXiszmhWuZk/s1600/hplip-supplies.png)