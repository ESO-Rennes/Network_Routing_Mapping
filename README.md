----- VERSION EN ESPAÑOL -----

Este trabajo fue realizado por [Hugo Thomas](https://perso.univ-rennes2.fr/hugo.thomas) y [Florent Demoraes](https://perso.univ-rennes2.fr/florent.demoraes) en la unidad de investigación ESO CNRS en Rennes (Francia), entre junio y diciembre de 2023. Este estudio es parte de la tesis doctoral de Hugo Thomas (Université Rennes 2, Francia / Universidad de los Andes, Colombia) así como de las actividades del [programa Modural](https://modural.hypotheses.org/le-projet-modural/el-proyecto) con recursos de la Agencial Nacional de Investigación Francesa (ANR). Los métodos desarrollados en R y aplicados a Bogotá y Lima son replicables a otras areas urbanas y encuestas de mobilidad abarcando otros modos de transporte.

![Bogota Smoothed map total distance-1.png](https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Bogota%20Smoothed%20map%20total%20distance-1.png)

![Lima Smoothed map total distance-1.png](https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Lima%20Smoothed%20map%20total%20distance-1.png)

# Cálculo de la distancia por el camino más corto en la red vial y la red de transporte público

Este repositorio contiene scripts y datos para calcular distancias por la red vial y la red de transporte público basadas en la Encuesta Origen-Destino de Hogares de 2019 (EODH 2019) en Bogotá y la Encuesta Origen-Destino de Hogares de 2012 (EODH 2012) en Lima. El análisis utiliza bases de datos de approx. 22,000 hogares y 120,000 viajes en cada ciudad, así como redes vial y de transporte público bajados de OpenStreetMap u otros repositorios de datos abiertos. Los principales productos de esta sección son las bases de viajes de cada ciudad con una variable adicional marcando la distancia de cada viaje.

Los primeros scripts hacen lo siguiente:

* Contar el número de acontecimientos de cada par OD en la base de viajes, y producir un mapa de calor.
* Realizar un análisis de sensibilidad de la ubicación de los puntos de inicio y fin de recorrido en cada ZAT.
* Discutir el impacto del método de asignación del modo principal.
* Calcular la distancia de cada viaje en la base, para todos los modos existentes.
* Producir estadística básica acerca de la distancia y los pasajeros-kilómetros recorridos (PKT).
* Mostrar ejemplos de viajes y discutir algunas cuestiones de enrutamiento.

Abajo encontrará:

* El script R para [Bogotá](Bogota_Routing_Distance_4.Rmd) y [Lima](Lima_Routing_Distance_v2.Rmd).
* El archivo HTML para [Bogotá](https://htmlpreview.github.io/?https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Bogota_Routing_Distance_4.html) y [Lima](https://htmlpreview.github.io/?https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Lima_Routing_Distance_v2.html).
* Los datos utilizados para [Bogotá](https://bit.ly/42mtehp) y [Lima](https://bit.ly/3Ou7fzh).

# Producción de mapas originales de la demanda de mobilidad y las emisiones de gases de efecto invernadero (GEI) y contaminantes aéreos

En un segundo tiempo, se produjo y mapeó indicadores basados en la distancia utilizando lisado espacial (spatial smoothing), buscando la eficiencia visual para el lector. Los indicadores calculados abarcan:

* Pasajeros-kilómetros totales (PKT) por día, dependiendo del lugar de residencia y del motivo de viaje.
* Distancia promedio per cápita dependiendo del lugar de residencia y del modo principal.
* Emisiones de GEI totales por día.
* Emisiones de GEI per cápita.
* Emisiones cotidianas totales de los siguientes contaminantes aéreos: CO, NOx, PM.2.5.
* Emisiones de contaminantes aéreos per cápita.

![Bogota Smoothed map car distance-1.png](https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Bogota%20Smoothed%20map%20car%20distance-1.png)

![Lima Smoothed map car distance-1.png](https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Lima%20Smoothed%20map%20car%20distance-1.png)

Abajo encontrará:
* El script R para [Bogotá](Bogota_Distance_Mapping_EN.Rmd) y [Lima](Lima_Distance_Mapping_EN.Rmd).
* El archivo HTML para [Bogotá](https://htmlpreview.github.io/?https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Bogota_Distance_Mapping_EN.html) y [Lima](https://htmlpreview.github.io/?https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Lima_Distance_Mapping_EN.html).


# Palabras clave

_mobilidad cotidiana; encuesta de movilidad de hogares; script R; cálculo de distancia por la red vial; pasajeros-kilómetro recorridos; emisiones de GEI; contaminación del aire_

----- ENGLISH VERSION -----

This work was carried out by [Hugo Thomas](https://perso.univ-rennes2.fr/hugo.thomas) and [Florent Demoraes](https://perso.univ-rennes2.fr/florent.demoraes) at the CNRS ESO research unit in Rennes (France), between June and December 2023. This study is part of a PhD thesis developed by Hugo Thomas (Université Rennes 2, France / Universidad de los Andes, Colombia) and also part of the activities of the [Modural program](https://modural.hypotheses.org/le-projet) funded by the French National Research Agency. The methods developed in R and applied to Bogotá and Lima are replicable to other urban areas and other mobility surveys using other travel modes.

![Bogota Smoothed map total distance-1.png](https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Bogota%20Smoothed%20map%20total%20distance-1.png)

![Lima Smoothed map total distance-1.png](https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Lima%20Smoothed%20map%20total%20distance-1.png)

# Routing shortest path distance in road and public transport networks

This repository contains scripts and data to carry out network-based distance computation based on a Household Travel Survey conducted in 2019 (HMS 2019) in Bogotá, and a Household Travel Survey conducted in 2012 (HMS 2012) in Lima. The analysis uses databases representing approx. 22,000 households and 120,000 trips in each city, as well as road and public transport networks downloaded from OpenStreetMap or open data repositories. The main outputs of this section are the trips databases of both cities with an additional variable accounting for the length of  each trip. 

The first scripts do the following:

* Counting the number of occurrences of each OD pair in the trips database and producing a heatmap.
* Providing a sensibility test of the location of the start and end point in each ZAT.
* Discussing the impact of the main mode assignation.
* Computing distance for each trip on the database, for all possible modes.
* Producing basic statistics about distance and passengers-kilometers traveled (PKT).
* Showing trip examples and discussing routing issues.

Please find below:

* The R script for [Bogotá](Bogota_Routing_Distance_4.Rmd) and [Lima](Lima_Routing_Distance_v2.Rmd).
* The HTML rendering for [Bogotá](https://htmlpreview.github.io/?https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Bogota_Routing_Distance_4.html) and [Lima](https://htmlpreview.github.io/?https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Lima_Routing_Distance_v2.html).
* The data used in this project for [Bogotá](https://bit.ly/42mtehp) and [Lima](https://bit.ly/3Ou7fzh).

# Producing original maps of mobility demand, greenhouse gas and air pollution emissions

In a second time, distance-based indicators were produced and mapped using spatial smoothing to seek visual effectiveness. We included indicators such as:

* Total passengers-kilometers traveled (PKT) per day according to the place of residence and the trip purpose.
* Average distance per capita according to the place of residence and the main mode.
* Total greenhouse gas (GHG) emissions per day.
* GHG emissions per capita.
* Total daily emissions of the pollowing air pollutants: CO, NOx, PM.2.5.
* Air pollutants emissions per capita.

![Bogota Smoothed map car distance-1.png](https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Bogota%20Smoothed%20map%20car%20distance-1.png)

![Lima Smoothed map car distance-1.png](https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Lima%20Smoothed%20map%20car%20distance-1.png)

 Please find below:
* The R script for [Bogotá](Bogota_Distance_Mapping_EN.Rmd) and [Lima](Lima_Distance_Mapping_EN.Rmd).
* The HTML rendering for [Bogotá](https://htmlpreview.github.io/?https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Bogota_Distance_Mapping_EN.html) and [Lima](https://htmlpreview.github.io/?https://github.com/ESO-Rennes/Network_Routing_Mapping/blob/main/Lima_Distance_Mapping_EN.html).


  
# Key words

_daily mobility; household travel survey; R script; network routing; passengers-kilometers traveled; GHG emissions; air pollution_

