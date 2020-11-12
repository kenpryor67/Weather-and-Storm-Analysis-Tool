# DATA601 Homework#2 
# Weather and Storm Analysis Tool
## Weather analysis Python code that interfaces with Weather API

## Overview: Convective cloud and storm development is a common occurrence over southwest Florida during the warm season (i.e., April - October). This Python code package provides a surface weather analysis technique that assesses the thermodynamic energy state of the atmosphere near the surface (ground) and identifies dynamic factors that favor or inhibit convective storm (i.e., thunderstorm) development over sub-tropical coastal areas.

## Goals:
This application will obtain surface weather observations from from [OpenWeather API](https://openweathermap.org/current) over a roughly 1-degree latitude by 1-degree longitude boxed area and perform a function to infer the presence of wind convergence and an associated frontal boundary. The theta-e parameter will then be analyzed to determine the potential development of cumulus clouds and thunderstorm activity.

## Motivation and Background: 
Convective cloud and storm development is a common occurrence over southwest Florida during the Northern Hemisphere warm season (i.e., April - October). Cumulus clouds develop in convection currents resulting from heating near the Earth’s surface. Deep, moist convection can also pose a threat to public safety and aviation operations. Convective cloud (i.e., cumulus cloud, see https://cloudatlas.wmo.int/en/cumulus-cu.html) and, in some cases, subsequent convective storm development can be effectively anticipated from observed weather conditions near the ground. Necessary ingredients for convective cloud development typically includes (1) a moist layer of sufficient depth in the lower atmosphere, and (2) adequate lifting of an air parcel from the moist layer to allow free convection (Johns and Doswell 1992). Equivalent potential temperature (theta-e) can indicate the amount of moist heating near the ground and the resultant instability that favors intense updrafts (i.e., vertically moving air at a high velocity). Lifting of an air parcel from the ground surface typically results from wind convergence (confluence) along the frontal boundary, defined as an air mass discontinuity. Theta-e values greater than 330 degrees Kelvin (K) strongly indicate the potential for deep, moist convective storms (i.e., thunderstorms), especially in the presence of a frontal boundary. Over southwestern Florida, sea-breeze fronts and cold fronts are the most commonly occurring. 

## Contents:
The notebook [WX_analysis_tool.ipynb](https://github.com/kenpryor67/Weather-and-Storm-Analysis-Tool/blob/main/WX_analysis_tool.ipynb) generates tables, weather reports, and diagnostic output. Consists of five blocks that are executed in succession:
1) Invoke Pandas to read and load weather observation data in JSON format from stations within the defined rectangular boundary.
2) Define and execute a function that calculates equivalent potential temperature (i.e., theta-e) from temperature and relative humidity values.
3) Invoke json_normalize function to generate a regional weather report in table format. Extract weather observation data and print weather reports for selected locations within the rectangular boundary.
4) Execute a decision tree to 1) determine the presence of a frontal boundary, and 2) determine the possibility of deep, moist convective storms (thunderstorms).
5) Build dictionaries and a data frame containing weather report and derived parameter data; save data frame as a .csv file in the “data” directory.

## Datasets:
### Input data:
1) Surface weather observation data via [OpenWeather API](https://openweathermap.org/current) in JSON format. 4 rows X 24 columns.

### Output data:
[wxanal.csv](https://github.com/kenpryor67/Weather-and-Storm-Analysis-Tool/blob/main/data/wxanal.csv):
  - 5 rows X 17 columns: Cumulus_clouds (True/False), Divergence (True/False), Humidity (%), Location 1, Location 2, Location 3, Location 4, Pressure (hPa), Scattered_storms (True/False), Severe_storms (True/False), Temperature (Imperial: Fahrenheit), Theta-e (Kelvin), Wind direction (degrees), Wind speed (Imperial: miles/hour), Wind_shift (True/False), delta_thetae (degrees)

## Software:
Python:
1) [Numpy](https://numpy.org/)
2) [Pandas](https://pandas.pydata.org/pandas-docs/stable/index.html)

## Important Links:
Current weather data: https://openweathermap.org/current

## References:
Johns, R. H., and C. A. Doswell, 1992: Severe local storms forecasting. Wea. Forecasting, 7, 588–612, DOI:10.1175/1520-0434(1992)007,0588:SLSF.2.0.CO;2.

Revering, Andrew. “Equivalent Potential Temperature.” gradsusr.org/pipermail/gradsusr/2010-January/010266.html. Accessed 8 October 2020.
