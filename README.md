# Análisis Exploratorio de Datos y Clasificación con Machine Learning


![machinelearning](https://github.com/DiegoMeloCoder/Machine_Learning_T3Profundizacion/assets/149011345/a04f0eb9-5618-4217-a56b-47687f9f4ff3)


## Objetivos:
- Realizar un análisis exploratorio con la base de datos que proporciona el cliente, encontrada en la carpeta base de datos.
- Entrenar un modelo de machine learning con la capcidad de clasificar datos faltantes, de acuerdo a su entrenamiento.
- Abordar el desarrollo del modelo haciendo un analisis de resultados en formato informe (encontrado a continuación).


## Descripción:

  Dentro del extenso ámbito del aprendizaje automático, se encuentran diversos tipos de modelos, cada uno con sus propias ventajas y características que los hacen aplicables a casos particulares y los distinguen de otros modelos. En el marco de este taller, nos enfocaremos en dos métodos específicos: la regresión logística y Random Forest (métodos de conjunto). La progresión de este taller se organiza en las siguientes etapas: análisis exploratorio de datos (EDA), entrenamiento del modelo seleccionado y predicción de la información faltante mediante el modelo más confiable." 
  

Como se puede observar en la primera imagen, los resultados obtenidos con el modelo de regresion logistica, no son buenos, dado que al tener dos valores unicos posbiles, este modelo se asemeja a uno al azar.
  
## EDA
Se generó un reporte usando el comando; “ProfileReport” de la librería “ydata_profiling” del dataset que se usara tanto para el entrenamiento del modelo usando Regresion Logistica como para el modelo usando Random Forest.

Figura 1
![datasetstatics](https://github.com/DiegoMeloCoder/Machine_Learning_T2Profundizacion/assets/149011345/321a7bef-5a21-4d06-b1d8-a357402e7a05)

## Entrenamiento
Usando comandos vistos previamente en clase se diseñó los modelos usando el dataset visto previamente en EDA. En dicho diseño se destinó el 20% de los datos al testeo del mismo, y el 80% restante al entrenamiento.
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


A continuación se presentan los resultados obtenidos mediante el uso del modelo random forest, en el siguiente archivo .csv: :+1: [predicciones_random_forest.csv](https://github.com/DiegoMeloCoder/Machine_Learning_T2Profundizacion/blob/main/Output%20de%20Predicciones/predicciones_random_forest.csv)

## Conclusiones

Para el modelo Logístico la precisión fue aproximadamente del 50%, sugiriendo un rendimiento similar al azar, por tanto se opta por el modelo de Random Forest, que logró una precisión superior al 90%, cumpliendo con éxito el objetivo de clasificar los datos faltantes.
Por tanto, la elección de Random Forest resalta la importancia de seleccionar modelos adecuados, ya que superó significativamente al modelo logístico.



## Instrucciones de Uso:
1. Abre y ejecuta los notebooks con extensión .ipynb para visualizar los datos y modelo empleados. POR FAVOR: antes de correr el codigo sube la base de datos datos_sensores encontrada en el menú
3. Encuentra las predicciones en el archivo predicciones.csv.

## Nota:
- La columna 'etiqueta' solo tiene dos valores posibles: 'Positivo' o 'Negativo'.
