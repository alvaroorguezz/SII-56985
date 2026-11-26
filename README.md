
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


Tercera práctica de SII: Comunicación mediante archivos proyectados en memoria

Durante esta tercera práctica se han implementado las siguientes funcionalidades:

-Gestión de ramas en Git:** Desarrollo aislado en la rama `practica3` y posterior fusión (*merge*) con la rama `master`.

-Estructura compartida (`DatosMemCompartida.h`):** Definición de la clase que almacena el estado de la esfera, la raqueta 1 y la acción a ejecutar (`1` arriba, `0` nada, `-1` abajo).

-Programa Bot (`bot.cpp`):** Creación del proceso independiente `bot` que abre y proyecta el archivo en memoria compartida (`mmap`), leyendo periódicamente (cada 25 ms) las coordenadas de la pelota y la raqueta para decidir el movimiento.

-Integración en el juego (`Mundo.h` y `Mundo.cpp`):** Creación del archivo compartido (`open` y `ftruncate`), proyección en memoria y actualización en `OnTimer()` para enviar posiciones y ejecutar automáticamente la acción decidida por el bot.

-Compilación (`CMakeLists.txt`):** Inclusión del ejecutable `bot` en la configuración de CMake.
