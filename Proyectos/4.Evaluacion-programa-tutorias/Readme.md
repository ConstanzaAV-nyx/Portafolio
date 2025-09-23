# 📚 Evaluación del Programa de Tutorías

Este proyecto simula un estudio para determinar si un nuevo programa de tutoría mejora el rendimiento académico de estudiantes. Se utilizan técnicas de estadística descriptiva, inferencia y pruebas de hipótesis.

---

## 🎯 Objetivo del Proyecto
Evaluar el impacto de un programa de tutoría en el rendimiento académico de los estudiantes mediante:
- Diseño experimental básico.
- Estadística descriptiva.
- Pruebas de hipótesis (t de Student).
- Cálculo de intervalos de confianza.

---

## 📝 Diseño del Experimento
- **Grupo A (Tutoría):** 15 estudiantes reciben el programa.
- **Grupo B (Control):** 15 estudiantes no reciben tutoría.
- Se mide el rendimiento mediante un examen estándar (0 a 100 puntos).
- Para reducir sesgos:
  - Asignación aleatoria de los estudiantes.
  - Características similares en ambos grupos.
  - Registro de calificaciones previas.

---

## 📊 Análisis Realizado

### 1. Estadísticas Descriptivas
- Media y desviación estándar para ambos grupos.
- Representación gráfica con **histogramas** y **boxplots**.

### 2. Prueba de Hipótesis
- **H0:** No hay diferencia en el rendimiento académico entre los dos grupos.
- **H1:** El grupo con tutoría tiene mejor rendimiento académico.
- Prueba t para muestras independientes con α = 0.05.
- Interpretación del valor-p.

### 3. Intervalo de Confianza
- Cálculo del 95% para la diferencia de medias entre grupos.
- Interpretación del intervalo.

### 4. Validación con TLC
- Simulación de distribución de medias muestrales para justificar el uso de la t de Student.

---

## 🗂️ Archivos del Proyecto
- `programa_tutorias.py` → código del análisis.
- `README.md` → este documento.

---

## 📈 Resultados Principales
- **Medias:** El grupo con tutoría muestra promedio superior al grupo control.
- **Prueba t:** Valor-p < 0.05 → se rechaza H0; el programa de tutorías mejora el rendimiento académico.
- **Intervalo de confianza:** El rango del 95% está completamente por encima de 0, confirmando diferencia significativa.

---

## ⚙️ Tecnologías Utilizadas
- **Python**  
  - pandas  
  - numpy  
  - scipy.stats  
  - matplotlib  
  - seaborn  

---

