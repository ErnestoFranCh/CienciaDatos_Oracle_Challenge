### [1. Store Analysis – ORACLE Data Science Challenge](Store/README_ES.md)

**Folder:** `Challenge_Store_ORACLE`

**Description:**
Project developed as part of the **ORACLE Data Science Program Challenges**, focused on analyzing the performance of **four stores in Colombia** to answer the key question:

> **Which store is the best investment option?**

The analysis combined **EDA techniques**, **time series modeling**, and **executive visualization** to support the decision.

Includes:

* **Exploratory analysis in Python** (sales, transactions, ratings, shipping costs)
* Identification of relevant patterns for each store
* **Product category evaluation** and overall performance comparison
* **Time series analysis (ARIMA)** to assess trend behavior

  * The series were determined to exhibit **white noise**, so an alternative method based on weekly sales intervals was applied
* **Selection of the store with the highest investment potential**, considering sales stability and total volume
* **Interactive Power BI dashboard** presenting key indicators, comparisons, and the final conclusion

**Key Findings:**

* **Stores 1 and 2** have the **highest total sales**, with Store 1 standing out.
* No significant differences were found in transaction volume or average shipping cost among stores.
* Store 3 and Store 2 have the highest ratings (4.05 and 4.02).
* The weekly sales series show **white noise**, so the analysis focused on weekly distribution:

  * **Store 1** showed the highest performance in upper sales intervals and the lowest share in lower intervals.
* **Conclusion:** **Store 1** is the best investment option.

**Tools:** Python, pandas, numpy, seaborn, matplotlib, statsmodels (ARIMA), Power BI, Power Query, Jupyter Notebook

View Dash: [Click](https://mavenshowcase.com/project/54225)

