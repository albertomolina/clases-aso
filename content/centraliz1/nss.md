title: Name Service Switch
slug: centraliz1/nss
date: 2020-03-19

Name Service Switch (nss) es el mecanismo genérico para la resolución
de nombres en GNU/Linux, para la resolución de nombres de usuarios,
grupos, equipos, etc.

Un sistema GNU/Linux elemental trae instaladas varias bibiliotecas
para estas resoluciones de nombres, que podemos ver con la
instrucción:

```
ls /lib/libnss_*
```

En el fichero /etc/nsswitch.conf se definen los métodos que se emplean
para las diferentes resoluciones de nombres, su contenido inicial es:

```
passwd: compat
group: compat
shadow: compat
hosts: files mdns4_minimal [NOTFOUND=return] dns mdns4
networks: files
protocols: db files
services: db files
ethers: db files
rpc: db files
netgroup: nis
```

Aunque en este tema las únicas líneas relevantes son las referentes a
passwd, group y shadow.

**Ejercicio**

1. Cambia arbitrariamente el contenido de las líneas passwd y group
    del fichero /etc/nsswitch.conf y comprueba con ls que el sistema
    no es capaz de resolver los UID y GID de los propietarios y grupos
    propietarios del sistema.
1. Vuelve a dejar el fichero como estaba
