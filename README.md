# Retencion_clientes_Proyecto_Machine_Learning
Este proyecto desarrolla un modelo de Machine Learning para predecir la probabilidad de que un cliente abandone (churn). Incluye análisis exploratorio, preprocesamiento, manejo de desbalance, comparación de modelos, optimización de hiperparámetros y explicación del modelo.


# Objetivos
* Identificar factores que explican la deserción de clientes.
* Construir modelos con alto recall para minimizar falsos negativos.
* Aplicar buenas prácticas de ciencia de datos para un caso de negocio real.

# Modelos utilizados
* Regresión logística
* SVM
* Random Forest
* XGBoost / CatBoost
* Optuna para optimización en cada modelo
* Evaluación mediante Recall, F1 y ROC-AUC: Para este proyecto, el recall será la métrica más importante para evaluar los modelos, ya que es fundamental para la empresa identificar a todos los clientes potenciales que podrían abandonar la compañía, para así reducir el porcentaje de estos.

# Resultados principales
## Regresión logística
* best_recall_score:0.50
* AUC:0.82
## SVM
* best_recall_score:0.83
* AUC:0.83
## Red neuronal
* best_recall_score:0.64
* AUC:0.80
## Random forest
* best_recall_score:0.80
* AUC:0.82
## XGBoost
* best_recall_score:0.83
* AUC:0.82
## CatBoost
* best_recall_score:0.81
* AUC:0.82

# Conclusiones
En primer lugar, durante el análisis exploratorio se encontró que hay algunas características particulares de los clientes que hacen que su retención sea más complicada. entre ellos está ser un adulto mayor, no tener pareja, no tener dependientes, tener servicio de fibra óptica. no tener backup online, no tener protección en los dispositivos, no tener servicio de soporte técnico, no tener servicio de streaming, tener contrato con renovación mes a mes, tener la factura física y que el método de pago sea electrónico.

Con respecto a los modelos, los mejores son el VM y el XGBoost, que presentaron buenos valores de recall en entrenamiento y en testeo (muy cercanos, lo que indica que sí hay aprendizaje y no overfitting). Además, tienen un valor de 0.82 de AUC, es decir, el modelo hace una buena generalización e identificación de las clases. Por otra parte, el modelo da prioridad al recall sobre la precision debido a que considera que es más importante invertir en clientes para retenerlos antes de que exista la posibilidad de perderlos.

Como sugerencia, el modelo de regresión logística es muy bueno identificando los clientes que no se van a ir y si se complementa con el modelo SVM o XGBoost, se podria precisar en clientes que se requeiere hacer campañas para su retención y ahorrar en los que realmente no lo requieren, pues la union de ambos modelos lograría una mayor diferenciación entre clases.

Para acceder al proyecto en colab puede ingresar al siguiente link: https://colab.research.google.com/drive/1Qxd8dUifSdLViLoUR3_BwqCtFeQRpejk?usp=sharing
