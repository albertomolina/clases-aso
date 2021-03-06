title: Compilación de un kérnel linux a medida
slug: kernel/compilacion-kernel.md
date: 10/12/2020

Al ser linux un kérnel libre, es posible descargar el código fuente,
configurarlo y comprimirlo. Además, esta tarea a priori compleja, es
más sencilla de lo que parece gracias a las herramientas disponibles.

En esta tarea debes tratar de compilar un kérnel completamente
funcional que reconozca todo el hardware básico de tu equipo y que sea
a la vez lo más pequeño posible, es decir que incluya un vmlinuz lo
más pequeño posible y que incorpore sólo los módulos
imprescindibles. Para ello utiliza el método explicado en clase y
entrega finalmente el fichero deb con el kérnel compilado por ti.

El hardware básico incluye como mínimo el teclado, la interfaz de red
y la consola gráfica (texto).

## Procedimiento a seguir

1. Instala el paquete linux-source correspondiente al núcleo que estés
   usando en tu máquina
1. Crea un directorio de trabajo (p.ej. mkdir ~/Linux)
1. Descomprime el código fuente del kérnel dentro del directorio de
   trabajo:
   
        tar xf /usr/src/linux-source-... ~/Linux/

1. Utiliza como punto de partida la configuración actual del núcleo:

        make oldconfig

1. Cuenta el número de componentes que se han configurado para incluir
   en vmlinuz o como módulos.

1. Configura el núcleo en función de los módulos que está utilizando
   tu equipo (para no incluir en la compilación muchos controladores
   de dispositivos que no utiliza el equipo):
   
        make localmodconfig

1. Vuelve a contar el número de componentes que se han configurado
   para incluir en vmlinuz o como módulos.

1. Realiza la primera compilación:

        make -j <número de hilos> bindeb-pkg

1. Instala el núcleo resultando de la compilación, reinicia el equipo
   y comprueba que funciona adecuadamente.
   
1. Si ha funcionado adecuadamente, utilizamos la configuración del
   paso anterior como punto de partida y vamos a reducir el tamaño del
   mismo, para ello vamos a seleccionar elemento a elemento.
   
        cp /boot/config-... .config
		make clean
		make xconfig

1. Vuelve a contar el número de componentes que se han configurado
   para incluir en vmlinuz o como módulos.

1. Vuelve a compilar:

		make -j <número de hilos> bindeb-pkg

1. Si se produce un error en la compilación, vuelve al paso de
   configuración, si la compilación termina correctamente, instala el
   nuevo núcleo y comprueba el arranque.
   
1. Continuamos reiterando el proceso poco a poco hasta conseguir el
   núcleo lo más pequeño posible que pueda arrancar en nuestro
   equipo.
   
