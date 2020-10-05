title: Ejercicios de dpkg/APT
slug: debian/ejercicios
date: 2020-10-05

En primer lugar prepara una máquina virtual con Debian buster, puedes
hacerlo de la forma que prefieras o usando el fichero Vagrantfile que
se proporciona.

La versión de debian buster a fecha de hoy, es la versión 10.6. Sobre
una máquina de versión anterior realizar las siguientes acciones:

## Trabajo con apt, aptitude, dpkg

1. Que acciones consigo al realizar apt update y apt upgrade. Explica
   detalladamente.
     
2. Lista la relación de paquetes que pueden ser actualizados. ¿Qué
   información puedes sacar a tenor de lo mostrado en el listado?.
       
3. Indica la versión instalada, candidata así como la prioridad del
   paquete openssh-client.
   
4. ¿Cómo puedes sacar información de un paquete oficial instalado o
   que no este instalado?
	
5. Saca toda la información que puedas del paquete openssh-client que
   tienes actualmente instalado en tu máquina.
	
6. Saca toda la información que puedas del paquete openssh-client
   candidato a actualizar en tu máquina.
	 
7. Lista todo el contenido referente al paquete openssh-client actual
   de tu máquina. Utiliza para ello tanto dpkg como apt.
	
8. Listar el contenido de un paquete sin la necesidad de instalarlo o
   descargarlo.
       
9. Simula la instalación del paquete openssh-client.
       
10. ¿Qué comando te informa de los posible bugs que presente un
    determinado paquete?
       
11. Después de realizar un apt update && apt upgrade. Si quisieras
    actualizar únicamente los paquetes que tienen de cadena
    openssh. ¿Qué procedimiento seguirías?. Realiza esta acción, con
    las estructuras repetitivas que te ofrece bash, así como con el
    comando xargs.
       
12. ¿Cómo encontrarías qué paquetes dependen de un paquete
    específico.
       	
13. Como procederías para encontrar el paquete al que pertenece un
    determinado archivo.
	
14. ¿Que procedimientos emplearías para eliminar liberar la cache en
    cuanto a descargas de paquetería?
       	
## Trabajo con ficheros .deb

15. Descarga un paquete sin instalarlo, es decir, descarga el fichero
    .deb correspondiente. Indica diferentes formas de hacerlo.
       
16. ¿Cómo puedes ver el contenido, que no extraerlo, de lo que se
    instalará en el sistema de un paquete deb?
	
17. Sobre el fichero .deb descargado, utiliza el comando ar. ar
    permite extraer el contenido de una paquete deb. Indica el
    procedimiento para visualizar con ar el contenido del paquete
    deb. Con el paquete que has descargado y utilizando el comando ar,
    descomprime el paquete. ¿Qué información dispones después de la
    extracción?. Indica la finalidad de lo extraído.
       
18. Indica el procedimiento para descomprimir lo extraído por ar del
    punto anterior. ¿Qué información contiene?

## Trabajo con repositorios

19. Añade a tu fichero sources.list los repositorios de backports y
    sid.
       
20. ¿Cómo añades la posibilidad de descargar paquetería de la
    arquitectura i386 en tu sistema. ¿Que comando has empleado?. Lista
    arquitecturas no nativas. ¿Cómo procederías para desechar la
    posibilidad de descargar paquetería de la arquitectura i386?
	
21. Si quisieras descargar un paquete, ¿cómo puedes saber todas las
    versiones disponible de dicho paquete?
	
22. Indica el procedimiento para descargar un paquete del repositorio
    stable.
	
23. Indica el procedimiento para descargar un paquete del repositorio
    de backports.
	
24. Indica el procedimiento para descargar un paquete del repositorio
    de sid.
	
25. Indica el procedimiento para descargar un paquete de arquitectura
i386.

## Trabajo con directorios 

26. Que cometidos tienen:

  1. `/var/lib/apt/lists/`
  2. `/var/lib/dpkg/available`
  3. `/var/lib/dpkg/status`
  4. `/var/cache/apt/archives/`

