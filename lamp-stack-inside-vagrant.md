Title: LAMP stack para usar con Vagrant
Date: 2015-03-31 16:50
Category: virtualizacion
Tags: 
Slug: lamp-stack-inside-vagrant
Author: abr4xas
twitter: abr4xas
Summary: Preparando un ambiente LAMP para usar con Vagrant.
image: http://d2wwfe3odivqm9.cloudfront.net/wp-content/uploads/2015/02/vagrant_logo-200x200.png

![Vagrant Logo](/images/logo_vagrant.png)

Como ya es sabemos **Vagrant** es un sistema que funciona sobre Virtual Box, es un software que sirve para instalar máquinas virtuales con otros Sistemas Operativos en nuestro equipo.

Pre-requisitos:
Hay 2 herramientas que debes tener en tu maquina para que puedas usar esta gran herramienta:

* [Vagrant](http://www.vagrantup.com/downloads.html)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

Para más info clic [aquí](entorno-virtual-vagrant.html).

## Que es lo que hace el script?

* Instalación de apache 2.4, php 5.5, MySQL, PHPMyAdmin, Composer, nodejs, npm, bower, git, python-pip y lftp.
* Configura un password pre-definido para MySQL y PHPMyAdmin que es: ```root```.
* Activa ```mod_rewrite``` y agrega ```AllowOverride All``` a la configuración del vhost.

```bash
#!/bin/bash
echo "Provisioning virtual machine..."
echo "Please, wait..."
# Use single quotes instead of double quotes to make it work with special-character passwords
PASSWORD='root'
# update 
sudo apt-get update -y > /dev/null 2>&1
# install apache 2.5 and php 5.5
sudo apt-get install apache2 -y > /dev/null 2>&1
sudo apt-get install php5 libapache2-mod-php5 php5-mcrypt php5-cli -y > /dev/null 2>&1
# install mysql and give password to installer
sudo debconf-set-selections <<< "mysql-server mysql-server/root_password password $PASSWORD"
sudo debconf-set-selections <<< "mysql-server mysql-server/root_password_again password $PASSWORD"
sudo apt-get install mysql-server libapache2-mod-auth-mysql php5-mysql -y > /dev/null 2>&1
# install phpmyadmin and give password(s) to installer
# for simplicity I'm using the same password for mysql and phpmyadmin
sudo debconf-set-selections <<< "phpmyadmin phpmyadmin/dbconfig-install boolean true"
sudo debconf-set-selections <<< "phpmyadmin phpmyadmin/app-password-confirm password $PASSWORD"
sudo debconf-set-selections <<< "phpmyadmin phpmyadmin/mysql/admin-pass password $PASSWORD"
sudo debconf-set-selections <<< "phpmyadmin phpmyadmin/mysql/app-pass password $PASSWORD"
sudo debconf-set-selections <<< "phpmyadmin phpmyadmin/reconfigure-webserver multiselect apache2"
sudo apt-get install phpmyadmin -y > /dev/null 2>&1
# setup hosts file
VHOST=$(cat <<EOF
<VirtualHost *:80>
    DocumentRoot "/var/www/html/"
    <Directory "/var/www/html/">
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
EOF
)
echo "${VHOST}" > /etc/apache2/sites-available/000-default.conf
# enable mod_rewrite
sudo a2enmod rewrite
# enable php5-mcrypt
sudo php5enmod mcrypt
# restart apache
sudo service apache2 restart
# install Composer
curl -s https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer
sudo apt-get install git -y > /dev/null 2>&1
sudo apt-get install nodejs -y > /dev/null 2>&1
sudo apt-get install npm -y > /dev/null 2>&1
sudo apt-get install python-pip -y > /dev/null 2>&1
sudo apt-get install lftp -y > /dev/null 2>&1
# Install globally dependencies
sudo npm install -g bower > /dev/null 2>&1
echo "Finished provisioning."
```

Pueden revisar este [repo](https://github.com/abr4xas/vagrant-config) para más info.