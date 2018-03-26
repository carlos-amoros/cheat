Instalación BIND en Debian 9
============================

[Manual de Howtoforge](https://www.howtoforge.com/tutorial/perfect-server-debian-9-stretch-apache-bind-dovecot-ispconfig-3-1/)

# Instalación Debian

* Instalar vmware tools
    * ```apt-get install open-vm-tools```
* Eliminar el cdrom de la lista de fuentes de paquetes. Editamos el fichero ```/etc/apt/sources.list```
* Instalar servidor ssh
    * ```apt-get install ssh openssh-server```
* Instalar editor de textos
    * ```apt-get install nano vim```
* Configurar el hostname
    * Editando el fichero /etc/hosts añadiendo: ```IP server.domain.es server```
    * Editando el fichero /etc/hostname y poniendo el nombre del servidor. 
    * Reiniciar el servidor
* Actualizar el sistema:
    * ```apt-get update```
    * ```apt-get upgrade```
* Sincronizar el reloj del sistema:
    * ```apt-get install ntp```
* Instalamos binutils
    * ```apt-get install binutils```

# Instalación BIND

http://man-es.debianchile.org/bind.html

* ```apt-get install bind9 dnsutils haveged```


apt-get --purge remove resolvconf

/etc/resolv.conf: nameserver 127.0.0.1

service bind9 restart

Prueba con dig www.debian.org

Deshabilitar reescritura resolv.conf
    editamos /etc/dhcp/dhclient.conf y comentamos (de request) domain-name, domain-name-servers y domain-search

Configuramos forwarders
    editamos /etc/bind/named.conf.options y descomentamos la parte de forwareders poniendo las ips correspondientes. Queda así:
        forwarders {
                8.8.8.8;
                8.8.4.4;
        };

Para añadir un registro:

Editamos el fichero /etc/bind/named.conf.local y añadimos al final:

zone "dominio.es" {
        type master;
        file "/etc/bind/db.dominio.es";
        allow-transfer { none; };
        allow-query { any; };
};


Y luego creamos el fichero /etc/bind/db.dominio.es y reiniciamos bind9

;
; archivo BIND para zona dominio.es
;
$TTL    604800
@       IN      SOA     dominio.es. hostmaster.dominio.es. (
                1       ; Serial
                           1200         ; Refresh
                            300         ; Retry
                        2419200         ; Expire
                           1200 )       ; Negative Cache TTL

dominio.es.    IN      NS      ns1.dominio.es.
dominio.es.    IN      NS      ns2.dominio.es.
dominio.es.    IN      MX      1 mx1.dominio.es.
dominio.es.    IN      MX      2 mx2.dominio.es.

localhost       IN      A       127.0.0.1
dominio.es.    IN      A       100.10.10.10

ns1             IN      A       100.10.10.10
ns2             IN      A       100.10.20.20

mx1             IN      A       100.10.10.10
mx2             IN      A       100.10.20.20

www             IN      A       100.10.10.10
smtp            IN      A       100.10.10.11
