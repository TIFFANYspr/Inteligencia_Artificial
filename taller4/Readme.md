# README

## Taller Práctico No. 4 – NumPy, Matplotlib y Seaborn

### Caso de estudio: Predicción de rotación de empleados en una empresa tecnológica

### Integrantes

* Ángel Santiago Estupiñán Gómez
* STEFANY Potosi Reyes
* Cristian David García Valderrama
* Jhon Edwar Suárez Quiñónez
* Jheison Estiben Cabal Chimbaco

## Introducción

Este notebook fue desarrollado para poner en práctica las librerías NumPy, Matplotlib y Seaborn estudiadas durante la asignatura de Inteligencia Artificial.

El objetivo principal del trabajo no fue construir un modelo de Machine Learning, sino comprender cómo se generan, procesan y analizan los datos antes de llegar a una etapa de modelado. Para ello se realizaron actividades teóricas y prácticas que permitieron explorar el funcionamiento de estas herramientas y su importancia dentro del análisis de datos.

Como caso de estudio se trabajó con la predicción de rotación de empleados en una empresa tecnológica. A partir de un conjunto de datos generado artificialmente, se buscó identificar qué variables parecen influir en la decisión de un empleado de permanecer o renunciar a la organización.

## Estructura del Notebook

El notebook está dividido en dos secciones principales.

### Parte I – Investigación Conceptual

En esta sección se desarrollan las preguntas teóricas propuestas en la guía del taller.

Se investigan temas relacionados con:

#### NumPy

* Concepto de ndarray.
* Ventajas frente a las listas tradicionales de Python.
* Relación con el álgebra lineal.
* Uso dentro de modelos de Inteligencia Artificial y Deep Learning.

#### Matplotlib

* Construcción de gráficos.
* Importancia de la visualización de datos.
* Aplicación en el análisis exploratorio.

#### Seaborn

* Visualización estadística.
* Mapas de calor.
* Matrices de correlación.
* Ventajas frente a Matplotlib.

### Parte II – Desarrollo del Caso de Estudio

En esta sección se desarrolla el ejercicio principal del taller mediante la generación de un conjunto de datos sintético de 500 empleados y su posterior análisis utilizando estadísticas descriptivas y visualizaciones.

## Configuración Inicial

El primer bloque de código importa las librerías necesarias para el desarrollo del proyecto.

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

Cada librería cumple una función específica:

* **NumPy:** operaciones numéricas y generación de datos.
* **Pandas:** organización y manipulación de datos tabulares.
* **Matplotlib:** creación de gráficos básicos.
* **Seaborn:** visualizaciones estadísticas avanzadas.

También se configura una semilla aleatoria para garantizar que los resultados obtenidos puedan reproducirse en futuras ejecuciones.

## Ejercicios de Práctica

Antes de desarrollar el caso principal se realizaron ejercicios para familiarizarse con las librerías estudiadas.

### Indexación de Matrices

Se creó una matriz de ejemplo para practicar la extracción de elementos, filas y columnas utilizando la indexación bidimensional de NumPy.

### Operaciones Estadísticas

Se calcularon indicadores básicos como:

* Promedio
* Valor máximo
* Valor mínimo
* Desviación estándar

Estos cálculos permiten resumir el comportamiento de un conjunto de datos y constituyen una parte fundamental del análisis exploratorio.

### Generación de Datos Aleatorios

Se utilizaron distribuciones normales para generar conjuntos de datos sintéticos y comprender cómo se comportan variables que siguen patrones estadísticos similares a los encontrados en situaciones reales.

### Construcción de Gráficos

Se desarrollaron ejemplos utilizando:

* Histogramas
* Gráficos de líneas
* Gráficos de barras
* Heatmaps
* Boxplots

El propósito fue comprender cómo representar visualmente la información antes de aplicarlo al caso de estudio.

## Generación del Dataset

Para el análisis principal se generó un conjunto de datos compuesto por 500 empleados.

Las variables consideradas fueron:

| Variable        | Descripción                         |
| --------------- | ----------------------------------- |
| Edad            | Edad del empleado                   |
| Salario Mensual | Ingreso mensual                     |
| Horas Extras    | Horas extras realizadas por mes     |
| Antigüedad      | Tiempo de permanencia en la empresa |
| Satisfacción    | Valor entre 1 y 10                  |
| Renunció        | Sí o No                             |

Los datos fueron generados mediante distintas distribuciones estadísticas con el fin de simular un escenario empresarial realista.

## Estadísticas Obtenidas

Después de generar el conjunto de datos se calcularon los principales indicadores descriptivos.

### Resultados

* Promedio salarial: $4.486.768
* Mediana salarial: $4.465.908
* Edad promedio: 41 años
* Desviación estándar salarial: $1.179.470
* Porcentaje de renuncia: 22.2%

Estos resultados permiten obtener una visión general de la población estudiada antes de realizar el análisis gráfico.

## Análisis de Gráficos

### Histograma de Salarios

![Histograma](<img width="698" height="460" alt="image" src="https://github.com/user-attachments/assets/096b27e4-5448-4562-8082-28ee8a360a4b" />)


Este gráfico permite observar la distribución de los salarios dentro de la empresa. La mayoría de los empleados se concentra en rangos salariales medios, mientras que un grupo reducido presenta salarios más altos.

### Distribución de Renuncias

![Renuncias](images/renuncias.png)

La gráfica muestra que la mayoría de los empleados permanece en la organización. Sin embargo, existe una proporción importante de trabajadores que renuncian, lo que justifica el análisis de los factores asociados a este fenómeno.

### Relación entre Salario y Satisfacción

![Scatter](images/scatter_salario_satisfaccion.png)

No se observa una relación directa entre el salario y el nivel de satisfacción. Esto sugiere que existen otros factores que influyen con mayor fuerza en la decisión de abandonar la empresa.

### Heatmap de Correlación

![Heatmap](images/heatmap_correlacion.png)

La matriz de correlación permite identificar relaciones entre las variables analizadas. La asociación más evidente se presenta entre las horas extras y la satisfacción laboral.

### Boxplot de Salarios

![Boxplot](images/boxplot_salarios.png)

La comparación entre empleados que renunciaron y quienes permanecieron muestra distribuciones salariales similares, indicando que el salario no parece ser el principal factor asociado a la rotación.

### Pairplot

![Pairplot](images/pairplot.png)

Esta visualización permite observar simultáneamente todas las variables numéricas y detectar patrones generales dentro del conjunto de datos.

## Conclusiones

A partir del análisis realizado se encontró que la satisfacción laboral es la variable que presenta una relación más fuerte con la renuncia de los empleados.

También se observó que una mayor cantidad de horas extras parece afectar negativamente la satisfacción y aumentar la probabilidad de rotación.

La antigüedad mostró un efecto positivo sobre la permanencia de los trabajadores, mientras que el salario no presentó una influencia tan significativa como se esperaba inicialmente.

En conjunto, los resultados evidencian la importancia de realizar análisis exploratorios antes de construir modelos predictivos, ya que permiten comprender mejor el comportamiento de los datos y las relaciones existentes entre las variables.

## Reflexión Final

Este taller permitió comprender la importancia del análisis de datos dentro de los proyectos de Inteligencia Artificial.

Las librerías NumPy, Matplotlib y Seaborn facilitaron la generación, exploración y visualización de información, permitiendo identificar patrones que no serían evidentes mediante la simple observación de tablas.

La experiencia obtenida constituye una base importante para futuros trabajos relacionados con Ciencia de Datos, Machine Learning e Inteligencia Artificial.
