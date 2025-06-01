# Reducción de Dimensionalidad con PCA y t-SNE

Este proyecto se enfoca en la aplicación y visualización de dos técnicas populares de reducción de dimensionalidad: el Análisis de Componentes Principales (PCA) y t-Distributed Stochastic Neighbor Embedding (t-SNE). El objetivo es transformar un conjunto de datos de alta dimensionalidad a un espacio de menor dimensión, facilitando la visualización y, potencialmente, mejorando el rendimiento de algoritmos de aprendizaje automático.

El análisis se desarrolla en el Jupyter Notebook `ReduccionDimensiones.ipynb`.

## Descripción del Proyecto

El notebook sigue los siguientes pasos para aplicar y evaluar las técnicas de reducción de dimensionalidad:
1.  **Carga de Librerías y Datos**:
    * Se importan las bibliotecas necesarias, incluyendo `numpy`, `pandas`, `matplotlib.pyplot`, `sklearn.datasets` (para cargar el dataset), `sklearn.preprocessing` (para escalar los datos), y `sklearn.decomposition.PCA`, `sklearn.manifold.TSNE` (para las técnicas de reducción).
    * Se carga el conjunto de datos de dígitos (`load_digits`) disponible en Scikit-learn.
2.  **Exploración Inicial de los Datos**:
    * Se muestra la forma (dimensiones) de los datos y las etiquetas.
    * Se visualizan algunos ejemplos de los dígitos para entender la naturaleza del dataset.
3.  **Preparación de Datos**:
    * Los datos se escalan utilizando `StandardScaler` para asegurar que todas las características contribuyan de manera equitativa a los algoritmos de reducción.
4.  **Aplicación de PCA (Análisis de Componentes Principales)**:
    * Se aplica PCA para reducir la dimensionalidad de los datos a 2 componentes.
    * Se calcula y muestra la varianza explicada por cada uno de los componentes seleccionados y la varianza total explicada.
    * Se visualizan los datos transformados por PCA en un gráfico de dispersión, coloreando los puntos según su etiqueta de dígito.
5.  **Aplicación de t-SNE (t-Distributed Stochastic Neighbor Embedding)**:
    * Se aplica t-SNE para reducir la dimensionalidad de los datos a 2 componentes, especificando parámetros como `n_iter`, `learning_rate` y `perplexity`.
    * Se visualizan los datos transformados por t-SNE en un gráfico de dispersión, también coloreando los puntos según su etiqueta de dígito.

## Características Principales / Análisis Realizado

* **Carga de Datos**: Uso del conjunto de datos `digits` de Scikit-learn, que contiene imágenes de dígitos escritos a mano.
* **Exploración Inicial**:
    * Verificación de las dimensiones del conjunto de datos (`X.shape`, `y.shape`).
    * Visualización de ejemplos de imágenes de dígitos.
* **Preprocesamiento**:
    * Escalado de las características utilizando `StandardScaler`.
* **Reducción de Dimensionalidad con PCA**:
    * Aplicación de PCA para reducir a 2 componentes.
    * Análisis de la varianza explicada por los componentes.
    * Visualización de los datos en el espacio de los 2 componentes principales.
* **Reducción de Dimensionalidad con t-SNE**:
    * Aplicación de t-SNE para reducir a 2 componentes.
    * Visualización de los datos en el espacio de los 2 componentes t-SNE.

## Conjunto de Datos

* El proyecto utiliza el conjunto de datos `digits`, que se carga directamente desde la biblioteca Scikit-learn (`sklearn.datasets.load_digits()`).
* Este conjunto de datos consta de 1797 imágenes de 8x8 píxeles de dígitos escritos a mano (0-9). Cada imagen se representa como un vector de 64 características (píxeles).

## Requisitos

Para ejecutar este proyecto, necesitarás tener instaladas las siguientes bibliotecas de Python:
* numpy
* pandas
* matplotlib
* scikit-learn
