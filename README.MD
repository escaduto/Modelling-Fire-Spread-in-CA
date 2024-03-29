# A Comprehensive Guide to: <u>Understanding Fire Driver’s Across California’s Diverse Ecoregions</u>

## Table of Contents  
- [Project Description](#project-Description)  
- [Introduction](#introduction)  
- [Primary Packages](#primary-packages)  
- [Study Region](#study-region) 
- [Methods](#methods)  
- [Supplemental Figures](#bay-area-2020-fires)
___


## Project Description
Wildland fires at varying intensities and frequencies are a critical ecological process across the western United States. Variability in fire behavior is heavily influenced by dynamic and often complex interactions between meteorological and biophysical components.
 
We here used a machine learning approach to investigate what factors caused the rapid spread of large wildfires in the recent decade, across six distinct ecoregions in California. Continuous daily fire spread and area burned were derived from MODIS and VIIRS active fire products.
 
The results from this study seek to provide insights on the efficacy of fuel management on reducing the rate of fire progression across ecologically diverse regions and help communities and managers to better anticipate and mitigate future risk of fast moving wildfires in the coming decades.

---

## Introduction

<figure class="image">
  <img src="./docs/assets/Figure1.jpg" alt="workflow diagram">
  <figcaption>Figure 1. High level diagram outlining modeling framework</figcaption>
</figure>


## Primary packages 

I. Setting up
* Colab: [What is Colaboratory](https://colab.research.google.com/notebooks/intro.ipynb)
* Earth Engine Python API: [Python Installation | Google Earth Engine](https://developers.google.com/earth-engine/guides/python_install)

II. Data & Spatial Processing
* Geopandas: [GeoPandas 0.8.0 — GeoPandas 0.8.0 documentation](https://geopandas.org/)
* Shapely: [Shapely · PyPI](https://pypi.org/project/Shapely/)
* NumPy: [NumPy.org](https://numpy.org/)
* Rtree: [Rtree · PyPI](https://pypi.org/project/Rtree/)
* GDAL: [GDAL — GDAL documentation](https://gdal.org/)

III. Visualization
* Matplotlib: [Matplotlib: Python plotting — Matplotlib 3.3.3 documentation](https://matplotlib.org/)
* Seaborn: [seaborn: statistical data visualization — seaborn 0.11.1 documentation](https://seaborn.pydata.org/index.html)
* Folium: [Folium — Folium 0.12.1 documentation](https://python-visualization.github.io/folium/)

IV. Modeling
* Sklearn: [scikit-learn: machine learning in Python — scikit-learn 0.24.1
documentation](https://scikit-learn.org/stable/)
* SHAP: [Welcome to the SHAP documentation — SHAP latest documentation](https://shap.readthedocs.io/en/latest/)


## Study Region 
This study examined fires larger than 200 hectares (~500 acres) from January 1, 2012 to September 15, 2020 across California encompassing seven Level-III ecoregions. 

<figure class="image">
  <img src="./docs/assets/Figure2.png" alt="study region">
  <figcaption>Figure 2. Fire perimeters in the entire study region, overlaid on top of EPA level III ecoregions. High risk years (2015, 2017, 2018, 2020) highlighted with multi-colored hash marks. </figcaption>
</figure>

<figure class="image">
  <img src="./docs/assets/gif1.gif" alt="study region">
  <figcaption>S1. Animation of annualy total burned area of large fires. </figcaption>
</figure>

## Methods 

To characterize fire spread, we derived daily fire perimeters by spatialy interpolating MODIS and VIIRS active fire products from the Fire Information for Resource Management System (FIRMS) 

Derived perimeters were used to calculate daily burned area, magnitude, and direction of fire spread. 

Gradient boosting (GB) machine learning algorithm was used for the prediction of daily burned areas and magnitude for the fires in the study region. 

<figure class="image">
  <img src="./docs/assets/Figure3.png" alt="workflow diagram">
  <figcaption>Figure 3. Example of 2018 Donnell fire showing high-level workflow; a) active fire points (resampled 375m MOD/MYD14 & VNP14IMG), b) original interpolation product and d) simplified-derived perimeters compared alongside e) Suomi 500m VIIRS burned area product (VNP64A1). Fire spread attributed c) magnitude and f) direction. </figcaption>
</figure>

## Data Layers
To delineate fuel, topography, fire weather, and human-influence components, 23 variables were chosen as inputs into the model. 

Data sources include: 
* Fire Information for Resource Management System ([FIRMS](https://firms.modaps.eosdis.nasa.gov/download/)) 
* Fire and Resource Assessment Program [(FRAP](https://frap.fire.ca.gov/))
* National interagency Fire Center ([NIFC](https://www.nifc.gov/fireInfo/fireInfo_main.html)) databases 
* Fuel type & height ([Landfire](http://landfire.gov/))
* Daily gridded weather data ([gridMET](http://www.climatologylab.org/gridmet.html)) 
* Remote Automated Weather Stations ([RAWS](https://raws.dri.edu/))


## Bay Area 2020 Fires

<figure class="image">
  <img src="./docs/assets/gif2.gif" alt="study region">
</figure>
<figure class="image">
  <img src="./docs/assets/fig11.jpg" alt="study region">
  <figcaption> S2. Del Puerto fire in the lightning ignited 2020 Bay Area fires. a) Animated fire progression of daily derived perimeters, satellite-detected hotspots, and building footprints (yellow). b) Plotted time series of area burned, magnitude, and day-time averages of weather station variables including temperature, vapor pressure deficit, and wind speed, along with c) percent fuel type based on LandFire.</figcaption>
</figure>




