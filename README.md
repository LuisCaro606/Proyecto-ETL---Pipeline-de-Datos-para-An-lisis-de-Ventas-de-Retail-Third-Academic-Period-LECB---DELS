# Proyecto-ETL---Pipeline-de-Datos-para-An-lisis-de-Ventas-de-Retail-Third-Academic-Period-LECB---DELS
Proyecto ETL - Pipeline de Datos para Análisis de Ventas de Retail (Third Academic Period) Luis Ernesto Caro Barrera- Daniel Esteban Lopez Suarez


# 🧠 Proyecto ETL de Ventas — Google Colab

Este proyecto implementa un **proceso ETL completo (Extracción, Transformación, Carga y Análisis)** sobre un conjunto de datos de ventas, productos y tiendas.  
Está desarrollado 100% en **Python** utilizando **Google Colab** y librerías como `pandas` y `matplotlib`.

---

## 🚀 Objetivo del Proyecto

El objetivo es construir un flujo de análisis de datos reproducible que:
1. Extraiga datos desde múltiples archivos CSV.
2. Limpie y transforme los datos para generar métricas de negocio.
3. Cargue resultados estructurados en un Data Mart.
4. Realice análisis visual y genere un reporte ejecutivo automático.

---

## 🧩 Estructura del Proyecto

etl-ventas-colab/
│
├── data/
│ ├── ventas_crudas.csv

│ ├── productos.csv

│ ├── tiendas.csv

│
├── output/
│ ├── ventas_transformadas.csv

│ ├── datamart_fact_ventas.csv

│ ├── datamart_dim_producto.csv

│ ├── datamart_dim_tienda.csv

│ ├── datamart_dim_tiempo.csv

│ ├── resumen_ejecutivo.csv

│ ├── reporte_ejecutivo.txt

│ ├── grafico_ventas_por_ciudad.png

│ ├── grafico_ventas_por_categoria.png

│ ├── grafico_transacciones_por_dia.png

│ └── histograma_venta_total.png

│
├── notebook/

│ └── ETL_Ventas.ipynb
│
└── README.md

yaml


---

## ⚙️ Requerimientos

Para ejecutar el proyecto necesitas:
- Python 3.10 o superior  
- Google Colab (o Jupyter Notebook local)
- Librerías:
  ```bash
  pip install pandas matplotlib
📊 Fases del Proceso ETL
🔹 Fase 1: Extracción (E)
Carga los tres archivos CSV (ventas_crudas, productos, tiendas).

Verifica que los archivos existan y estén correctamente formateados.

Muestra estadísticas básicas de los registros cargados.

🔹 Fase 2: Transformación (T)
Corrige formatos de fecha inconsistentes.

Rellena valores nulos (cliente_id → “CLIENTE_DESCONOCIDO”).

Elimina duplicados de ID.

Calcula la métrica venta_total = cantidad × precio_unitario.

Crea una categoría de venta (Baja, Media, Alta).

Une información de productos y tiendas.

Agrega dimensiones temporales (año, mes, día_semana).

Controla la calidad de los datos (rango de valores, integridad referencial).

🔹 Fase 3: Carga (L)
Guarda el dataset transformado final (ventas_transformadas.csv).

Crea un Data Mart con dimensiones (producto, tienda, tiempo).

Genera un resumen ejecutivo con métricas agregadas (resumen_ejecutivo.csv).

🔹 Fase 4: Análisis y Reportes (A)
Genera gráficos automáticos:

Ventas totales por ciudad (barras)

Distribución por categoría (pie)

Transacciones por día de la semana (barras)

Distribución de montos de venta (histograma)

Crea un reporte ejecutivo en texto plano con:

Métricas de negocio

Top performers

Indicadores de calidad de datos

▶️ Cómo Ejecutarlo en Google Colab
Abre el notebook desde Google Colab:

Archivo → Subir notebook

Sube ETL_Ventas.ipynb

En el panel izquierdo, sube los CSV dentro de la carpeta data/:

ventas_crudas.csv

productos.csv

tiendas.csv

Ajusta las rutas en el notebook si es necesario:

python
Copiar código
ventas_csv_path = "data/ventas_crudas.csv"
productos_csv_path = "data/productos.csv"
tiendas_csv_path = "data/tiendas.csv"
Ejecuta todas las celdas secuencialmente (Fase 1 → Fase 4).

Descarga tus resultados desde la carpeta output/.

🧾 Resultados Principales
Reporte ejecutivo: reporte_ejecutivo.txt

Resumen CSV: resumen_ejecutivo.csv

Visualizaciones: archivos .png con los gráficos principales

Data Mart: archivos CSV estructurados para análisis de BI

👨‍💻 Autores
Luis Ernesto Caro Barrera - Daniel Esteban Lopez Suarez

Proyecto académico — Análisis ETL de Ventas

Desarrollado con Python y Google Colab
