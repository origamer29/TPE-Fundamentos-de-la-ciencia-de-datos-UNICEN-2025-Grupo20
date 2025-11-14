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

## ⚙️ Instalación y Ejecución del Proyecto

Para que puedas jugar con nuestro notebook y descubrir todos los secretos del dataset, te dejamos dos caminos:  
👉 **usar Jupyter Notebook en tu compu** o 👉 **abrirlo directamente en Google Colab**.  
---

### 💻 Opción A: Ejecutar en Jupyter Notebook (local)

1. 🐍 **Instalar Python (3.9 o superior)**  
   Asegurate de tener Python instalado.  

2. 📥 **Clonar el repo**  
   ```bash
   git clone https://github.com/TPE-Fundamentos-de-la-ciencia-de-datos-UNICEN-2025-Grupo20/TPE-Fundamentos-de-la-ciencia-de-datos-UNICEN-2025-Grupo20.git
   cd TPE-Fundamentos-de-la-ciencia-de-datos-UNICEN-2025-Grupo20
   ```

3. 🎭 **Crear un entorno virtual**  
   ```bash
   python -m venv .venv
   ```
   - En macOS/Linux:  
     ```bash
     source .venv/bin/activate
     ```
   - En Windows:  
     ```bash
     .venv\Scripts\activate
     ```

4. 📦 **Instalar dependencias**  
   Si existe `requirements.txt`:  
   ```bash
   pip install -r requirements.txt
   ```
   Si no, instalá Jupyter y los paquetes básicos:  
   ```bash
   pip install jupyter numpy pandas matplotlib scikit-learn
   ```

5. 🧑‍💻 **Abrir Jupyter Notebook**  
   ```bash
   jupyter notebook
   ```
   - Se abrirá en tu navegador 🌐.  
   - Buscá el archivo `TPE.ipynb` y abrilo.  
   - Ejecutá las celdas con **Shift+Enter**.  

---

## 🧰 Extra: Ejecutar el notebook desde VSCode

1. 🧩 **Instalar extensiones**  
   - **Python** (Microsoft)  
   - **Jupyter** (Microsoft)

2. 🐍 **Seleccionar intérprete**  
   - Abrí VSCode en la carpeta del repo.  
   - Presioná `Ctrl+Shift+P` → “Python: Select Interpreter” → elegí tu entorno virtual `.venv`.

3. 📒 **Abrir el `.ipynb`**  
   - Hacé doble clic en `TPE.ipynb` desde el explorador.  
   - En la esquina superior derecha, **seleccioná el kernel** del entorno virtual (ej.: “Python (.venv)”).

4. ▶️ **Ejecutar celdas**  
   - Usá el botón “Run” o `Shift+Enter`.  
   - Si faltan paquetes, instalalos en el terminal integrado:
     ```bash
     pip install -r requirements.txt
     ```
   - Si el notebook usa rutas relativas, asegurate de abrir VSCode desde la **raíz del repo**.

5. 🎯 **Tip útil**  
   - Si el kernel no aparece, instalá el soporte:
     ```bash
     pip install ipykernel
     python -m ipykernel install --user --name=grupo20-kernel --display-name "Python (Grupo20)"
     ```

---

### ☁️ Opción B: Ejecutar en Google Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/TPE-Fundamentos-de-la-ciencia-de-datos-UNICEN-2025-Grupo20/blob/main/TPE.ipynb)
1. 🌐 **Abrir Colab** → [Google Colab](https://colab.research.google.com)  

2. 🔗 **Cargar el notebook desde GitHub**  
   - Pega la URL del repo o del `TPE.ipynb`.  
   - Seleccioná el archivo y abrilo.  

3. 📦 **Instalar dependencias dentro del notebook**  
   - Si hay `requirements.txt`:  
     ```python
     !pip install -r https://raw.githubusercontent.com/TPE-Fundamentos-de-la-ciencia-de-datos-UNICEN-2025-Grupo20/TPE-Fundamentos-de-la-ciencia-de-datos-UNICEN-2025-Grupo20/main/requirements.txt
     ```
   - O instalá manualmente:  
     ```python
     !pip install numpy pandas matplotlib scikit-learn
     ```

4. 📂 **Clonar el repo para acceder a datos**  
   ```python
   !git clone https://github.com/TPE-Fundamentos-de-la-ciencia-de-datos-UNICEN-2025-Grupo20/TPE-Fundamentos-de-la-ciencia-de-datos-UNICEN-2025-Grupo20.git
   %cd TPE-Fundamentos-de-la-ciencia-de-datos-UNICEN-2025-Grupo20
   ```

5. ▶️ **Ejecutar las celdas**  
   Usá **Shift+Enter** y disfrutá de los resultados 🎉.  

---

### 🛠️ Tips y Problemas Comunes

- ❌ **FileNotFoundError** → asegurate de estar en la carpeta correcta (`%cd TPE-Fundamentos-de-la-ciencia-de-datos-UNICEN-2025-Grupo20` en Colab).  
- 🔄 **Kernel incorrecto en Jupyter** → seleccioná el kernel del entorno virtual creado.  
- 📦 **Paquetes faltantes** → instalalos con `pip install paquete`.  
- 🧩 **Versiones incompatibles** → revisá `requirements.txt` y ajustá con `pip install paquete==x.y.z`.  

---

### 🎨 Recomendación de estructura del notebook

Para mantener el flujo claro y reproducible, sugerimos organizar el notebook en las siguientes secciones:

- 🔧 **Setup inicial**  
  Importaciones de librerías, instalación de dependencias y configuración del entorno.

- 📊 **Carga de datos**  
  Lectura del dataset (`online_shoppers_intention.csv`), verificación de rutas y primeras inspecciones.

- 🧮 **Procesamiento / Limpieza**  
  - Tratamiento de valores faltantes.  
  - Estandarización de variables.  
  - Creación de métricas derivadas (ej.: `Tiempo_Total`).  

- 📈 **Análisis exploratorio (EDA)**  
  Visualizaciones (boxplots, heatmaps, scatterplots) y estadísticas descriptivas.

- 🧪 **Tests estadísticos**  
  Aplicación de pruebas como Shapiro-Wilk, Levene, Mann-Whitney, Kruskal-Wallis y Chi-cuadrado.

- 📐 **Modelado**  
  Modelos lineales (OLS) y técnicas de reducción de dimensionalidad (t-SNE, UMAP).

- 🎯 **Conclusiones**  
  Resumen de hallazgos respecto a las hipótesis planteadas.

- 💾 **Exportación de resultados**  
  Guardado de gráficos, tablas o métricas en la carpeta `outputs/` (si se utiliza).

