Title: How to fix $MFTMirr does not match $MFT (record 0)
Date: 2014-05-27 10:20
Category: Linux
Tags: linux
Slug: ntfs-3g-ntfsprogs
Author: abr4xas
Summary: How to fix $MFTMirr does not match $MFT (record 0)
image: http://1.bp.blogspot.com/-m5_fC220XYc/UpzRdbfs60I/AAAAAAAAIzc/6CqNWmq3fP0/s1600/tux-hdd-mount.jpg

Bueno, para resolver ese "pequeño" problema vamos a usar:

# NTFS-3G + Ntfsprogs

Lo que debemos hacer:

 * Bajarnos el paquete desde (link: http://tuxera.com/opensource/ntfs-3g_ntfsprogs-2014.2.15.tgz)
 
Luego debemos descomprimir el archivo usando: 

     tar -xvzf

Despues: 

     ./configure
     make
     make install # or 'sudo make install' if you aren't root

Ahora, nuevamente en consola escribimos: 

     fdisk -l

Vemos el dispositivo en cuestion (que en mi caso era /dev/sdf1 )y escribimos en la terminal:

     ntfsfix /dev/sdf1

NOTA: sdf1 es su dispositivo... 

Luego, vamos a  tener una salida parecida a esta:

     hp abr4xas # ntfsfix /dev/sdf1
     Mounting volume... $MFTMirr does not match $MFT (record 0).
     FAILED
     Attempting to correct errors... 
     Processing $MFT and $MFTMirr...
     Reading $MFT... OK
     Reading $MFTMirr... OK
     Comparing $MFTMirr to $MFT... FAILED
     Correcting differences in $MFTMirr record 0...OK
     Processing of $MFT and $MFTMirr completed successfully.
     Setting required flags on partition... OK
     Going to empty the journal ($LogFile)... OK
     Checking the alternate boot sector... OK
     NTFS volume version is 3.1.
     NTFS partition /dev/sdf1 was processed successfully.

Listo :D