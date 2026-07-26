# Análisis y Visualización de Sismicidad en Chile 🌋📊

## 📌 Descripción del Proyecto
Este proyecto consiste en el procesamiento, limpieza y análisis visual de datos telúricos ocurridos en Chile. El flujo de trabajo abarca desde la preparación del dataset (*Data Preparation*) utilizando Python/Pandas hasta la creación de un Dashboard interactivo de varias páginas en **Looker Studio** para la toma de decisiones y el análisis espacial/temporal de sismos.

---

## 🔗 Dashboard Interactivo
Puedes acceder y explorar el dashboard interactivo de Looker Studio directamente a través del siguiente enlace:

👉 **[Ver Dashboard de Sismicidad en Chile](https://datastudio.google.com/reporting/98fb92eb-f13b-4e75-a63c-971a2acbe96a)**

---

## 🛠️ Flujo de Trabajo (Pipeline)

### 1. Preparación y Limpieza del Dataset (Python / Pandas)
* **Filtrado Geográfico:** Selección exclusiva de registros sísmicos ocurridos dentro del territorio chileno (`place` conteniendo la palabra "Chile").
* **Depuración de Variables:** Eliminación de campos irrelevantes (`Nst`).
* **Tratamiento de Nulos:** Imputación por mediana para variables numéricas y moda para variables categóricas.
* **Conservación de Outliers:** Se mantuvieron los valores atípicos sin eliminar para preservar la distribución real de los fenómenos sísmicos.
* **Transformación Geográfica:** Generación del campo concantenado `LATLON` (`latitude,longitude`) para habilitar la geolocalización precisa en Looker Studio.
* **Exportación:** Generación del archivo procesado en formato Excel (`.xlsx`).

### 2. Dashboard Interactivo (Looker Studio)
El dashboard se estructuró en varias páginas de análisis:

* **Página 1-3 (Base):** Visualización general de variables sísmicas, evolución temporal y campos calculados con condicionales `CASE` para clasificar la magnitud (*Muy Leve, Leve, Moderado, Fuerte, Muy Fuerte*).
* **Página 4 (Análisis por Profundidad):** Clasificación técnica de sismos (*Superficial: 0-50km, Intermedio: 50-150km, Profundo: >150km*) vinculando gráficos de barras, tablas detalladas y un mapa de burbujas interactivo con filtros cruzados.
* **Página 5 (Aplicación a la Toma de Decisiones):** Vista analítica a libre elección orientada a identificar patrones espaciales y de severidad para la gestión del riesgo sísmico.
* `sismicidad_chile_procesado.xlsx`: Dataset limpio y transformado listo para análisis.
* `limpieza_sismicidad.ipynb`: Script/Notebook utilizado para la preparación de los datos en Python.
* `README.md`: Documentación del proyecto.
