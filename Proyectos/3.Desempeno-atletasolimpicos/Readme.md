# 🏅 Análisis del Desempeño de Atletas Olímpicos

Este proyecto analiza datos de atletas olímpicos con el objetivo de identificar patrones de rendimiento, factores clave asociados al éxito deportivo y realizar predicciones simples sobre la cantidad de medallas obtenidas.

---

## 📋 Objetivo del Proyecto
Evaluar la relación entre características de los atletas (edad, altura, peso, entrenamientos semanales, país y disciplina) y su desempeño en las competiciones (medallas obtenidas).

---

## ⚙️ Tecnologías y Librerías Utilizadas
- **Python** (pandas, numpy)
- **Visualización:** seaborn, matplotlib
- **Estadística:** scipy.stats
- **Modelado Predictivo:** scikit-learn (LinearRegression)

---

## 🔹 Metodología Aplicada

### 1. Análisis Exploratorio de Datos
- Carga del dataset.
- Limpieza de datos (valores nulos, duplicados).
- Estadísticas descriptivas.
- Histogramas de variables relevantes.

### 2. Estadística Descriptiva
- Identificación de tipo de variable (categórica/numérica).
- Media, mediana y moda de las medallas obtenidas.
- Desviación estándar de altura.
- Boxplot de peso para detectar outliers.

### 3. Análisis de Correlación
- Correlación de Pearson entre entrenamientos semanales y medallas totales.
- Scatterplots entre variables clave.
- Interpretación de los coeficientes de correlación.

### 4. Regresión Lineal
- Modelo predictivo de medallas en función de entrenamientos semanales.
- Obtención de coeficientes (β0, β1).
- Cálculo de R².
- Visualización con regplot de seaborn.

### 5. Visualización de Datos
- Heatmap de correlación entre variables numéricas.
- Boxplot de medallas por disciplina deportiva.
- Personalización de títulos y etiquetas.

---

## 📈 Principales Resultados
- **Correlaciones:** moderada entre entrenamientos semanales y medallas; positiva fuerte entre peso y altura.
- **Modelo predictivo:** regresión lineal simple para estimar medallas según entrenamientos semanales.
- **Insights visuales:** diferencias en medallas según disciplina.

---

## 🗂️ Archivos del Proyecto
- `olimpicos.csv`: dataset original.
- `analisis_olimpicos.py` 
- `Images`: Visualizaciones generadas (histogramas, scatterplots, heatmaps, boxplots).

---
