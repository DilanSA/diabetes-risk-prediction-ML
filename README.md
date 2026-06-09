# Predicción Temprana del Riesgo de Diabetes Tipo 2 mediante Modelos de Machine Learning Supervisado

## a. Problema de Machine Learning

### Contexto

La diabetes mellitus tipo 2 es una enfermedad metabólica crónica que representa uno de los principales desafíos para los sistemas de salud a nivel mundial. Su detección temprana permite implementar intervenciones oportunas que contribuyen a reducir complicaciones asociadas, mejorar la calidad de vida de los pacientes y optimizar el uso de recursos sanitarios.

Los avances en Machine Learning han permitido desarrollar modelos predictivos capaces de identificar patrones complejos en datos clínicos, facilitando la estratificación de riesgo y el apoyo a la toma de decisiones en salud.

### Definición del problema

Este proyecto aborda un problema de aprendizaje supervisado de clasificación binaria cuyo objetivo es predecir la presencia o ausencia de diabetes utilizando variables clínicas y antropométricas de pacientes.

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
Análisis Exploratorio de Datos (EDA)
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

## c. Descripción del Dataset con su Respectivo Diccionario de Datos

### Fuente

Pima Indians Diabetes Database.

### Descripción General

El conjunto de datos contiene información clínica y antropométrica de mujeres adultas pertenecientes a la población indígena Pima. El objetivo original del estudio fue identificar factores asociados al desarrollo de diabetes mellitus.

El dataset contiene:

- 768 observaciones
- 8 variables predictoras
- 1 variable objetivo

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

### Calidad de los Datos

Durante el análisis exploratorio se identificaron valores iguales a cero en variables fisiológicamente imposibles como glucosa, presión arterial, espesor del pliegue cutáneo, insulina e índice de masa corporal. Estos valores fueron tratados como datos faltantes implícitos y corregidos durante la etapa de preprocesamiento.

---

## d. Model Card

### Resumen del Modelo

Este proyecto desarrolla y compara diferentes modelos de Machine Learning para la predicción temprana de diabetes tipo 2 utilizando variables clínicas y antropométricas.

El objetivo es identificar el algoritmo con mejor desempeño predictivo y analizar las variables que tienen mayor influencia en la clasificación de pacientes con y sin diabetes.

### Detalles del Modelo

| Característica | Descripción |
|---------------|-------------|
| Nombre del modelo | Diabetes Risk Prediction Model |
| Versión | 1.0.0 |
| Tipo de problema | Clasificación binaria |
| Variable objetivo | Outcome |
| Framework principal | Scikit-Learn |
| Algoritmos evaluados | Logistic Regression, Random Forest, XGBoost y CatBoost |
| Fecha de creación | Junio 2026 |

### Uso Previsto

#### Uso principal

Predecir la probabilidad de que un individuo presente diabetes tipo 2 utilizando variables clínicas y antropométricas.

#### Usuarios previstos

- Estudiantes de Machine Learning.
- Investigadores biomédicos.
- Profesionales interesados en aplicaciones de Inteligencia Artificial en salud.

#### Usos no recomendados

- Diagnóstico clínico.
- Toma de decisiones médicas.
- Evaluación individual de pacientes en entornos asistenciales.

### Datos Utilizados

#### Dataset

Pima Indians Diabetes Database.

#### Tamaño del Dataset

| Característica | Valor |
|---------------|--------|
| Observaciones | 768 |
| Variables predictoras | 8 |
| Variable objetivo | 1 |

#### Variables de Entrada

- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age

#### Variable de Salida

**Outcome**

- 0 = No diabetes
- 1 = Diabetes

### Preprocesamiento

Las actividades realizadas incluyen:

- Análisis exploratorio de datos.
- Identificación de valores fisiológicamente imposibles.
- Tratamiento de valores faltantes implícitos.
- Imputación de datos faltantes.
- División de datos en entrenamiento y prueba.
- Escalamiento de variables cuando fue requerido por el algoritmo.

### Metodología

Se evaluaron múltiples algoritmos de clasificación supervisada:

1. Logistic Regression
2. Random Forest Classifier
3. XGBoost Classifier
4. CatBoost Classifier

La selección del modelo final se realizó mediante comparación de métricas de desempeño sobre datos no utilizados durante el entrenamiento.

### Métricas de Evaluación

#### Métrica principal

- ROC-AUC

#### Métricas secundarias

- Accuracy
- Precision
- Recall
- F1-Score

### Interpretabilidad

Para comprender el comportamiento del modelo se analizará la importancia relativa de las variables clínicas mediante técnicas de Feature Importance y, de manera opcional, SHAP (SHapley Additive Explanations).

### Consideraciones Éticas

Este modelo fue desarrollado exclusivamente con fines educativos y de investigación.

No debe utilizarse para diagnóstico clínico ni para la toma de decisiones médicas sin validación clínica independiente.

### Limitaciones

- El conjunto de datos corresponde a una población específica.
- El tamaño muestral es relativamente pequeño.
- No se realizó validación externa en otras poblaciones.
- Los resultados no garantizan desempeño equivalente en entornos clínicos reales.

### Trabajo Futuro

- Incorporar nuevas variables clínicas y bioquímicas.
- Validar el modelo en poblaciones independientes.
- Explorar técnicas avanzadas de explicabilidad.
- Comparar algoritmos adicionales.
- Desarrollar herramientas para inferencia de nuevos casos.

---

## e. Resultados con Métricas de Evaluación Offline y Online

### Evaluación Offline

| Modelo              | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| ------------------- | -------: | --------: | -----: | -------: | ------: |
| Logistic Regression |   0.7078 |    0.6000 | 0.5000 |   0.5455 |  0.8130 |
| Random Forest       |   0.7792 |    0.7273 | 0.5926 |   0.6531 |  0.8192 |
| XGBoost             |   0.7597 |    0.6735 | 0.6111 |   0.6408 |  0.8081 |
| CatBoost            |   0.7403 |    0.6400 | 0.5926 |   0.6154 |  0.8224 |

### Mejor Modelo

Random Forest fue seleccionado como modelo final debido a que obtuvo el mejor desempeño global, alcanzando una Accuracy de 0.7792, Precision de 0.7273, F1-Score de 0.6531 y un ROC-AUC de 0.8192.

---

## f. Conclusiones

## f. Conclusiones

1. Se desarrolló un flujo completo de Machine Learning para la predicción de diabetes tipo 2, incluyendo análisis exploratorio de datos, preprocesamiento, entrenamiento de modelos y evaluación de desempeño.

2. Durante la etapa de preprocesamiento se identificaron valores fisiológicamente imposibles en variables como glucosa, presión arterial, espesor del pliegue cutáneo, insulina e índice de masa corporal. Estos valores fueron tratados como datos faltantes implícitos e imputados mediante la mediana.

3. Se compararon cuatro algoritmos de clasificación supervisada: Logistic Regression, Random Forest, XGBoost y CatBoost. Entre ellos, Random Forest presentó el mejor desempeño global, alcanzando una Accuracy de 0.7792, Precision de 0.7273, F1-Score de 0.6531 y ROC-AUC de 0.8192.

4. El análisis de importancia de variables mostró que la concentración de glucosa fue el predictor más relevante para la clasificación de pacientes con diabetes, seguida por el índice de masa corporal (BMI), la función de riesgo hereditario de diabetes y la edad. Estos hallazgos son consistentes con factores de riesgo ampliamente descritos en la literatura médica.

5. Los resultados obtenidos evidencian que los modelos de Machine Learning pueden contribuir a la identificación temprana de individuos con riesgo de diabetes utilizando únicamente variables clínicas y antropométricas.

6. Debido a que el estudio se realizó sobre un conjunto de datos público y una población específica, se recomienda realizar validaciones adicionales con cohortes independientes antes de considerar cualquier aplicación clínica o asistencial del modelo desarrollado.
