# DATA601 Homework#2 
# Weather and Storm Analysis Tool
Weather analysis Python code that interfaces with Weather API

Overview: Convective cloud and storm development is a common occurrence over southwest Florida during the warm season (i.e., April - October). This Python code package provides a surface weather analysis technique that assesses the thermodynamic energy state of the atmosphere near the surface (ground) and identifies dynamic factors that favor or inhibit convective storm (i.e., thunderstorm) development over sub-tropical coastal areas.

Abstract: Convective cloud and storm development is a common occurrence over southwest Florida during the Northern Hemisphere warm season (i.e., April - October). Cumulus clouds develop in convection currents resulting from heating near the Earth’s surface. Deep, moist convection can also pose a threat to public safety and aviation operations. Convective cloud (i.e., cumulus cloud, see https://cloudatlas.wmo.int/en/cumulus-cu.html) and, in some cases, subsequent convective storm development can be effectively anticipated from observed weather conditions near the ground. Necessary ingredients for convective cloud development typically includes (1) a moist layer of sufficient depth in the lower atmosphere, and (2) adequate lifting of an air parcel from the moist layer to allow free convection (Johns and Doswell 1992). Equivalent potential temperature (theta-e) can indicate the amount of moist heating near the ground and the resultant instability that favors intense updrafts (i.e., vertically moving air at a high velocity). Lifting of an air parcel from the ground surface typically results from wind convergence (confluence) along the frontal boundary, defined as an air mass discontinuity. Theta-e values greater than 330 degrees Kelvin (K) strongly indicate the potential for deep, moist convective storms (i.e., thunderstorms), especially in the presence of a frontal boundary. Over southwestern Florida, sea-breeze fronts and cold fronts are the most commonly occurring. 
This application will obtain surface weather observations over a roughly 1-degree latitude by 1-degree longitude boxed area and perform a function to infer the presence of wind convergence and an associated frontal boundary. The theta-e parameter will then be analyzed to determine the potential development of cumulus clouds and thunderstorm activity.

References:
Johns, R. H., and C. A. Doswell, 1992: Severe local storms
forecasting. Wea. Forecasting, 7, 588–612, DOI:10.1175/
1520-0434(1992)007,0588:SLSF.2.0.CO;2.
