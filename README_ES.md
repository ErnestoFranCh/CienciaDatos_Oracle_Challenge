
### [1. Análisis de Tiendas – Challenge ORACLE Data Science](Store/README_ES.md)

**Carpeta:** `Challenge_Store_ORACLE`

**Descripción:**
Proyecto desarrollado como parte de los **Challenges del programa de Ciencia de Datos de ORACLE**, enfocado en analizar el desempeño de **cuatro tiendas de Colombia** para responder a la pregunta clave:

> **¿En qué tienda conviene invertir?**

El análisis combinó técnicas de **EDA**, **series de tiempo**, y **visualización ejecutiva** para fundamentar la decisión.

Incluye:

* **Análisis exploratorio en Python** (ventas, transacciones, calificaciones, costos de envío)
* Identificación de patrones relevantes por tienda
* **Evaluación por categorías de producto** y desempeño general
* **Análisis de series de tiempo (ARIMA)** para estimación de tendencias

  * Se determinó que las series presentan **ruido blanco**, por lo que se aplicó un criterio alternativo basado en intervalos de ventas semanales
* **Selección de la tienda con mayor potencial de inversión**, considerando estabilidad y volumen de ventas
* **Dashboard interactivo en Power BI**, mostrando indicadores clave, comparativos y conclusión final

**Hallazgos clave:**

* Las tiendas **1 y 2** presentan las **mayores ventas totales**, destacando Tienda 1.
* No hubo diferencias significativas en volumen de transacciones o costo de envío promedio entre tiendas.
* Tienda 3 y Tienda 2 poseen las mejores calificaciones (4.05 y 4.02).
* Las ventas por tienda muestran **ruido blanco**, por lo que se analizó la distribución semanal:

  * **Tienda 1** presentó el mayor desempeño en rangos altos de ventas y el menor porcentaje en rangos bajos.
* **Conclusión:** **Tienda 1** es la mejor opción para inversión.

**Herramientas:** Python, pandas, numpy, seaborn, matplotlib, statsmodels (ARIMA), Power BI, Power Query, Jupyter Notebook

View Dash: [Click](https://mavenshowcase.com/project/54225)
