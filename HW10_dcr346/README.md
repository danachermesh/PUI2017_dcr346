# HW10_dcr346 - Time Series Analysis of MTA

## Task 1 - Event Detection
Using 3 leveled for loop I extraced from each station and each card type the total rides per week and created a one-dimentional list of total rides per week.

Plotting this list and calculating it's mean, std, and threshold of 3 sigma's under the mean, it was easy to detect the irregular week in which an event occured. Looking at the dates, it turned to reveal Hurricane Sandy in Oct 22nd, 2012.

Worked alone on this task; discussed it after completing with Rebecca and Emily.

## Task 2 - Assesing Stationarity
Used np.nansum and np.average functions to create a 2-D (23,194) array in which all MTA card types contains the data of all MTA stations (weighted average) rides per week.

......

Worked on most of it with Rebbeca and Emily, the rest of this assignment was completed alone.
