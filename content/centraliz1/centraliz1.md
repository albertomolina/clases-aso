title: Configurar un sistema centralizado de cuentas con kerberos, LDAP y NFS4
slug: centraliz1/centraliz1
date: 2020-03-19

Esta tarea consiste en configurar un completo sistema centralizado de
cuentas de usuario con kerberos, OpenLDAP y NFS4.

**Objetivos**

* Comprender el funcionamiento de kerberos
* Aprender mecanismos de autenticación de LDAP (SASL/GSSAPI)
* Configurar NFS con autenticación kerberos
* Configurar un sistema de cuentas centralizado seguro

**Pasos a realizar**

1. Sincroniza los relojes de los dos equipos.
1. Configura (o verifica que esté configurado) el servidor DNS en
   todos los equipos de la red virtual.
1. Instala y configura el servidor kerberos en el servidor. Añade
   todos los principales que estimes oportunos. 
1. Configura (o verifica que esté configurado) OpenLDAP en el servidor
   con objetos tipo posixAccount. 
1. Configura gssapi para la autenticación de LDAP con kerberos. 
1. Configura adecuadamente pam para realizar autenticación con
   kerberos y gestionar los datos de la cuenta con LDAP.
1. Crea las cuentas de usuario en el directorio /home/users del
   servidor y expórtalas utilizando NFS4.
1. Configura el cliente para que monte el directorio /home/users del
   servidor de forma automática.
1. Verifica el funcionamiento conjunto de todos los servicios, de
   manera que un usuario pueda autenticarse de forma centralizada y su
   cuenta se gestione con NFS4.
