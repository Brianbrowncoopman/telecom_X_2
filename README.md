# 📊 Informe del Proyecto: Análisis de Clientes – Telecom_X_2

## 📁 Repositorio
[GitHub - Telecom_X_2](https://github.com/Brianbrowncoopman/telecom_X_2)

## 🧩 Descripción General

Este proyecto forma parte del desafío **Telecom_X_2** propuesto por Alura. El objetivo principal es analizar los datos de clientes de una empresa de telecomunicaciones para identificar patrones relevantes relacionados con la evasión (churn), el comportamiento de los usuarios, servicios contratados y sus características sociodemográficas.

---

## 🔍 Fuentes de Datos

Se trabajó inicialmente con tres datasets:

- `df_limpio.csv`
- `df_limpio_1.csv`
- `df_limpio_2.csv`

Tras revisión de estructura y contenido, se optó por utilizar **`df_limpio.csv`** como dataset principal, ya que contiene toda la información relevante consolidada.

---

## 🧼 Limpieza y Preparación de los Datos

- Eliminación de valores nulos o inconsistencias.
- Conversión de variables categóricas a formatos adecuados (`object`, `bool`, `int`, etc.).
- Exploración inicial con métodos como `.head()`, `.info()`, `.shape()`, `.describe()`.
- Verificación de duplicados y coherencia interna.

---

## 📈 Análisis Exploratorio (EDA)

A través del uso de **Pandas, Matplotlib y Seaborn**, se realizaron visualizaciones y estadísticas descriptivas para obtener información relevante:

### 🔹 Distribución de Clientes

- Predominio de clientes con servicio de **Internet Fibra**.
- Mayor proporción de clientes con múltiples servicios contratados (telefonía, streaming, soporte técnico).

### 🔹 Churn (Evasión de Clientes)

- Alta correlación entre **servicio de fibra óptica** y **probabilidad de evasión**.
- Clientes con contratos **mensuales** tienen mayor tendencia a cancelar el servicio.
- Usuarios con múltiples cargos adicionales (servicios complementarios) presentan mayores tasas de churn.

### 🔹 Facturación

- Clientes que abandonan el servicio tienen, en promedio, una **facturación mensual más alta**.
- Se detectaron segmentos con cargos muy bajos que podrían corresponder a clientes inactivos o con subsidios/promociones.

### 🔹 Servicios Adicionales

- El servicio de **soporte técnico en línea**, **streaming de películas** y **protección de dispositivos** parecen influir en la permanencia de los clientes.

---

## 🔧 Herramientas Utilizadas

- Python (Colab)
- Bibliotecas: `pandas`, `numpy`, `matplotlib`, `seaborn`

---

## 📌 Insights Relevantes

- 💡 **Los contratos mensuales representan el mayor riesgo de pérdida de clientes.**
- 💡 **El churn se asocia con mayores montos de facturación mensual.**
- 💡 **Los servicios de valor agregado (streaming, soporte técnico) tienen impacto positivo en la retención.**
- 💡 **Clientes con método de pago por débito automático tienden a permanecer más tiempo.**

---

## ✅ Recomendaciones

- Incentivar la migración hacia **contratos anuales o semestrales**.
- Ofrecer paquetes promocionales a clientes con múltiples servicios activos.
- Identificar y contactar proactivamente a clientes de alto riesgo (contrato mensual, sin servicios extra, alta factura mensual).
- Evaluar si los clientes con cargos muy bajos están realmente activos o son candidatos a depuración.


