# Predicción de recuperación de oro – Optimización de procesos industriales 🪙

Este proyecto se centra en la **predicción del porcentaje de recuperación de oro** en distintas etapas de un **proceso metalúrgico industrial**. Predecir con precisión la recuperación permite **optimizar la eficiencia del proceso**, reducir pérdidas y mejorar la toma de decisiones en plantas de procesamiento de minerales.

## 🎯 Objetivo

Predecir el **porcentaje de recuperación de oro** en dos etapas clave del proceso:

- `rougher.output.recovery`
- `final.output.recovery`

El objetivo es construir modelos de regresión que minimicen el error de predicción utilizando la métrica **sMAPE**.

## 📂 Dataset

El proyecto utiliza tres archivos de datos:

- `/datasets/gold_recovery_train.csv`
- `/datasets/gold_recovery_test.csv` *(no contiene las columnas objetivo)*
- `/datasets/gold_recovery_full.csv` *(utilizado para análisis y validación)*

### Estructura del dataset

- Las variables de entrada incluyen concentraciones químicas, parámetros del proceso y métricas operativas.
- Variables objetivo:
  - `rougher.output.recovery`
  - `final.output.recovery`

## 🧠 Metodología y técnicas utilizadas

- Limpieza y preprocesamiento de datos
- Manejo de valores faltantes
- Verificación de la **fórmula de recuperación de oro** a partir de los datos originales
- Análisis exploratorio de datos (EDA)
- Alineación de características entre los conjuntos de entrenamiento y prueba
- Entrenamiento de modelos de regresión
- Implementación personalizada de la métrica **sMAPE**
- Evaluación y comparación de modelos

## 📊 Métrica de evaluación

La métrica principal de evaluación es **sMAPE (Symmetric Mean Absolute Percentage Error)**, calculada como un promedio ponderado:

- 25% para `rougher.output.recovery`
- 75% para `final.output.recovery`

Valores más bajos de sMAPE indican un mejor desempeño del modelo.

## ✅ Resultados y conclusión

- El modelo seleccionado obtuvo el **menor sMAPE total** en el conjunto de validación.
- Los resultados destacan la importancia de una correcta preparación de los datos y consistencia de variables.
- El proyecto demuestra cómo el aprendizaje automático puede aplicarse para **optimizar procesos industriales de recuperación de oro**.

---

📌 **Tecnologías utilizadas**:
- Python
- pandas
- NumPy
- scikit-learn
- matplotlib / seaborn
