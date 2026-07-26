# Regresión Lineal Simple OLS: League of Legends (LoL) 🎮📈

## 📌 Descripción del Proyecto
Implementación del flujo completo de un modelo de Regresión Lineal Simple mediante **Mínimos Cuadrados Ordinarios (OLS)** utilizando un dataset de League of Legends. El objetivo principal es seleccionar dos variables cuantitativas continuas, modelar su relación predictiva, interpretar las métricas de ajuste y evaluar las limitaciones prácticas del modelo.

---

## 🛠️ Flujo de Trabajo (Pipeline)
1. **Carga y Exploración:** Lectura de `df_sub_lol.xlsx` y visualización inicial con Pandas.
2. **Selección de Variables:** Definición fundamentada de la variable independiente ($X$) y dependiente ($y$).
3. **Análisis de Dispersión y Correlación:** Generación de gráficos con *Seaborn/Matplotlib* y cálculo del coeficiente de correlación de Pearson.
4. **Modelamiento OLS:** Construcción del modelo de regresión lineal, ajuste con `.fit()` y extracción de pendiente ($b_1$) e intercepto ($b_0$).
5. **Visualización de la Recta:** Gráfico de la nube de puntos con la recta de regresión superpuesta y la ecuación $y = b_0 + b_1 x$.
6. **Métricas de Evaluación:** Cálculo de $MSE$, $RMSE$, $MAE$ y $R^2$.
7. **Interpretación y Discusión:** Análisis crítico de los resultados, capacidad predictiva del modelo y sus limitaciones prácticas en el contexto del juego.

---

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** Python 3.x
* **Entorno:** Jupyter Notebook / Google Colab
* **Librerías principales:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn / Statsmodels
