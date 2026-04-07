# Bike-Sharing-UCI

El Bike Sharing Dataset es un conjunto de datos multivariado utilizado principalmente para tareas de regresión que contiene registros horarios y diarios del número de bicicletas alquiladas en el sistema Capital Bikeshare entre 2011 y 2012, integrando variables temporales (fecha, hora, estación), condiciones climáticas (temperatura, humedad, viento) y factores contextuales (días festivos, laborales), con un total de 17,389 instancias y 13 variables principales, donde la variable objetivo es el número total de alquileres (cnt); este dataset es ampliamente usado en análisis de series temporales y aprendizaje automático, ya que refleja el comportamiento de movilidad urbana y permite modelar la demanda de bicicletas en función de factores ambientales y temporales.

La columna dteday fue convertida de tipo object a datetime para permitir la extracción de características temporales.
Se crearon las siguientes nuevas columnas a partir de dteday para capturar patrones de tiempo: year, month, day, weekday, dayofyear, weekofyear, hour, is_weekend.
Una vez extraídas las características, la columna dteday original fue eliminada ya que los modelos de ML trabajan mejor con representaciones numéricas de tiempo.
La columna instant, siendo un identificador consecutivo sin valor predictivo, fue eliminada para evitar posibles problemas como el sobreajuste en los modelos.
