Evaluación de Modelo de Clasificación con PyCaret, MLflow y FastAPI
Este proyecto se enfoca en la creación, evaluación y despliegue de un modelo de clasificación utilizando PyCaret, MLflow y FastAPI. Los datos provienen del desafío de Kaggle: Playground Series - Season 4, Episode 1. El objetivo es entrenar un modelo de clasificación para predecir los resultados a partir de los datos, gestionando los experimentos y versiones del modelo con MLflow, y desplegando un servicio de predicción con FastAPI.

Componentes Clave del Proyecto
Carga de Archivos de Entrenamiento y Prueba:

Los archivos train.csv y test.csv son los conjuntos de datos utilizados para el entrenamiento y la evaluación del modelo.
Los datos se cargan en la API mediante FastAPI en formato CSV y se procesan en pandas para generar DataFrames que serán utilizados en el modelo de clasificación.
Uso de PyCaret para Entrenamiento del Modelo:

PyCaret es una biblioteca de machine learning de bajo código que facilita la experimentación con varios modelos de clasificación.
Durante el entrenamiento, PyCaret se encarga de:
Preprocesamiento de los datos: PyCaret se encarga automáticamente de manejar datos faltantes, normalización, codificación categórica, etc.
Comparación de Modelos: PyCaret permite comparar varios modelos de clasificación (e.g., Random Forest, SVM, XGBoost) de manera rápida y eficiente.
Tuning de Hiperparámetros: PyCaret incluye una funcionalidad automática para ajustar los hiperparámetros del modelo elegido.
Registro con MLflow: PyCaret se integra automáticamente con MLflow, lo que permite registrar los experimentos, métricas y modelos sin necesidad de configuración adicional.
MLflow para la Gestión del Ciclo de Vida del Modelo:

MLflow gestiona los experimentos de PyCaret y permite:
Registrar automáticamente los modelos y los parámetros probados en PyCaret.
Guardar métricas de rendimiento como precisión, recall, F1-score, AUC, entre otras.
Versionar los modelos entrenados para identificar fácilmente el mejor modelo.
Comparar modelos en función de las métricas obtenidas en los experimentos.
MLflow almacena los artefactos y permite una gestión clara de cada versión del modelo y de las pruebas realizadas.
Despliegue del Modelo con FastAPI:

Una vez que el modelo es entrenado y registrado en MLflow a través de PyCaret, se despliega en una API utilizando FastAPI.
Endpoints principales:
/upload: Para cargar los conjuntos de datos de entrenamiento y prueba.
/train: Para entrenar el modelo utilizando PyCaret.
/predict: Para realizar predicciones sobre nuevos datos utilizando el mejor modelo almacenado en producción.
FastAPI toma los datos de entrada en formato JSON o CSV y realiza predicciones basadas en el modelo entrenado con PyCaret.

Evaluación de Modelo de Clasificación con PyCaret, MLflow y FastAPI
Este proyecto se enfoca en la creación, evaluación y despliegue de un modelo de clasificación utilizando PyCaret, MLflow y FastAPI. Los datos provienen del desafío de Kaggle: Playground Series - Season 4, Episode 1. El objetivo es entrenar un modelo de clasificación para predecir los resultados a partir de los datos, gestionando los experimentos y versiones del modelo con MLflow, y desplegando un servicio de predicción con FastAPI.

Componentes Clave del Proyecto
Carga de Archivos de Entrenamiento y Prueba:

Los archivos train.csv y test.csv son los conjuntos de datos utilizados para el entrenamiento y la evaluación del modelo.
Los datos se cargan en la API mediante FastAPI en formato CSV y se procesan en pandas para generar DataFrames que serán utilizados en el modelo de clasificación.
Uso de PyCaret para Entrenamiento del Modelo:

PyCaret es una biblioteca de machine learning de bajo código que facilita la experimentación con varios modelos de clasificación.
Durante el entrenamiento, PyCaret se encarga de:
Preprocesamiento de los datos: PyCaret se encarga automáticamente de manejar datos faltantes, normalización, codificación categórica, etc.
Comparación de Modelos: PyCaret permite comparar varios modelos de clasificación (e.g., Random Forest, SVM, XGBoost) de manera rápida y eficiente.
Tuning de Hiperparámetros: PyCaret incluye una funcionalidad automática para ajustar los hiperparámetros del modelo elegido.
Registro con MLflow: PyCaret se integra automáticamente con MLflow, lo que permite registrar los experimentos, métricas y modelos sin necesidad de configuración adicional.
MLflow para la Gestión del Ciclo de Vida del Modelo:

MLflow gestiona los experimentos de PyCaret y permite:
Registrar automáticamente los modelos y los parámetros probados en PyCaret.
Guardar métricas de rendimiento como precisión, recall, F1-score, AUC, entre otras.
Versionar los modelos entrenados para identificar fácilmente el mejor modelo.
Comparar modelos en función de las métricas obtenidas en los experimentos.
MLflow almacena los artefactos y permite una gestión clara de cada versión del modelo y de las pruebas realizadas.
Despliegue del Modelo con FastAPI:

Una vez que el modelo es entrenado y registrado en MLflow a través de PyCaret, se despliega en una API utilizando FastAPI.
Endpoints principales:
/upload: Para cargar los conjuntos de datos de entrenamiento y prueba.
/train: Para entrenar el modelo utilizando PyCaret.
/predict: Para realizar predicciones sobre nuevos datos utilizando el mejor modelo almacenado en producción.
FastAPI toma los datos de entrada en formato JSON o CSV y realiza predicciones basadas en el modelo entrenado con PyCaret.
