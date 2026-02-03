Credit Scoring – Loan Approval Analysis
Objetivo del Proyecto

Desarrollar y evaluar modelos de scoring crediticio para predecir la aprobación de préstamos minoristas, replicando un escenario real de evaluación de riesgo, con foco en interpretabilidad, estabilidad del modelo y criterios de negocio.

Dataset

4.269 solicitudes de crédito

Variables socioeconómicas, financieras y de historial crediticio

Incluye score crediticio CIBIL

Variable objetivo binaria: aprobado / rechazado

Distribución de clases balanceada a nivel negocio (≈62% aprobados)

Enfoque Analítico

EDA orientado a riesgo crediticio

Detección de inconsistencias y multicolinealidad

Análisis del rol del score crediticio como driver independiente del ingreso y patrimonio

Preprocesamiento con foco en reproducibilidad

Modelado

Regresión Logística como modelo baseline (interpretabilidad)

Random Forest como modelo comparativo

Evaluación mediante ROC-AUC

Análisis de estabilidad excluyendo el cibil_score para simular escenarios sin información de bureau

Resultados Clave

Con score de bureau: alta capacidad discriminatoria en entorno simulado (ROC-AUC ≈ 0.99)

Sin score de bureau: degradación significativa del desempeño (ROC-AUC ≈ 0.58)

Evidencia clara del valor del score crediticio en la originación de préstamos

Conclusiones

El proyecto demuestra un flujo completo de análisis de riesgo crediticio, cuantificando el impacto del historial crediticio en la toma de decisiones y alineándose con prácticas reales de la industria financiera.

El detalle técnico completo (EDA, preprocesamiento y modelado) se encuentra documentado en el README y notebooks del repositorio.