# Prediccion-RUL-Motores
Predicción de vida útil remanente (RUL) de motores

NOTA: El repositorio contiene un informe a nivel general así como diferentes ANEXOS con el código de cada sección.

## Contenido:
ANEXO A - EDA  
ANEXO B - IMPUTACIÓN  RUL  
ANEXO C - TRANSFORMACIÓN Y SELECCIÓN DE VARIABLES  
ANEXO D - ENTRENAMIENTO Y EVALUACIÓN - MODELO SIN DEPENDENCIA TEMPORAL (CATBOOST)  
ANEXO E - ANÁLISIS DE SERIE TEMPORAL  
ANEXO F - ENTRENAMIENTO Y EVALUACIÓN - CON ANÁLISIS TEMPORAL (CATBOOST)  
ANEXO G - ENTRENAMIENTO Y EVALUACIÓN - RED NEURONAL RECURRENTE PARTE I (LSTM)  
ANEXO H - ENTRENAMIENTO Y EVALUACIÓN - RED NEURONAL RECURRENTE PARTE II (LSTM)  
ANEXO I - DESPLIEGUE DEL MODELO  
ANEXO J - ACCESO A DATOS   


## Estrategia de modelado: 
En este proyecto el enfoque utilizado consistió en un desarrollo gradual, partiendo de un modelo inicial que no considera la dimensión temporal de los datos, hasta llegar a una estrategia más sofisticada que aprovecha la naturaleza secuencial de los registros. En la primera etapa, se explora un modelo que trata cada observación de manera independiente, sin considerar su orden temporal. Aquí, se utiliza el conjunto de variables existentes y se aplican técnicas de regresión para predecir la RUL. Sin embargo, al reconocer la importancia de la temporalidad en estos datos, se genera una segunda fase. En esta segunda fase se incorpora el factor temporal al análisis. Se generan nuevas variables como variables rezagadas (lags) y estadísticos móviles (rolling) para capturar patrones y correlaciones a lo largo del tiempo. Esta estrategia enriquece la capacidad para captar tendencias y dependencias secuenciales en los datos, y por tanto se espera que mejore los resultados. Finalmente, se lleva la exploración un paso más allá, adoptando un enfoque de modelado más avanzado utilizando Long Short-Term Memory (LSTM). Esta arquitectura de red neuronal recurrente tiene la capacidad inherente de capturar relaciones temporales y secuenciales en los datos. Al emplear LSTM, buscamos explotar plenamente la riqueza de información temporal presente en los registros del conjunto de datos.
