----- ENGLISH VERSION -----

This work was carried out by [Hugo Thomas](https://perso.univ-rennes2.fr/hugo.thomas) and [Florent Demoraes](https://perso.univ-rennes2.fr/florent.demoraes) at the CNRS ESO research unit in Rennes (France), between June and December 2023. This study is part of a PhD thesis developed by Hugo Thomas (Université Rennes 2, France / Universidad de los Andes, Colombia) and also part of the activities of the [Modural program](https://modural.hypotheses.org/le-projet) funded by the French National Research Agency. The methods developed in R and applied to Bogotá and Lima are replicable to other urban areas and other mobility surveys using other travel modes.

# Routing shortest path distance in road and public transport

This repository contains scripts and data to carry out network-based distance computation based on a Household Travel Survey conducted in 2019 (HMS 2019) in Bogotá, and a Household Travel Survey conducted in 2012 (HMS 2012) in Lima. The analysis uses database representing 22,000 households and 120,000 trips in each city, as well as road and public transport networks downloaded from OpenStreetMap or open data repositories. The main outputs of this section are the trips databases of both cities with an additional variable accounting for the length of  each trip. 

The first scripts do the following:

* Counting the number of occurrences of each OD pair in the trips database and producing a heatmap.
* Providing a sensibility test of the location of the start and end point in each ZAT.
* Discussing the impact of the main mode assignation.
* Computing distance for each trip on the database, for all possible modes.
* Producing basic statistics about distance in Lima.
* Showing trip examples and discussing routing issues.

Please find below:

* The R script for [Bogotá](Bogota_Routing_Distance_4.Rmd) and [Lima](Lima_Routing_Distance_v2.Rmd).
* The HTML rendering for [Bogotá](Bogota_Routing_Distance_4.html) and [Lima](Lima_Routing_Distance_v2.html).
* The data used in this project for [Bogotá](https://bit.ly/42mtehp) and [Lima](https://bit.ly/3Ou7fzh).

# Producing original maps of mobility demand, greenhouse gas and air pollution emissions

In a second time, distance-based indicators were produced and mapped in [Bogotá](Bogota_Distance_Mapping_EN.Rmd) and [Lima](Lima_Distance_Mapping_EN.Rmd) using spatial smoothing to seek visual effectiveness. We included indicators such as:

* Total passengers-kilometers traveled (PKT) per day according to the place of residence and the trip purpose.
* Average distance per capita according to the place of residence and the main mode.
* Total greenhouse gas (GHG) emissions per day.
* GHG emissions per capita.
* Total daily emissions of the pollowing air pollutants: CO, NOx, PM.2.5.
* Air pollutants emissions per capita.

 Please find below:
* The R script for [Bogotá](Bogota_Distance_Mapping_EN.Rmd) and [Lima](Lima_Distance_Mapping_EN.Rmd).
* The HTML rendering for [Bogotá](Bogota_Distance_Mapping_EN.html) and [Lima](Lima_Distance_Mapping_EN.html).
  
# Key words

_daily mobility; household travel survey; R script; network routing; passengers-kilometers traveled; GHG emissions; air pollution_

