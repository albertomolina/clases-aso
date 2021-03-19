title: Pluggable Authentication Module (PAM)
slug: centraliz1/pam
date: 2020-03-19

Al igual que nss es el mecanismo encargado de la resolución de nombres
en los sistemas GNU/Linux, PAM es el mecanismo encargado de la
autenticación en el sistema.

La autenticación en un sistema puede ser muy variada y depender de
diferentes dispositivos, aunque en este tema sólo nos centraremos en
la autenticación de usuarios a través del par usuario/contraseña

Cada mecanismo de autenticación del sistema (login, ssh, su, etc.)
puede tener un fichero específico en el que se definan las reglas o
definirse reglas de forma general en los ficheros /etc/pam.d/common-*

La sintaxis simple de cada regla de un fichero de pam es:
tipo control ruta-a-modulo argumentos

Por ejemplo:
```
auth required pam_unix.so
```
Los tipos disponibles son:

* account: Se utiliza para restringir o permitir acceso a un servicio
  dependiendo de algún cirterio: hora del día, recursos del sistema
  disponibles, tipo de usuario, etc.
* auth: Proporciona dos aspectos diferentes de autenticación:
    * Verifica si el usuario es quien dice ser (verificando la contraseña por ejemplo).
    * Puede garantizar la pertenecia a un grupo u otros privilegios
* password: Se utiliza para actualizar el "token" asociado con el usuario
* session: Se utiliza para cosas necesarias antes o después de que el
  usuario utilice un servicio: verificaciones, montaje de directorio,
  etc.

**Ejercicio**

1. Crea un nuevo usuario en el sistema de forma manual siguiendo los siguientes pasos:
    1. Edita el fichero /etc/passwd, /etc/group y /etc/shadow y añade
    las líneas necesarias para que exista el nuevo usuario
	1. Utiliza el módulo pam_mkhomedir para que se cree de forma
       automática el home del usuario la primera vez que ingrese en el
       sistema.
