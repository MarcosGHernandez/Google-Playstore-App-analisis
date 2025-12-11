# Análisis de apps google playstore


![Pandas](https://img.shields.io/badge/Data-Cleaning-green)
![Status](https://img.shields.io/badge/Status-Finalizado-success)

## Descripción del trabajo 
Este repositorio documenta el flujo de trabajo completo ("End-to-End") para el análisis de datos del proyecto **[Análisis de apps google playstore]**. El objetivo principal es transformar datos brutos en información estratégica, pasando por un proceso de limpieza en Python hasta la generación de gráficos para la presentación ejecutiva.

---

## Metodología de Limpieza (Data Cleaning)
Antes de cualquier análisis, los datos crudos (*raw data*) fueron procesados utilizando **Python (Pandas)** para asegurar su calidad.

**Decisiones y Criterios aplicados:**

1.  **Manejo de Valores Nulos (Missing Values):**
    * *Numéricos:* Se realizó imputación por la **media/mediana** para preservar la distribución estadística sin perder registros.
    * *Categóricos:* Se etiquetaron como `"Sin Información"` para mantener la trazabilidad de los datos faltantes.

2.  **Eliminación de Duplicados:**
    * Se eliminaron registros redundantes basándose en identificadores únicos para evitar el conteo doble de transacciones y de apps duplicadas.

3.  **Normalización de Formatos:**
    * **Fechas:** Conversión estándar a objetos `datetime`.
    * **Texto:** Limpieza de strings (eliminación de espacios, unificación de mayúsculas/minúsculas) para corregir inconsistencias en categorías (ej. "MX", "Mx", "mx").

4.  **Tratamiento de Outliers:**
    * Se filtraron los valores extremos que superaban el rango intercuartílico habitual para evitar distorsiones en los promedios presentados.

---

## Estrategia de Visualización
Los gráficos generados no son aleatorios; fueron seleccionados para responder preguntas de negocio específicas en la presentación final:

* **Tendencias (Line Charts):** Para visualizar la evolución temporal y detectar estacionalidades.
* **Comparativas (Bar Charts):** Para rankear el desempeño entre categorías o regiones de forma clara.
* **Distribución (Histograms/Boxplots):** Utilizados internamente para entender la dispersión de los datos y validar la limpieza.

---
