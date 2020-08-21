
# Máster en Data Science

## Predicción de la contaminación en Barcelona

### Objetivo

El ánalisis tiene como objetivo la predicción de la contaminación en Barcelona. Para este estudio se ha utilizado distintas fuentes de datos:

-Los datos de contaminación  y los datos meteorológicos de Barcelona, adquiridos mediante los datos abiertos de Catalunya.

-Los datos de los sensores de tráfico de Barcelona, adquiridos mediante Opendata Bcn.

### Descripción de los datos 

#### Datos de la contaminación

Los datos de la contaminación se encuentran en los datos abiertos de Catalunya en la división de 'Dades d'immissió dels punts de mesurament de la Xarxa de Vigilància i Previsió de la Contaminació Atmosfèrica'.

En Barcelona hay diez estaciones de medición de contaminación, estos datos comprenden un período de tres años desde enero del 2017 a diciembre de 2019. Para hacer este proyecto se ha seleccionado sólo tres 
estaciones de las diez estaciones que hay en Barcelona porque no había datos en todas las estaciones. Esa estación es Sants, que sólo tiene mediciones de los óxidos de nitrógeno de esta manera se ha acotado el
 proyecto. A continuación, se han seleccionado las dos otras estaciones que tienen estos contaminantes, el Eixample y Sant Gervasi-Gràcia.

A continuación, Los datos de la contaminación se limpian hasta obtener la serie temporal para poder hacer los modelos para obtener las predicciones.

#### Datos de las variables meteorológicas

Los datos de las variables meteorólogicas se encuentran en los datos abiertos de Catalunya en la división de 'Dades meteorológicas del XEMA'.

Hay cuatro estaciones meteorológicas en Barcelona pero para poder acotar el proyecto se ha hecho un mapa a partir de la librería de folium donde se han creado unos círculos con un radio de 3000 el centro de 
círculos son las estaciones de medición de la contaminación que se ha elegido anteriormente. Esto da como resultado que las estaciones meteorológicas de Zona Universitaria y el Raval las relacionamos con la
 estación de contaminates de Sants. Las estaciones meteorológicas del Raval y la situada en el Zoo van relacionada con la estación de contamianción del Eixample.Y finalmente, la estación meteorológica del
 Raval va relacionada con la estación de Sant Gervasi-Gràcia. De esta forma cuando se han hecho los modelos se han realizado de esta forma. 

Como los datos ade la contaminación se tienen que limpiar hasta obtener la serie temporal para poder obtener las predicciones.

#### Datos de los sensores de tráfico

Los datos de los sensores de tráfico se encuentran en Opendata Bcn en la división de aforo de valores de IMD.

Barcelona tiene más de 600 sensores de tráfico se debe acotar la selección. Para hacerlo se ha procedido hacer  un mapa con unos córculos con un radio de 270 donde el centro de los círculos son las estaciones 
de la medición de la contaminación. Cuando se han creado estos círculos se han seleccioando los sensores para las distintas estaciones.Para la estación del Eixample s eha relacionado con los sensores 4071,
 4095 y 20013, a continuación la estación de Sants se relaciona con los sensores 2020 y 2021 y, por último la estación de Sant Gervasi-Gràcia se relaciona con los sensores 8001 y 8039.

Como los datos anteriores se deben limpiar y preparar para obtener la serie temporal para obtener las predicciones.

### Predicción de la contaminación
 
Para realizar la mejor predicción posible con los datos listos se han utilizado distintos modelos para llegar a una buena predicción.
Primero, se ha intentado con un modelo Arima pero se ha visto que es bueno sólo para tener un buen baseline. Después de esto, se ha hecho una regresión lineal para ver si ajusta mejor pero como se puede 
comprobar en los notebooks se ve que no. Para tener un poco más de libertad en la exploración de los datos y metiendo todas las features de las variables meteorológicas y de los sensores de tráfico pero 
tampoco da un buen resultado.
A continuación, para poder mejorar la predicción de los datos se ha escogido los árboles de decisión con regresión al principio no daba una buena predicción pero este modelo tiene un parámetro llamado
max_depth que controla la profundidad de los árboles con ello hace que el modelo empieza ajustarse pero no lo suficiente. Por eso se ha procedido con otra técnica de machine learning,
el ensemble. La primera técnica esta dentro de la técnica del bagging donde se combina diferentes árboles para poder obtener una mejor predicción es el Random Forest. Pero no ajustado bien por eso se han creado
diferentes features para poder ajustarlo mejor y que la predicción sea mejor. Se ha podido comprobar que sí pero aún puede ser mejor por eso se ha procedido con la técnica del boosting para esto se ha utilizado
el algoritmo del XGBoost donde se ha podido comprobar que es el mejor modelo que se ha visto en el proyecto el score del modelo es muy alto.
Todos estos modelos se han hecho para todos las estaciones de contaminates para cada contaminante en relación a sus variables meteorológicas y los sensores de tráfico que les corresponde.

### Visualizaciones

 



