# 🌍 Análisis de Migración Humana en el Siglo XXI con Apache Spark

Este proyecto es para estudiar tendencias de migración humana en el siglo XXI. Usamos **Apache Spark y PySpark** para procesar un conjunto de datos sobre migraciones, sus causas y su impacto socioeconómico en las regiones de origen y destino.

---

## 🎯 Objetivos del proyecto

1. **Aplicar conceptos de Big Data** utilizando Apache Spark y PySpark.  
2. **Explorar y transformar** datos con RDDs y DataFrames.  
3. Realizar **consultas con Spark SQL** para identificar patrones migratorios.  
4. **Implementar modelos de aprendizaje automático con MLlib** para predecir flujos migratorios.

---

## 📂 Dataset

El conjunto de datos incluye campos como:

- País de **Origen** y **Destino**  
- **Población** involucrada en la migración  
- **Razón** principal de migración  
- Variables **socioeconómicas** de origen y destino (PIB, tasa de desempleo, nivel educativo, etc.)

---

## ⚙️ Metodología

### 1️⃣ Carga y exploración de datos
- Crear una sesión Spark y cargar el CSV en un **DataFrame**.  
- Convertir los datos a **RDD** cuando sea necesario.  
- Inspeccionar el esquema, las primeras filas y estadísticas descriptivas.

### 2️⃣ Procesamiento con RDDs y DataFrames
- Aplicar transformaciones con RDDs: `filter`, `map`, `flatMap`.  
- Realizar acciones con RDDs: `collect`, `take`, `count`.  
- Operaciones con DataFrames: filtrado, agregación y ordenamiento.  
- Guardar resultados intermedios en **Parquet** para eficiencia y reproducibilidad.

### 3️⃣ Consultas con Spark SQL
- Registrar el DataFrame como tabla temporal.  
- Consultas para identificar principales países de origen/destino.  
- Agrupar por región y analizar razones de migración por región.

### 4️⃣ Predicción con MLlib
- Preparar features con `VectorAssembler` y escalar con `StandardScaler`.  
- Construir un modelo de **Regresión Logística** (o alternativo) para predecir la probabilidad de migración.  
- Evaluar con métricas como **AUC** y **accuracy**; iterar sobre features y parámetros.

---

## 📈 Resultados principales (resumen)

- Identificación de principales corredores migratorios y regiones con mayores flujos.  
- Determinación de razones predominantes de migración por región (ej. económicas, conflicto, medio ambiente).  
- Modelo de clasificación (regresión logística) con rendimiento evaluado mediante **AUC** y **accuracy**, útil como primera aproximación para predecir probabilidad de migración a partir de factores socioeconómicos.

---

## 🔍 Conclusiones y recomendaciones

- Spark permite procesar y transformar volúmenes grandes de datos de manera eficiente y pasar rápidamente a análisis predictivo con MLlib.  
- Los resultados pueden informar políticas públicas: focalización de intervención en regiones vulnerables, políticas de empleo y cooperación internacional.  
- Recomendaciones:
  - Incluir series temporales para modelar tendencias a lo largo de años.  
  - Probar modelos adicionales (Random Forest, GBT) y técnicas de oversampling/undersampling si clases están desbalanceadas.  
  - Integrar variables contextuales adicionales (conflictos, indicadores climáticos) para mejorar el poder predictivo.

---

## 🛠 Tecnologías utilizadas

- **Apache Spark / PySpark**  
- **Spark SQL**  
- **MLlib**  
- **Pandas** (para carga inicial y verificación)  
- **Matplotlib / Seaborn** (visualizaciones auxiliares)

---

## 📄 Archivos del repositorio (sugeridos)

- `migraciones.csv` — dataset original  
- `analisis_migracion_spark.py` — script principal con carga, transformación y MLlib  
---

