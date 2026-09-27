# Laboratorio 7. Spark MLlib

CC3066 Data Science, Universidad del Valle de Guatemala, segundo semestre 2026

Análisis de salarios de personas asalariadas con las bases de Personas de la ENEIC del INE. Se usan los cuatro trimestres de 2025 para desarrollo y el primer trimestre de 2026 para la prueba final.

## Contenido

- `notebooks/lab07_spark_mllib.ipynb` contiene el notebook con código, gráficas e interpretación
- `requirements.txt` lista las librerías de Python
- `data/raw` es la carpeta donde van los archivos originales de Excel

## Cómo ejecutar

1. Instalar Java 17 y las librerías con `pip install -r requirements.txt`. Se recomienda Python 3.10 a 3.12
2. Copiar los cinco archivos de Personas en `data/raw`. Los nombres deben ser `ENEIC_2025_I_Personas.xlsx`, `ENEIC_2025_II_Personas.xlsx`, `ENEIC_2025_III_Personas.xlsx`, `ENEIC_2025_IV_Personas.xlsx` y `ENEIC_2026_I_Personas.xlsx`, o se cambia la lista `ARCHIVOS` del notebook
3. Ejecutar el notebook de principio a fin. Tarda unos 10 minutos

El notebook se puede abrir desde la carpeta `notebooks` y cambia solo a la raíz del proyecto para leer `data/raw`.

### Notas sobre el entorno

- En Windows, Spark no puede escribir Parquet sin `winutils.exe` y `hadoop.dll`. La forma más simple de evitarlo es ejecutar el notebook en WSL2 o en el Docker del curso
- `pyspark` 3.5 importa `distutils`, que no existe desde Python 3.12. Por eso `requirements.txt` incluye `setuptools`
- Con Java 21 o posterior Spark 3.5 puede fallar al iniciar. Se usó Java 17

El notebook genera los conjuntos preparados en `data/processed` y los modelos elegidos en `models`. Ninguna de las dos carpetas se sube al repositorio.

## Contenido del notebook

Análisis exploratorio y segmentación:

1. Carga, armonización y calidad de datos
2. Estadística descriptiva
3. Relaciones entre variables numéricas
4. Segmentación de perfiles con KMeans

Modelado supervisado:

5. Pipeline de regresión lineal
6. Pipeline de Random Forest
7. Entrenamiento final y evaluación en 2026
8. Visualización y análisis de errores

## Partición de los datos

Los trimestres I, II y III de 2025 se usan para entrenar. El trimestre IV de 2025 se usa para elegir la configuración de cada algoritmo. El primer trimestre de 2026 queda reservado para la evaluación final y no se toca en las secciones anteriores. En la sección 7 se reajusta cada configuración elegida con los cuatro trimestres de 2025 y se evalúa una sola vez sobre 2026.
