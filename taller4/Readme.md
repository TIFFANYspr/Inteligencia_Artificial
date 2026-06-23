# README

## Taller Práctico No. 4 – NumPy, Matplotlib y Seaborn

### Caso de estudio: Predicción de rotación de empleados en una empresa tecnológica

### Integrantes

* Ángel Santiago Estupiñán Gómez
* STEFANY Potosí Reyes
* Cristian David García Valderrama
* Jhon Edwar Suárez Quiñónez
* Jheison Estiben Cabal Chimbaco

---

## ¿De qué trata este trabajo?

Este notebook fue desarrollado para poner en práctica las librerías NumPy, Matplotlib y Seaborn vistas durante la asignatura de Inteligencia Artificial.

La idea principal no era construir un modelo de Machine Learning, sino aprender a trabajar con datos: generarlos, analizarlos, obtener estadísticas y representarlos mediante gráficos que facilitaran su interpretación.

Para ello se trabajó con un caso relacionado con la rotación de empleados en una empresa tecnológica. A partir de un conjunto de datos generado artificialmente, se buscó identificar qué variables parecen influir más en la decisión de un empleado de permanecer o renunciar a la organización.

---

# Estructura del notebook

El notebook está dividido en dos grandes partes.

## Parte I – Investigación conceptual

En esta sección se desarrollan las preguntas teóricas propuestas en la guía.

Aquí se explica:

### NumPy

Se investigó qué es NumPy, cuál es la función de los arreglos multidimensionales (ndarray), por qué NumPy es más eficiente que las listas tradicionales de Python y cuál es su importancia dentro del aprendizaje automático.

### Matplotlib

Se estudió el uso de Matplotlib para construir gráficos que permitan representar visualmente los datos y facilitar su interpretación.

### Seaborn

Se analizó la utilidad de Seaborn como complemento de Matplotlib para crear visualizaciones estadísticas más avanzadas con menos líneas de código.

---

## Parte II – Caso de estudio

La segunda parte corresponde al desarrollo práctico del taller.

Aquí se genera un conjunto de datos sintético de 500 empleados y posteriormente se realiza un análisis exploratorio utilizando estadísticas y gráficos.

---

# Configuración inicial

Al comienzo del notebook se importan las librerías necesarias:

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

Cada una cumple una función específica:

* NumPy: generación y procesamiento de datos numéricos.
* Pandas: organización de los datos en tablas.
* Matplotlib: creación de gráficos básicos.
* Seaborn: visualizaciones estadísticas avanzadas.

También se configura una semilla aleatoria para garantizar que los resultados puedan reproducirse cada vez que se ejecute el código.

---

# Ejercicios de práctica

Antes de desarrollar el caso de estudio se realizaron varios ejercicios sencillos para comprender mejor el funcionamiento de las librerías.

### Indexación de matrices

Se creó una matriz de ejemplo y se practicó la extracción de filas, columnas y elementos específicos.

### Estadística básica

Se calcularon medidas como:

* Promedio
* Máximo
* Mínimo
* Desviación estándar

Estas medidas permiten resumir el comportamiento de un conjunto de datos.

### Distribuciones normales

Se generaron datos aleatorios utilizando distribuciones normales para comprender cómo funcionan variables que siguen patrones estadísticos reales.

### Construcción de gráficos

Se elaboraron ejemplos de:

* Histogramas
* Gráficos de líneas
* Gráficos de barras
* Mapas de calor
* Boxplots

El objetivo fue familiarizarse con las herramientas antes de aplicarlas al caso principal.

---

# Generación del dataset

Para el caso de estudio se generó un conjunto de datos de 500 empleados.

Las variables creadas fueron:

| Variable        | Descripción                    |
| --------------- | ------------------------------ |
| Edad            | Edad del empleado              |
| Salario Mensual | Ingreso mensual                |
| Horas Extras    | Horas extras realizadas al mes |
| Antigüedad      | Tiempo en la empresa           |
| Satisfacción    | Valor entre 1 y 10             |
| Renunció        | Sí o No                        |

Los datos fueron generados utilizando diferentes distribuciones estadísticas para simular situaciones similares a las que podrían encontrarse en una empresa real.

---

# Estadísticas obtenidas

Después de generar el dataset se calcularon varios indicadores descriptivos.

Resultados obtenidos:

* Promedio salarial: $4.486.768
* Mediana salarial: $4.465.908
* Edad promedio: 41 años
* Desviación estándar salarial: $1.179.470
* Porcentaje de renuncia: 22.2%

Estos valores permiten obtener una visión general de la población analizada antes de construir los gráficos.

---

# Análisis de gráficos

## Histograma de salarios

![Histograma](images/histograma_salarios.png)

Este gráfico permite observar cómo se distribuyen los salarios de los empleados.

La mayoría se concentra alrededor de los salarios medios, mientras que un grupo reducido posee salarios más altos.

---

## Distribución de renuncias

![Renuncias](images/renuncias.png)

Se observa que la mayor parte de los empleados permanece en la empresa.

Sin embargo, existe un porcentaje importante de trabajadores que renuncian, por lo que resulta útil estudiar las variables asociadas a este fenómeno.

---

## Relación entre salario y satisfacción

![Scatter](images/scatter_salario_satisfaccion.png)

La gráfica muestra que el salario no parece ser el principal factor relacionado con la satisfacción laboral.

Los empleados que renuncian aparecen distribuidos en distintos niveles salariales.

---

## Heatmap de correlación

![Heatmap](images/heatmap_correlacion.png)

La matriz de correlación permite identificar relaciones entre las variables.

La asociación más visible aparece entre las horas extras y la satisfacción laboral.

---

## Boxplot de salarios

![Boxplot](images/boxplot_salarios.png)

Este gráfico permite comparar la distribución salarial entre empleados que renunciaron y empleados que permanecieron.

Las diferencias encontradas no son suficientemente grandes para concluir que el salario sea el principal factor de rotación.

---

## Pairplot

![Pairplot](images/pairplot.png)

Esta visualización reúne todas las variables numéricas y permite observar patrones generales.

Aquí se aprecia con mayor claridad que los empleados con menor satisfacción y más horas extras presentan una tendencia más alta a renunciar.

---

# Conclusiones personales del análisis

Después de realizar el análisis exploratorio se encontró que la satisfacción laboral es la variable que más parece influir en la renuncia de los empleados.

También se observó que el exceso de horas extras puede afectar negativamente el bienestar de los trabajadores y aumentar la probabilidad de rotación.

Por otro lado, la antigüedad parece actuar como un factor de estabilidad, ya que los empleados con más tiempo dentro de la empresa muestran una menor tendencia a abandonar la organización.

Finalmente, aunque el salario es una variable importante dentro de cualquier empresa, en este caso no mostró una relación tan fuerte con la decisión de renunciar como inicialmente se esperaba.

---

# Reflexión final

Este taller permitió comprender que antes de construir modelos de Inteligencia Artificial es necesario conocer y entender los datos con los que se trabaja.

Las librerías NumPy, Matplotlib y Seaborn facilitan enormemente este proceso, ya que permiten generar información estadística, detectar patrones y representar visualmente los resultados.

La experiencia obtenida durante este ejercicio ayuda a sentar las bases para futuros proyectos relacionados con Machine Learning y Ciencia de Datos.
