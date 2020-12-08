title: Configurar LDAP en alta disponibilidad
slug: ldap/tarea-ldap-ha
date: 2020-12-8

Vamos a instalar un servidor LDAP en sancho que va a actuar como
servidor secundario o de respaldo del servidor LDAP instalado en
frestón, para ello habrá que seleccionar un modo de funcionamiento y
configurar la sincronización entre ambos directorios, para que los
cambios que se realicen en uno de ellos se reflejen en el otro.

* Selecciona el método más adecuado para configurar un servidor LDAP
  secundario, viendo y/o probando las opciones posibles.
* Explica claramente las características, ventajas y limitaciones del
  método seleccionado
* Realiza las configuraciones adecuadas en el directorio cn=config
* Como prueba de funcionamiento, prepara un pequeño fichero ldif, que
  se insertará en el directorio en la corrección y se verificará que
  se ha sincronizado.

