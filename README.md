# TPE-Fundamentos-de-la-ciencia-de-datos-UNICEN-2025-Grupo20
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

## 📦 Instalación de Dependencias

Asegurate de tener Python 3.8+ instalado.  
Luego ejecutá:

```bash
pip install -r requirements.txt


### 🚀 Ver el Análisis y Ejecutar el Código
Todo el proceso de limpieza, los tests estadísticos, las visualizaciones y las conclusiones de cada hipótesis se encuentran en el Jupyter Notebook principal:

**TPE.ipynb**

Para ver el informe final consolidado, puedes consultar:

* **Informe_Grupo20.pdf**

---
