title: Ejercicios de clientes LDAP
slug: ldap/ejercicios-clientes.md
date: 2020-12-1

1. Configura tu equipo para que las aplicaciones de línea de comandos
   usen adecuadamente el certificado raíz `gonzalonazareno.crt`.
1. Configura `ldap-utils` (fichero `/etc/ldap/ldap.conf`) para que se
   utilice el servidor ldaps://ldap.gonzalonazareno.org y realiza una
   búsqueda para encontrar el objeto en el que estás definido tú a
   través de tu nombre de usuario:
   
```
ldapsearch -x uid=<nombre de usuario>
```
   
1. Instala `Apache Directory Studio` en tu equipo y configúralo para
   que pueda usar la conexión a `ldaps://ldap.gonzalonazareno.org`.
1. Modifica la entrada correspondiente a tu usuario de LDAP con ADS y
   añade una imagen en formato JPEG de 20 KiB como máximo.
