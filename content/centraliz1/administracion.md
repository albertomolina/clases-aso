title: Administración del Sistema de Cuentas Centralizadas
slug: centraliz1/administracion
date: 2020-03-19

Una vez configurado el sistema de cuentas centralizadas, queda la
parte de la administración de usuarios, grupos y permisos.

A diferencia de la administración de un dominio Windows, que se
realiza principalmente con las consolas de administración de "usuarios
y grupos del directorio activo" y "políticas de grupo", en sistemas
UNIX debemos tocar los siguientes elementos:

* Políticas de contraseñas de Kerberos
* Listas de control de Acceso en LDAP
* Centralización de grupos en LDAP
* Permisos de ficheros UNIX
* Grupos UNIX

Teniendo esto en cuenta, realiza las siguientes restricciones en
nuestro sistema de cuentas centralizadas:

1. Crea un usuario que sea root en todas las máquinas del sistema de
   cuentas centralizadas.
1. Crea el grupo users, cuyos miembros podrán utilizar los
   dispositivos extraibles del equipo.
1. Configura el directorio skel para que todos los usuarios del grupo
   users tengan el mismo escritorio.
1. Configura el sistema de cuotas, para que los usuarios del grupo.
    users, tengan una cuota de 300MB en su cuenta. 
1. Crea una política de contraseñas por defecto para que las
contraseñas de todos los usuarios nuevos tengan por lo menos 8
caracteres.
1. Crea un usuario invitado que no pueda utilizar ningún medio
   extraible, pero sí pueda acceder a Internet.
