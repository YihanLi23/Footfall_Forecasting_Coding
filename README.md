# Forecasting Pedestrian Footfall in London’s Retail Areas

## Overview

This research aims to develop a predictive model for forecasting pedestrian footfall in London’s retail areas, utilizing the XGBoost algorithm. The study integrates datasets from SmartStreetSensor Footfall Data, weather conditions, and Transport for London (TfL) transit data to evaluate how these factors influence pedestrian footfall.

## Research Problem

The central research question addressed in this study is: How accurately can pedestrian footfall in London’s retail areas be predicted by integrating environmental and transport data? The study seeks to determine the impact of weather and public transportation on pedestrian flow and identify the key factors that most significantly influence foot traffic.

## Research Year and Research Area

This study focuses on the year 2018 in Greater London, United Kingdom. 

### Modeling Focused on October's First Week

The modeling phase of this research specifically targets the first week of October 2018. This period was chosen because October represents a peak in pedestrian footfall, particularly during weekdays, and avoided the potential impact from Holidays. By focusing on this high-activity period, the study aims to capture the dynamics of pedestrian flow under conditions of maximum footfall. 

## Data Sources
Due to the proprietary nature and size of some datasets, they are not included in this repository. However, links to the data sources are provided for access:

| Data Name                       | Source Name                         | Source Link                                                                                                                                            |
|---------------------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| SmartStreetSensor Footfall Data | Consumer Data Research Centre (CDRC) | [footfall-data-research-aggregated-data](https://data.cdrc.ac.uk/dataset/local-data-company-smartstreetsensor-footfall-data-%E2%80%93-research-aggregated-data)                          |
| Retail Centre Boundaries        | Consumer Data Research Centre (CDRC) | [retail-centre-boundaries](https://data.cdrc.ac.uk/dataset/retail-centre-boundaries-and-open-indicators)                                                                   |
| Transportation Data             | Transport for London (TfL)           | [tfl.gov.uk](http://crowding.data.tfl.gov.uk/) (File: ByQhrEntryExit_2018.xlsx)                                                                              |
| Weather Data                    | Meteostat                           | [meteostat](https://dev.meteostat.net/python/)                                                                                                              |
| Statistical GIS Boundary Files for London | Greater London Authority   | [statistical-gis-boundary](https://www.data.gov.uk/dataset/6cdebf5d-c69b-4480-8c9c-53ab8a816b9d/statistical-gis-boundary-files-for-london)                                 |
| London Stations Coordinates      | Doogal                              | [london_stations Coordinates](https://www.doogal.co.uk/london_stations#google_vignette)                                                                                       |


Note: The SmartStreetSensor Footfall Datasets are not publicly available and require access permissions through CDRC.

## Research Approach and Methodology

The analysis follows a structured approach, beginning with data cleaning and preprocessing, and progressing through various stages of modeling:

### 1. Data Cleaning

Removed sensors located outside of Greater London and Excluded sensors that did not have sufficient data coverage over time to maintain data quality.

### 2. Data Preprocessing

After aggregating the footfall data at various levels, we provided descriptive statistics and visualizations to understand the distribution and characteristics of the data.

### 3. Identify the Retail Area with the Highest Sensor Density

Mapped sensor locations to visually identify areas with high sensor density. Calculate Sensor Density and Identify the Highest Density Area.

### 4. Initial Modeling

First, conducted an initial analysis using only footfall data for all devices in the Highest Density Area to establish a baseline predictive model. Then, integrated temperature data with hourly aggregation, to evaluate its impact on footfall predictions. Similarly, added precipitation data with hourly aggregation and analyzed its influence on the predictive accuracy.

### 5. Further Modeling and Case Study

First, after doing calculations, we selected Holborn station and its sensors (Device 1018 and Device 1833) for in-depth analysis. Second, assessed how each device performed using only footfall data. Third, examined the impact of temperature data on the predictions, comparing hourly aggregated and non-aggregated data. Fourth, added both temperature and precipitation, again comparing the effects of aggregation. Finally, incorporated TfL transit data into the model to further refine predictions, comparing the effects of aggregation and analyzing the combined effects of factors.

### 6. Results and Comparison

Summarized the outcomes from different modeling approaches, highlighting the most effective feature combinations for predicting pedestrian footfall.

## How to Run the Analysis

This repository includes the following key files:

- `dissertation_coding.ipynb`: Contains all the code and analysis performed in the study.
- `figures/`: Contains visualizations generated during the analysis.

To reproduce the analysis:

1. Clone this repository.
2. Open `dissertation_coding.ipynb` in a Jupyter Notebook environment.
3. Run the notebook to perform the analysis and generate the results.

