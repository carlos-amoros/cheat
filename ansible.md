Ansible
=======

## Instalación ANSIBLE


http://docs.ansible.com/ansible/intro_installation.html#latest-release-via-yum

* Añadir EPEL. Para Centos:
	* ```yum install epel-release```
	* ```yum update```
	* ```yum install ansible```

* Tutoriales Ansible
	* https://www.youtube.com/watch?v=ut8aoPA5-G4
	* https://www.youtube.com/watch?v=41kc_ETJTNs
	* http://blog.deiser.com/primeros-pasos-con-ansible/

 ```/etc/ansible/hosts```: fichero de configuración de servidores a controlar.

* Se pueden ejecutar comandos ad hoc o playbooks

* ```ansible all -m ping```
* ```ansible all -a "cat /etc/hostname"```
* ```ansible db -s -m apt -a "name=ntp update_cache=yes"```
* ```(ansible grupo_hosts -s (sudo) -m modulo -a ...)```

Ejemplo: Reinicio servicio ntp
* ```ansible all -s -m service -a "name=ntp state=restarted"```
* ```ansible all -m setup``` : obtiene la configuración de todos los hosts

Ansible usa Jinja2 para hacer plantillas.

Para reutilizar playbooks se usan roles. En los playbooks se usan roles. 

ansible galaxy es un repositorio de roles. Hay un comando, ansible-galaxy que se descarga repositorios. 
Ansible gestiona casi cualquier cosa de AWS. 

Libros:
	- Ansible for DevOps
	- Ansible for AWS
	- Ansible Up & Running
	
Configuración
=============

En el servidor de ansible:
Generamos las claves:
ssh-keygen
Importamos la clave al servidor al que nos conectaremos:
ssh-copy-id -i ~/.ssh/id_rsa.pub root@host

Edito el fichero /etc/ansible/ansible.cfg y añado:
private_key_file = /root/.ssh/id_rsa

## Host de Ansible
/etc/ansible/hosts 

Se pueden agrupar grupos en otros grupos.

Probamos:
ansible all -m ping -u root
ansible grupo_hosts -a "free -m"


https://www.youtube.com/watch?v=41kc_ETJTNs