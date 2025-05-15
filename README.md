# 🐾 Predicción de Adopción de Mascotas con Redes Neuronales (Keras)

## 🎯 Resumen del Proyecto

Este proyecto demuestra la aplicación de técnicas de **Deep Learning** para construir un modelo predictivo que determina la probabilidad de adopción de una mascota. Utilizando el dataset `petfinder-mini.csv`, se desarrolló una **red neuronal con Keras (TensorFlow)** 🧠 para clasificar si una mascota será adoptada o no, basándose en sus características.

El objetivo fue transformar un problema de predicción de velocidad de adopción (múltiples categorías) en una tarea de **clasificación binaria** (adoptado ✅ vs. no adoptado ❌), donde `AdoptionSpeed == 4` (no adoptado) se mapea a la clase `0` y el resto (adoptado) a la clase `1`.

## 🛠️ Metodología Aplicada

El flujo de trabajo implementado cubre las etapas esenciales de un proyecto de Machine Learning:

1.  **📊 Preparación de Datos:**
    *   Carga y limpieza inicial del dataset utilizando **Pandas**.
    *   Transformación de la variable objetivo a un formato binario.

2.  **✨ Ingeniería y Preprocesamiento de Características:**
    *   Identificación y separación de características numéricas y categóricas.
    *   **Normalización** de variables numéricas.
    *   **Codificación One-Hot** para variables categóricas.
    *   Todo el preprocesamiento se realizó eficientemente utilizando **capas de preprocesamiento de Keras** (`Normalization`, `StringLookup`, `IntegerLookup`, `CategoryEncoding`), resultando en un conjunto final de 216 características de entrada para el modelo.

3.  **🧠 Desarrollo del Modelo de Deep Learning:**
    *   Diseño y construcción de una **red neuronal secuencial** en Keras.
    *   Arquitectura con múltiples capas densas (Dense) y funciones de activación ReLU.
    *   Implementación de técnicas de regularización para combatir el sobreajuste: **Regularización L2, Batch Normalization y Dropout**.
    *   Capa de salida con activación **sigmoide**, adecuada para clasificación binaria.

4.  **⚙️ Entrenamiento y Optimización:**
    *   Compilación del modelo utilizando el optimizador **Adam** y la función de pérdida `binary_crossentropy`.
    *   Entrenamiento del modelo monitoreando la métrica de `accuracy`.
    *   Uso de `EarlyStopping` para detener el entrenamiento de forma óptima y evitar el sobreajuste, restaurando los mejores pesos obtenidos durante la validación.

5.  **📈 Evaluación del Rendimiento:**
    *   Análisis de las curvas de aprendizaje (pérdida en entrenamiento vs. validación).
    *   Cálculo y visualización de la **matriz de confusión** para evaluar el desempeño en el conjunto de prueba.
    *   Reporte de la precisión (accuracy) final.

## 💻 Tecnologías Clave Utilizadas

*   **Lenguaje:** Python 3 🐍
*   **Deep Learning:** TensorFlow & Keras 🔥
*   **Manipulación de Datos:** Pandas 🐼, NumPy
*   **Machine Learning (utilidades):** Scikit-learn sklearn
*   **Visualización:** Matplotlib 📊, Seaborn 📉
*   **Entorno de Desarrollo:** Jupyter Notebook 📓

## 🏆 Resultados Destacados

*   El modelo de red neuronal alcanzó una **precisión (accuracy) del 73.18%** en el conjunto de datos de prueba.
*   La precisión en el conjunto de entrenamiento fue del **73.33%**, indicando un buen equilibrio y evitando un sobreajuste significativo gracias a las técnicas de regularización implementadas.
*   La matriz de confusión y las curvas de pérdida (disponibles en el notebook) ofrecen una visión detallada del comportamiento y la capacidad de generalización del modelo.

## 💡 Conclusión

Este proyecto demuestra la capacidad de construir modelos de Deep Learning robustos para problemas de clasificación con datos tabulares, gestionando el preprocesamiento de características directamente dentro del pipeline de Keras y aplicando estrategias efectivas para el entrenamiento y la evaluación.

---
