# Credit Scoring – Loan Approval

Proyecto de **Credit Scoring** orientado a evaluación de riesgo crediticio para aprobación de préstamos, combinando análisis exploratorio, modelos supervisados y validaciones de estabilidad.

El objetivo principal es **simular el flujo de trabajo real de un equipo de Credit Risk / Data Analytics**, priorizando interpretabilidad, control de riesgo y buenas prácticas de versionado.

---

## Objetivos del proyecto

* Analizar un dataset de solicitudes de préstamo.
* Construir modelos de clasificación para **default / aprobación**.
* Comparar modelos lineales vs no lineales.
* Evaluar dependencia de variables críticas (CIBIL Score).
* Analizar estabilidad y sensibilidad del modelo.
* Documentar decisiones como en un entorno bancario real.

---

## Modelos desarrollados

### Regresión Logística

* Modelo baseline.
* Alta interpretabilidad.
* Usado como punto de comparación.

### Random Forest

* Modelo no lineal.
* Captura interacciones complejas entre variables.
* Desempeño significativamente superior al baseline.

### Random Forest sin CIBIL Score

* Test de **estabilidad estructural**.
* Evalúa la dependencia del modelo respecto a un score externo.
* Permite analizar el aporte marginal del resto de las variables.

---

## Estructura del proyecto

```
credit-scoring-loan-approval/
│
├── data/
│   └── processed/
│       └── credit_df_processed.csv
│
├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_logistic_regression.ipynb
│   ├── 04_random_forest.ipynb
│   ├── 05_model_stability_no_cibil.ipynb
│   └── 06_sensitivity_analysis.ipynb
│
├── models/
│   ├── logistic_regression.pkl
│   ├── random_forest.pkl
│   └── random_forest_no_cibil.pkl
│
├── reports/
│   ├── figures/
│   └── summary.md
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Notebooks (flujo de trabajo)

| Notebook                            | Descripción                                      |
| ----------------------------------- | ------------------------------------------------ |
| `01_eda.ipynb`                      | Análisis exploratorio y entendimiento del riesgo |
| `02_preprocessing.ipynb`            | Limpieza, encoding y preparación del dataset     |
| `03_logistic_regression.ipynb`      | Modelo baseline e interpretación                 |
| `04_random_forest.ipynb`            | Modelo principal y feature importance            |
| `05_model_stability_no_cibil.ipynb` | Evaluación sin variable crítica                  |
| `06_sensitivity_analysis.ipynb`     | Impacto de cambios en variables clave            |

---

## Métricas clave

* Accuracy
* Precision
* Recall
* F1‑Score
* ROC‑AUC
* Matrices de confusión
* Curvas ROC comparativas

El enfoque está puesto en **minimizar riesgo financiero**, priorizando el análisis de falsos positivos y sensibilidad del modelo.

---

## Nota sobre los modelos entrenados (`.pkl`)

Los archivos de modelos entrenados (`.pkl`) se incluyen en este repositorio **con fines de portfolio y reproducibilidad**.

En un entorno productivo o regulado, estos artefactos suelen gestionarse fuera del control de versiones (model registry, storage seguro).  
Aquí se incluyen para permitir la ejecución directa del flujo analítico y la revisión completa del proyecto.

---

## Análisis de estabilidad y sensibilidad

* Se demuestra la **dependencia crítica del CIBIL Score**.
* Sin esta variable, el desempeño del modelo cae drásticamente.
* El análisis de sensibilidad muestra cómo pequeñas variaciones en:

  * Ingreso anual
  * Monto del préstamo
  * Score crediticio

afectan la probabilidad de aprobación.

Esto replica prácticas habituales en **validación de modelos regulatorios**.

---

## Tecnologías utilizadas

* Python
* Pandas / NumPy
* Scikit‑learn
* Matplotlib / Seaborn
* Jupyter Notebook
* Git / GitHub

---

## Próximos pasos

* Cross‑validation y validación fuera de muestra
* Calibration (PD)
* Threshold optimization
* Feature selection sin score externo
* Documentación tipo *Model Validation Report*

---

## 👤 Autor

**Franco Aranda**
Data Analyst · Credit Risk

Proyecto desarrollado con fines académicos y de portfolio profesional.
