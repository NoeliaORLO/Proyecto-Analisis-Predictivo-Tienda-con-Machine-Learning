# Proyecto: Análisis Predictivo de Ventas para una Tienda con Machine Learning 🛒🤖
Proyecto con Aprendizaje Supervisado que predice las ventas del año 2026 para una tienda minorista basándose en ventas previas del año 2022.
 
## ¿Qué pretende este proyecto?
Este es mi primer proyecto aplicando Machine Learning, en concreto Aprendizaje Supervisado, a través del uso del modelo predictivo de Bosque Aleatorio 🏕️. 
Combino conocimientos de Pandas, NumPy, Matplotlib y Seaborn a lo largo de todo el proyecto, generando visualizaciones para interpretar los resultados.
 
Primero genero un DataFrame a partir del archivo "Ventas.csv", el cual contiene los datos de ventas de todos los días del año 2022, con las columnas Fecha, DíaDeLaSemana, Promociones (0/1), Festivo (0/1) y Ventas.
Tras la preparación de los datos y su preprocesamiento (transformación del tipo de dato Fecha, creación de una nueva columna Mes...), elijo las variables independientes y la variable dependiente del modelo, 
dividiendo los datos en grupo de entrenamiento (85%) y grupo de prueba (15%) con `train_test_split`. Utilizo `random_state` para fijar la semilla generadora de números aleatorios y garantizar la reproducibilidad.
 
Posteriormente realizo un EDA (Análisis Exploratorio de Datos) generando con Seaborn varios gráficos de tipo barplot para analizar el comportamiento de las ventas de 2022, sacando como conclusión que la variable 
que más influye en las ventas es el día de la semana, y descubriendo que Festivo es redundante, ya que los únicos festivos que hay en los datos son los domingos.
 
Tras ello, selecciono el modelo más adecuado de entre Regresión Lineal, Árbol de Decisión y Bosque Aleatorio. Tras comparar sus Coeficientes de Determinación (R²), elijo este último, y procedo a entrenarlo con el 
conjunto de entrenamiento y a evaluarlo sobre el conjunto de prueba.
 
Por último, genero con ayuda de Claude un nuevo csv con datos simulados de Ventas de 2026, sobre el que aplico el modelo para predecir las ventas, y muestro en un gráfico la comparación de ventas a lo largo de los
días de la semana del año 2022 y del año 2026. Únicamente uso este gráfico ya que, como se ve en el último punto, "Importancia de cada variable en el modelo", el día de la semana influye casi al 100% en las ventas.
 
## Para ejecutar el script...
Se necesita tener un intérprete de Python que contenga las librerías Pandas, NumPy, Matplotlib, Seaborn y Scikit-Learn. En mi caso yo uso conda (obtenible mediante la descarga de Anaconda), 
ejecutando el notebook desde Jupyter Notebook o VS Code.
