# Proyecto: **Análisis de Tiendas – Challenge ORACLE Data Science**

## Descripción General

Este challenge forma parte del programa de certificación en **Data Science de ORACLE**.
El objetivo del proyecto fue analizar la información proporcionada por **cuatro tiendas de Colombia** con el fin de responder la pregunta central:

> **¿En qué tienda conviene invertir?**

El proyecto abarca análisis exploratorio, evaluación de métricas de negocio, análisis de series de tiempo y visualización de resultados mediante un dashboard en Power BI.

---

## Análisis en Python

El análisis se realizó en dos notebooks principales:
`AnalisisTiendas.ipynb` (EDA) y `ARIMA.ipynb` (Series de tiempo).

### **1. Análisis Exploratorio de Datos (EDA)**

Archivo: **`AnalisisTiendas.ipynb`**

Se estudiaron métricas clave de las cuatro tiendas y se identificaron patrones relevantes para evaluar su desempeño.

### **Hallazgos principales del EDA**

**Promedios diarios generales entre las tiendas:**

| Métrica                 | Valor Promedio |
| ----------------------- | -------------- |
| Costo de envío          | $24,875.14     |
| Calificación promedio   | 4/5            |
| Cantidad de cuotas      | 3              |
| Transacciones mensuales | 61             |

**Insights obtenidos:**

* El **precio del producto no influye en la calificación del cliente**.
* Las tiendas ajustan los **costos de envío según el valor del artículo**, por lo que este costo puede considerarse un indicador del segmento de precios.
* No existen diferencias relevantes entre el **volumen de transacciones** de cada tienda.
* Las tiendas con **mayores ventas totales** fueron:

  * **Tienda 1:** $1,151 M
  * **Tienda 2:** $1,116 M
* Las categorías con más ventas fueron **Electrónicos**, **Electrodomésticos** y **Muebles**.
* Las tiendas con mejor calificación promedio fueron:

  * **Tienda 3:** 4.05
  * **Tienda 2:** 4.02

---

## **2. Análisis de Series de Tiempo – ARIMA**

Archivo: **`ARIMA.ipynb`**

El plan inicial consistía en entrenar un modelo **ARIMA por tienda** para identificar tendencias de crecimiento.
Sin embargo, los análisis de autocorrelación (ACF) y la prueba **Ljung–Box** confirmaron lo siguiente:

> **Las series de ventas semanales presentan ruido blanco**,
> es decir, no existe estructura temporal aprovechable para predicción.

Ante esto, se aplicó un **método alternativo de evaluación**, basado en:

1. Identificación de ventas semanales mínimas y máximas (eliminando atípicos mediante análisis cuartílico).
2. Definición de un **intervalo superior e inferior** alrededor de esos valores (según el número de desviaciones estandar).
3. Conteo del porcentaje de semanas donde cada tienda cae en cada rango.
4. Comparación del desempeño general entre tiendas.

### **Conclusiones del análisis temporal**

* **Tienda 1** pasa:

  * **20.6 %** del tiempo en el **intervalo superior**,
  * **31.8 %** del tiempo en el **intervalo inferior**,
    siendo la tienda con **menos semanas en el rango más bajo**.
* Además, es la tienda con las **mayores ventas totales** entre las cuatro.

> **Conclusión final:**
> **Tienda 1** es la mejor opción de inversión, combinando un buen comportamiento semanal, menor presencia en rangos bajos y el mayor nivel de ventas acumuladas.

![Serie de tiempo Semanal](VentasTienda1.png)

---

## Dashboard en Power BI

Se desarrolló un **dashboard interactivo** que permite visualizar:

* Comparación entre las cuatro tiendas
* Ventas 
* Indicadores clave (KPIs)
* Resultados del análisis temporal

View Dash: [Click](https://mavenshowcase.com/project/54225)
---

## Estructura del Proyecto

```
Challenge_Store_ORACLE/
│
├── data/                      # Bases originales de las cuatro tiendas
│
├── data_resul/                # Bases procesadas y limpias
│
├── AnalisisTiendas.ipynb      # Análisis exploratorio (EDA)
│
├── ARIMA.ipynb                # Análisis de series de tiempo
│
└── Dashboard (Power BI)       # Archivo PBIX con conclusiones
```

---

## Tecnologías Utilizadas

* **Python**

  * pandas
  * numpy
  * seaborn
  * matplotlib
  * statsmodels (ARIMA)
* **Power BI**

  * Modelado de datos
  * Visualización
  * Dashboards ejecutivos
* **Jupyter Notebook** para análisis iterativo

---

## Autor

**Ernesto F.**

> *Analista de Datos Jr. | Trainee en Data Science
> Especializado en análisis, modelado y visualización de datos para la toma de decisiones.*
