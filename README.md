# ProyectoFinalModelosyAprendizaje
Proyecto Final Modelos y Aprendizajes UIDE Maestria
LILIAN AMÁN

MODELOS Y APRENDIZAJES.

El proyecto pretende mediante el análisis y modelos de aprendizaje automático identificar en base a muestras que provienen de mujeres, si un paciente tiene o no cáncer.

MODELOS USADOS PARA EL ANALISIS Y APRENDIZAJE AUTOMÁTICO.

    1. RANDOM FOREST
    2. REGRESION LOGÍSTICA
    3. SVM (Support Vector Machine)

PARA LLEVAR A CABO EL ANALISIS, VERIFICACIÓN Y APRENDIZAJE DEL MODELO:

    1. Se debe importar todas las librerias necesarias y recomendadas para el aprendizaje de nuestros modelos.
    2. Cargar el dataset que contiene la información con la cual se va abordar el entrenamiento.
    3. Para la preparación de datos eliminando todas las columnas NaN
    4. Adicional para un análisis correcto y un mejor tratamiento de la informaciónse tratará la columna de diagnóstico con datos binarios
    5. Para la construcción de  nuestro modelo de aprendizaje automático separamos las caracteristicas en la variable (X) y las etiquetas en la variable (y) del data set (df_dataset)
    6. Dividimos los datos en subconjuntos de entrenamiento y prueba.
    7. Con la ayuda de la libreria scikit-learn, para nuestro entrenamiento especificaremos el 20% de los datos se utilizarán como conjunto de prueba, mientras que el 80% se utilizarán como conjunto de entrenamiento. Además proporcionaremos una semilla para el generador de numeros aleratorios, lo que nos garantizará que la división de los datos sea reproducible. Estos conjuntos se utilizarán para entrenar y evaluar los modelos de aprendizaje automático. La división en conjuntos de entrenamiento y prueba es fundamental para evaluar el rendimiento del modelo en datos no vistos y evitar el sobreajuste.
    8. Normalizamos las características para que el modelo tenga un mejor rendimiento y de esta manera poder evitar el sesgo por características que tienen valores mayores.Configurar datos en valores entre 0 y 1 es importante tener en cuenta que muchos algoritmos de aprendizaje automatico, en especial en especial aquellos que son sensibles a la escala de caracteristicas como las SVM, redes neuronales y los algoritmos de gradiente descendente, el uso de 'MinMaxScaler' asegura que las caracteristicas estén en el mismo rango, lo que ayuda a mejorar la convergencia del modelo y su rendimiento general.
    
A nivel general dentro del análisis desarrollado en los modelos se tomo en cuenta en cada uno:

    1. Análisis de la Matriz de Confusión
    2. Análisis de la Puntuación de Precisión
    3. Análisis de Sensibilidad y Valor F1
    
    RANDOM FOREST
    
    1. Análisis de la Matriz de Confusión
    
    * Verdaderos positivos (TP): 70 casos fueron correctamente clasificados como positivos (cáncer de mama).
    * Verdaderos negativos (TN): 40 casos fueron correctamente clasificados como negativos (no cáncer de mama).
    * Falsos positivos (FP): 3 casos fueron incorrectamente clasificados como positivos (falsos alarmas de cáncer de mama).
    * Falsos negativos (FN): 1 caso fue incorrectamente clasificado como negativo (cáncer de mama no detectado).

En base a los resultados del modelo de Random Forest podemos decir que logró un buen rendimiento, con un pequeño número de falsos positivos y falsos negativos. Esto indica que el modelo tiene una buena capacidad para distinguir entre los casos de cáncer de mama y los casos sin cáncer de mama en el conjunto de prueba.
    
    2. Análisis de la Puntuación de Precisión
    
La precisión del modelo de Random Forest es del 95.89%. Esto significa que el 95.89% de las muestras que el modelo clasificó como positivas (cáncer de mama) fueron verdaderamente positivas, mientras que el resto fueron falsos positivos. 

La precisión es una métrica importante que indica la proporción de predicciones positivas que son correctas en relación con el total de predicciones positivas realizadas por el modelo.

En nuestro contexto el alta precisión significa que el modelo tiene una baja tasa de falsos positivos, lo cual es importante para evitar diagnosticar erróneamente a pacientes sanas como positivas.

    3. Análisis de Sensibilidad y Valor F1
   
El modelo de Random Forest tiene una sensibilidad (recall) del 98.59% y un valor F1 del 97.22%. Esto nos dice que el modelo es muy efectivo en identificar correctamente los casos positivos de cáncer de mama (verdaderos positivos) y minimizar tanto los falsos negativos como los falsos positivos.

La sensibilidad (recall) del 98.59% indica que el modelo identifica correctamente el 98.59% de todos los casos positivos de cáncer de mama en el conjunto de prueba. En otras palabras, de todas las muestras que realmente son positivas, el 98.59% fueron correctamente identificadas por el modelo como positivas.

El valor F1 del 97.22% es una medida combinada de precisión y sensibilidad que proporciona una evaluación equilibrada del modelo. Un valor alto de F1 indica un buen equilibrio entre precisión y sensibilidad. En este caso, el valor F1 nos sugiere que el modelo tiene un buen rendimiento en términos de minimizar tanto los falsos positivos como los falsos negativos.
    
    REGRESION LOGÍSTICA
    
    1. Análisis de la Matriz de Confusión

    * Verdaderos positivos (TP): 71 casos fueron correctamente clasificados como positivos (cáncer de mama).
    * Verdaderos negativos (TN): 41 casos fueron correctamente clasificados como negativos (no cáncer de mama).
    * Falsos positivos (FP): 2 casos fueron incorrectamente clasificados como positivos (falsos alarmas de cáncer de mama).
    * Falsos negativos (FN): 0 casos fueron incorrectamente clasificados como negativos (cáncer de mama no detectado).

El modelo de Regresión Logística tiene un buen desempeño en la detección del cáncer de mama en el conjunto de prueba, con una cantidad muy baja de falsos positivos y falsos negativos. Esto sugiere que el modelo tiene una alta precisión y sensibilidad en la clasificación de los casos de cáncer de mama.

    2. Análisis de la Puntuación de Precisión
    
La puntuación de precisión del Modelo 2 (Regresión Logística) es del 97.26%. Esto significa que el 97.26% de las muestras que el modelo clasificó como positivas (cáncer de mama) fueron verdaderamente positivas, mientras que el resto fueron falsos positivos.

La precisión es una métrica importante que indica la proporción de predicciones positivas que son correctas en relación con el total de predicciones positivas realizadas por el modelo.

En la detección de cáncer de mama, una alta precisión significa que el modelo tiene una baja tasa de falsos positivos, lo cual es importante para evitar diagnosticar erróneamente a pacientes sanas como positivas.
    
    3. Análisis de Sensibilidad y Valor F1
    
Para el Modelo 2 (Regresión Logística), ha calculado una sensibilidad (recall) del 100% y un valor F1 del 98.61%.

Ante los valores obtenidos podemos decir que son resultados muy buenos:

Un recall del 100% significa que el modelo identificó correctamente todas las muestras positivas de cáncer de mama en el conjunto de prueba. No hubo ningún falso negativo, lo que sugiere que el modelo es muy sensible para detectar los casos positivos.

Un valor F1 del 98.61% indica un buen equilibrio entre precisión y sensibilidad. Es una medida combinada que tiene en cuenta tanto la precisión como el recall del modelo. Un valor F1 alto nos indica que el modelo tiene un buen rendimiento en términos de minimizar tanto los falsos positivos como los falsos negativos.

El Modelo de Regresión Logística muestra un excelente desempeño en la detección del cáncer de mama en el conjunto de prueba.
    
    SVM (Support Vector Machine)
    
    1. Análisis de la Matriz de Confusión
    
    Interpretación:

    * Verdaderos positivos (TP): 70 casos fueron correctamente clasificados como positivos (cáncer de mama).
    * Verdaderos negativos (TN): 41 casos fueron correctamente clasificados como negativos (no cáncer de mama).
    * Falsos positivos (FP): 2 casos fueron incorrectamente clasificados como positivos (falsos alarmas de cáncer de mama).
    * Falsos negativos (FN): 1 caso fue incorrectamente clasificado como negativo (cáncer de mama no detectado).

El Modelo SVM (Support Vector Machine) también tiene un buen desempeño en la detección del cáncer de mama en el conjunto de prueba, con una cantidad muy baja de falsos positivos y un solo falso negativo.

Esto sugiere que el modelo tiene una alta precisión y sensibilidad en la clasificación de los casos de cáncer de mama, aunque hay una pequeña diferencia con respecto al Modelo 2 de REGRESION LOGÍSTICA.
    
    2. Análisis de la Puntuación de Precisión
    
La puntuación de precisión del Modelo 3 (SVM) es del 97.22%. Esto significa que el 97.22% de las muestras que el modelo clasificó como positivas (cáncer de mama) fueron verdaderamente positivas, mientras que el resto fueron falsos positivos.

La precisión es una métrica importante que indica la proporción de predicciones positivas que son correctas en relación con el total de predicciones positivas realizadas por el modelo.
    
    3. Análisis de Sensibilidad y Valor F1
    
Para el Modelo 3 (SVM), ha calculado una sensibilidad (recall) del 98.59% y un valor F1 del 97.90%.

Un recall del 98.59% indica que el modelo identificó correctamente casi todas las muestras positivas de cáncer de mama en el conjunto de prueba. Sin embargo, hubo algunos casos de falsos negativos, lo que sugiere que el modelo podría haber pasado por alto algunos casos positivos.

Un valor F1 del 97.90% es una medida combinada de precisión y sensibilidad. Es una métrica útil para evaluar el equilibrio entre precisión y recall del modelo. Un valor alto de F1 indica un buen equilibrio entre estas dos métricas.

El Modelo SVM muestra un buen desempeño en la detección del cáncer de mama en el conjunto de prueba, aunque hay margen de mejora para reducir aún más la tasa de falsos negativos.

CONCLUSIÓN DEL ANALISIS DE LOS MODELOS DE APRENDIZAJE.

En base a los resultados obtenidos podemos afirmar que:

Los tres modelos funcionan bien, pero el principal objetivo es centrarnos en minimizar los falsos positivos, pues es importante que se pasen por alto los casos malignos.

Dentro de los tres modelos evaluadores el que destaca y minimiza los falsos positivos es el modelo de Regresión Logística el cual logra:

        Un 100% para casos malignos lo que significa que identifica eficientemente todas las muestras malignas ante estos resultados es importante tener en cuenta que un rendimiento perfecto en el conjunto de entrenamiento puede indicarnos un sobreajuste, por lo que se deberia evaluar el modelo en un conjunto de datos independientes.

        La puntuación F1 es alta 0.9861111111111112 el 98.61% indica un buen equilibrio entre precisión y sensibilidad. Es una medida combinada que tiene en cuenta tanto la precisión como el recall del modelo. Un valor F1 alto nos indica que el modelo tiene un buen rendimiento en términos de minimizar tanto los falsos positivos como los falsos negativos.


