# 🎶 Proyecto – Análisis de Preferencias Musicales y Clusterización por País

Este proyecto corresponde al análisis de **preferencias musicales en distintos países** usando técnicas de **aprendizaje no supervisado**. El objetivo es **detectar patrones de consumo musical** y **agrupar países según sus similitudes** en géneros escuchados.

---

## 🎯 Objetivos

- Aplicar **clusterización** para encontrar grupos de países con patrones de escucha similares.
- Utilizar **reducción de dimensionalidad** para visualizar la estructura de los datos.
- Evaluar diferentes algoritmos de clusterización y justificar sus ventajas y desventajas.
- Interpretar los resultados en un contexto **cultural y social**.

---

## 📂 Contenido del repositorio

- `dataset_generos_musicales.csv` – Dataset con la popularidad de distintos géneros musicales en cada país.  
- `preferencias_musicales.py` – Script principal con todo el análisis.  


---

## 📝 Desarrollo del proyecto

### 1️⃣ Carga y exploración de datos
- Dataset: Chile, EE.UU., México, Corea, Japón, Alemania, Rusia e Italia.  
- Inspección inicial: valores faltantes y duplicados.  
- Análisis exploratorio:
  - **Mapa de calor de correlaciones** entre géneros musicales.
  - **Boxplot** para visualizar la distribución y detectar outliers.  

### 2️⃣ Aplicación de algoritmos de clusterización

#### 🔹 K-Means
- K inicial = 3.  
- Determinación del K óptimo con **método del codo** y **coeficiente de silueta**.  
- Visualización de clusters y centroides.  

#### 🔹 Clustering jerárquico
- Generación de **dendrograma** para estimar el número óptimo de clusters.  
- Aplicación de **Agglomerative Clustering**.  
- Comparación con resultados de K-Means.  

#### 🔹 DBSCAN
- Pruebas con diferentes valores de `eps` y `min_samples`.  
- Uso del gráfico **k-dist** para escoger parámetros.  
- Identificación de **outliers** y clusters no esféricos.  

---

### 3️⃣ Reducción de dimensionalidad

#### 🔹 PCA
- Cálculo de varianza explicada y determinación de componentes principales para ≥90% de varianza.  
- Visualización bidimensional de países con las dos primeras componentes principales.  

#### 🔹 t-SNE
- Visualización 2D de relaciones entre países.  
- Pruebas con distintos valores de **perplexity** para evaluar cambios en la representación.  

---

### 4️⃣ Análisis de resultados y conclusiones

#### 🔹 Comparación de métodos
- **K-Means:** rápido y eficiente, pero requiere definir K.  
- **Jerárquico:** permite ver relaciones con dendrograma, pero es más costoso computacionalmente.  
- **DBSCAN:** no requiere K y detecta outliers, pero es sensible a la densidad y parámetros.  
- En este caso, **K-Means y jerárquico coincidieron** en la formación de 3 clusters; DBSCAN detectó puntos dispersos pero no replicó las agrupaciones principales.  

#### 🔹 PCA vs. t-SNE
- **PCA** permitió agrupar países y ver distancias relativas claras entre ellos.  
- **t-SNE** con perplexity moderada (≈5) replicó patrones similares, ofreciendo una visualización más flexible.  

#### 🔹 Interpretación cultural y social
- Los clusters no siguieron exactamente criterios geográficos o culturales esperados.  
- Se observa influencia global en géneros urbanos (reggaetón, hip-hop), electrónicos y pop.  
- La globalización y plataformas estadounidenses han homogeneizado en parte las preferencias musicales internacionales.  

---

## 📈 Hallazgos principales
- **Patrones compartidos** entre países aparentemente distintos.  
- **Globalización musical:** fuerte influencia de EE.UU. y géneros urbanos en casi todos los países.  
- **Homogeneización de gustos:** diferencias culturales no siempre se reflejan en las agrupaciones estadísticas.  

---

## 🧰 Tecnologías utilizadas
- Python 3  
- pandas, numpy  
- matplotlib, seaborn  
- scikit-learn (KMeans, AgglomerativeClustering, DBSCAN, PCA, t-SNE)  

---
