# Proyecto MLP para Clasificación Fashion MNIST - 
## Evaluación Parcial N° 1 - Fundamentos de Deep Learning (DLY0100)

Este repositorio contiene el trabajo realizado para la primera evaluación parcial de la asignatura Fundamentos de Deep Learning. El objetivo fue implementar, entrenar, optimizar y evaluar un Perceptrón Multicapa (MLP) para clasificar imágenes del dataset Fashion MNIST.

**Integrantes:**
*   Boris Arriagada
*   Alejandro Troncoso
*   Jaime Vicencio

## Contenido del Repositorio

*   **`evaluacion_1_deep_learning.ipynb`**: El cuaderno Jupyter de Google Colab que contiene todo el código, análisis, visualizaciones y documentación del proceso. Incluye:
    *   Carga y Exploración de Datos (EDA) del dataset Fashion MNIST.
    *   Preprocesamiento de imágenes y etiquetas.
    *   Definición de una función flexible para crear modelos MLP.
    *   Implementación de un Test Harness para la experimentación sistemática con:
        *   Funciones de activación (ReLU, Sigmoid, Tanh).
        *   Arquitecturas (neuronas/capas).
        *   Tasas de Dropout y comparación sin regularización.
        *   Tasas de Aprendizaje y Optimizadores (Adam, SGD).
        *   Tamaño de Lote (Batch Size).
        *   (Opcional) Batch Normalization.
        *   (Opcional) Data Augmentation.
    *   Uso de Early Stopping para optimizar el número de épocas.
    *   Análisis comparativo de resultados (tablas y curvas de aprendizaje).
    *   Selección y evaluación detallada del mejor modelo encontrado (incluyendo reporte de clasificación, matriz de confusión y visualización de predicciones).
    *   Guardado del modelo final entrenado.
*   **`MLP_ReLU_128_64_D0.2_best_model_ES.keras`**: El archivo del modelo Keras final, entrenado y guardado, listo para ser cargado y utilizado para inferencia. (Asegúrate de que el nombre coincida con el archivo que subiste).
*   **`README.md`**: Este archivo.

## Resumen del Mejor Modelo

Tras la experimentación, el modelo seleccionado como el de mejor rendimiento fue:

*   **Nombre Base:** `MLP_ReLU_128_64_D0.2` 
*   **Arquitectura:** Flatten -> Dense(128, ReLU) -> Dropout(0.2) -> Dense(64, ReLU) -> Dropout(0.2) -> Dense(10, Softmax)
*   **Optimizador:** Adam (LR=0.001)
*   **Entrenamiento:** Con Early Stopping (mejor época: ~20)
*   **Accuracy en Test:** 88.92% 
*   **F1-Score Ponderado en Test:** 0.8893

<p align="center">
  <img src="curvas.png" alt="Descripción del gráfico" width="1200">
</p>


## Cómo Ejecutar

1.  Abrir el notebook `evaluacion_1_deep_learning.ipynb` en Google Colab.
2.  Ejecutar las celdas en orden. El Test Harness puede tardar un tiempo considerable en completarse.

## Dependencias Principales

*   TensorFlow / Keras
*   NumPy
*   Pandas
*   Scikit-learn
*   Matplotlib
*   Seaborn (para matriz de confusión)

---
