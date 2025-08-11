# RA-Data-Imputation

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Last Commit](https://img.shields.io/github/last-commit/hectorleonidas/RA-Data-Imputation)

Flujo de trabajo en Python para **analizar datos de estaciones meteorológicas**, **visualizar correlaciones** y **realizar experimentos de imputación de datos** usando conjuntos de datos de reanálisis (CFSR, CFSv2).  

El proyecto se enfoca en datos de **temperatura** y **precipitación** de estaciones en el **Norte de Chile**, generando vacíos **continuos** y **aleatorios** para evaluar el rendimiento de diferentes técnicas de imputación.

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
├── Analisis exploratorio/ # Notebooks de análisis de datos y visualización
├── Mapas/ # Generamiento de mapas para visualizar cantidad y distancia entre estaciones
├── Matrices/ # Análisis de correlación de spearman y pruebas de normalidad para la selección de estaciones
├── Experimento/ # Scripts para creación, imputación de vacíos y generamiento de gráficos
├── KNIME/ # Archivos para flujo de trabajo en KNIME, donde se realizó la creación de archivos .csv con las estaciones seleccionadas para el experimento
└── README.md # Este archivo


> **Nota:** Los notebooks contienen comentarios detallados en cada línea para facilitar su comprensión.

---

> > **Nota:**  
> Algunos archivos CSV que contienen datos pesados no están incluidos en el repositorio por limitaciones de tamaño.  
> Para reproducir los análisis, es necesario obtenerlos a partir de las fuentes originales o generar los datos mediante los scripts proporcionados.

## 🖼️ Ejemplos de salidas

### Mapa de estaciones
![Mapa de estaciones](results/ejemplo_mapa_estaciones.png)

### Matriz de correlación
![Matriz de correlación](results/ejemplo_matriz_correlacion.png)

*(Las imágenes anteriores son ejemplos generados por los notebooks del proyecto.)*

---

## ⚙️ Requisitos

- **Python** 3.8+
- **Jupyter Notebook** / **JupyterLab**
- Librerías recomendadas:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `geopandas`
  - `scikit-learn`
  - `xarray`
  - `netCDF4`

## 🚀 Uso paso a paso

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/hectorleonidas/RA-Data-Imputation.git
   cd RA-Data-Imputation

   Ejecutar los notebooks en el siguiente orden:

2. Exploración y análisis de datos (notebooks/)
    Cálculo de matrices de correlación
    Generación de mapas de estaciones
    Creación de vacíos y ejecución de imputación (experimento/)

3. (Opcional) Usar KNIME:
    Abrir los flujos en la carpeta knime/ para reproducir la preparación de datos.

📊 Experimento de imputación
En experimento/ se encuentran scripts que:
Simulan vacíos continuos y aleatorios.
Rellenan vacíos usando tecnicas de imputación aprovechando los datos de reanálisis.
Comparan distintas técnicas de imputación.
Evalúan precisión del uso de datos de reanálisis como alternativa en función del tipo de vacío.\
