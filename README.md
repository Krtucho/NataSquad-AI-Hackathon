# NataSquad-AI-Hackathon

## A Modo General
Para resolver el problema de pronóstico de series temporales de la demanda eléctrica en Inglaterra, es necesario seguir un proceso sistemático que involucre los siguientes pasos:

1. Carga y exploración de datos: Es importante cargar los datos y explorarlos para comprender mejor la naturaleza de la serie temporal. Esto implica analizar la tendencia, la estacionalidad y la presencia de valores atípicos en los datos. También es importante identificar cualquier patrón o relación que pueda existir entre la demanda eléctrica y cualquier variable externa, como la temperatura.

2. Preprocesamiento de datos: Se deben realizar varias tareas de preprocesamiento de datos para prepararlos para el modelado. Esto incluye la eliminación de cualquier valor atípico o dato faltante, normalización de la serie temporal, transformación de la frecuencia de muestreo, si es necesario, y separación de los datos en conjuntos de entrenamiento y prueba.

3. Selección de modelo: Una vez que los datos han sido preprocesados, se debe seleccionar un modelo adecuado para el pronóstico de la serie temporal. Algunos de los modelos comunes utilizados para el pronóstico de series temporales incluyen ARIMA, SARIMA, modelos de regresión, modelos de redes neuronales, entre otros. Es importante seleccionar un modelo que sea apropiado para la naturaleza de los datos y tenga un buen rendimiento.

4. Entrenamiento y validación del modelo: Una vez que se ha seleccionado un modelo, se debe entrenar utilizando los datos de entrenamiento. Es importante validar el modelo para asegurarse de que esté ajustado correctamente a los datos y tenga un buen rendimiento. Esto se puede lograr utilizando técnicas de validación cruzada y evaluando varias métricas, como el error cuadrático medio (MSE), la raíz del error cuadrático medio (RMSE) y el error absoluto medio (MAE).

5. Pronóstico de la serie temporal: Una vez que se ha seleccionado y validado un modelo, se puede utilizar para pronosticar el horizonte de pronóstico, es decir, los siguientes períodos de tiempo.

6. Evaluación del modelo: Es importante evaluar el rendimiento del modelo utilizando métricas de evaluación apropiadas, como el MSE, RMSE, MAE, entre otras. Además, se debe realizar un análisis de residuos para verificar si el modelo se ajusta correctamente a los datos.

En el caso específico del problema de pronóstico de series temporales de la demanda eléctrica en Inglaterra, se puede utilizar el conjunto de datos proporcionado por National Grid ESO para realizar estos pasos. Además, se puede considerar el uso de modelos específicos como ARIMA y modelos de regresión lineal para el pronóstico de la serie temporal. Es importante respetar los supuestos de los modelos utilizados y realizar un análisis de residuos para verificar si el modelo se ajusta adecuadamente a los datos.

## Modelo de Regresion

 En el contexto del pronóstico de series temporales, el modelo de regresión lineal se puede utilizar para predecir la demanda eléctrica en función de variables externas, como la temperatura, la humedad, la hora del día, el día de la semana, entre otros.

 En cuanto a por qué se escogió el modelo de regresión lineal para el pronóstico de la serie temporal de la demanda eléctrica en Inglaterra, esta elección podría haberse basado en varias razones, como:

Simplicidad: El modelo de regresión lineal es un modelo simple y fácil de entender, que no requiere de muchos recursos computacionales, lo que lo hace una buena opción para iniciar el análisis.

Correlación entre variables: Es posible que se haya observado una relación lineal entre la demanda de energía eléctrica y alguna variable externa, como la temperatura o la hora del día, lo que sugiere que un modelo de regresión lineal podría ser apropiado.

Buena interpretación de coeficientes: Los coeficientes de regresión en un modelo de regresión lineal son fáciles de interpretar y proporcionan información valiosa sobre la relación entre las variables.

Buen rendimiento: El modelo de regresión lineal puede proporcionar un buen rendimiento en términos de precisión y capacidad de generalización, si se ajusta adecuadamente a los datos y se seleccionan variables adecuadas.

Sin embargo, es importante tener en cuenta que el modelo de regresión lineal tiene ciertas limitaciones, como la suposición de linealidad y la falta de capacidad para capturar patrones no lineales en los datos. Por lo tanto, es importante evaluar cuidadosamente el rendimiento del modelo y considerar otros modelos si el rendimiento no es satisfactorio.

### Proceso para el modelo de Regresion

El proceso que se ejecutó en este código se puede resumir de la siguiente manera:

1. Cargar y explorar los datos: Se cargó un conjunto de datos de la demanda de energía eléctrica en Inglaterra desde 2009 hasta 2023. Se realizó una exploración básica de los datos, incluyendo la visualización de gráficos para comprender mejor la serie temporal.

2. Preprocesamiento: Se realizó un preprocesamiento de los datos para prepararlos para el modelado, lo que incluyó la conversión de la columna de fecha en un índice de fecha y hora, la normalización de la columna de demanda utilizando `StandardScaler` y la conversión de la columna de hora a segundos.

3. Dividir datos: Se dividió el conjunto de datos en dos conjuntos de entrenamiento y prueba, utilizando datos hasta el 31 de diciembre de 2022 para el conjunto de entrenamiento y datos desde el 1 de enero de 2023 en adelante para el conjunto de prueba.

4. Modelos: Se utilizó una regresión lineal para crear un modelo de predicción de la demanda eléctrica a partir de las variables explicativas del conjunto de datos. Se realizaron validaciones cruzadas con cinco divisiones para evaluar el rendimiento del modelo.

5. Realizar predicciones en un conjunto de datos de prueba: Se utilizó el modelo entrenado para realizar predicciones en el conjunto de datos de prueba.

6. Evaluar el rendimiento del modelo utilizando métricas de regresión: Se calcularon las métricas de regresión, incluyendo el error cuadrático medio (MSE), la raíz del error cuadrático medio (RMSE) y el error absoluto medio (MAE), para evaluar el rendimiento del modelo en el conjunto de datos de prueba.

7. Realizar un análisis de residuos: Se realizó un análisis de residuos para evaluar la calidad de las predicciones del modelo en el conjunto de datos de prueba.

Los resultados obtenidos indican que el modelo de regresión lineal tiene un rendimiento razonablemente bueno en la predicción de la demanda eléctrica en el conjunto de datos de prueba. El MSE fue de 0.008, RMSE fue de 0.094 y MAE fue de 0.079 después de normalizar la columna de demanda eléctrica.

## Modelo ARIMA

El modelo ARIMA (AutoRegressive Integrated Moving Average) es otro modelo comúnmente utilizado para el pronóstico de series temporales, incluyendo la demanda eléctrica. Este modelo es capaz de capturar patrones complejos en los datos de series temporales y puede ser especialmente efectivo en la identificación de patrones de estacionalidad y tendencia.

A continuación, se presentan algunas razones por las cuales se podría considerar el uso de un modelo ARIMA para el pronóstico de la demanda eléctrica en Inglaterra:

1. Estacionalidad: La demanda eléctrica puede variar de manera estacional, con patrones diarios, semanales o mensuales. El modelo ARIMA está diseñado para capturar patrones de estacionalidad y puede ser una buena opción para pronosticar la demanda eléctrica en función de estos patrones.

2. Diferenciación: El modelo ARIMA incluye una etapa de diferenciación para eliminar la tendencia de los datos y hacerlos estacionarios. Esto puede ser útil para eliminar cualquier tendencia o patrón no estacional en los datos de la demanda eléctrica y facilitar la identificación de patrones de estacionalidad.

3. Flexibilidad: El modelo ARIMA es un modelo flexible que puede ajustarse a una amplia variedad de patrones en los datos de la demanda eléctrica, incluyendo patrones no lineales y patrones de estacionalidad irregulares.

4. Historial de datos: El modelo ARIMA es capaz de utilizar el historial de datos para pronosticar la demanda eléctrica futura. Esto significa que puede ser una buena opción si se dispone de una cantidad suficiente de datos históricos para ajustar el modelo.

Es importante destacar que el modelo ARIMA también tiene algunas limitaciones, como la suposición de estacionariedad y la dificultad para manejar patrones de estacionalidad complejos. Además, el modelo ARIMA puede ser más complejo y difícil de interpretar que el modelo de regresión lineal. Por lo tanto, es importante evaluar cuidadosamente la naturaleza de los datos y el rendimiento del modelo antes de decidir utilizar el modelo ARIMA para el pronóstico de la demanda eléctrica en Inglaterra.

### Proceso para el modelo ARIMA

El código muestra un ejemplo de cómo utilizar el modelo ARIMA para predecir la demanda de energía en un sistema de transmisión. A continuación, una breve explicacion de lo que se hace en cada paso:

1. Se cargan los datos históricos en un DataFrame de Pandas. Los datos deben estar en un archivo CSV y deben incluir una columna con la fecha y hora y otra columna con la demanda del sistema de transmisión (TSD). Se utiliza la función `read_csv()` de Pandas para cargar los datos y la función `set_index()` para establecer la columna de fecha como índice del DataFrame.

2. Se realiza un análisis exploratorio de datos y se visualiza la serie temporal para entender mejor las características de los datos. Se utiliza la función `plot()` de Matplotlib para visualizar la serie temporal.

3. Se realiza una prueba de estacionariedad para determinar si la serie temporal es estacionaria o no. Se utiliza la prueba de Dickey-Fuller aumentada (ADF) para esto. Si el valor p es menor que 0.05, se puede rechazar la hipótesis nula de que la serie temporal es no estacionaria. De lo contrario, la serie temporal no es estacionaria y se debe aplicar una transformación. En este ejemplo, no se realiza una transformación ya que la serie temporal parece ser estacionaria.

4. Se aplica una transformación a la serie temporal si es necesario. Una transformación común es la diferenciación de la serie temporal. En este ejemplo, se aplica la diferenciación de primer orden utilizando la función `diff()` de Pandas.

5. Se determinan los valores óptimos de los parámetros AR, I y MA del modelo ARIMA utilizando técnicas como la autocorrelación y la autocorrelación parcial. Se utilizan las funciones `plot_acf()` y `plot_pacf()` de statsmodels para visualizar estos gráficos.

6. Se ajusta el modelo ARIMA utilizando los valores óptimos de los parámetros. Se utiliza la función `ARIMA()` de statsmodels para crear el modelo y la función `fit()` para ajustar el modelo a los datos.

7. Se realizan predicciones en los datos de prueba utilizando el modelo ARIMA ajustado. Se utiliza el método `predict()` de statsmodels para realizar las predicciones.

8. Se evalúa el rendimiento del modelo utilizando métricas como el error cuadrático medio (MSE) y el error absoluto medio (MAE). También se analizan los residuos para asegurarse de que no haya patrones significativos en ellos.

Al final se lleva a cabo una breve explicacion de las conclusiones a las que se pudieron llegar luego de analizar y comparar ambos modelos.