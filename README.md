# ML_PROYECTO_AlanJafetLeonLoeza

## INSTRUCCIONES DEL PROYECTO

Objetivos:
•	Que el estudiante pueda emplear técnicas de ML para realizar predicciones.
•	Que el estudiante siga reforzando sus conocimientos en el análisis y exploración de los datos.
•	Que el estudiante siga realizando actividades que pueda subir en su Git para crear un portafolio de proyectos.
Descripción de la actividad:
Este proyecto consiste en cuatro etapas principales:
1.	EDA.
2.	Manipulación y tratamiento de los datos.
3.	Machine Learning
4.	Presentación del proyecto.

El dataset a utilizar se llama “cirrhosis.csv, en la imagen se muestra la información del dataset. 
![image](https://github.com/jallrampage/ML_PROYECTO_AlanJafetLeonLoeza/assets/108102222/e0f72f88-79c3-463a-8b19-0f56afb088f9)

Desgloce de pasos: 

PARTE I: EDA.
Paso 1. Carga y muestra.
- Cargue el dataset llamado "cirrhosis.csv" en un dataframe, posteriormente muestre su información.
Paso 2. Análisis estadístico.
- De las columnas numéricas, muestre la información estadística relevante (promedio, cuartíles, desviación estándar y coeficiente de variación).
- A través del coeficiente de variación determine qué columnas presentan mucha dispersión en sus datos.
Paso 3. Búsqueda de nulos y datos atípicos.
- Muestre cuántos datos nulos tienen las columnas, puede apoyarse de un gráfico para mostrar la cantidad de nulos que hay.
- Muestre las distribuciones de las columnas numéricas y mencione si presentan datos atípicos/anomalías/outliers.
Paso 4. Análisis de categorización.
- Revise las columnas que son de tipo objeto, analice la cantidad de posibilidades que tienen.
- Determine si una (o algunas) puede ser categorizable, aún no la(s) categorice.
Paso 5. Correlación y análisis del problema.
- Muestre la correlación de los datos numéricos con respecto a la columna "Status", para ello tendrá que volver numérica dicha columna (para este paso puede usar un encoder).
- El objetivo es predecir con estos datos la variable "Status".
- ¿Con los datos que se tienen se puede predecir correctamente esa variable?
- Si tuviera que seleccionar un modelo para hacer las predicciones, ¿cuál sería?

  
PARTE II: MANIPULACIÓN Y TRATAMIENTO.
Paso 1. Tratamiento de datos nulos.
- Trate los datos nulos acorde a lo que se ha visto previamente en el curso.
- Muestre la cantidad de datos nulos antes y después del tratamiento.
Paso 2. Tratamiento de anomalías.
- Enfrente los datos extremos y las anomalías.
- Es libre de utilizar los métodos que prefiera, trate de no perder muchos datos (se tiene un dataset pequeño).
- Muestre las distribuciones tratadas antes y después del tratamiento.
Paso 3. Categorización.
- Seleccione las columnas de tipo objeto candidatas a la categorización.
- Realice la categorización.
- Muestre la información del dataframe para demostrar que se realizó con éxito.
Paso 4. Tratamiento de incosistencias.
- En la categorización anterior, ¿hay inconsistencias?
- Revise las posibles opciones de cada columna categorizada, si encuentra alguna inconsistencia hay que tratarla.
- Puede emplear gráficas de conteos para validar si una categoría se podría considerar como inconsistente.
Paso 5. Conversión a numérico.
- Ya que tiene un dataframe sin datos nulos, sin inconsistencias y sin anomalías, hay que convertirlo a numérico.
- Emplee un tipo de encoding adecuado a cada columna.
- Construya un nuevo dataframe completamente numérico (incluyendo "Status", este debe ser forzosamente mediante LabelEncoding).
- Muestre la información del nuevo dataframe.


PARTE III: MACHINE LEARNING.
Paso 1. División de los datos.
- Divide las columnas en la variable "X" y la variable "y".
- Muestree los datos en dos: entrenamiento y pruebas. La proporción de cada muestra queda a decisión suya.
- Utilice una semilla para que los resultados puedan ser reproducibles.
Paso 2. Abordaje mediante modelo simple.
- Importe un modelo simple de ML, puede ser KNN, Regresión Logística o un árbol de decisión.
- Entrene el modelo con los datos y realice las predicciones con la muestra de pruebas.
- Muestre los resultados con f1_score, accuracy_score y classification_report.
- Analizando el reporte de clasificación, ¿qué tal se desempeñó su modelo?
Paso 3. Mejorando el modelo.
- Emplee GridSearchCV para encontrar los mejores hiperparámetros para su modelo.
- Valide con varias opciones.
- Si su modelo no logra mejorar mucho, no se preocupe, es parte del aprendizaje.
Paso 4. Ensambles.
- Utilice el ensamble de VotingClassifier para mejorar el rendimiento.
- Seleccione al menos 4 modelos simples diferentes y úselos dentro del ensamble (Stacking).
- Entrene el meta-modelo y valide su rendimiento con f1_score, accuracy_score y classification_report.
- Analizando el classification_report, ¿qué tal se desempeñó el modelo?
Paso 5. Modelo supremo.
- Con los resultados del paso 4 y 5, determine qué camino seguirá: tomar un modelo y mejorarlo o usar el meta-modelo y mejorarlo.
- Mejore su modelo hasta el máximo, para eso se recomienda utilizar una Pipeline (puede ser con Pipeline o make_pipeline).
- Dependiendo del modelo que haya seleccionado, debe buscar mejores hiperparámetros, escalar, normalizar, estandarizar o hacer cambios importantes en los datos (como seleccionar únicamente las variables de mayor correlación), también puede emplear PCA para reducir dimensionalidad.
- El objetivo es que el modelo generado en este paso sea superior a los modelos del paso 4 y 5.
- Para este paso también puede utilizar las SVM, RandomForest y Redes Neuronales Artificiales (SKLearn).


PARTE IV. PRESENTACIÓN.
- Emplee PCA con las columnas de la variable X (con los datos completos) y reduzca su dimensionalidad a 2.
- Muestre un gráfico de dispersión entre esas dos características PCA y colorice con la columna "Status". Para esto puede construir un nuevo dataframe con las 2 columnas obtenidas por PCA y añadiendo la columna "Status" antes de la transformación.
- Analice si los grupos se pueden separar dentro de ese gráfico.
