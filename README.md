# Telecom Customer Churn Analysis

## Descripción del Proyecto

Este proyecto analiza un conjunto de datos de clientes de telecomunicaciones para predecir la rotación de clientes (churn). El conjunto de datos contiene información demográfica de los clientes, detalles de sus servicios contratados y patrones de facturación.

## Estructura del Código

El código está organizado en un notebook de Jupyter (`Telecom2.ipynb`) con las siguientes secciones principales:

### 1. Carga y Exploración Inicial de Datos
- Importación de bibliotecas (pandas, scikit-learn, matplotlib, seaborn)
- Carga del dataset desde una URL
- Eliminación de la columna 'customerID'
- Visualización de las primeras filas del dataset

### 2. Preprocesamiento de Datos
- Codificación de la variable objetivo 'Churn' (No=0, Yes=1)
- One-hot encoding para variables categóricas nominales
- Eliminación de filas con valores no numéricos en 'account.Charges.Total'
- Conversión de 'account.Charges.Total' a tipo numérico

### 3. Análisis Exploratorio de Datos (EDA)
- Distribución de clases (Churn vs No Churn)
- Visualización de la distribución de clases
- Matriz de correlación entre variables numéricas

## Variables del Dataset

El dataset contiene las siguientes variables:

### Información del Cliente
- `Churn`: Indicador si el cliente abandonó el servicio
- `customer.gender`: Género del cliente
- `customer.SeniorCitizen`: Indicador de cliente senior
- `customer.Partner`: Si tiene pareja
- `customer.Dependents`: Si tiene dependientes
- `customer.tenure`: Meses de permanencia

### Servicios de Teléfono
- `phone.PhoneService`: Si tiene servicio telefónico
- `phone.MultipleLines`: Si tiene múltiples líneas

### Servicios de Internet
- `internet.InternetService`: Tipo de servicio de internet
- `internet.OnlineSecurity`: Seguridad en línea
- `internet.OnlineBackup`: Backup en línea
- `internet.DeviceProtection`: Protección de dispositivo
- `internet.TechSupport`: Soporte técnico
- `internet.StreamingTV`: Streaming TV
- `internet.StreamingMovies`: Streaming de películas

### Información de Cuenta
- `account.Contract`: Tipo de contrato
- `account.PaperlessBilling`: Facturación sin papel
- `account.PaymentMethod`: Método de pago
- `account.Charges.Monthly`: Cargos mensuales
- `account.Charges.Total`: Cargos totales

## Hallazgos Importantes

1. **Distribución de clases**: 
   - 73.46% de clientes se mantienen (No churn)
   - 26.54% de clientes abandonan (Churn)

2. **Correlaciones**:
   - La variable `customer.tenure` tiene correlación negativa con churn (-0.35)
   - Los cargos totales (`account.Charges.Total`) tienen correlación negativa con churn (-0.19)
   - Los cargos mensuales (`account.Charges.Monthly`) tienen correlación positiva con churn (0.19)

## Próximos Pasos

1. Balanceo de clases (debido al desbalance moderado)
2. Ingeniería de características adicionales
3. Entrenamiento de modelos de machine learning
4. Evaluación de modelos y selección del mejor
5. Implementación de estrategias para reducir el churn

## Requisitos

Las bibliotecas principales utilizadas son:
- pandas
- scikit-learn
- matplotlib
- seaborn

## Uso

Ejecutar las celdas del notebook en orden para reproducir el análisis. El código está comentado para facilitar su comprensión.
