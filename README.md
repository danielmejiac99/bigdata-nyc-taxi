# Proyecto Final Big Data: Data Lakehouse (NYC Green Taxi)

## Descripción
Este proyecto implementa un pipeline de datos (ETL) utilizando Apache Spark (PySpark) bajo una arquitectura Medallion (Bronze, Silver, Gold). El objetivo es procesar registros de viajes del Green Taxi de Nueva York para extraer KPIs de negocio y predecir tarifas.

## Arquitectura y Tecnologías
*   **Entorno:** Docker (Contenedor Jupyter/PySpark)
*   **Procesamiento:** PySpark (Batch)
*   **Machine Learning:** Spark MLlib (Regresión Lineal)
*   **Visualización:** Power BI

## Estructura del Pipeline
1.  **Capa Bronze (Ingesta):** Lectura de datos crudos `.parquet` y catálogo de zonas `.csv`.
2.  **Capa Silver (Limpieza):** Filtrado de outliers (distancias/tarifas en 0), eliminación de nulos y extracción de variables temporales.
3.  **Capa Gold (Agregación):** Creación de 4 DataFrames orientados a negocio (Demanda, Rentabilidad, Pagos y Dispersión) exportados a CSV para el Dashboard final.

## Cómo ejecutar este proyecto
1. Clonar el repositorio.
2. Ejecutar `docker-compose up` en la terminal para levantar el contenedor.
3. Abrir el enlace local de Jupyter (ej: `http://127.0.0.1:8888/lab`).
4. Abrir y ejecutar las celdas del archivo `Notebook.ipynb` en orden.
