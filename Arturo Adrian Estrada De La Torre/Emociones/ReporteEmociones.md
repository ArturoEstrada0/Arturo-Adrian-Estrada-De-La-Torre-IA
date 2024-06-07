# Reporte Detector de Emociones Arturo Adrián Estrada De La Torre

Este proyecto de detección facial con un modelo entrenado nos sirve para identificar rostros y emociones en imágenes. Aquí se explica cómo se preparan los datos, se entrena el modelo y se utiliza para hacer predicciones en tiempo real. Las emociones que evaluamos en este proyecto fueron:

Feliz, Sorpresa y Tristeza.

## 1. Herramientas Necesarias

Primero, necesitamos algunas herramientas (librerías de Python) para trabajar:
- `cv2`: Para trabajar con imágenes y videos.
- `numpy`: Para manejar números y datos.
- `os`: Para trabajar con archivos y directorios.

## 2. Preparar los Datos

Se cargan las imágenes de un dataset, organizadas en carpetas según la emoción o la categoría que representan. Estas imágenes se leen en escala de grises y se almacenan junto con sus etiquetas correspondientes. Si no se encuentran imágenes, se muestra un error y se detiene el programa.

## 3. Entrenar el Modelo

Se utiliza `LBPHFaceRecognizer` de OpenCV para entrenar el modelo con las imágenes y sus etiquetas. El modelo se guarda en un archivo XML para su uso posterior. Este modelo permite reconocer y clasificar rostros basándose en las características aprendidas.

## 4. Detectar y Reconocer en Tiempo Real

Para hacer predicciones en tiempo real:
- Se carga el modelo entrenado desde el archivo XML.
- Se utiliza una cámara para capturar video.
- Se detectan rostros en cada frame del video usando `CascadeClassifier`.
- Los rostros detectados se procesan y se pasan al modelo para obtener una predicción.
- Si el modelo reconoce el rostro, se muestra la categoría (Feliz, Sorpresa o Tristeza) en la pantalla.

## 5. Redimensionar Imágenes

Adicionalmente, hay un script para redimensionar todas las imágenes en una carpeta a un tamaño específico (28x28 píxeles en este caso). Esto es útil para normalizar las imágenes antes de usarlas en el modelo.

## 6. Conclusión

Fue importante jugar con lo tonos de luz al cargar la dataset de cada emocion y poder agarrar diferentes rostros tanto de mujeres y hombres con sus diferentes caracteristicas, ademas como tambien poder cargar una cantidad similar de imagenes en cada carpeta de emociones para que no hubiera una mayor predonminancia. En general funciono bastante bien y pudimos observar los diferentes comportamientos del aprendizaje para saber que cambiar en la dataset que teniamos.