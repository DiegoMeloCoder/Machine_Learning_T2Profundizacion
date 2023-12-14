# Análisis Exploratorio de Datos y Clasificación con Machine Learning


![machinelearning](https://github.com/DiegoMeloCoder/Machine_Learning_T3Profundizacion/assets/149011345/a04f0eb9-5618-4217-a56b-47687f9f4ff3)


## Objetivos:
- Realizar un análisis exploratorio con la base de datos que proporciona el cliente, encontrada en la carpeta base de datos.
- Entrenar un modelo de machine learning con la capcidad de clasificar datos faltantes, de acuerdo a su entrenamiento.
- Abordar el desarrollo del modelo haciendo un analisis de resultados en formato informe (encontrado a continuación).


## Descripción:
  Dentro del extenso ámbito del aprendizaje automático, se encuentran diversos tipos de modelos, cada uno con sus propias ventajas y características que los hacen aplicables a casos particulares y los distinguen de otros modelos. En el marco de este taller, nos enfocaremos en dos métodos específicos: la regresión logística y Random Forest (métodos de conjunto). 

## Resultados
Resulta interesante la precision del modelo Logistico, pues fue de aproximadamente 0.5, es decir que acierta en la mitad de las predicciones, podriamos realicionar esta prediccion con el azar. Despues de buscar un modelo en el que la precision aumente, nos tomamos con Random Forest, del 
paquete scikit-learn, en el cual con el uso de una semilla aleatoria se obtuvo una precision por encima del 90%. De esta manera se cumple con el objetivo del taller, pues los 100 datos faltantes podran ser predecidos con una taza de acierto muy alta, asi la mision se cumple con exito

![RegresiónAccuracy](https://github.com/DiegoMeloCoder/Machine_Learning_T2Profundizacion/assets/149011345/174135af-f723-4c64-9a2b-5f6db856de77)

![RandomForestAccuracy](https://github.com/DiegoMeloCoder/Machine_Learning_T2Profundizacion/assets/149011345/0d8d06ca-d3a1-4cb0-b205-cd48277b063a)

![MatrizConfusionRandomForest](https://github.com/DiegoMeloCoder/Machine_Learning_T2Profundizacion/assets/149011345/668cc860-b905-453d-a386-3a3f73387c35)


## Conclusiones





## Instrucciones de Uso:
1. Abre y ejecuta los notebooks con extensión .ipynb para visualizar los datos y modelo empleados. POR FAVOR: antes de correr el codigo sube la base de datos datos_sensores encontrada en el menú
3. Encuentra las predicciones en el archivo predicciones.csv.

## Nota:
- La columna 'etiqueta' solo tiene dos valores posibles: 'Positivo' o 'Negativo'.
