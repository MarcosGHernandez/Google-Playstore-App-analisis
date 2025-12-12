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
    * *Categóricos:* Se etiquetaron como `Nan` para mantener la trazabilidad de los datos faltantes.

2.  **Eliminación de Duplicados:**
    * Se eliminaron registros redundantes basándose en identificadores únicos para evitar el conteo doble de transacciones y de apps duplicadas.

3.  **Normalización de Formatos:**
    * **Fechas:** Conversión estándar a objetos `datetime`.
    * **Texto:** Limpieza de strings (eliminación de espacios, unificación de mayúsculas/minúsculas) para corregir inconsistencias en categorías (ej. "MX", "Mx", "mx").

---

## Estrategia de Visualización
Los gráficos generados no son aleatorios; fueron seleccionados para responder preguntas de negocio específicas en la presentación final:


* **Comparativas (Bar Charts):** Para rankear el desempeño entre categorías o regiones de forma clara.


---
Resultados del Análisis 

A partir de la limpieza y exploración de los datos (*Data Cleaning & EDA*), se han respondido las preguntas clave de negocio:

### 1. Top Categorías por Volumen
**Pregunta:** ¿Cuáles son las 3 categorías de Apps con mayor volumen de descargas promedio?
**Respuesta:**
Basado en el análisis de descargas promedio por categoría, el mercado está dominado por la comunicación y el consumo de contenido:
1.  **COMMUNICATION:** Lidera el ranking (aprox. 66 Millones/app), impulsada por mensajería instantánea y navegadores.
2.  **SOCIAL:** En segundo lugar (aprox. 45 Millones/app), reflejando la masividad de las redes sociales.
3.  **VIDEO PLAYERS:** En tercer lugar (aprox. 36 Millones/app).

### 2. Calidad vs. Precio
**Pregunta:** ¿Las Apps de pago (Paid) tienen, en promedio, mejor calificación (Rating) que las gratuitas (Free)?
**Respuesta:** **SÍ.**
El análisis comparativo revela que las aplicaciones de pago tienen una calificación promedio superior (**4.3**) frente a las gratuitas (**4.2**). Aunque la diferencia parece pequeña numéricamente, indica que los usuarios que pagan tienden a percibir mayor calidad o valor en el producto final (menos anuncios, mejores funcionalidades).

### 3. Oportunidad de Mercado (Usuarios Insatisfechos)
**Pregunta:** ¿Cuál es la categoría con el promedio de calificación (Rating) más BAJO?
**Respuesta:**
La categoría **DATING** (Citas) presenta uno de los promedios más bajos del dataset (**~4.04**).
* **Insight:** Esto representa una clara **oportunidad de mercado**. La baja calificación sugiere que los usuarios actuales están insatisfechos con la oferta existente (probablemente por algoritmos deficientes, perfiles falsos o monetización agresiva). Lanzar una App de citas que resuelva estos dolores de usuario tendría una alta probabilidad de éxito competitivo.

### 4. Dato Curioso (Bonus)
**Pregunta:** ¿Cuál es la aplicación más cara del dataset?
**Respuesta:**
Se identificó la aplicación **"I'm Rich - Trump Edition"** con un precio de **$400.00 USD**.
Este es un *outlier* extremo que funciona más como un símbolo de estatus que como una herramienta funcional, pero valida que el sistema permite precios libres sin tope estándar.

---
### 5. Evidencia Visual
Estas conclusiones están respaldadas por el Dashboard interactivo generado, donde se incluyen:
* Gráfico de Barras horizontales para el **Top de Descargas**.
* Gráfico de Barras agrupadas para la comparativa **Free vs Paid**.
* Gráfico de Barras ordenado para visualizar el rating de **Dating** vs otras categorías.
---
## Conclusiones y Hallazgos Clave

### 1. ¿Qué categorías dominan el mercado en volumen?
**Hallazgo:** Las categorías **"Communication"** y **"Social"** son los líderes indiscutibles en términos de descargas (superando los 60 millones de instalaciones promedio).
* **Interpretación:** El mercado masivo se concentra en la conectividad interpersonal. Sin embargo, la saturación en estas categorías es alta, lo que implica una barrera de entrada elevada para nuevos competidores.

### 2. ¿Existe una relación entre el precio y la satisfacción del usuario?
**Hallazgo:** Sí. Aunque las aplicaciones **Gratuitas** acumulan la inmensa mayoría del tráfico (más de 75 mil millones de descargas totales vs. 57 millones en apps de pago), las aplicaciones de **Pago** obtienen un promedio de calificación superior (**4.3** vs 4.2).
* **Interpretación:** Los usuarios que pagan por una aplicación tienden a ser más exigentes pero también recompensan la calidad y la ausencia de publicidad con mejores puntuaciones. La existencia de valores atípicos como la app *"I'm Rich"* ($400 USD) confirma la existencia de nichos *premium* dispuestos a pagar precios elevados.

### 3. ¿Qué categorías generan mayor compromiso (Fidelidad)?
**Hallazgo:** Mediante el cálculo del *Índice de Fidelidad* (Reviews / Installs), identificamos que categorías como **COMICS**, **SOCIAL** y **GAMES** poseen las tasas más altas de interacción.
* **Interpretación:** Los usuarios de estas categorías no son pasivos; forman comunidades vocales. A diferencia de las aplicaciones utilitarias (que se usan y se olvidan), estas categorías generan un vínculo emocional que motiva al usuario a dejar reseñas.

### 4. ¿Dónde están las oportunidades de mercado no saturadas?
**Hallazgo:** Al analizar las calificaciones promedio por categoría, detectamos nichos de excelencia en **"Travel & Local"**, **"Video Players"** y **"Tools"**, los cuales mantienen ratings promedio superiores a **4.04**.
* **Recomendación Estratégica:** Estas categorías representan la "Oportunidad de Mercado". A diferencia de la categoría "Social" (altamente competitiva), estos segmentos muestran usuarios satisfechos y demandantes de herramientas de calidad, representando un terreno fértil para el desarrollo de nuevas aplicaciones con menor competencia directa.

---

### Resumen Ejecutivo
El análisis sugiere que, si bien el volumen está en lo "Gratuito y Social", la rentabilidad y la satisfacción del usuario se maximizan en modelos de nicho especializados (Herramientas/Viajes) o modelos de pago que garanticen calidad. La estrategia recomendada es priorizar la fidelización (Engagement) sobre la adquisición masiva de descargas.
