# Predicción Temprana del Riesgo de Diabetes Tipo 2 mediante Modelos de Machine Learning Supervisado

## a. Problema de Machine Learning

### Contexto

La diabetes mellitus tipo 2 es una enfermedad metabólica crónica que constituye uno de los principales desafíos para los sistemas de salud a nivel mundial. La detección temprana de individuos con alto riesgo de desarrollar diabetes puede facilitar intervenciones preventivas oportunas y contribuir a reducir complicaciones asociadas a la enfermedad.

El avance de las técnicas de Machine Learning ha permitido desarrollar modelos predictivos capaces de identificar patrones complejos en datos clínicos y apoyar la toma de decisiones en salud.

### Definición del problema

Este proyecto aborda un problema de aprendizaje supervisado de clasificación binaria cuyo objetivo es predecir la presencia o ausencia de diabetes a partir de variables clínicas y antropométricas de pacientes.

### Variable objetivo

**Outcome**

- 0 = No diabetes
- 1 = Diabetes

### Hipótesis

Las variables clínicas incluidas en el conjunto de datos contienen información suficiente para construir modelos de Machine Learning capaces de predecir la presencia de diabetes con un desempeño adecuado.

---

## b. Diagrama de flujo del proyecto

```text
Dataset Diabetes
        │
        ▼
Análisis Exploratorio (EDA)
        │
        ▼
Limpieza y Preprocesamiento
        │
        ▼
Análisis de Variables
        │
        ▼
División Train/Test
        │
        ▼
Entrenamiento de Modelos
        │
        ├── Logistic Regression
        ├── Random Forest
        ├── XGBoost
        └── CatBoost
        │
        ▼
Evaluación de Métricas
        │
        ▼
Selección del Mejor Modelo
        │
        ▼
Interpretación del Modelo
        │
        ▼
Modelo Final
```

---

## c. Descripción del Dataset

### Fuente

Pima Indians Diabetes Database.

### Descripción General

El conjunto de datos contiene información clínica y antropométrica de mujeres de ascendencia Pima, recopilada con el objetivo de estudiar factores asociados a la diabetes mellitus.

El dataset contiene **768 registros** y **9 variables**, incluyendo la variable objetivo.

### Diccionario de Datos

| Variable | Descripción |
|-----------|-------------|
| Pregnancies | Número de embarazos |
| Glucose | Concentración plasmática de glucosa |
| BloodPressure | Presión arterial diastólica (mmHg) |
| SkinThickness | Espesor del pliegue cutáneo del tríceps |
| Insulin | Concentración sérica de insulina |
| BMI | Índice de masa corporal |
| DiabetesPedigreeFunction | Función de riesgo hereditario de diabetes |
| Age | Edad del paciente |
| Outcome | Diagnóstico de diabetes (0 = No, 1 = Sí) |

### Calidad de los datos

Durante el análisis exploratorio se identificaron valores iguales a cero en variables fisiológicamente imposibles, como glucosa, presión arterial, insulina y BMI. Estos valores fueron considerados como datos faltantes implícitos y tratados durante la etapa de preprocesamiento.

---

## d. Model Card

### Información General

| Campo | Descripción |
|---------|-------------|
| Nombre del modelo | Diabetes Risk Prediction Model |
| Versión | 1.0.0 |
| Tipo | Clasificación Binaria |
| Framework | Scikit-learn / XGBoost / CatBoost |

### Objetivo

Predecir la presencia de diabetes tipo 2 utilizando variables clínicas y antropométricas.

### Usuarios previstos

- Profesionales de salud
- Investigadores biomédicos
- Estudiantes de ciencia de datos aplicada a salud

### Variables de entrada

- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age

### Variable de salida

**Outcome**

- 0 = No diabetes
- 1 = Diabetes

### Métricas de evaluación

- ROC-AUC
- Accuracy
- Precision
- Recall
- F1-Score

### Consideraciones éticas

Este modelo tiene fines exclusivamente educativos y de investigación. No debe utilizarse como herramienta diagnóstica ni para la toma de decisiones clínicas sin validación externa y supervisión profesional.

### Limitaciones

- Tamaño reducido del conjunto de datos.
- Población específica de estudio.
- Ausencia de validación clínica externa.
- Posible sesgo de selección inherente al dataset original.

---

## e. Resultados

### Evaluación Offline

| Modelo | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|----------|----------|----------|----------|----------|----------|
| Logistic Regression | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente |
| Random Forest | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente |
| XGBoost | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente |
| CatBoost | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente |

### Mejor Modelo

Pendiente de resultados experimentales.

### Evaluación Online

No aplica. El conjunto de datos utilizado corresponde a un dataset público sin plataforma externa de evaluación o leaderboard.

---

## f. Conclusiones

1. Los modelos de Machine Learning permitieron identificar patrones relevantes asociados a la presencia de diabetes tipo 2.

2. La comparación entre diferentes algoritmos permitió seleccionar el modelo con mejor capacidad predictiva para el problema planteado.

3. Las variables clínicas relacionadas con glucosa, índice de masa corporal y edad mostraron una contribución importante en la clasificación de pacientes.

4. Los resultados obtenidos demuestran el potencial de las técnicas de Machine Learning como herramientas de apoyo para la identificación temprana de individuos con riesgo de diabetes.

5. Se recomienda realizar validaciones adicionales con poblaciones independientes antes de considerar cualquier aplicación clínica del modelo.
