# Reporte del Juego en Phaser 3 Balas Arturo Adrián Estrada De La Torre

Este proyecto es un juego desarrollado con Phaser, donde el objetivo principal es evitar las balas y obstáculos mientras el jugador se mueve en un escenario. Aquí se explica cómo se configuran los elementos del juego, se maneja la física y se integran técnicas de aprendizaje automático para mejorar la jugabilidad.

## 1. Herramientas Necesarias

Primero, necesitamos algunas herramientas (librerías y frameworks) para trabajar:
- `Phaser`: Para desarrollar el juego.
- `Synaptic`: Para integrar una red neuronal y manejar el aprendizaje automático.

## 2. Configuración Inicial

Se definen las dimensiones del juego y se crean las variables globales necesarias para manejar los elementos del juego como el jugador, el fondo, las balas, y la física del juego. También se establecen las velocidades mínimas y máximas para las balas y el jugador.

## 3. Cargar Recursos

En la función `preload()`, se cargan todos los recursos necesarios como imágenes para el fondo, el jugador, las naves, las balas y el menú. Estos recursos se encuentran en la carpeta `assets`.

## 4. Crear el Juego

En la función `create()`, se inicializan los elementos del juego:
- Se habilita la física y se establece la gravedad.
- Se añaden los sprites del fondo, el jugador, las naves y las balas.
- Se habilita la física para el jugador y las balas.
- Se añaden animaciones para el jugador.
- Se configuran los controles del juego como el movimiento del jugador y la pausa.

## 5. Red Neuronal

Se crea una red neuronal utilizando `Synaptic`, con 9 entradas, 18 neuronas en la capa oculta y 3 salidas. Esta red se entrena con los datos recogidos durante el juego para mejorar el comportamiento del jugador.

## 6. Modo Automático y Manual

El juego puede ser jugado en modo automático o manual:
- En modo manual, el jugador controla el movimiento utilizando las teclas del teclado.
- En modo automático, la red neuronal controla el movimiento del jugador basándose en los datos de entrenamiento.

## 7. Actualizar el Juego

En la función `update()`, se actualiza la posición del fondo y se manejan las colisiones entre las balas y el jugador. También se capturan los estados de las teclas para controlar el movimiento del jugador y se registran los datos de entrenamiento para la red neuronal.

## 8. Disparar Balas

Se definen varias funciones (`disparo()`, `disparo2()`, `disparo3()`) para manejar el disparo de balas desde diferentes posiciones y con diferentes velocidades. Las balas se mueven a lo largo del escenario y el jugador debe esquivarlas.

## 9. Colisiones

La función `colisionH()` maneja las colisiones entre las balas y el jugador. Si el jugador es golpeado por una bala, el juego se pausa y se muestra un menú.

## 10. Conclusión

Este proyecto es un juego interactivo donde el jugador debe esquivar balas utilizando controles manuales y luego dejando que una red neuronal controle el movimiento.
La red neuronal no solo debia aprender sobre el comportamiento de las balas para poder esquivarlas, se tuvo que tomar en cuenta el estilo de juego del jugador para que se viera reflejado, si el jugador se mueve demacido, el entranimiento replica ese estilo de juego e de igual manera si el jugador es mas tranquilo y casi no ejecuta movimientos, el entrenamiento aprende de ese comportamiento con respecto a las 3 balas.
