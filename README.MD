# A Comprehensive Guide to: <u>Understanding Fire Driver’s Across California’s Diverse Ecoregions</u>

##  Project Description
Wildland fires at varying intensities and frequencies are a critical ecological process across the western United States. Variability in fire behavior is heavily influenced by dynamic and often complex interactions between meteorological and biophysical components. This study uses a machine learning approach to investigate what factors are linked to the rapid spread of large wildfires in the recent decade,
across six distinct ecoregions in California. Continuous daily fire spread and area burned were derived from MODIS and VIIRS active fire products. Ultimately the results from this study seek to provide
insights on the efficacy of fuel management on reducing the rate of fire progression across ecologically diverse regions and help communities and managers to better anticipate and mitigate future risk of fast
moving wildfires in the coming decades.

## Introduction
This documentation is meant to serve as a guide to execute the central workflow of the project (see figure below).
Six primary iPython notebooks (.ipynb) files are made available in the Scripts folder to run consecutively. We recommend using Google Colab, which is a Python development environment that allows you to run Jupyter notebooks in the browser i.e. so you don’t have to locally. When running the scripts using Google’s Colab notebook, each step has pre-existing set-up
lines to enable a smooth runtime. Although unlikely, to prevent any overloading and crashes when using [Colab Pro](https://colab.research.google.com/notebooks/pro.ipynb) be sure to access the high-memory runtime whenever possible. 

![GitHub Logo](./docs/assets/general_framework.jpg)

## Supporting installation and usage guidelines

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


## Supplementary Links
- Complete Setup Guidelines [Here](./howto.pdf)

- 2020 AGU Virtual iPoster [Here](https://agu2020fallmeeting-agu.ipostersessions.com/?s=1D-7D-6F-65-CB-79-56-47-9A-0D-35-25-8B-F0-66-03&token=ElIZFHSxIyuu1Nts5yRODx6rQpgpK28xidOcuGisNUk)