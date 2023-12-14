# Análisis Exploratorio de Datos y Clasificación con Machine Learning
Modelo entrenado por: Jhon Sebastian Montenegro, Giovanni Pantoja Mora, Diego Alejandro Melo

![machinelearning](https://github.com/DiegoMeloCoder/Machine_Learning_T3Profundizacion/assets/149011345/a04f0eb9-5618-4217-a56b-47687f9f4ff3)


## Objetivos:
- Realizar un análisis exploratorio con la base de datos que proporciona el cliente, encontrada en la carpeta base de datos.
- Entrenar un modelo de machine learning con la capcidad de clasificar datos faltantes, de acuerdo a su entrenamiento.
- Abordar el desarrollo del modelo haciendo un analisis de resultados en formato informe (encontrado a continuación).


## Descripción:

Dentro del extenso ámbito del aprendizaje automático, se encuentran diversos tipos de modelos, cada uno con sus propias ventajas y características que los hacen aplicables a casos particulares y los distinguen de otros modelos. En el marco de este taller, nos enfocaremos en dos métodos específicos: la regresión logística y Random Forest (métodos de conjunto). La progresión de este taller se organiza en las siguientes etapas: análisis exploratorio de datos (EDA), entrenamiento del modelo seleccionado y predicción de la información faltante mediante el modelo más confiable." 
  

  
## EDA
Se generó un reporte usando el comando; “ProfileReport” de la librería “ydata_profiling” del dataset que se usara tanto para el entrenamiento del modelo usando Regresion Logistica como para el modelo usando Random Forest.



![datasetstatics](https://github.com/DiegoMeloCoder/Machine_Learning_T2Profundizacion/assets/149011345/321a7bef-5a21-4d06-b1d8-a357402e7a05)

## Entrenamiento
Usando comandos vistos previamente en clase se diseñó los modelos usando el dataset visto previamente en EDA. En esta sección, empleamos la base de datos proporcionada por el docente, seleccionando como variables predictoras las columnas correspondientes a 'tamaño', 'clasificación', 'sensor_orion', 'sensor_vega', 'sensor_polaris' y 'sensor_antares'. La elección de estas columnas se realizó mediante una consulta (query) que fue estudiada en la primera parte del curso de Profundización en Automatización y Control. Posteriormente, importamos y leímos los datos utilizando las bibliotecas 'pandas' y 'sqlite3'. En dicho diseño se destinó el 20% de los datos al testeo del mismo, y el 80% restante al entrenamiento.
Los resultados del testeo se muestran en las siguientes imágenes.



## Resultados

Regresion logística.

Resulta interesante la precision del modelo Logistico, pues fue de aproximadamente 0.5, es decir que acierta en la mitad de las predicciones, podriamos realicionar esta prediccion con el azar.

![RegresiónAccuracy](https://github.com/DiegoMeloCoder/Machine_Learning_T2Profundizacion/assets/149011345/bddcb550-c8c2-4dab-b1b1-74942587974f)

Random Forest.

Despues de buscar un modelo en el que la precision aumente, nos topamos con Random Forest, del 
paquete scikit-learn, en el cual con el uso de una semilla aleatoria se obtuvo una precision por encima del 90%. De esta manera se cumple con el objetivo del taller, pues los 100 datos faltantes podran ser predecidos con una taza de acierto muy alta, asi la mision se cumple con exito

![RandomForestAccuracy](https://github.com/DiegoMeloCoder/Machine_Learning_T2Profundizacion/assets/149011345/a6bef6c8-b657-4479-8918-2687d8575cee)


Basándonos en las imágenes anteriores, podemos deducir dos observaciones importantes. 

En primer lugar, el modelo más adecuado para completar los datos faltantes en la columna 'etiqueta', proporcionada por el docente en la base de datos, es el Random Forest, con una tasa de acierto de aproximadamente el 93%. 
En segundo lugar, notamos que el modelo de regresión logística parece estar realizando predicciones aleatorias, lo cual podría explicarse mediante el teorema de Shannon. Según este teorema, en la transmisión de datos en bits, el error máximo que se puede cometer es del 50%. En consecuencia, podríamos inferir análogamente que nuestro modelo de regresión logística asignó bits de 0 y 1, correspondientes a negativo y positivo respectivamente, de manera aleatoria.


A continuación se presentan los resultados obtenidos mediante el uso del modelo random forest, en el siguiente archivo .csv:  [predicciones_random_forest.csv](https://github.com/DiegoMeloCoder/Machine_Learning_T2Profundizacion/blob/main/Output%20de%20Predicciones/predicciones_random_forest.csv)

## Conclusiones

Para el modelo Logístico la precisión fue aproximadamente del 50%, sugiriendo un rendimiento similar al azar, por tanto se opta por el modelo de Random Forest, que logró una precisión superior al 90%, cumpliendo con éxito el objetivo de clasificar los datos faltantes.
Por tanto, la elección de Random Forest resalta la importancia de seleccionar modelos adecuados, ya que superó significativamente al modelo logístico.

El resultado que se obtiene mediante el arbol de decisiones en el modelo Random Forest implica que, en la clasificacion de salida participaron desde el primer "rama" hasta la ultima, pues todas estan interconectadas, es por esto que este modelo es capaz de analisar datos no relacionados linealmente y muy amplios, lo que en consecuencia lo hace un modelo computacionalmente costoso.

Tras realizar el analisis de datos, se observa que los datos mas relevantes para lograr obtener una predicción adecuada son los que se encuentra en los respectivos sensores de cada satelite y los de tamaño y categoria en la tabla de datos basicos, ademas del id en la tabla de clasificación.


## Instrucciones de Uso:
1. Abre y ejecuta los notebooks con extensión .ipynb encontrados en [Notebooks Ejecutables](https://github.com/DiegoMeloCoder/Machine_Learning_T2Profundizacion/tree/main/Notebooks%20ejectuables) para visualizar los datos y modelo empleados.

3. Encuentra el resultado de la prediccion del modelo, en la siguiente carpeta [Outputs](https://github.com/DiegoMeloCoder/Machine_Learning_T2Profundizacion/tree/main/Output%20de%20Predicciones)

## Nota:
- La columna 'etiqueta' solo tiene dos valores posibles: 'Positivo' o 'Negativo'.
