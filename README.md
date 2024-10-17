Evaluación de Modelo de Clasificación con MLflow y FastAPI

Este proyecto tiene como objetivo desarrollar un flujo completo para la evaluación de un modelo de clasificación utilizando MLflow, pycaret para gestionar el ciclo de vida del modelo y FastAPI para desplegar un servicio de predicción accesible. El flujo incluye la carga y procesamiento de los conjuntos de datos de entrenamiento y prueba, la creación de experimentos en MLflow, el almacenamiento de los modelos, y la integración de un servicio API para realizar predicciones basadas en el modelo entrenado.

Componentes Clave del Proyecto
Carga de Archivos de Entrenamiento y Prueba:

Se cargan dos conjuntos de datos: el conjunto de entrenamiento y el de prueba, ambos necesarios para el desarrollo del modelo de clasificación.
Estos archivos pueden ser cargados en la API mediante FastAPI en formato CSV o cualquier otro formato estructurado que permita el procesamiento en pandas.

Entrenamiento del Modelo:

Los datos de entrenamiento se procesan para preparar el modelo de clasificación usando pycaret.
El modelo puede ser cualquier algoritmo de clasificación (e.g., Random Forest, SVM, XGBoost).
Durante el entrenamiento, se configuran experimentos en MLflow para:
Registrar los parámetros del modelo.
Guardar las métricas de rendimiento (precisión, F1-score, AUC, etc.).
Almacenar el modelo entrenado.

MLflow para Gestión del Ciclo de Vida del Modelo:

Se utilizan experimentos en MLflow para monitorear el rendimiento de los modelos, realizar el seguimiento de los experimentos, y gestionar múltiples versiones del modelo.

Los experimentos se registran automáticamente con MLflow, que almacena:
    Parámetros del modelo (como hiperparámetros ajustados).
    Métricas de rendimiento (como precisión, recall, etc.).
    Artefactos como gráficos o informes generados durante la evaluación del modelo.
    Modelos en producción, para su uso en la API.
    Esto permite una fácil comparación entre experimentos y facilita la selección del mejor modelo para producción.

Despliegue del Modelo con FastAPI:

Una vez que el modelo de clasificación es entrenado y registrado en MLflow, se implementa una API en FastAPI que sirve para realizar predicciones.

Endpoints principales de la API:
/upload: Para subir archivos de entrenamiento y prueba.
/train: Para entrenar el modelo utilizando los datos de entrenamiento.
/predict: Para realizar predicciones sobre nuevos datos utilizando el modelo en producción.
FastAPI toma los datos de entrada (nuevas observaciones) en formato JSON o CSV y utiliza el modelo de clasificación previamente registrado en MLflow para devolver una predicción.

Capturas de Pantalla:
