# McboTechMeetUp
Ansible, Vagrant, Docker examples McboTechMeetUp

Este proyecto es el codigo ejemplo mostrado en el McboTechMeetUp el 16/04/2016.


# Ansible y Vagrant

* Para ejecutar el [Vagrant](vagrantup.com) provisionado por [Ansible](ansible.com) primero se necesita instalar algunos [Roles de ansible](http://docs.ansible.com/ansible/playbooks_roles.html). Usando `ansible-galaxy install -r requeriments.txt` instalara los roles correspondientes.

* Para instalar Vagrant primero necesitaras instalar [VirtualBox](https://www.virtualbox.org/)

* Si luego de correr `vagrant up` presenta unas fallas bajando el [box](https://www.vagrantup.com/docs/boxes.html) `vagrant box add ubuntu/trusty64 https://atlas.hashicorp.com/ubuntu/boxes/trusty64/versions/20160323.0.0/providers/virtualbox.box`

* Automaticamente luego de correr `vagrant up` ansible se ejecuta, de todas maneras si se requiere correrlo de nuevo se puede ejecutar `vagrant provision`


# Ansible

Este playbook ejecuta las siguientes tareas:

  * Instala todo lo correspondiente a Node para correr el app


# Docker
Este docker genera un contenedor para correr Node dentro de el. Para generarlo se puede correr `docker build -t any_app_name .`

Luego para correr el contenedor `docker run -d --name any_container_name -p any_container_port:8080 any_app_name`
