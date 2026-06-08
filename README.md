# Predicción Temprana del Riesgo de Diabetes Tipo 2 mediante Modelos de Machine Learning Supervisado

## Descripción del Proyecto

Este proyecto tiene como objetivo desarrollar y evaluar modelos de Machine Learning supervisado para la predicción de diabetes tipo 2 utilizando variables clínicas y antropométricas de pacientes.

La diabetes mellitus tipo 2 representa uno de los principales problemas de salud pública a nivel mundial. La identificación temprana de individuos con alto riesgo puede contribuir a intervenciones oportunas y mejorar los resultados clínicos. Mediante técnicas de Machine Learning, se busca construir modelos predictivos capaces de identificar pacientes con diabetes a partir de información clínica obtenida durante la atención médica rutinaria.

---

## Problema de Machine Learning

### Tipo de aprendizaje

**Aprendizaje Supervisado**

### Subtipo

**Clasificación Binaria**

### Variable objetivo

`Outcome`

- 0 = No Diabetes
- 1 = Diabetes

### Pregunta de investigación

> ¿Es posible predecir la presencia de diabetes tipo 2 utilizando variables clínicas y antropométricas mediante algoritmos de Machine Learning supervisado?

---

## Hipótesis

### Hipótesis principal (H1)

> Las variables clínicas incluidas en el dataset contienen información suficiente para construir modelos de Machine Learning capaces de predecir la presencia de diabetes con un desempeño adecuado.

### Hipótesis secundaria (H2)

> Los algoritmos basados en árboles de decisión presentarán un mejor desempeño predictivo que los modelos lineales debido a su capacidad para capturar relaciones no lineales entre las variables clínicas.

---

## Objetivo General

Desarrollar y evaluar modelos de Machine Learning supervisado para la predicción de diabetes tipo 2 utilizando variables clínicas y antropométricas de pacientes.

---

## Objetivos Específicos

1. Realizar un análisis exploratorio del conjunto de datos para identificar patrones y características relevantes.
2. Implementar técnicas de preprocesamiento para mejorar la calidad de los datos.
3. Entrenar y comparar diferentes algoritmos de clasificación.
4. Evaluar el desempeño de los modelos utilizando métricas apropiadas para clasificación binaria.
5. Identificar las variables con mayor contribución en la predicción de diabetes.

---

## Justificación

La aplicación de técnicas de Machine Learning en salud puede contribuir al desarrollo de herramientas de apoyo para la toma de decisiones clínicas. La detección temprana de individuos con riesgo elevado de diabetes podría facilitar intervenciones preventivas y optimizar la asignación de recursos en los sistemas de salud.

---

## Dataset

### Diccionario de Datos

| Variable | Tipo | Descripción |
|-----------|---------|-------------|
| Pregnancies | Numérica | Número de embarazos |
| Glucose | Numérica | Concentración plasmática de glucosa |
| BloodPressure | Numérica | Presión arterial diastólica (mmHg) |
| SkinThickness | Numérica | Espesor del pliegue cutáneo del tríceps |
| Insulin | Numérica | Concentración sérica de insulina |
| BMI | Numérica | Índice de masa corporal |
| DiabetesPedigreeFunction | Numérica | Riesgo hereditario de diabetes |
| Age | Numérica | Edad del paciente |
| Outcome | Binaria | Presencia de diabetes (1) o ausencia (0) |

---

## Estructura del Proyecto

```text
diabetes-risk-prediction-ml/
│
├── README.md
│
├── data/
│   ├── raw/
│   │   └── diabetes.csv
│   │
│   └── processed/
│       └── diabetes_clean.csv
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   └── 02_machine_learning_and_model_interpretability.ipynb
│
├── artifacts/
│   ├── models/
│   │   └── best_model.pkl
│   │
│   ├── metrics/
│   │   └── metrics.csv
│   │
│   └── figures/
│
├── src/
│   ├── train.py
│   ├── predict.py
│   └── utils.py
│
├── docs/
│   ├── model_card.md
│   └── git_strategy.md
│
├── requirements.txt
├── .gitignore
└── LICENSE
```

---

## Flujo de Trabajo

```text
Dataset
   │
   ▼
Data Exploration
   │
   ▼
Data Cleaning
   │
   ▼
Feature Analysis
   │
   ▼
Train/Test Split
   │
   ▼
Model Training
   │
   ├── Logistic Regression
   ├── Random Forest
   ├── XGBoost
   └── CatBoost
   │
   ▼
Model Evaluation
   │
   ▼
Model Selection
   │
   ▼
Model Interpretation
   │
   ▼
Final Artifact
```

---

## Modelos a Evaluar

### Baseline
- Logistic Regression

### Ensemble
- Random Forest

### Gradient Boosting
- XGBoost

### Gradient Boosting Avanzado
- CatBoost

---

## Métricas de Evaluación

### Métrica Principal

- ROC-AUC

### Métricas Secundarias

- Accuracy
- Precision
- Recall
- F1-Score

### Justificación

Dado que el costo de no identificar correctamente a un paciente con diabetes puede ser elevado, se priorizará el análisis de Recall y ROC-AUC durante la evaluación de los modelos.

---

## Interpretabilidad

Para comprender el comportamiento de los modelos se evaluarán:

- Feature Importance
- SHAP (SHapley Additive exPlanations)

Preguntas a responder:

- ¿Cuál es la variable más importante para la predicción?
- ¿La glucosa es el principal predictor?
- ¿Qué impacto tienen el BMI y la edad?
- ¿Cómo contribuyen las variables clínicas al resultado final?

---

## Estrategia Git

Se utilizará una estrategia simplificada basada en Git Flow.

```text
main
  │
  └── development
```

Proceso:

1. Crear la rama `development`.
2. Realizar el desarrollo y pruebas en dicha rama.
3. Crear Pull Request hacia `main`.
4. Aprobar y fusionar cambios.
5. Crear Release estable.

---

## Release

### Versión

`v1.0.0`

### Release Notes

- Exploratory Data Analysis
- Data Preprocessing
- Model Training
- Model Comparison
- Model Interpretation
- Documentation
- Model Card

---

## Resultado Esperado

Se espera identificar el modelo con mejor capacidad predictiva para la detección de diabetes tipo 2 y determinar cuáles son las variables clínicas más relevantes en la clasificación de pacientes.

Asimismo, se busca demostrar la aplicación de buenas prácticas de Machine Learning Engineering mediante documentación, control de versiones, reproducibilidad y organización estructurada del proyecto.
