title: Ejercicios de manejo de módulos
slug: kernel/ejercicios-modulos.md
date: 2020-10-19

1. Comprueba los módulos cargados en tu equipo.
1. Cuenta el número de módulos disponibles en el núcleo que estás
   usando.
1. Conecta un lápiz USB y observa la salida de la instrucción `sudo
   dmesg`.
1. Elimina el módulo correspondiente a algún dispotivo no esencial y
   comprueba qué ocurre. Vuelve a cargarlo.
1. Selecciona un módulo que esté en uso en tu equipo y configura el
   arranque para que no se cargue automáticamente.
1. Carga el módulo loop, obtén información de qué es y para qué
   sirve. Lista el contenido de `/sys/modules/loop/parameters` y
   configura el equipo para que se puedan cargar como máximo 12
   dispositvos loop la próxima vez que se arranque.
