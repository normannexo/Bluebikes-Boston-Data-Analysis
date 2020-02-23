# Boston Bluebikes data
## by Torben Flickinger

## Dataset

Bluebikes is Metro Boston's public bike share program, with more than 1,800 bikes at over 200 stations across Boston, Brookline, Cambridge and Somerville. Bluebikes is owned by the municipalities of Boston, Brookline, Cambridge and Somerville, and operated by Motivate. Bluebikes publishes trip data regularly on https://www.bluebikes.com/system-data . For my analysis I downloaded the trip data for all months of 2019.
To be able to investigate possible relationships of the use of this service to weather data, I additionally downloaded a dataset with historical weather data for Boston from the National Oceanic and athmospheric Administration https://www.ncdc.noaa.gov/cdo-web/datasets/GHCND/stations/GHCND:USW00014739/detail.

The datasets used in this project have been gathered from 2 sources.  

1. Bluebike's historical trip data - downloaded from https://www.bluebikes.com/system-data
2. NOAAA weather data - obtained from https://www.ncdc.noaa.gov/cdo-web/datasets/GHCND/stations/GHCND:USW00014739/detail.

## Data Exploration

I approached the data by first looking into some more superficial features like the distribution of the usage in the course of the months and then
digging deeper and get to know the usage by the different user types, their gender and their age, while always keeping an eye on possible implausibilities showing
up in the data. For example, there are some inconsistencies in the birth year data, that had to be taken into account in the analysis. I looked into the most popular start and end stations and tried
to discover patterns in their usage. Finally, I joined the weather data from 2019 to the historical trip data to see if our expectations regarding the relationship
of the service's usage and local weather conditions can be confirmed or whether there are any surprising insights.

## Questions

In this project I tried to explore analytically the usage of Boston's public bike share program.
Some of the questions I found of particular interest were:

- Who (age groups, gender) uses this service and how is it used?
- What are the most popular start and end stations in the service and how are they used by the customers?
- Does the data confirm our expectation to find a strong correlation between the usage rate and outdoor temperatures and weather conditions in general?

## Included files
The following files are included in this repository

- `exploration_bluebikes_Boston.ipynb`: In this notebook all explorative analysis is carried out
- `slide_deck_bluebikes.ipnyb`: This notebook contains the explanatory insights and is the basis for the slide deck html
- `data/weather_data_boston.csv`: the csv data file with historical weather data obtained from the National Oceanic and atmospheric Administration



## used libraries
Besides numpy, pandas, matplotlib the following libraries have been used in this project:
- `BeautifulSoup` for gathering trip data from www.bluebikes.com
- `Folium` for rendering map data
- `Geopy` for calculation the geodesic distances between two points
