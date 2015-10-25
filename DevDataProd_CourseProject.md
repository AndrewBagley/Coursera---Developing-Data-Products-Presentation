Developing Data Products - Course Project
========================================================
author: Andrew B
date: 20/14/2015
transition: rotate


NOAA Storm Database Explorer
========================================================
type: sub-section

This presentation is being created as part of the peer assessment for the coursera developing data products class. The assignment is geared toward ensuring the following concepts were well understood by the students

- **shiny** to build data product application
- **R-Presentation or slidify** to create data product related presentations

Application Information and Functionality
========================================================
type: sub-section
To display the understanding of using **shiny** to build an application, a simple application called **NOAA Storm Database Explorer** has been developed and deployed at: 
https://andrew-b.shinyapps.io/Coursera---Developing-Data-Products/

The application allows the user to:
- Select the inputs like- the range of years, types of events. 
- Select the output to be displayed on the map, or as a graph, or as a table 
  - Also has a option to download the filtered data.

The Data
========================================================
type: sub-section
This application references the U.S. National Oceanic and Atmospheric Administration's (NOAA) storm database.

The dataset was obtained from [StorageLink](https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2FStormData.csv.bz2) and processed for the course project. This is the same file that is used for Cousera's Reproducible Research Course.

Source code for the project is available on the [GitHub](https://github.com/AndrewBagley/Coursera---Developing-Data-Products).


Data
=====================
type: sub-section
Read Data

```r
library(data.table)
dt <- fread('events.agg.csv')
head(dt)
```

```
   YEAR   STATE  EVTYPE COUNT FATALITIES INJURIES PROPDMG CROPDMG
1: 1950 alabama TORNADO     2          0       15 0.02750       0
2: 1951 alabama TORNADO     5          0       13 0.03500       0
3: 1952 alabama TORNADO    13          6      116 5.45250       0
4: 1953 alabama TORNADO    22         16      248 3.07000       0
5: 1954 alabama TORNADO    10          0       36 0.60753       0
6: 1955 alabama TORNADO     8          5       27 7.58000       0
```
