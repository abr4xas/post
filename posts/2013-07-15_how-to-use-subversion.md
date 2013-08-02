# Usando subversion 

Subversion es un sistema de control de versiones de código fuente libre / abierto (VCS). Es decir, Subversion maneja ficheros y directorios, y los cambios introducidos en ellos, con el tiempo. Esto le permite recuperar versiones antiguas de sus datos, o examinar la historia de cómo cambiaron sus datos. En este sentido, muchas personas piensan de un sistema de control de versiones como una especie de "máquina del tiempo".

Si quieres saber m&aacute;s de SVN lee este libro [Version Control with Subversion [DRAFT]](http://svnbook.red-bean.com/nightly/en/index.html "Version Control with Subversion [DRAFT]"), esta en ingles :D



En ese ejemplo usare el "How to Use Subversion" de wordpress ya que recientemente hice unos cambios a un par de plugins y habia olvidado como usar SVN xD

Bueno, debemos hacer lo siguiente:

 1. Check out a el repositorio en blanco.
 2. Añadir sus archivos al directorio trunk/ de su copia local del repositorio.
 3. Check in esos archivos en el repositorio central.

En otras palabras, hay que hacer esto:

<pre class="prettyprint">
# Creamos una carpeta para hacer la copia del repo

$ mkdir my-local-dir

# Check out a el repositorio en blanco.

$ svn co http://plugins.svn.wordpress.org/your-plugin-name my-local-dir
> A	my-local-dir/trunk
> A	my-local-dir/branches
> A	my-local-dir/tags

# Copiamos los archivos del plugin en el directorio trunk/ por ahora

$ cd my-local-dir/
my-local-dir/$ cp ~/my-plugin.php trunk/my-plugin.php
my-local-dir/$ cp ~/readme.txt trunk/readme.txt


# Agregamos esos archivos al repo central con

my-local-dir/$ svn add trunk/*

# Enviamos todos los cambios que realizamos con

my-local-dir/$ svn ci -m 'Adding first version of my plugin'
> Adding	trunk/my-plugin.php
> Adding	trunk/readme.txt
> Transmitting file data .
> Committed revision 11326.

# All done!
</pre>

En otra oportunidad, escribire como enviar cambios a un pluging que ya este en el servidor.



NOTA:

En el 2012 hice un par de plugins para #wordpress, uno de ellos con la finalidad de optimizar un poco la instalaci&oacute;n para no estar editando directamente el c&oacute;digo y el otro, solo por diversion xD
 

Estos son los plugins: 

 * [BOFH excuses](http://wordpress.org/plugins/bofh-excuses/ "BOFH excuses")
 * [Functions](http://wordpress.org/plugins/refu-regulatory-functions/ "Functions")

:D


