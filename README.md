# 📊 Telecom X - Análisis de Evasión de Clientes (Churn)

Este proyecto realiza un **análisis completo de la evasión de clientes (Churn)** en una empresa de telecomunicaciones ficticia llamada **Telecom X**, utilizando un flujo de trabajo de **ETL (Extracción, Transformación y Carga)** y un **Análisis Exploratorio de Datos (EDA)** con visualizaciones.

El objetivo es **identificar patrones de cancelación de clientes** para proponer estrategias que reduzcan la pérdida de usuarios.

---

## 🚀 Características del Proyecto

- **ETL completo**:
  - Extracción de datos desde **API / JSON estructurado**.
  - Transformación: limpieza, normalización y estandarización de datos.
  - Carga final para análisis y visualización.

- **Análisis Exploratorio de Datos (EDA)**:
  - Estadísticas descriptivas (media, mediana, desviación estándar).
  - Distribución de **churn** global y por variables categóricas.
  - Análisis de variables numéricas (`charges_monthly`, `charges_total`, `tenure`).
  - **Visualizaciones** con `Matplotlib` y `Seaborn`.

- **Tablas Resumen**:
  - Conteos y proporciones de churn por cada variable relevante.
  - Métricas estadísticas por grupo de churn para análisis comparativo.

- **Informe Final Integrado**:
  - Introducción y objetivos.
  - Limpieza y tratamiento de datos.
  - Visualizaciones de distribución de churn.
  - Conclusiones e **insights accionables**.
  - **Recomendaciones estratégicas** para reducir la evasión.

---

## 📊 Tecnologías Utilizadas

- **Python 3.x**
- **Pandas** – Limpieza y manipulación de datos.
- **NumPy** – Operaciones numéricas.
- **Matplotlib & Seaborn** – Visualización de datos.
- **Jupyter Notebook / Google Colab** – Análisis interactivo.
- **Markdown** – Documentación e informes.

---

## 📈 Ejemplos de Análisis

Algunos de los gráficos generados:

1. **Distribución global de churn**  
2. **Churn por tipo de contrato, método de pago y género**  
3. **Boxplots de `charges_total` y `tenure` por churn**  
4. **Tablas resumen con proporciones de cancelación**  

---

## 📝 Conclusiones del Proyecto

- El **26% de los clientes** abandonan el servicio.  
- La mayor evasión ocurre en clientes con:  
  - **Contratos mensuales**  
  - **Pago por cheque electrónico**  
  - **Menor antigüedad (<18 meses)**  
- Clientes **sin dependientes y con Internet Fiber Optic** muestran mayor propensión a cancelar.

**Recomendaciones Estratégicas**:
1. Incentivar **contratos anuales/bianuales** con descuentos.
2. Programas de **fidelización temprana** para clientes nuevos.
3. Promover **pagos automáticos** en lugar de cheques electrónicos.
4. Bonificaciones y seguimiento a clientes de **alto riesgo** según perfil identificado.

---




