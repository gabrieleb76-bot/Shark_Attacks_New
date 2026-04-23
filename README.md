Análisis de actividades asociadas a ataques de tiburón
Objetivo del proyecto

El objetivo de este proyecto es analizar qué actividades acuáticas aparecen con mayor frecuencia asociadas a ataques de tiburón registrados en el dataset del Global Shark Attack File (GSAF).

A través de un proceso de limpieza de datos y análisis exploratorio (EDA), buscamos identificar patrones que permitan comprender en qué contextos se registran más incidentes y qué prácticas acuáticas aparecen más frecuentemente en estos ataques.

Este análisis permite transformar un dataset complejo y desestructurado en información interpretable mediante técnicas de data wrangling y agregación de datos.

Dataset

El análisis utiliza el dataset histórico de ataques de tiburón recopilado por el Global Shark Attack File (GSAF).

Fuente:
Global Shark Attack File

El dataset contiene registros históricos de ataques de tiburón ocurridos en diferentes países y contextos.

Para este proyecto se utilizaron principalmente las siguientes variables:

Variable    Descripción
Activity        Actividad realizada por la persona en el momento del ataque
Country         País donde ocurrió el incidente
Year            Año del incidente
Sex             Sexo de la víctima
Age             Edad de la víctima
Fatal Y/N       Indica si el ataque fue fatal

Durante el proceso de limpieza, la variable Activity fue transformada para agrupar múltiples variantes textuales en categorías más generales.

La nueva variable creada (activity_group) agrupa actividades similares en categorías como:

Surf
Natación
Pesca
Buceo
Navegación
Snorkel
Otros

Esto permitió reducir la dispersión de valores y facilitar el análisis.

Proceso de análisis

El análisis se desarrolló siguiendo las etapas habituales de un proyecto de análisis de datos.

1. Exploración inicial del dataset

Se analizó la estructura general del dataset para identificar:

número de registros
tipos de datos
columnas disponibles
presencia de valores nulos
posibles duplicados

2. Limpieza de datos

Se aplicaron varias técnicas de limpieza:

eliminación de registros duplicados
tratamiento de valores nulos en columnas clave
normalización de texto
limpieza de valores inconsistentes en la variable Fatal Y/N

3. Transformación de variables

La variable Activity presentaba numerosas variantes textuales para referirse a actividades similares.

Para mejorar el análisis se creó la variable:

activity_group

Esta variable agrupa actividades similares utilizando patrones de texto (regex), lo que permitió reducir cientos de valores distintos a un pequeño conjunto de categorías comparables.

4. Análisis exploratorio de datos (EDA)

Se aplicaron técnicas de agregación utilizando groupby() para identificar patrones relevantes en el dataset.

Se realizaron dos análisis principales:

Análisis principal

Identificación de las actividades agrupadas con mayor número de ataques registrados.

Análisis complementario

Relación entre tipo de actividad y fatalidad del ataque.

Además, se utilizaron visualizaciones para facilitar la interpretación de los resultados.

Resultados / Insights

El análisis permitió identificar varios patrones relevantes:

Algunas actividades acuáticas aparecen con mayor frecuencia asociadas a ataques de tiburón registrados.
Categorías como Surf, Natación y Pesca concentran una gran parte de los incidentes documentados.
La mayoría de los ataques registrados en el dataset no resultan fatales.
La agrupación de actividades fue un paso clave para transformar una variable con gran dispersión en información útil para el análisis.

Es importante destacar que estos resultados reflejan la frecuencia dentro del dataset, y no necesariamente el riesgo absoluto real de cada actividad.

Próximos pasos

Si se dispusiera de más tiempo o más datos, el análisis podría ampliarse mediante:

análisis geográfico por país o región
análisis temporal por décadas
análisis demográfico por edad y sexo
uso de visualizaciones interactivas
integración con datos externos sobre actividad turística o marítima

Estas extensiones permitirían comprender mejor el contexto de los ataques registrados.

Replicación del análisis

Este proyecto permite la reproducibilidad del análisis, ya que proporciona el código, el dataset y el flujo completo de procesamiento de datos necesario para obtener los mismos resultados.

Una replicación completa del estudio implicaría aplicar la misma metodología a nuevos datos independientes sobre ataques de tiburón para verificar si los patrones identificados se mantienen.

Pasos para garantizar una replicación exitosa
Documentar el origen: Registra de dónde provienen los datos y cualquier filtro inicial aplicado.
Estandarizar los datos: Asegúrate de que las columnas y filas sigan un orden lógico (limpieza y codificación) antes de replicar el análisis.
Sincronizar el proyecto según las tecnologías utilizadas.


Tecnologías utilizadas
Python
Pandas
NumPy
Matplotlib
Jupyter Notebook


