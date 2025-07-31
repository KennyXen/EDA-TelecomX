# 📊 Informe Final de Análisis de Evasión de Clientes (Churn)

---

## 1️⃣ Introducción

El presente informe tiene como objetivo **analizar el comportamiento de los clientes** de un servicio de telecomunicaciones, con el propósito de **identificar patrones de evasión** (Churn) y proponer estrategias para **reducir la pérdida de clientes**.

- **Problema**: La empresa presenta una tasa de evasión significativa, lo que impacta en sus ingresos recurrentes.  
- **Objetivo del análisis**:  
  1. Detectar patrones de comportamiento asociados a la cancelación del servicio.  
  2. Proporcionar información para diseñar estrategias de **retención de clientes**.  

---

## 2️⃣ Limpieza y Tratamiento de Datos

Se realizó un proceso completo de **ETL (Extracción, Transformación y Carga)**, que incluyó:

1. **Extracción** de los datos desde la API y conversión a DataFrame.
2. **Transformación**:
   - Aplanamiento de datos anidados en JSON.
   - Conversión de variables numéricas (`Charges_Monthly` y `Charges_Total`) a formato float.
   - Normalización de valores categóricos (`Yes/No`, `No internet service`, `Unknown`).
   - Creación de la columna **`Cuentas_Diarias`** para obtener el costo diario promedio.
   - Eliminación de **duplicados** y estandarización de nombres de columnas.
3. **Carga**: Los datos se encuentran listos para análisis, con dimensiones finales: **7267 registros y 22 columnas**.

**Resumen de la limpieza**:
- **Valores nulos**: 0  
- **Duplicados**: 0  
- **Variables numéricas finales**: `charges_monthly`, `charges_total`, `tenure`  
- **Variable objetivo**: `churn` (No / Yes / Unknown)

---

## 3️⃣ Análisis Exploratorio de Datos (EDA)

### 🔹 3.1 Distribución General de Churn

- Total clientes: **7267**
- Distribución:

| Churn    | Conteo | Proporción |
|---------|--------|-----------|
| No      | 5174   | 71.2% |
| Yes     | 1869   | 25.7% |
| Unknown | 224    | 3.1% |

**Insight**: Aproximadamente **1 de cada 4 clientes abandona el servicio**.

---

### 🔹 3.2 Distribución de Churn por Variables Categóricas

Se analizaron variables como **género, tipo de contrato, método de pago, dependientes y servicios contratados**.

**Hallazgos principales**:

- **Tipo de contrato**:  
  - Los clientes **"Month-to-month"** representan el 55% del total y concentran la **mayor evasión (1655 de 1869)**.
- **Internet Service**:  
  - **Fiber optic** concentra la mayor evasión (69% de los que cancelan).  
- **Método de pago**:  
  - **Electronic check** tiene la tasa de evasión más alta (44%).  
- **Dependientes**:  
  - Clientes **sin dependientes** muestran mayor propensión al churn (82%).

---

### 🔹 3.3 Distribución de Churn por Variables Numéricas

| Variable           | No (mean) | Yes (mean) | Insight |
|--------------------|----------|-----------|--------|
| Charges_Monthly    | 61.27    | 74.44     | Clientes que abandonan pagan más por mes. |
| Charges_Total      | 2555.34  | 1531.80   | Clientes que abandonan acumulan menos gasto total (tenencia corta). |
| Tenure (meses)     | 37.57    | 17.98     | Clientes nuevos son más propensos a abandonar. |

**Insight**:  
El **perfil de cliente propenso a la evasión** tiene:
- Contrato **mensual**,  
- Pago por **cheque electrónico**,  
- **Menor tiempo de permanencia (≈18 meses)**,  
- **Gasto mensual alto pero total bajo**.

---

## 4️⃣ Conclusiones e Insights

1. **Churn elevado (≈26%)** impacta ingresos recurrentes.  
2. La **mayor evasión ocurre en clientes con contratos mensuales**, que pagan más por mes pero llevan menos tiempo en la compañía.  
3. Los **clientes sin dependientes** y con **Internet Fiber Optic** muestran más cancelaciones.  
4. Los **métodos de pago electrónicos** (cheque electrónico) están asociados con mayor churn.  

---

## 5️⃣ Recomendaciones Estratégicas

1. **Incentivar contratos a largo plazo** (anual o bianual) con descuentos.  
2. **Programas de fidelización temprana** para clientes nuevos (primeros 12-18 meses).  
3. **Campañas segmentadas** a usuarios de **cheque electrónico**, promoviendo pagos automáticos.  
4. **Bonificaciones a clientes sin dependientes**, quienes muestran mayor propensión a cancelar.  
5. **Monitoreo proactivo** de clientes con **alto gasto mensual pero corta tenencia**.

---

✅ Con este análisis, la empresa puede **focalizar sus esfuerzos de retención** en los perfiles de mayor riesgo, reduciendo la evasión y mejorando la estabilidad financiera.
