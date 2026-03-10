

# Telecom X: Predicción de Evasión (Churn)

Este proyecto aplica un flujo de **Data Science** para identificar y predecir la fuga de clientes en una empresa de telecomunicaciones.

## Resumen del Pipeline

1. **ETL & Limpieza:**
* Normalización de JSON anidado.
* Auditoría de "Datos Trampa" (corregidos 11 registros inconsistentes y cargos nulos).
* Ingeniería de variables: `Cargos_Diarios`.


2. **Análisis (EDA):**
* Identificación de segmentos críticos: Clientes con contratos **mes a mes** y servicios de **fibra óptica**.


3. **Modelado Predictivo:**
* Algoritmo: **Regresión Logística**.
* Preprocesamiento: `OneHotEncoder` (categorías) y `StandardScaler` (escalado).


4. **Optimización:**
* Búsqueda dinámica del **umbral óptimo** para maximizar el F1-Score.



## Resultados del Modelo (Optimizado)

| Métrica | Valor |
| --- | --- |
| **Umbral Óptimo** | **0.32** (Dinámico) |
| **Recall (Clase 1)** | **77%** |
| **F1-Score** | **0.62** |
| **Accuracy** | **75%** |

> **Insight clave:** Al reducir el umbral de decisión, logramos detectar al **77% de los clientes en riesgo**, mejorando la capacidad de retención proactiva del negocio.

## 📦 Entregables

* `df_clean.csv`: Dataset procesado y estandarizado.
* `modelo_churn_telecomX.pkl`: Modelo entrenado.
* `escalador_telecomX.pkl`: Escalador para nuevos datos.