![logo](https://climate.copernicus.eu/sites/default/files/custom-uploads/branding/LogoLine_horizon_EC_Cop_ECMWF.png)

# C3S Satellite-Observations (ECV) - Hydrology and Cryosphere Tutorial

**PLEASE NOTE THAT THIS A DEVELOPMENT INSTANCE, THESE NOTE BOOKS ARE OFFICIALLY PUBLISHED ELSEWHERE**

This Jupyter book is a sub-module of the core C3S training material, it is published here for reviewing the
content prior to publication.

Satellite observations play a crucial role in monitoring various aspects of the Earth's atmosphere, surface, and cryosphere. This tutorial series explores the utilization of satellite data for comprehensive meteorological analyses and environmental monitoring for Hydrology and Cryosphere domains. 


## Surface Water

Surface water plays a vital role in the Earth's hydrological cycle, encompassing various components such as soil moisture, lakes, and rivers. This subsection focuses on the analysis of different aspects of surface water dynamics, including soil moisture anomalies and the characteristics of lake water bodies.

### Soil Moisture Anomaly Analysis

In this tutorial we will download C3S Satellite Soil Moisture data from the [Copernicus Climate Data Store (CDS)](https://doi.org/10.24381/cds.d7782f18), read data stacks in python using [xarray](https://xarray.pydata.org/) and perform simple analyses of soil moisture anomalies over selected study areas.

The tutorial consists of the following main steps:

1. A short description of the data sets
2. Download satellite soil moisture images from CDS using the CDS API
3. Application 1: Open downloaded data and visualize the soil moisture variable
4. Application 2: Extract a time series for a single location and compute the soil moisture anomaly
5. Application 3: Vectorized anomaly computation and data extraction for a study area

![logo](./img/.png)


### Lake Water Level Timeseries

In this tutorial we will access lake products from the Climate Data Store (CDS) and analyse the timeseries of the lake water level on a selected lake. The tutorial comprises two main steps:

1. Dowload and decompress data
2. Visualise the location of the lake in a map
3. Visualise and save water level timeseries
4. Visualise and save the yearly water level anomalies

![logo](./img/.png)

### Lake Surface Water Temperature Analysis

In this tutorial we will access lake surface water temperature data from the Climate Data Store (CDS) and plot

- the timeseries at the lake centre for a given day of the year and
- the LSWT, uncertainty and quality level for all the pixels on the given lake on a selected day.

The tutorial comprises two main steps:

1. Dowload and decompress data for every year on record on the selected day of the year
2. Visualise and save the lake surface water temperature **timeseries** (displaying quality levels and uncertainty) **at the lake centre**, but other locations can be given through their lat/lon coordinates
3. Visualise the location of the lake centre (or of the preferred location) on the lake mask
4. Plot the **LSWT, uncertainty and quality level for all the available pixels** on the selected lake **on a given date**

![logo](./img/.png)

## Ice Sheets

Ice sheets are vast expanses of glacial ice covering landmasses, primarily Antarctica and Greenland. These ice sheets play a crucial role in global climate dynamics and sea level rise. This tutorial series provides insights into various aspects of ice sheet dynamics and related measurements.

### Ice Sheet Surface Elevation

This tutorial will demonstrate how to plot a map of the average surface elevation change rates across the Greenland or Antarctic ice sheets, using data from the Copernicus Climate Change Service (C3S).

It should be noted that the Antarctica product is not updated since February 2023, hence are the folowing code provided using the version 3 of the CDS data. Newer dataversion are avilable for Greenland.

It will show you how to download data from the C3S Climate Data Store (CDS), calculate average change rates over a selectable period, and display the results.

![logo](./img/.png)

### Ice Sheet Velocity

This tutorial will demonstrate how to plot velocity maps and flow vectors of the Greenland Ice Sheet and its major outlet glaciers, using ice velocity data from the Copernicus Climate Change Service (C3S).

It will show you how to download data from the C3S Climate Data Store (CDS), plot the maps and and display flow vectors on top.

![logo](./img/.png)

### Ice Sheet Mass Balance

This tutorial will demonstrate how to plot the Gravimetric Mass Balance (GMB) data for selected regions across the Greenland or Antarctic ice sheets, using data from the Copernicus Climate Change Service (C3S).

It will show you how to download data from the C3S Climate Data Store (CDS), calculate average change rates over a selectable period, and display the results.

![logo](./img/.png)

### Glacier Mass Change

Glaciers are smaller ice masses distinct from ice sheets but still contribute significantly to sea level rise. Glacier mass change refers to variations in the volume and mass of glaciers over time, primarily driven by climate factors. This tutorial section explores the processes influencing glacier mass change, techniques for measuring glacier mass balance, and the implications of glacier dynamics for global sea level rise.

![logo](./img/.png)
