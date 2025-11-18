# Anlisis de Calidad dem Vinos
Implementación y análisis comparativo de modelos de ML sobre el dataset Wine Quality. Demostré la superioridad de LDA en clasificación (75.6% Accuracy) y contrasté Ridge vs Lasso en regresión, destacando la capacidad de Lasso para la selección de características clave.

# 🍷 Análisis de Calidad de Vinos: Clasificación y Regresión Regularizada

¡Hola! Soy **Rubén**, Ingeniero en Ciencias de Datos e Inteligencia Artificial.

En este repositorio comparto un proyecto práctico donde analizo el dataset **"Wine Quality"** para predecir la calidad del vino basándome en sus propiedades fisicoquímicas. El objetivo principal no fue solo obtener métricas, sino entender el comportamiento de diferentes algoritmos frente a datos reales correlacionados.

## 🚀 Resumen del Proyecto

El trabajo se divide en dos enfoques principales:
1.  **Clasificación:** Determinar si un vino es "bueno" o "malo".
2.  **Regresión:** Predecir el puntaje exacto de calidad.

Para ello, realicé una comparación técnica entre modelos probabilísticos y modelos de regularización.

## 📊 Principales Hallazgos

A continuación, detallo las conclusiones más relevantes a las que llegué tras el entrenamiento y evaluación:

### 1. Clasificación: ¿GNB o LDA?
Puse a prueba **Gaussian Naive Bayes (GNB)** contra **Linear Discriminant Analysis (LDA)**.
* **El Ganador:** LDA fue superior con un **Accuracy del 75.6%** (frente al 72.2% de GNB).
* **¿Por qué?** El análisis de correlación mostró que las variables del vino no son independientes (ej. acidez fija vs. pH). GNB asume independencia, y al violarse esta suposición, su rendimiento cae. LDA, en cambio, maneja mejor estas relaciones entre variables.

### 2. Regresión Regularizada: Ridge vs. Lasso
Evalué modelos lineales con penalización L1 (Lasso) y L2 (Ridge) para evitar el sobreajuste.
* **El Ganador en Predicción:** **Ridge (alpha=100)** logró el menor error (**RMSE: 0.6266**) y un mejor R².
* **El Valor de Lasso:** Aunque tuvo un error ligeramente mayor (**RMSE: 0.6625**), Lasso fue extremadamente útil para la **selección de características**. De las 11 variables originales, Lasso eliminó 8 (llevando sus coeficientes a 0), destacando que los factores más determinantes para la calidad son:
    * Alcohol (+)
    * Volatile Acidity (-)
    * Sulphates (+)

## 🛠️ Tecnologías Utilizadas
* **Python**
* **Pandas & NumPy** (Manipulación de datos)
* **Matplotlib & Seaborn** (Visualización y matrices de confusión)
* **Scikit-Learn** (Modelado, GridSearchCV y Preprocesamiento)

---
*Este proyecto fue desarrollado como parte de mi formación continua en Machine Learning. Si tienes sugerencias o dudas sobre el código, ¡no dudes en contactarme!*
