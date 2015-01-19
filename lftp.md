Title: Conociendo un poco a #lftp
Date: 2015-01-19 02:35
Category: Linux
Tags: 
Slug: lftp
Author: abr4xas
twitter: abr4xas
Summary: El servidor apache tiene muchas funcionalidades y "*mods*" que se emplean en el servidor para sacarle un mayor provecho al mismo.
image: http://lftp.yar.ru/lftp1.png

> lftp es un programa de transferencia de archivos (FTP) por medio de la linea de comandos para UNIX y sistemas basados en UNIX. Fue escrito por Alexander Lukyanov y esta diponible bajo GPL.

Leer mas en [wiki/Lftp](http://en.wikipedia.org/wiki/Lftp).

## Uso basico

```bash
lftp ftp://ftp.my-domain.com
lftp ftp.my-domain.com:~> user myuser
Password:
```

### Comandos de ayuda

```bash
lftp myuser@ftp.my-domain.com:/www> help
        !<shell -command>                    (commands)
        alias [<name> [<value>]]            anon
        bookmark [SUBCMD]                   cache [SUBCMD]
        cat [-b] <files>                    cd <rdir>
        chmod [OPTS] mode file...           close [-a]
        [re]cls [opts] [path/][pattern]     debug [<level>|off] [-o <file>]
        du [options] <dirs>                 exit [<code>|bg]
        get [OPTS] <rfile> [-o <lfile>]     glob [OPTS] <cmd> <args>
        help [<cmd>]                        history -w file|-r file|-c|-l [cnt]
        jobs [-v]                           kill all|<job_no>
        lcd <ldir>                          lftp [OPTS] <site>
        ls [<args>]                         mget [OPTS] <files>
        mirror [OPTS] [remote [local]]      mkdir [-p] <dirs>
        module name [args]                  more <files>
        mput [OPTS] </files><files>                 mrm </files><files>
        mv <file1> <file2>                  [re]nlist [<args>]
        open [OPTS] <site>                  pget [OPTS] <rfile> [-o <lfile>]
        put [OPTS] </lfile><lfile> [-o <rfile>]     pwd [-p]
        queue [OPTS] [<cmd>]                quote </cmd><cmd>
        repeat [delay] [command]            rm [-r] [-f] <files>
        rmdir [-f] <dirs>                   scache [<session_no>]
        set [OPT] [<var> [<val>]]           site <site_cmd>
        source <file>                       user <user |URL> [<pass>]
        version                             wait [<jobno>]
        zcat <files>  
```

### Subir un archivo

```bash
lftp myuser@ftp.my-domain.com:/www> put file.ext
64714 bytes transferred in 8 seconds (7.9K/s)
```


### Un pequeño tip

Si en algun momento, intentan subir algo a un servidor puede que obtengas este error:

```bash
Lftp Fatal Error: Certificate Verification: Not Trusted
```

La solucion es facil, solo se debe agrear en ```/etc/lftp.conf``` lo siguiente:

```bash
set ssl:verify-certificate no
```
---

### Link de interes

- Official web site: 
[http://lftp.yar.ru/](http://lftp.yar.ru/)

- Wikipedia: [http://en.wikipedia.org/wiki/Lftp](http://en.wikipedia.org/wiki/Lftp)

### Mailing lists

Mailing lists and archives (since July 2011):

- [http://univ.uniyar.ac.ru/mailman/listinfo/lftp-devel](http://univ.uniyar.ac.ru/mailman/listinfo/lftp-devel)
- [http://univ.uniyar.ac.ru/mailman/listinfo/lftp](http://univ.uniyar.ac.ru/mailman/listinfo/lftp)

List archives (including prior to July 2011):

- [http://www.mail-archive.com/lftp@uniyar.ac.ru/](http://www.mail-archive.com/lftp@uniyar.ac.ru/)
- [http://www.mail-archive.com/lftp-devel@uniyar.ac.ru/](http://www.mail-archive.com/lftp-devel@uniyar.ac.ru/)

### Code

Browse the source code:

- [https://github.com/lavv17/lftp](https://github.com/lavv17/lftp)
- [http://fossies.org/dox/lftp-4.3.3/](http://fossies.org/dox/lftp-4.3.3/)

Bug trackers

- [http://linux.overshoot.tv/project/issues/lftp](http://linux.overshoot.tv/project/issues/lftp)
- [https://github.com/lavv17/lftp/issues](https://github.com/lavv17/lftp/issues)