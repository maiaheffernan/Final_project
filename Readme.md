# Larval Transpot Modeling
#### Maia Heffernan


##### **Project Goals**
The focus of this study is the larval form of the deep-sea snail, *Ifremeria nautilei*. This model seeks to emulate larval transport by interpolating larval behavior and life history with regional water movement data. This will give the best estimate of where larvae will be transported once released into the water column and how *I. nautilei* populations establish themselves.

##### **Motivation for Project**
In the Spring of 2022, I participated in a research cruise led by Dr. Shawn Arellano (Western Washington University), Dr. Roxanne Beinart (University of Rhode Island), and Dr. Craig Young (Oregon institute of Marine Biology) to the Lau Back-Arc Basin in the Kingdom of Tonga in the South Pacific. We were studying deep sea hydrothermal vent communities, with a specific focus on the symbiotic relationships between four different snail species and the chemoautotrophic bacteria in the water at this location.

I had my own project which focused on the larval form of the snail species *Ifremeria nautilei*. This larval form is known as the Warén's larva (named after the Swedish deep sea biologist who discovered the snail species). Since returning, we have been analyzing our data and thinking about the stories we want to show with what we have collected.

One project that has arisen is to try to see if we can understand larval transport methods to see how and where *I. nautilei* might develop. Understanding larval transport is critical for studying population/species dynamics. This project attempts to create a model that connects important larvae biology and behavior to regional water movement to make estimates about how future populations might develop as larvae are swept up in oceanic currents when released into the water column.


##### **Data**
The datasets for larval behavior come from the data we colled on our research cruise. They are CSV files that include respiration data, culture survival data, and vertical swimming speed data. Some of these sets are still being processed and will not be completed by the due date of this project, but one of the focuses of this model is to create the basecode that is needed so that one can easily plug in different datasets and analyze results. 

The Regional Oceanic Monitoring System (ROMS) dataset will ultimately be used for the water movement aspect of this project. However, this data is still being processed by a colleague, so instead this dataset uses a net CDF file from the USGS that looks at sediment transport on oceanic shelves and slopes in California. Though this is in a completely different part of the world from the area where the biological data was collected, the idea is again to simply create a structure that will allow for the future use of the ROMS data for the Lau Back-Arc Basin.

##### **Analysis Methods**
The respirtaion and culture survival data sets will be used to determine survival rate and will be shown with a Kaplan-Meier fitted graph. Creating a Kaplan-Meier graph is a specific function in python called `kmf.fit()`. This requires the arguments `durations` and `event observed`.

The swimming speed data will not require any analysis in python. It will be interpolated into the model that shows how all of these things affect larval transport.

The netCDF dataset will be read in with the package `netCDF`, and the variables will be manipulated with `pandas` and `numpy`. 

While still under consideration, the biological and physical datasets will be comined via manipulating and interpolating the datasets via functions in `pandas` in order to create a time-series model that will show survial over time based on both types of data.

##### **Takeaways**
One thing I am quickly discovering is that figuring out what to do with data and how to connect two very different types of information is very difficult. There is not much information about how to do this, so it requires a lot of creativity!

