
# Análisis de Evasión de Clientes: Telecom X

Este proyecto implementa un flujo completo de **ETL (Extracción, Transformación y Carga)** y **Análisis Exploratorio de Datos (EDA)** para identificar los factores que influyen en la pérdida de clientes (*Churn*) en la empresa de telecomunicaciones **Telecom X**.

El objetivo principal es limpiar y preparar los datos para que el equipo de ciencia de datos pueda desarrollar modelos predictivos de retención.

---

## Estructura del Proyecto

El análisis se divide en cinco secciones estratégicas:

1. **Extracción:** Conexión a la fuente de datos original (JSON) y normalización de estructuras anidadas.
2. **Transformación:** Limpieza de datos "trampa", corrección de tipos y creación de nuevas métricas.
3. **Carga y Análisis:** Visualización de la distribución de evasión y perfiles demográficos.
4. **Análisis de Correlación:** Identificación de las variables con mayor peso estadístico en el abandono.
5. **Informe Final:** Resumen de hallazgos y recomendaciones estratégicas para el negocio.

---

## Tecnologías Utilizadas

* **Python 3.11.3**
* **Pandas:** Para la manipulación y limpieza de datos.
* **Seaborn & Matplotlib:** Para la generación de gráficos estadísticos.
* **JSON:** Formato de origen de los datos.

---

## Hallazgos Principales (Insights)

A través del análisis, se identificaron patrones críticos que explican por qué los clientes abandonan el servicio:

* **La Variable "Evasión" (Churn):** * **No:** Clientes que permanecen activos (Valor 0).
* **Yes:** Clientes que cancelaron el servicio en el último mes (Valor 1).


* **Factores de Riesgo:**
* Los clientes con **contratos mes a mes** presentan la mayor tasa de fuga.
* Existe una **correlación negativa** entre la antigüedad y la evasión: a menor tiempo en la empresa, mayor es el riesgo de pérdida.
* Los cargos mensuales elevados suelen ser un detonante para el abandono del servicio.



---

## Calidad de los Datos y Auditoría

Para garantizar la fiabilidad de los resultados, se aplicaron filtros de calidad para detectar "datos trampa":

* **Tratamiento de Nulos:** Conversión de espacios en blanco en la columna de cargos totales a valores numéricos.
* **Consistencia Matemática:** Se auditó la relación entre los meses de contrato y los cargos totales, asegurando que los clientes nuevos no presentaran cobros incoherentes.
* **Binarización:** Preparación de variables categóricas para el análisis matemático y modelos de Machine Learning.

---

## Recomendaciones

1. **Fidelización Temprana:** Implementar campañas agresivas de retención durante los primeros 6 meses de contrato.
2. **Migración de Contratos:** Incentivar el paso de planes mensuales a planes anuales mediante descuentos.
3. **Monitoreo de Precios:** Revisar la competitividad de los precios en clientes con facturación alta para evitar la fuga por costo.

