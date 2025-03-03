# Predicción de Cancelaciones de Contratos en Interconnect

## Descripción del Proyecto

La retención de clientes es un desafío clave para las empresas de telecomunicaciones, y **Interconnect** no es la excepción. Este proyecto tiene como objetivo desarrollar un modelo de **Machine Learning** capaz de predecir qué clientes tienen mayor probabilidad de cancelar su contrato. Con esta información, la empresa podría ofrecer incentivos como descuentos o planes personalizados para mejorar la satisfacción y fomentar la lealtad de los clientes.

Se han analizado diversos factores que influyen en la cancelación de contratos, y se han evaluado diferentes modelos para encontrar la mejor solución.

---

## Estructura de Datos

El dataset utilizado contiene información sobre los clientes, sus contratos y los servicios contratados. Se divide en las siguientes tablas:

### **1. Contratos (**``**)**

- `customerId`: Identificador único del cliente.
- `BeginDate`: Fecha de inicio del contrato.
- `EndDate`: Fecha de finalización del contrato o "No" si sigue activo.
- `Type`: Tipo de contrato (mes a mes, 1 año, 2 años).
- `PaperlessBilling`: Indica si la facturación es electrónica (`Yes` / `No`).
- `PaymentMethod`: Método de pago.
- `MonthlyCharges`: Cargo mensual.
- `TotalCharges`: Cargos totales del cliente.

### **2. Servicios de Internet (**``**)**

- `customerID`: Identificador único del cliente.
- `InternetService`: Tipo de conexión (DSL o Fibra óptica).
- `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`: Servicios adicionales contratados (`Yes` / `No`).

### **3. Datos Personales (**``**)**

- `customerID`: Identificador único del cliente.
- `gender`: Género (`Female` / `Male`).
- `SeniorCitizen`: Indica si es adulto mayor (`1` / `0`).
- `Partner`: Indica si tiene pareja (`Yes` / `No`).
- `Dependents`: Indica si tiene dependientes (`Yes` / `No`).

### **4. Telefonía (**``**)**

- `customerID`: Identificador único del cliente.
- `MultipleLines`: Indica si tiene varias líneas de teléfono (`Yes` / `No`).

*Nota:* La tabla de telefonía podría fusionarse con la de servicios de internet para un análisis conjunto.

---

## Análisis y Resultados

1. **Factores Clave en la Cancelación**
   - La mayoría de las cancelaciones ocurren entre **octubre y enero**. Se recomienda ofrecer descuentos en esos meses.
   - Los clientes con **contratos a largo plazo** presentan menor tasa de cancelación.
   - **Telefonía fija** tiene mayor retención que internet por fibra óptica, lo que sugiere posibles problemas técnicos con este servicio.
   - **Clientes con dependientes** muestran una menor tasa de cancelación, lo que sugiere que podrían beneficiarse de ofertas especiales.
2. **Desempeño de Modelos de Machine Learning**
   - Se probaron varios algoritmos, incluyendo:
     - **Regresión Logística** (rendimiento apenas superior a una predicción aleatoria).
     - **Random Forest** y **XGBoost**, que obtuvieron mejores resultados.
     - **XGBoost** fue el modelo más efectivo, con buenas métricas en el conjunto de prueba.
3. **Equilibrio del Dataset**
   - Los datos estaban desbalanceados, y aunque se probaron métodos para balancearlos, las mejoras fueron mínimas.
   - Se eliminaron columnas innecesarias para mejorar la calidad del modelo.

---

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

## Contacto

Para más información sobre este proyecto, puedes contactar a:

📧 smsanmartinlepin@gmail.com\
🐙 https://github.com/Scarleth6o6\
💼 www.linkedin.com/in/scarlethsan-martin\

---

© 2025 - Interconnect Churn Prediction

