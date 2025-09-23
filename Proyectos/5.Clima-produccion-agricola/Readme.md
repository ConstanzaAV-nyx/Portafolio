# 🌱 Proyecto 5 – Cambio Climático y Seguridad Alimentaria: Análisis y Modelado Predictivo

Este proyecto es sobre cambio climático y seguridad alimentaria, donde debes evaluar cómo los factores climáticos afectan la producción agrícola en distintos países aplicando **modelos de aprendizaje supervisado**.

---

## 🎯 Objetivos

- Aplicar técnicas de **regresión** para predecir la producción agrícola en función de variables climáticas.  
- Utilizar algoritmos de **clasificación** para categorizar los países según el impacto del cambio climático.  
- Evaluar el desempeño de los modelos mediante **métricas adecuadas**.  
- Aplicar **preprocesamiento de datos** para mejorar la calidad del análisis.  
- Optimizar modelos con **ajuste de hiperparámetros**.  

---

## 📂 Contenido del repositorio

- `cambio_climatico_agricultura.csv` – Dataset original  
- `produccion_agricola.py` (o notebook) – Código principal  

---

## 📝 Desarrollo del proyecto

### 1️⃣ Carga y exploración de datos
- Carga del dataset con variables de **temperatura promedio**, **cambio en precipitaciones**, **frecuencia de sequías** y **producción agrícola**.
- Inspección inicial, detección de valores faltantes y duplicados.
- Análisis gráfico:
  - Pairplot y PairGrid para explorar relaciones entre variables.
  - Gráfico de barras de producción promedio por país.
  - Matriz de correlación y mapa de calor.
  - Boxplots para detectar valores atípicos.

### 2️⃣ Preprocesamiento y escalamiento
- Eliminación de valores nulos y duplicados.
- **Codificación de variables categóricas** (OneHotEncoding para países).
- **Normalización/Estandarización** de variables numéricas (MinMaxScaler y StandardScaler).
- División del dataset en **train/test (80%/20%)**.

### 3️⃣ Modelos de aprendizaje supervisado

#### 🔹 Regresión
- **Regresión lineal** para predecir producción de alimentos.
- Evaluación con **MSE**, **MAE** y **R²**.
- Comparación con **Árbol de Decisión** y **Random Forest**.
- Visualización: scatter plots Real vs Predicho y análisis de residuales.

#### 🔹 Clasificación
- Creación de variable **Impacto_climático** con 3 niveles: **Bajo**, **Medio**, **Alto**.
- Entrenamiento de modelos **KNN**, **Árbol de Decisión** y **SVM**.
- Evaluación con matriz de confusión, precisión, sensibilidad y **curva ROC-AUC**.

### 4️⃣ Optimización de modelos
- Ajuste de hiperparámetros usando **GridSearchCV**, **RandomizedSearchCV** y **BayesSearchCV**.
- Aplicación de técnicas de regularización (**Ridge**, **Lasso**, **ElasticNet**) y comparación de resultados.

### 5️⃣ Análisis de resultados y conclusiones
- **Random Forest** mostró mejor capacidad de generalización en regresión.  
- En clasificación, **SVM** obtuvo la mayor exactitud (80%).  
- La matriz de correlación indicó que **mayor temperatura promedio reduce las lluvias** y **aumenta la frecuencia de sequías**, siendo esta última la variable más correlacionada negativamente con la producción alimentaria.  
- El cambio climático impacta fuertemente la producción de alimentos y genera riesgos para la **seguridad alimentaria global**.

---

## 📈 Hallazgos principales

- Las variables climáticas están fuertemente interrelacionadas:
  - A mayor temperatura promedio → menos lluvias (−0.81).
  - Mayor frecuencia de sequías (0.83).
  - Producción de alimentos correlación negativa con sequías (−0.72).
- El cambio climático **reduce la producción alimentaria mundial** y genera riesgos de **precios altos**, **interrupciones de cadenas de suministro**, **incremento de desigualdad regional** y **migraciones**.
- Respuesta necesaria: cooperación internacional, inversión en tecnología de adaptación y resiliencia agrícola.

---

## 🧰 Tecnologías utilizadas

- Python 3  
- pandas, numpy, matplotlib, seaborn  
- scikit-learn (modelos de regresión y clasificación)  
- GridSearchCV / RandomizedSearchCV / BayesSearchCV  
- Técnicas de regularización (Ridge, Lasso, ElasticNet)  

---


