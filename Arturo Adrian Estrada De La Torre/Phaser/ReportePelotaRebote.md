# Reporte del Juego en Phaser Arturo Adrián Estrada De La Torre

Este proyecto es un juego desarrollado con Phaser, donde el objetivo principal es evitar una pelota que se mueve por la pantalla. Aquí se explica cómo se configuran los elementos del juego, se maneja la física y se integran técnicas de aprendizaje automático para mejorar la jugabilidad.

## 1. Herramientas Necesarias

Primero, necesitamos algunas herramientas (librerías y frameworks) para trabajar:
- `Phaser`: Para desarrollar el juego.
- `Synaptic`: Para integrar una red neuronal y manejar el aprendizaje automático.

## 2. Configuración Inicial

Se definen las dimensiones del juego y se crean las variables globales necesarias para manejar los elementos del juego como el jugador, el fondo, la pelota y los sonidos de juego. También se establecen las vidas del jugador y el sistema de puntuación.

## 3. Cargar Recursos

En la función `preload()`, se cargan todos los recursos necesarios como imágenes para el fondo, el jugador, la pelota, el menú, y el sonido de game over. Estos recursos se encuentran en la carpeta `assets`.

## 4. Crear el Juego

En la función `create()`, se inicializan los elementos del juego:
- Se habilita la física y se establece la gravedad.
- Se añaden los sprites del fondo, el jugador y la pelota.
- Se habilita la física para el jugador y la pelota.
- Se añaden animaciones para el jugador.
- Se configura el sistema de puntuación y el conteo de vidas.

## 5. Red Neuronal

Se crea una red neuronal utilizando `Synaptic`, con 5 entradas, 10 neuronas en la capa oculta y 4 salidas. Esta red se entrena con los datos recogidos durante el juego para mejorar el comportamiento del jugador.

## 6. Modo Automático y Manual

El juego puede ser jugado en modo automático o manual:
- En modo manual, el jugador controla el movimiento utilizando las teclas del teclado.
- En modo automático, la red neuronal controla el movimiento del jugador basándose en los datos de entrenamiento.

## 7. Actualizar el Juego

En la función `update()`, se actualiza la posición del fondo y se manejan las colisiones entre la pelota y el jugador. También se capturan los estados de las teclas para controlar el movimiento del jugador y se registran los datos de entrenamiento para la red neuronal.

## 8. Movimiento de la Pelota

La función `setRandomBalaVelocity()` se encarga de establecer una velocidad aleatoria para la pelota, haciendo que su movimiento sea impredecible y desafiando al jugador a evitarla.

## 9. Colisiones

La función `colisionH()` maneja las colisiones entre la pelota y el jugador. Si el jugador es golpeado por la pelota, se reduce el número de vidas y, si las vidas llegan a cero, se muestra el mensaje de fin de juego y se ofrece la opción de entrar en modo automático.

## 10. Conclusión

Este proyecto es un juego interactivo donde el jugador debe esquivar una pelota utilizando controles manuales o dejando que una red neuronal controle el movimiento. En este juego me gusto mucho mas el resultado que en el juego de 3 balas, ya que las entras y salidas las pudimos adaptar mucho mejor y el entrenamiento fue mucho mas notorio y claro sobre el resultaod esperado.