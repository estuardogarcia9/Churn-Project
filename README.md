# Churn-Project
En este proyecto de predicción de churn se desarrolla un modelo de machine learning capaz de anticipar qué clientes tienen mayor probabilidad de cancelar su suscripción. Reducir la tasa de churn es clave para maximizar los ingresos de la empresa y optimizar el gasto en adquisición de nuevos clientes. Aquí exploraremos los factores principales que impulsan la pérdida de usuarios y construiremos un clasificador robusto capaz de apoyar decisiones de retención.

2. Descripción de los datos
Los datos provienen de un histórico de clientes en formato CSV e incluyen:

Demográficos: edad, género.
Métricas de uso: duración de la suscripción (meses), frecuencia de uso del servicio.
Facturación: importe mensual, número de pagos atrasados.
Atención al cliente: cantidad de tickets o incidencias abiertas, tiempo medio de respuesta.
La variable objetivo churn indica si el cliente canceló su servicio (1 = churn, 0 = retención).

3. Metodología
El flujo de trabajo consta de cinco fases:

Análisis exploratorio (EDA):

Inspección de valores faltantes.

Distribución de variables y desequilibrio de clases.

Correlaciones y visualización de relaciones clave.

Limpieza y preprocesamiento:

Imputación de valores nulos.

Codificación de variables categóricas con OneHotEncoder.

Escalado de variables numéricas con StandardScaler.

Ingeniería de características:

Creación de ratios (por ejemplo, tickets_soporte / antigüedad).

Flags binarios (por ejemplo, pagos_retrasados > 0).

Selección de las variables más informativas.

Modelado y ajuste:

Entrenamiento de varios clasificadores (Regresión Logística, Random Forest, Gradient Boosting y SVM).

Validación cruzada (5-fold) y búsqueda de hiperparámetros con GridSearchCV.

Manejo del desequilibrio con class_weight='balanced' o SMOTE.

Evaluación e interpretación:

Métricas: ROC-AUC, precisión, recall, F1 y matriz de confusión.

Curvas ROC y de precisión-recall.

Análisis de importancia de variables y explicaciones con SHAP.
