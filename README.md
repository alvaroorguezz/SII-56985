
Primer dia de Laboratorio de SII (08/10/2026):

-Nos hemos familiarizado con el entorno de github y la consola de linux.

-Hemos estado aprendiendo una serie de comandos que vamos a estar utilizando como ls gedit...

-De cara al proyecto de laboratorio hemos clonado el repositorio de la practica para poder editarlo individualmente.

Segunda practica de laboratorio de SII:

-Creación y gestión de ramas en Git: Desarrollo realizado aislando los cambios en la rama practica2 y posterior fusión (merge) a la rama principal.

-Programa Logger independiente: Creación del ejecutable logger que genera, abre, lee y destruye una tubería FIFO (fifo_tenis) para registrar los eventos del juego.

-Comunicación entre procesos (IPC): Modificación de la clase Mundo del juego base para enviar por la tubería los mensajes de texto con los puntos de cada jugador en tiempo real utilizando la llamada al sistema write.

-Actualización de compilación: Modificación del archivo CMakeLists.txt para incluir la compilación automática del nuevo programa logger.

-Condición de finalización: Se ha añadido lógica en el juego para que tanto el proceso del tenis como el del logger terminen automáticamente y de forma limpia cuando cualquier jugador alcance los 3 puntos.
