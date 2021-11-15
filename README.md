# NASA Hackweek 2021 - Upwelling

## Spatio-temporal changes in global upwelling patterns

### Project Summary

Exploration of spatial and temporal variability in coastal upwelling patterns using satellite data that more directly measures in-situ coastal upwelling: SST and upward velocity (via [SSH](https://journals.ametsoc.org/view/journals/phoc/50/1/jpo-d-19-0172.1.xml)).

I am interested in 2D and 3D image machine learning to study this spato-temporal variability, but for this project I will likely focus on simpler metrics of upwelling: SST offshore-nearshore differential and "coastal SST - mean long-term SST" as a metric for upwelling intensity.

### Collaborators on this project

Project lead: Eli Holmes, NOAA; OTHERS WELCOME TO JOIN!

### The problem

Upwelling brings nutrient rich water to the surface and supplies nutrition necessary for biological productivity. “Coastal upwelling ecosystems like the U.S. west coast are some of the most productive ecosystems in the world and support many of the world’s most important fisheries. Although coastal upwelling regions account for only one percent of the ocean surface, they contribute roughly 50 percent of the world’s fisheries landings” (NOAA Ocean Explorer). While upwelling is generally thought of as positive (bringing nutrients to the surface), it also brings low oxygenated water to the surface and intense upwelling is associated with coastal hypoxia, causing large scale fish kills.

![](upwelling_fig.gif)
Upwelling with wind-driven mechanism shown. Note not all upwelling is wind-driven. (fig from NOAA Oceanservices)

Already 30 years ago, Bakun (1990) postulated that global warming would impact major coastal upwelling systems: "Evidence from several different regions suggests that the major coastal upwelling systems of the world have been growing in upwelling intensity as greenhouse gases have accumulated in the earth's atmosphere" due to "increased onshore-offshore atmospheric pressure gradients, intensified alongshore winds, and accelerated coastal upwelling circulation". Models suggest that the effects will be stronger at pole-ward latitudes, which will cause a shift in the location of coastal upwelling (Rykaczewski, R. R. et al. 2015, Wang et al. 2015). Since then, a number of researchers (e.g. Bakun et al. 2015, Garcia et al. 2015, Garreaud and Falvey 2009, Xie et al. 2018) have found direct or model evidence of changes in coastal upwelling patterns that match the Bakun's predictions. 

However this work has focused on the wind-driven eastern boundary upwelling systems: California, Humboldt (off Peru), Benguela (off SW coast of Africa) and Canary (off the NW coast of Africa). These are major upwelling systems and are responsible for ca 20% of the global fish catch, but they are only a fraction of the world's upwelling systems. The world's upwelling systems are diverse, some wind-driven while others are not, some continual while many are seasonal, and some current-driven.

![](images/upwelling_zones_crop.png)


### Sample data

If you already have some data to explore, briefly describe it here (size, format, how to access).

### Specific Questions

List the specific tasks you want to accomplish or research questions you want to answer.

### Existing methods

I have been doing some pilot projects using the Optimal Interpolation SST dataset (2.5 deg grid).

**A nearshore-offshore upwelling detection method** Simple and straight-forward to apply.

![](images/auto-detection1.png)

**Image decomposition algorithms: PCA and hierarchical clustering**

![](images/unnamed-chunk-9-1.png)


### Proposed methods/tools

I'd like to try the SST differential idea with some different SST products and extend this to the entire N and S Americas. I have a 20km and 300km coastal shape files with sample points every 100km along the 20km coast line along with the point closest to that sample point but on the 300km line. So a pair of points: nearshore and offshore. 
![](images/coast-samples.png)

I'd like to get statistics (SST plus whatever else seems appropriate) around those points. Currently I am using mean SST. 
![](images/global-coast-lines.png)

I'm thinking a 2 x (# sample points) x (# days) xarray with the statistics.



### Background reading

Bakun, Andrew. 1990. Global Climate change and intensification of coastal ocean upwelling.” Science 247: 198–201. http://www.jstor.org/stable/2873492.

Bakun, A. et al. 2015. Anticipated effects of climate change on coastal upwelling ecosystems. Curr. Clim. Change Rep. 1, 85–93.

García-Reyes M, Sydeman WJ, Schoeman DS, Rykaczewski RR, Black BA, Smit AJ and Bograd SJ. 2015. Under pressure: climate change, upwelling, and eastern boundary upwelling ecosystems. Front. Mar. Sci. 2:109. doi: 10.3389/fmars.2015.00109

Garreaud, R. D. & Falvey, M. 2009. The coastal winds off western subtropical South America in future climate scenarios. Int. J. Climatol. 29, 543–554.

Rykaczewski, R. R. et al. 2015. Poleward displacement of coastal upwelling-favorable winds in the ocean’s eastern boundary currents through the 21st century. Geophysical Research Letters 42, 6424–6431.

Wang, D., Gouhier, T. C., Menge, B. A. & Ganguly, A. R. 2015. Intensification and spatial homogenization of coastal upwelling under climate change. Nature 518, 390–394 (2015).

Xiu, P., Chai, F., Curchitser, E.N. et al. 2018. Future changes in coastal upwelling ecosystems with global warming: The case of the California Current System. Sci Rep 8, 2866. https://doi.org/10.1038/s41598-018-21247-7


### Notes




