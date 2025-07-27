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

modelo de "ML"

Resultados Comparativos de Modelos
Tras evaluar múltiples algoritmos, los resultados en el conjunto de prueba fueron:

Modelo	Accuracy	Precisión (Abandono)	Recall (Abandono)	F1-Score (Abandono)	ROC AUC
Árbol de Decisión	0.720	0.476	0.535	0.504	0.661
K-Vecinos Cercanos	0.704	0.463	0.714	0.562	0.769
Regresión Logística	0.747	0.516	0.797	0.626	0.842
Selección Final del Modelo
Regresión Logística fue seleccionada como modelo óptimo debido a:

Mayor equilibrio general: Mejor puntuación F1 (0.626) para la clase minoritaria (abandono)

Alto recall (79.7%): Capacidad para identificar correctamente la mayoría de los casos de abandono real

Mejor AUC (0.842): Superior desempeño en la distinción entre clases en todos los umbrales

Interpretabilidad: Coeficientes claros para acciones de negocio


Interpretación del Modelo Final
Variables más Influyentes:
Variable	Coeficiente	Impacto en Abandono
Tipo_contrato_Month-to-month	+1.82	Alto aumento
Antigüedad_cliente	-1.45	Reducción importante
Cargos_mensuales	+1.28	Aumento significativo
Servicio_Internet_Fiber optic	+0.94	Aumento moderado
Facturación_paperless	+0.62	Aumento moderado
Método_pago_Electronic check	+0.58	Aumento moderado



nterpretación de coeficientes:

Variables positivas aumentan probabilidad de abandono

Variables negativas reducen probabilidad de abandono

Magnitud indica fuerza de relación

Validación de Supuestos
Multicolinealidad: VIF < 5 para todas las variables

Relación Lineal: Análisis de residuos confirmó linealidad

Outliers: Tratados con winsorization (1% en ambos extremos)



Análisis de Errores
El modelo tiene mejor desempeño en:

Clientes nuevos (<6 meses)

Usuarios de fibra óptica

Clientes con factura paperless

Principales limitaciones:

Dificultad para predecir abandono en clientes 6-18 meses

22% de falsos positivos en segmento premium

## ✅ Recomendaciones

- Incentivar la migración hacia **contratos anuales o semestrales**.
- Ofrecer paquetes promocionales a clientes con múltiples servicios activos.
- Identificar y contactar proactivamente a clientes de alto riesgo (contrato mensual, sin servicios extra, alta factura mensual).
- Evaluar si los clientes con cargos muy bajos están realmente activos o son candidatos a depuración.

## BRIAN BROWN 
