# The Beginnings of a Larval Transpot Model
#### Maia Heffernan


##### **Project Goals**
The focus of this study is the larval form of the deep-sea snail, *Ifremeria nautilei*. This project aims to eventually create an interpolated model to emulate larval transport by interpolating larval behavior and life history with regional water movement data. This will give the best estimate of where larvae will be transported once released into the water column and how *I. nautilei* populations establish themselves.

This is the larger goal, however. This final project focuses on importing needed datasets, creating base code to work with future datasets, and creates a few figures to highlight study and sampling locations and results.

##### **Motivation for Project**
In the Spring of 2022, I participated in a research cruise led by Dr. Shawn Arellano (Western Washington University), Dr. Roxanne Beinart (University of Rhode Island), and Dr. Craig Young (Oregon institute of Marine Biology) to the Lau Back-Arc Basin in the Kingdom of Tonga in the South Pacific. We were studying deep sea hydrothermal vent communities, with a specific focus on the symbiotic relationships between four different snail species and the chemoautotrophic bacteria in the water at this location.

I had my own project which focused on the larval form of the snail species *Ifremeria nautilei*. This larval form is known as the Warén's larva (named after the Swedish deep sea biologist who discovered the snail species). Since returning, we have been analyzing our data and thinking about the stories we want to show with what we have collected.

One project that has arisen is to try to see if we can understand larval transport methods to see how and where *I. nautilei* might develop. Understanding larval transport is critical for studying population/species dynamics. the eventual goal of this project is to create a model that connects important larvae biology and behavior to regional water movement to make estimates about how future populations might develop as larvae are swept up in oceanic currents when released into the water column. As explained above, however, this is a bigger project, so my final is just the beginning steps for this.


##### **Data**
The datasets for larval behavior come from the data we colled on our research cruise. They are CSV files that include respiration and culture survival data. Some of these sets are still being processed and will not be completed by the due date of this project, but one of the focuses of this model is to create the basecode that is needed so that one can easily plug in different datasets and analyze results. 

The Regional Oceanic Monitoring System (ROMS) dataset will ultimately be used for the water movement aspect of this project. However, this data is still being processed by a colleague, so instead this dataset uses a netCDF file from NOAA's Environmental Research Division Data Access Program (ERDDA) database. It includes the topographical information of the region where we conducted our sampling. To acquire the data, ERDDA asks the user to specify longitude and latitude ranges, and provides topographical information for that area. More information can be found here: [NOAA ERDDAP](https://www.ncei.noaa.gov/products/weather-climate-models/using-erddap).

##### **Analysis Methods**
The respirtaion and culture survival data sets will be used to determine survival rate and will be shown with a Kaplan-Meier fitted graph. Creating a Kaplan-Meier graph is a specific function in python called `kmf.fit()`. This requires the arguments `durations` and `event observed`.

The netCDF dataset will be read in with the package `netCDF`, and the variables will be manipulated with `pandas` and `numpy`. 

The figures that are present in this project are created with Basemap and Matplotlib. They show topographic and depth information, respectively. Including these figures is the first step in thinking about how to utilize netCDF data for visualization purposes.

##### **Takeaways**
One thing I am quickly discovering is that figuring out what to do with data and how to connect two very different types of information is very difficult. There is not much information about how to do this, so it requires a lot of creativity!

Also, in creating the maps, I got very excited when things started to show up in clear contrast. Though ArcGIS is the norm for mapping, it seems python does a pretty good job in a pinch!


