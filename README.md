# DATA601 Homework#2 
# Weather and Storm Analysis Tool
Weather analysis Python code that interfaces with Weather API

Overview: Convective cloud and storm development is a common occurrence over southwest Florida during the warm season (i.e., April - October). This Python code package provides a surface weather analysis technique that assesses the thermodynamic energy state of the atmosphere near the surface (ground) and identifies dynamic factors that favor or inhibit convective storm (i.e., thunderstorm) development over sub-tropical coastal areas.

Abstract: Convective cloud and storm development is a common occurrence over southwest Florida during the Northern Hemisphere warm season (i.e., April - October). Cumulus clouds develop in convection currents resulting from heating near the Earth’s surface. Deep, moist convection can also pose a threat to public safety and aviation operations. Convective cloud (i.e., cumulus cloud, see https://cloudatlas.wmo.int/en/cumulus-cu.html) and, in some cases, subsequent convective storm development can be effectively anticipated from observed weather conditions near the ground. Necessary ingredients for convective cloud development typically includes (1) a moist layer of sufficient depth in the lower atmosphere, and (2) adequate lifting of an air parcel from the moist layer to allow free convection (Johns and Doswell 1992). Equivalent potential temperature (theta-e) can indicate the amount of moist heating near the ground and the resultant instability that favors intense updrafts (i.e., vertically moving air at a high velocity). Lifting of an air parcel from the ground surface typically results from wind convergence (confluence) along the frontal boundary, defined as an air mass discontinuity. Theta-e values greater than 330 degrees Kelvin (K) strongly indicate the potential for deep, moist convective storms (i.e., thunderstorms), especially in the presence of a frontal boundary. Over southwestern Florida, sea-breeze fronts and cold fronts are the most commonly occurring. 
This application will obtain surface weather observations over a roughly 1-degree latitude by 1-degree longitude boxed area and perform a function to infer the presence of wind convergence and an associated frontal boundary. The theta-e parameter will then be analyzed to determine the potential development of cumulus clouds and thunderstorm activity.

The notebook “WX_analysis_tool.ipynb” generates tables, weather reports, and diagnostic output. Consists of six blocks that are executed in succession:
1) Load modules and invoke OpenWeather API.
2) Invoke Pandas to read and load weather observation data in JSON format from stations within the defined rectangular boundary.
3) Define and execute a function that calculates equivalent potential temperature (i.e., theta-e) from temperature and relative humidity values.
4) Invoke json_normalize function to generate a regional weather report in table format. Extract weather observation data and print weather reports for two selected locations within the rectangular boundary.
5) Execute a decision tree to 1) determine the presence of a frontal boundary, and 2) determine the possibility of deep, moist convective storms (thunderstorms).
6) Build dictionaries and a data frame containing weather report and derived parameter data; save data frame as a .csv file in the “data” directory.

Further research: Validate frontal and storm diagnosis against regional remote sensing datasets, including weather radar and satellite imagery.

Important Links:
Current weather data: https://openweathermap.org/current

References:
Johns, R. H., and C. A. Doswell, 1992: Severe local storms
forecasting. Wea. Forecasting, 7, 588–612, DOI:10.1175/
1520-0434(1992)007,0588:SLSF.2.0.CO;2.

Revering, Andrew. “Equivalent Potential Temperature.” gradsusr.org/pipermail/gradsusr/2010-January/010266.html. Accessed 8 October 2020.
