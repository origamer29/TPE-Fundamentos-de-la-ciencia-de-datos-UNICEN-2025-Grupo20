# TPE-Fundamentos-de-la-ciencia-de-datos-UNICEN-2025-Grupo20
## 📄 Descripción del Dataset

El dataset contiene **12.330 sesiones**, cada una perteneciente a **un usuario distinto**, registradas durante un período de **1 año**.  
Esto elimina sesgos ligados a campañas temporales, perfiles de usuario o fechas específicas.

El conjunto incluye:

### 🧮 **10 variables numéricas**
- **Administrative**, **Administrative_Duration**  
- **Informational**, **Informational_Duration**  
- **ProductRelated**, **ProductRelated_Duration**  
  > Representan cantidad y duración de visitas a distintos tipos de páginas.  
- **BounceRates**, **ExitRates**  
  > Métricas de Google Analytics por sesión.  
- **PageValues**  
  > Valor promedio de las páginas vistas antes de una compra.  
- **SpecialDay**  
  > Proximidad a un evento especial (San Valentín, Día de la Madre, etc.).

### 🔤 **8 variables categóricas**
Incluyen:
- **OperatingSystems**, **Browser**, **Region**  
- **TrafficType**  
- **VisitorType** (nuevo / recurrente)  
- **Weekend** (True/False)  
- **Month**

### 🎯 **Variable objetivo**
- **Revenue** → indica si la sesión terminó en compra (1) o no (0).

Se realizó un proceso de **limpieza, estandarización y creación de nuevas métricas**, como la **tasa de tiempo por visita (Tiempo_Total)** construida a partir de las duraciones por categoría de página.

---

## 🎓 Objetivo del Proyecto

El trabajo busca responder **6 hipótesis planteadas desde una perspectiva de negocio**, utilizando:

- Análisis exploratorio (EDA)
- Visualizaciones avanzadas (boxplots, heatmaps, scatterplots)
- Tests estadísticos:
  - Shapiro-Wilk  
  - Levene  
  - Mann-Whitney  
  - Kruskal-Wallis  
  - Chi-cuadrado  
- Modelos lineales (OLS)
- Técnicas de reducción de dimensionalidad:
  - **t-SNE**
  - **UMAP**

---

## 🧪 Hipótesis Analizadas

### **H1 — Engagement vs. Compra**
Los usuarios que realizan compras presentan una mayor **tasa de tiempo por visita (Tiempo_Total)** que quienes no compran.

### **H2 — Factores que influyen en el Engagement**
Variables como **BounceRates**, **ExitRates**, **PageValues** y **SpecialDay** influyen significativamente en la tasa de tiempo por visita.

### **H3 — Visitantes Nuevos vs. Recurrentes**
Aunque los visitantes recurrentes generan más compras en volumen, los visitantes nuevos presentan una **tasa de conversión significativamente superior**.

### **H4 — Ruido en Page Value**
El 70% de las sesiones muestran un **PageValue ≤ 1**, lo que revela navegación exploratoria sin intención de compra.

### **H5 — Tasa de Rebote vs. Contexto**
La **tasa de rebote (BounceRate)** varía significativamente según la **región**, el **mes** y si la visita ocurre **en fin de semana**.

### **H6 — Tecnología vs. Tasa de Abandono**
El **Browser**, el **Operating System** y el **Tipo de Tráfico** influyen de manera significativa en la **ExitRate**.

---

## 🚀 Instalación y Ejecución

