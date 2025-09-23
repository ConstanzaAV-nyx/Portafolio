# 🗂️ Análisis de Datos de Migración con NumPy y Pandas  

En este proyecto se trabajó con datos reales de migración del siglo XXI para identificar tendencias y factores socioeconómicos que afectan los movimientos de población.

## 🎯 Objetivo del Proyecto  
- Evaluar la capacidad para **manejar, limpiar y transformar datos** usando Python (NumPy y Pandas).  
- Extraer información útil para **apoyar la toma de decisiones** en materia de migración internacional.

## 📊 Dataset  
Archivo CSV con información de migración entre distintos países:
- Cantidad de migrantes  
- Razones de migración  
- Variables económicas (PIB, IDH)  

🔗 [Ver dataset en GitHub](https://github.com/ConstanzaAV-nyx/Portafolio/blob/main/Proyectos/2.Analisis-migracion/migracion.csv)

## 🛠️ Pasos Realizados  

### 1. Limpieza y Transformación de Datos  
- Carga del dataset en Pandas  
- Identificación y tratamiento de valores perdidos  
- Detección y filtrado de outliers con **Rango Intercuartílico (IQR)**  
- Reemplazo de valores en `Razon_Migracion` usando un diccionario (ej. Económica → Trabajo)  

### 2. Análisis Exploratorio  
- Visualización de las primeras filas del dataset  
- Obtención de info general (`.info()` y `.describe()`)  
- Cálculo de estadísticas clave:  
  - Media y mediana de la cantidad de migrantes  
  - PIB promedio de países de origen y destino  
  - Conteo de movimientos por razón de migración  

### 3. Agrupamiento y Sumarización  
- Agrupación de datos por `Razon_Migracion` y suma total de migrantes  
- Media del **IDH de origen** por cada tipo de migración  
- Ordenamiento de datos de mayor a menor cantidad de migrantes  

### 4. Filtros y Selección  
- Migraciones por conflicto (filtrado)  
- Filtrado por IDH de destino ≥ 0.90  
- Creación de nueva columna `Diferencia_IDH`  

### 5. Exportación  
- Guardado del DataFrame final limpio como `Migracion_Limpio.csv` (sin índice)  

## 📂 Archivos del Proyecto  
- `migracion.csv` – dataset original  
- `migracion.py` – script de análisis en Python  
- `Migracion_Limpio.csv` – dataset limpio exportado  

## 📝 Resultados e Interpretación  
- Se logró limpiar el dataset y eliminar outliers.  
- Se identificaron patrones en migración por tipo y diferencias de IDH.  
- Se creó un archivo limpio listo para análisis más avanzados o visualizaciones.  



