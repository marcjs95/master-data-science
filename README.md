
# Máster en Data Science

## Predicción de la contaminación en Barcelona

### Objetivo

El ánalisis tiene como objetivo la predicción de la contaminación en Barcelona. Para este estudio se ha utilizado distintas fuentes de datos:

-Los datos de contaminación  y los datos meteorológicos de Barcelona, adquiridos mediante los datos abiertos de Catalunya.

-Los datos de los sensores de tráfico de Barcelona, adquiridos mediante Opendata Bcn.

### Descripción de los datos 

#### Datos de la contaminación

En Barcelona hay diez estaciones de medición de contaminación, estos datos comprenden un período de tres años, desde enero del 2017 a diciembre de 2019. Para hacer este proyecto, se ha seleccionado sólo tres 
estaciones de las diez estaciones que hay en Barcelona, porque no había datos en todas las estaciones.

Las estaciones seleccionadas son Sants, el Eixample y Sant Gervasi-Gràcia. 

Los contaminantes seleccionados son los óxidos de nitrógeno porque Sants sólo registra estos contamiantes.

A continuación, Los datos de la contaminación se limpian hasta obtener la serie temporal para poder hacer los modelos y así,  obtener las predicciones.

#### Datos de las variables meteorológicas

Las estaciones seleccionadas son el Raval, Zona Universitat y Zoo.

Las variables seleccionadas son la temperatura, el viento, la humedadd relativa, la presión y la precipitación. 

Como los datos de la contaminación se tienen que limpiar hasta obtener la serie temporal y así, obtener las predicciones.

#### Datos de los sensores de tráfico

Barcelona tiene más de 600 sensores de tráfico se debe acotar la selección.

Los sensores selecionados han sido el 4071, 4095, 20013, 2020, 2021, 8001 y 8039, con su respectiva zona.

Como los datos anteriores se deben limpiar y preparar para obtener la serie temporal y así, obtener las predicciones.

### Predicción de la contaminación
 
Para realizar la mejor predicción posible con los datos listos, se ha utilizado distintos modelos para llegar a una buena predicción.

Los modelos que se han llevado ha cabo son ARIMA, Regresión Lineal, Polinómica, Árboles de Decisión, Random Forest y  XGBoost.

Todos estos modelos, se han hecho para todos las estaciones de contaminates para cada contaminante en relación a sus variables meteorológicas y los sensores de tráfico que les corresponde.

### Visualizaciones

Para poder ver la relación entre los contaminantes y los parámetros seleccionados, se han hecho distintos dashboards con Tableau.  



