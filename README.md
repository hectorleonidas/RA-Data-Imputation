# RA-Data-Imputation

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Last Commit](https://img.shields.io/github/last-commit/hectorleonidas/RA-Data-Imputation)

Flujo de trabajo en Python para **analizar datos de estaciones meteorológicas**, **visualizar correlaciones** y **realizar experimentos de imputación de datos** usando conjuntos de datos de reanálisis (CFSR, CFSv2).  

El proyecto se enfoca en datos de **temperatura** y **precipitación** de estaciones en el **Norte de Chile**, generando vacíos **continuos** y **aleatorios** para evaluar el rendimiento de diferentes técnicas de imputación en conjunto con datos de reanálisis.

---

## 📌 Características

- Análisis exploratorio de datos de estaciones.
- Mapas de ubicación de estaciones.
- Cálculo de matrices de correlación por **región** y **variable**.
- Creación de vacíos de datos simulados (continuos y aleatorios).
- Imputación de datos usando reanálisis meteorológico.
- Preparación de datasets para flujos de trabajo en **KNIME**.

---

## 📂 Estructura del repositorio
``` your tree 
├── notebooks/ # Notebooks de análisis y visualización
├── Análisis exploratorio/ # Análisis de los datos trabajados
├── Mapas/ # Creación de mapas de ubicación de las estaciones
├── Matrices/ # Calculo de matrices de correlación y pruebas de normalidad para seleccionar las estaciones
├── experimento/ # Scripts para creación e imputación de vacíos y calculos de estadisticas para evaluar las técnicas de imputación
├── knime/ # Archivos para flujo de trabajo en KNIME, donde se crean los archivos .csv con las estaciones seleccionadas
└── README.md # Este archivo
```

**Nota:**  
Los notebooks contienen comentarios detallados en cada línea para facilitar su comprensión.  
Algunos archivos CSV que contienen datos pesados no están incluidos en el repositorio por limitaciones de tamaño.  
Para reproducir los análisis, es necesario obtenerlos a partir de las fuentes originales o generarlos mediante los scripts proporcionados.

---

## ⚙️ Requisitos

- **Python** 3.8+
- **Jupyter Notebook** / **JupyterLab**
- Librerías recomendadas:
  - `numpy`
  - `pandas`
  - `folium`
  - `matplotlib`
  - `seaborn`
  - `geopandas`
  - `scikit-learn`
  - `sklearn.metrics`
  - `scipy.stats`

## 🚀 Uso paso a paso

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/hectorleonidas/RA-Data-Imputation.git
   cd RA-Data-Imputation

   Ejecutar los notebooks en el siguiente orden:

2. Exploración y análisis de datos (notebooks/)
  - Cálculo de matrices de correlación
  - Generación de mapas de estaciones
  - Creación de vacíos y ejecución de imputación (experimento/)

3. (Opcional) Usar KNIME:
  - Abrir los flujos en la carpeta knime/ para reproducir la preparación de datos.

📊 Experimento de imputación
  - En experimento/ se encuentran scripts que:
  - Simulan vacíos continuos y aleatorios.
  - Rellenan vacíos usando tecnicas de imputación aprovechando los datos de reanálisis.
  - Comparan distintas técnicas de imputación.
  - Evalúan precisión del uso de datos de reanálisis como alternativa en función del tipo de vacío.\
