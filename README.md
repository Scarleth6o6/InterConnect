# Interconnect: Predicción de Cancelación de Clientes

## Descripción
Interconnect busca predecir qué clientes tienen mayor probabilidad de cancelar su contrato mediante un modelo de Machine Learning. Se analizaron distintos factores que influyen en la cancelación y se compararon múltiples algoritmos para encontrar la mejor solución.

## Tecnologías Utilizadas
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

## Modelos y Métricas
Se evaluaron tres modelos principales utilizando diversas métricas de rendimiento:

| Modelo               | F1 Score | AUC ROC | Recall  | Precisión | Exactitud |
|----------------------|---------|---------|---------|-----------|-----------|
| LogisticRegression  | 0.6349  | 0.8637  | 0.8547  | 0.5051    | 0.7551    |
| RandomForest        | 0.6944  | 0.9025  | 0.8091  | 0.6081    | 0.8226    |
| XGBoost             | **0.8736**  | **0.9722**  | 0.7977  | **0.9655**  | **0.9425**  |

Resultados de **XGBoost** en el conjunto de prueba:
- **F1 Score:** 0.8333
- **AUC ROC:** 0.9603
- **Recall:** 0.7353
- **Precisión:** 0.9615
- **Exactitud:** 0.9219

## Conclusión
El modelo **XGBoost** obtuvo el mejor rendimiento en todas las métricas, destacándose en precisión y AUC ROC. Esto lo convierte en la mejor opción para predecir cancelaciones de clientes y tomar medidas preventivas para mejorar la retención.



## Requisitos

Para ejecutar el código, asegúrate de tener instaladas las siguientes librerías:

```bash
pip install pandas numpy scikit-learn xgboost matplotlib seaborn
```

---

## Ejecución del Proyecto

Para entrenar y evaluar el modelo:

1. Cargar los datos y preprocesarlos.
2. Seleccionar y entrenar los modelos.
3. Evaluar los resultados.

El notebook principal (`notebook.ipynb`) contiene todo el proceso de análisis y predicción.

---

## Conclusión y Futuro del Proyecto

- Se recomienda mejorar la calidad del servicio de internet por fibra óptica para reducir cancelaciones.
- Crear incentivos para clientes con contratos cortos.
- Explorar nuevas técnicas de balanceo de datos para mejorar el rendimiento de los modelos.

---
© 2025 - Interconnect Churn Prediction

