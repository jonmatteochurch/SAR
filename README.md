# SAR: Spatial Auto-Regression
Project for **Applied Statistics**

Using [R](https://www.r-project.org/) (2.6.2)

Linear regression is among the most used techniques in statistics.
Nevertheless, when it is used on a spatially distributed dataset, the 
resulting model is neglecting all information relative to the spatial 
correlation in the observations and its predictive power is sub-optimal. 
In particular, the regression error is spatially auto-correlated and the
fundamental hypothesis that errors are independent is not satisfied.

SAR implements a sub-model for the regression error by means of a 
distance matrix for which estimation $n^3$  operations are required. 
This high order complexity is reduced by observing that spatial 
correlation vanishes as the observations distance increases, allowing to 
neglect the contribution of most observations for each data entry 
considering exclusively contributions from the nearest $m$ observations.
