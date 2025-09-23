# 📊 Predicción de la Tasa de Natalidad con Redes Neuronales

Este proyecto se centra en la investigación en demografía y tiene como objetivo desarrollar un modelo de red neuronal capaz de predecir la tasa de natalidad en distintos países a partir de variables socioeconómicas clave.

---

## 🎯 Objetivos del proyecto

- Diseñar y entrenar una red neuronal para resolver un problema de regresión.

- Aplicar funciones de activación, optimizadores y técnicas para prevenir sobreajuste.

- Evaluar y comparar resultados con distintas configuraciones.

- Analizar la influencia de cada variable en la predicción y extraer conclusiones sobre patrones demográficos globales.

---
## 📂 Dataset

Se utilizó un dataset con información socioeconómica de distintos países:

- PIB per cápita

- Acceso a servicios de salud (% población)

- Nivel educativo promedio

- Tasa de empleo femenino

- Edad promedio de maternidad

- Índice de urbanización

- Tasa de natalidad (variable objetivo)

## 📂 Contenido del repositorio
-`dataset_natalidad.csv` - Dataset

-`tasa_natalidad.py` - Script principal con el análisis

---

## ⚙️ Metodología
## 1️⃣ Carga y exploración de datos

Limpieza de valores faltantes y duplicados.

Análisis exploratorio: pairplots, histogramas y mapa de calor para estudiar correlaciones.

## 2️⃣ Preprocesamiento

División del dataset en train/test (80/20).

Estandarización de variables con StandardScaler.

## 3️⃣ Diseño del modelo

Red neuronal secuencial (TensorFlow/Keras) con:

Capa de entrada = nº de variables predictoras.

Capas ocultas:

Dense(128, activación ReLU, regularización L2) + Dropout(0.2)

Dense(64, activación Sigmoid) + Dropout(0.2)

Dense(32, activación ReLU)

Capa de salida: Dense(1, activación Linear).

Función de pérdida: MSE.

Optimizador: Adam (variando learning rates).

## 4️⃣ Entrenamiento y optimización

Entrenamiento con distintos learning rates, batch sizes, unidades y dropout.

Selección del mejor modelo según loss/MAE en el conjunto de test.

Evaluación del impacto de cada variable mediante los pesos de la primera capa.

## 5️⃣ Evaluación

Visualización de pérdida de entrenamiento vs validación.

Predicciones vs valores reales de tasa de natalidad.

Cálculo del MAE.

## 📈 Resultados principales

PIB per cápita resultó ser la variable más influyente (correlación negativa con la natalidad).

También se observó influencia del acceso a servicios de salud y de la urbanización.

Países con mayor PIB tienden a tener tasas de natalidad menores, en línea con tendencias demográficas globales.

El modelo mostró buen ajuste tras optimizar hiperparámetros.

## 🔍 Conclusiones

La red neuronal permitió capturar patrones demográficos complejos.

Se confirma la relación entre desarrollo socioeconómico y descenso de la natalidad.

El enfoque de redes neuronales es útil para predicciones multivariables en demografía.

## 🚀 Posibles mejoras

Añadir más capas ocultas o usar redes más profundas.

Incorporar nuevas variables (políticas públicas, fertilidad, cultura).

Evaluar otros modelos (árboles de decisión, random forest, XGBoost) para comparar desempeño.

Hacer validación cruzada para robustecer resultados.

---

## 🛠️ Tecnologías utilizadas

Python 3.10+

TensorFlow / Keras

NumPy / Pandas

Seaborn / Matplotlib

Scikit-learn

## 📊 Visualizaciones generadas

- Mapa de calor de correlaciones.

- Histogramas y boxplots de las variables socioeconómicas.

- Gráfico de pérdidas (training vs validation).

- Gráfico de importancia de características.

- Dispersión de predicciones vs valores reales.
