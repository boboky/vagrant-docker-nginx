vagrant-docker-nginx
==

Deploy nginx container using Docker Compose as Vagrant provisioner, with CentOS7.

Created on following environments.

- Ubuntu 16.04.3 LTS (xenial)
- Vagrant 2.0.0
- VirtualBox 5.1.28
- CentOS/7
- Ansible
- Docker 17.09.0-ce
- Docker Compose 1.11.2
- Alpine

## Requirements

Install the following on your management server or Local Machine

```
$ sudo apt-get install virtualbox -y
$ curl -O https://releases.hashicorp.com/vagrant/2.0.1/vagrant_2.0.1_x86_64.deb
$ sudo dpkg -i vagrant_2.0.1_x86_64.deb
$ vagrant plugin install vagrant-hostmanager
$ sudo apt-get install software-properties-common -y
$ sudo apt-add-repository ppa:ansible/ansible -y
$ sudo apt-get update -y
$ sudo apt-get install ansible -y
```

Plugins

- vagrant-vbguest
- vagrant-docker-compose
- vagrant-hostsupdater

Install plguins

```
$ vagrant plugin install vagrant-vbguest
$ vagrant plugin install vagrant-docker-compose
$ vagrant plugin install vagrant-hostsupdater
```

## Start Virtual Machine

```
$ cd /path/to/repos
$ vagrant up
```

Run Test of Infrastructure with Ansible
```
$ ansible-playbook main.yml 
```

For Debug Mode
```
$ ansible-playbook main.yml -vvv
```
Once provisioning done successfully, you can confirm a working nginx application via browsers by accessing to [`http://192.168.3.10/1.html`](http://http://192.168.3.10/1.html).

## Licence


## Author

[ola akinyemi](https://github.com/boboky)
