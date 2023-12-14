# Análisis Exploratorio de Datos y Clasificación con Machine Learning

## Objetivos:
- Realizar un análisis exploratorio con los datos proporcionados.
- Entrenar un modelo de machine learning para clasificar los datos faltantes en la columna 'etiqueta'.
- Generar un informe completo que resuma los resultados y conclusiones.

## Descripción:
Este proyecto aborda la exploración de datos, modelado predictivo y clasificación de datos faltantes en una columna específica ('etiqueta'). Se realiza un análisis exploratorio de los datos seguido de la implementación de un modelo de machine learning para clasificar los registros que carecen de etiqueta.

##Resultados
Resulta interesante la precision del modelo Logistico, pues fue de aproximadamente 0.5, es decir que acierta en la mitad de las predicciones, podriamos realicionar esta prediccion con el azar. Despues de buscar un modelo en el que la precision aumente, nos tomamos con Random Forest, del 
paquete scikit-learn, en el cual con el uso de una semilla aleatoria se obtuvo una precision por encima del 90%. De esta manera se cumple con el objetivo del taller, pues los 100 datos faltantes podran ser predecidos con una taza de acierto muy alta, asi la mision se cumple con exito
(Imagenes que contienen la precision de cada modelo pueden ser encontradas en la carpeta de imagenes en la rama Main)

##Conclusiones


![nick1](https://github.com/DiegoMeloCoder/Machine_Learning_T3Profundizacion/assets/149011345/3ab71518-d17b-47e6-82a9-8b4224d53fba)


## Instrucciones de Uso:
1. Abre y ejecuta los notebooks con extensión .ipynb para visualizar los datos y modelo empleados. POR FAVOR: antes de correr el codigo sube la base de datos datos_sensores encontrada en el menú
3. Encuentra las predicciones en el archivo predicciones.csv.

## Nota:
- La columna 'etiqueta' solo tiene dos valores posibles: 'Positivo' o 'Negativo'.
