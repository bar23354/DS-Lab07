# Laboratorio 7. Spark MLlib

CC3066 Data Science, Universidad del Valle de Guatemala, segundo semestre 2026

Análisis de salarios de personas asalariadas con las bases de Personas de la ENEIC del INE. Se usan los cuatro trimestres de 2025 para desarrollo y el primer trimestre de 2026 para la prueba final.

## Contenido

- `notebooks/lab07_spark_mllib.ipynb` contiene el notebook con código, gráficas e interpretación
- `requirements.txt` lista las librerías de Python
- `data/raw` es la carpeta donde van los archivos originales de Excel

## Cómo ejecutar

1. Instalar Java 17 y las librerías con `pip install -r requirements.txt`
2. Copiar los cinco archivos de Personas en `data/raw`
3. Revisar que los nombres coincidan con la lista `ARCHIVOS` del notebook, o cambiar la lista
4. Ejecutar el notebook de principio a fin

El notebook genera los conjuntos preparados en `data/processed`. Los datos no se suben al repositorio.

## Avance

La primera entrega cubre la sección de análisis exploratorio y segmentación.

1. Carga, armonización y calidad de datos
2. Estadística descriptiva
3. Relaciones entre variables numéricas
4. Segmentación de perfiles con KMeans
