# Reporte Detección de Wally Arturo Adrián Estrada De La Torre

Este proyecto se utiliza para encontrar a Wally en imágenes. Para lograrlo, alimentamos un dataset con imágenes usando Cascade Trainer GUI, que nos generó archivos XML para el modelo de aprendizaje. Las imágenes se organizaron en dos carpetas: `n` para las imágenes donde no estaba Wally y `p` para las imágenes donde sí estaba Wally.

## 1. Herramientas Necesarias

Primero, necesitamos algunas herramientas (librerías de Python) para trabajar:
- `cv2`: Para trabajar con imágenes y videos.
- `numpy`: Para manejar números y datos.

## 2. Preparar los Datos

Se cargan las imágenes y se organizan en dos carpetas:
- `n`: Imágenes donde Wally no está presente.
- `p`: Imágenes donde Wally sí está presente.

El modelo se entrena con estas imágenes usando Cascade Trainer GUI, que genera archivos XML necesarios para la detección.

## 3. Probar el Modelo

Para poner a prueba el modelo:
- Se carga una imagen de prueba.
- Se convierte la imagen a escala de grises.
- Se carga el archivo XML generado por el entrenamiento (`cascade.xml`).
- Se aplican los parámetros necesarios para detectar a Wally en la imagen (como `scaleFactor`, `minNeighbors` y `minSize`).

## 4. Detectar a Wally

Para detectar a Wally en una imagen:
- Se procesan las imágenes con el modelo entrenado.
- Si Wally es detectado, se dibujan rectángulos alrededor de su ubicación y se añade el texto "Wally".

## 5. Mostrar el Resultado

Finalmente, se muestra la imagen con las detecciones resaltadas, permitiendo ver claramente dónde está Wally en la imagen.

## 6. Conclusión

Este proyecto nos permite encontrar a Wally en imágenes usando un modelo entrenado con Cascade Trainer GUI. Fue complicado preparar el dataset y ajustar los parámetros del modelo para lograr detecciones precisas. Principalmente se tuvo que jugar mucho con FactorScale, minSize y MinNeighbors para poder adaptarlo a cada prueba de Wally no pudimos generalizar los resultados para que en todas las pruebas fuera exitoso con la misma configuración