# README — Evaluación Parcial 1: MLP con Fashion-MNIST

## Instrucciones para ejecutar el notebook

Este README explica cómo ejecutar correctamente el notebook `DLY0100_Evaluacion_Parcial_1_MLP_FashionMNIST_F.ipynb`.

### 1. Requisitos

Se recomienda utilizar Python 3.x con las siguientes librerías:

- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook o JupyterLab

Si es necesario instalarlas:

```bash
pip install tensorflow numpy pandas matplotlib scikit-learn jupyter
```

### 2. Abrir el notebook

1. Mantener el archivo `.ipynb` en una carpeta.
2. Abrir una terminal en esa carpeta.
3. Ejecutar:

```bash
jupyter notebook
```

También se puede utilizar:

```bash
jupyter lab
```

4. Abrir el archivo `DLY0100_Evaluacion_Parcial_1_MLP_FashionMNIST_F.ipynb`.

### 3. Ejecutar el notebook

El notebook debe ejecutarse **desde la primera celda hasta la última y en orden**.

Para ejecutar una celda, seleccionar la celda y presionar:

`Shift + Enter`

También se puede utilizar la opción **Run All / Ejecutar todo**.

Es importante respetar el orden porque las variables, funciones, modelos y resultados utilizados en las celdas posteriores dependen de las celdas anteriores.

### 4. Flujo del notebook

El notebook realiza las siguientes etapas:

1. Importación de librerías.
2. Carga del dataset Fashion-MNIST.
3. Exploración de los datos.
4. Preprocesamiento de las imágenes.
5. División en entrenamiento y validación.
6. Definición de funciones de activación y pérdida.
7. Construcción del modelo MLP.
8. Experimentos con hiperparámetros.
9. Comparación de funciones de pérdida.
10. Comparación de funciones de activación.
11. Evaluación de técnicas de regularización.
12. Selección de la configuración final.
13. Evaluación final sobre el conjunto de test.
14. Cálculo de métricas y matriz de confusión.
15. Análisis de errores y conclusiones.

### 5. Consideraciones

- Las imágenes de Fashion-MNIST tienen tamaño `28 × 28` y se transforman en `784` características para ingresar al MLP.
- Los valores de los píxeles se normalizan a `[0, 1]`.
- El conjunto de entrenamiento se divide en entrenamiento y validación.
- El conjunto de test se mantiene reservado para la evaluación final.
- Los experimentos comparan los parámetros de manera controlada.
- Se utilizan Accuracy, Precision, Recall y F1-score para evaluar el desempeño.

### 6. Configuración final del modelo

La configuración seleccionada en el notebook es:

- Batch size: `128`
- Learning rate: `0.001`
- Épocas: `15`
- Activación: `LeakyReLU`
- Pérdida: `Sparse Categorical Crossentropy`
- Dropout: `0.2`
- Batch Normalization: activada
- L2: `0.0`

Arquitectura:

```text
784 entradas
    ↓
Dense(128) + LeakyReLU
    ↓
Dense(64) + LeakyReLU
    ↓
Dense(10) + Softmax
```

### 7. Resultados finales

**Validación**

- Accuracy: `0.8893`
- Precision: `0.8906`
- Recall: `0.8893`
- F1-score: `0.8880`

**Test**

- Accuracy: `0.8748`
- Precision: `0.8753`
- Recall: `0.8748`
- F1-score: `0.8735`

### 8. Para reproducir los resultados

1. Instalar las dependencias.
2. Abrir el notebook.
3. Ejecutar todas las celdas en orden.
4. Esperar a que finalice cada entrenamiento antes de continuar.
5. No modificar los parámetros de los experimentos si se desea reproducir los resultados presentados.
6. Revisar las tablas, métricas y gráficos generados.

> **Nota:** el tiempo de ejecución puede variar según el computador y el entorno utilizado.
