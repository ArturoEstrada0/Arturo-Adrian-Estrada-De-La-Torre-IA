# Reporte CNN Arturo Adrián Estrada De La Torre



Este proyecto de CNN nos sirve para categorizar o identificar eventos como incendios, tornados, inundaciones, asaltos y robos a casas. Las CNN son un tipo de inteligencia artificial que se usa principalmente para trabajar con imágenes.

## 2. Herramientas Necesarias

Primero, necesitamos algunas herramientas (librerías de Python) para trabajar:
- `numpy`: para manejar números y datos.
- `os` y `re`: para trabajar con archivos y buscar cosas en textos.
- `matplotlib.pyplot`: para hacer gráficos y visualizar datos.
- `sklearn`: para dividir datos y medir el rendimiento.
- `keras` y `tensorflow`: para crear y entrenar las redes neuronales.

## 3. Preparar los Datos

Se cargan imágenes y se dividen en dos grupos: entrenamiento y prueba. Esto es para que el modelo pueda aprender de un grupo y ser probado en otro para ver qué tan bien funciona.

## 4. Construir el Modelo

Aquí es donde se crea la red neuronal. Algunas de las partes importantes son:
- **Conv2D**: capas que buscan características específicas en las imágenes.
- **MaxPooling2D**: capas que reducen el tamaño de las imágenes, conservando las características importantes.
- **Dropout**: capas que ayudan a evitar que el modelo aprenda demasiado de los datos de entrenamiento (esto se llama sobreajuste).
- **Dense**: capas que hacen la clasificación final.

Se ajusta el modelo con un optimizador y una función de pérdida para que aprenda a clasificar correctamente.

## 5. Entrenar el Modelo

Se entrena el modelo usando los datos de entrenamiento. Esto significa que el modelo ajusta sus parámetros para hacer predicciones más precisas. Se monitorea el rendimiento del modelo en un conjunto de validación para asegurarse de que no se sobreajuste.

## 6. Evaluar el Modelo

Después de entrenar, se prueba el modelo con el conjunto de prueba para ver qué tan bien funciona. Se usan métricas como precisión y recall para medir su rendimiento en la clasificación de incendios, tornados, inundaciones, asaltos y robos a casas.

## 7. Conclusión

Este proyecto o modelo nos sirvio para trabajar con clasificaciones de imagenes que se evaluaron en nuestro dataset. Pudimos ver sobre el ruido que pueden generar la data de cada categoria que hicimos, entendimos mejor los puntos de referencia que se toman del aprendizaje y como este puede influir en la toma de desicion en la clasificacion que hace el modelo CNN. En general el modelo funciona bien, es mas cosa de trabajar bien la información en el dataset de donde aprendera este modelo. Fue interesante y desafiante poder generar toda la información adecuada para poder hacer una predicción mas acertada y concluyente. 
