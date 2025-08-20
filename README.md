# challenge-telecom-x-part2
Proyecto del Programa Alura -  Realizado por Zaleth Rivas Calderón

Proyecto de Predicción de Cancelación de Clientes (Churn)
🚀 Objetivo

El propósito de este proyecto es anticipar qué clientes tienen mayor probabilidad de cancelar sus servicios, con el fin de que la empresa implemente estrategias de retención proactivas.

Este trabajo corresponde a la Parte 2 del Desafío, donde se construyen modelos de Machine Learning para la predicción de churn, complementando el análisis exploratorio realizado previamente.

📌 Flujo del Proyecto
1️⃣ Preprocesamiento de Datos

Eliminación de columnas irrelevantes (ej. identificadores).

Codificación de variables categóricas mediante One-Hot Encoding.

División en datos de entrenamiento y prueba (70/30).

Escalado aplicado únicamente a los modelos sensibles a la escala (ej. Regresión Logística).

Verificación y tratamiento del desbalance de clases (uso de SMOTE como prueba).

2️⃣ Modelos Construidos

Se entrenaron dos modelos principales:

Regresión Logística (con escalado)

Random Forest (sin escalado)

Esto permitió comparar un modelo lineal e interpretable con uno no lineal y robusto.

3️⃣ Evaluación de Modelos

📊 Resultados principales:

Regresión Logística

Accuracy: 79.3%

Precision (Churn): 68.2%

Recall (Churn): 36.6%

F1-score (Churn): 47.6%

ROC-AUC: 83.7%

Random Forest

Accuracy: 75.2%

Precision (Churn): 51.1%

Recall (Churn): 79.4%

F1-score (Churn): 62.2%

ROC-AUC: 83.8%

📌 Análisis crítico:

La Regresión Logística tiene mayor precisión, pero bajo recall → clasifica bien cuando predice cancelación, pero detecta menos clientes en riesgo.

El Random Forest presenta recall alto, lo que lo hace mejor para identificar clientes en riesgo de churn, aunque con menor precisión.

Ambos modelos tienen ROC-AUC ≈ 0.84, lo que indica buena capacidad discriminativa.

4️⃣ Importancia de Variables

🔹 Regresión Logística (coeficientes más influyentes):

Factores que reducen el churn: mayor tiempo de contrato (Meses_Contrato), contratos a 1–2 años, uso de TechSupport/OnlineSecurity.

Factores que aumentan el churn: internet de fibra óptica, facturación electrónica, método de pago electrónico, gasto mensual elevado.

🔹 Random Forest (Top 10 variables):

Contract_two year

InternetService_no

InternetService_fiber optic

Meses_Contrato

PaymentMethod_electronic check

Gasto_Total

Gasto_Mensual

Gasto_Diario

Charges.Calculado

PaperlessBilling

5️⃣ Conclusiones y Estrategias

✅ Factores clave de cancelación:

Clientes con fibra óptica, facturación electrónica y pagos electrónicos.

Clientes con gastos mensuales elevados.

Contratos cortos y poca antigüedad.

✅ Factores protectores contra el churn:

Contratos de 1–2 años.

Servicios de soporte y seguridad digital (TechSupport, OnlineSecurity).

💡 Recomendaciones estratégicas:

Incentivar contratos largos con beneficios o descuentos.

Mejorar la experiencia de clientes de fibra óptica (calidad del servicio o relación costo/beneficio).

Ofrecer planes personalizados o descuentos a clientes con gasto mensual alto.

Revisar la experiencia de pago electrónico y facturación digital para reducir fricciones.

Promover activamente los servicios de seguridad y soporte, que reducen la cancelación.

🛠️ Tecnologías Utilizadas

Python 3

Pandas, NumPy (procesamiento de datos)

Scikit-learn (modelado y métricas)

Matplotlib, Seaborn (visualización)

Imbalanced-learn (SMOTE) (balanceo de clases)
