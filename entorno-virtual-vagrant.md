Title: Entendiendo un poco de #Vagrant
Date: 2015-02-25 21:10
Category: virtualizacion
Tags: 
Slug: entorno-virtual-vagrant
Author: abr4xas
twitter: abr4xas
Summary: Create and configure lightweight, reproducible, and portable development environments.
image: http://d2wwfe3odivqm9.cloudfront.net/wp-content/uploads/2015/02/vagrant_logo-200x200.png

![Vagrant Logo](/images/logo_vagrant.png)

**Vagrant** es un sistema que funciona sobre Virtual Box, es un software que sirve para instalar máquinas virtuales con otros Sistemas Operativos en nuestro equipo.

Pre-requisitos:
Hay 2 herramientas que debes tener en tu maquina para que puedas usar esta gran herramienta:

* [Vagrant](http://www.vagrantup.com/downloads.html)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

## Setup

Primero, necesitamos un archivo llamado "*Cheffile*" y otro archivo llamado "*Vagrantfile*" los podemos obtener en [Rove.io](http://rove.io/).

Despues de obtener esos archivos debemos colocarlos en una carpeta donde vamos a tener nuestro entorno de trabajo.

Para crear nuesto entorno con **vagrant** solo debemos escribir en la terminal:
```bash
$ curl -L http://rove.io/install | bash
```

## Conectandonos a nuestra VM
Antes de usar nuestra VM podemos instalar de forma adicional "*VirtualBox Guest Additions Plugin*" con el siguiente comando:

```bash
$ vagrant plugin install vagrant-vbguest
```
Luego de esto:

* Iniciamos nuestra maquina virtual con:
```bash
$ vagrant up
```
*Esto va a tomar cierto tiempo ya que tiene que descargar el SO y todas las herramientas previas configuradas :)*

* Para conectarnos a la maquina virtual usando SSH
```bash
$ vagrant ssh
```
* Para detener la maquina virtual
```bash
$ vagrant halt
```
* Suspenderla:
```bash
$ vagrant suspend
```
* Para reiniciar (si ya esta corriendo)
```bash
$ vagrant reload
```
* Para eliminar completamente
```bash
$ vagrant destroy
```

Yo tengo un repo en [github](https://github.com/abr4xas/vagrant-config) con las configuraciones que yo necesito para las cosas que hago.

En ese repo, hay una carpeta llamada ```development``` y ella sera el contenedor de todos mis trabajos.

## Configuracion del Vagrantfile

Esta es la configuracion que actualmente tiene mi **Vagrantfile**

```
# encoding: utf-8
# This file originally created at http://rove.io/b12db7f9a4eea1c71e136e4ab8960440

# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"
  config.ssh.forward_agent = true
  config.vm.network :forwarded_port, guest: 8000, host: 1234
  config.vm.boot_timeout = 300    
  config.vm.synced_folder "development/", "/home/vagrant/development"
  
  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = ["cookbooks"]
    chef.add_recipe :apt
    chef.add_recipe 'php'
    chef.add_recipe 'python'
    chef.add_recipe 'nodejs'
    chef.add_recipe 'vim'
    chef.add_recipe 'git'
    chef.json = {
      :git => {
        :prefix => "/usr/local"
      }
    }
  end
    
    # Install dependencies
    config.vm.provision :shell, :path => "dependencies.sh"
    
end
```

### Lecturas recomendadas

* [Vagrant Documentation](https://docs.vagrantup.com/v2/)