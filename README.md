# Area Estimation & Accuracy Assessment (AREA2) Toolbox

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3451452.svg)](https://doi.org/10.5281/zenodo.3451452)

## About

[Link to Earth Engine Code](https://code.earthengine.google.com/?accept_repo=projects/AREA2/public)

[Documentation](https://area2.readthedocs.io/en/latest/)

This repository provides tools and guidance for estimating map accuracy and area on the Google Earth Engine. The tools provided in this repository should be seen an non-exhaustive and relying on existing tools as much as possible (such as [TimeSync](http://timesync.forestry.oregonstate.edu/) or [Collect Earth](http://www.openforis.org/tools/collect-earth.html)). This is an ongoing project and community involvement is welcomed. 

## Background
One of the most common results of remote sensing analyses is a quantification of various phenomena on the land surface, such as deforestation, farmland expansion, urbanization, land use patterns, etc. Remote sensing has the advantage of providing wall-to-wall coverage of the area of interest at little or no cost, but results are never perfect! Classification errors are inevitable when trying to translate reflected sunlight or backscattered longwave radiation into information about complex land surface processes. The presence of errors may introduce substantial bias in remote sensing-based maps<sup>1</sup>. For remote sensing science to impact policy and decision-making for the benefit of Earth and its inhabitants, satellite image-based analyses must produce valid scientific inference -- maps that lack inference-based assessments of the parameters of interest are of little utility for scientific inference; “essentially, they may be just pretty pictures”<sup>2</sup>. With the emergence of free data and powerful computing platforms, map-making has never been easier, which makes the “pretty pictures” statement more true than ever before. Luckily, a typical remote sensing analysis is attractive from the perspective of design-based inference<sup>3</sup>. In a design-based inference framework, a sample of population units (i.e. pixels in this case) is selected such that it represents the much larger population (i.e. all the pixels in the map), and reference conditions are observed at each sample location. Application of an unbiased estimator, that accommodates the effects of classification errors, to the sample data provides area estimates that are bias-adjusted. Measures of map accuracy are also estimated from the sample data. Further, application of a variance estimator allows for quantification of the uncertainty of estimates in the form of confidence intervals. 

A common bottleneck in the implementation of inference protocols is the collection of reference observations. A powerful source of reference data is the Landsat archive because it allows for examination of time series of observations at each sample location but downloading the data and extracting time series data require much storage space and time, especially for large areas. Google Earth Engine alleviates such demands as time series of Landsat in combination with Sentinel-2 data -- both of which are hosted on GEE -- can be extracted for any pixel in the world without having download a byte of data! This application provides support for selecting a sample from a study area (sampling design), extracting reference data for sample locations (response design), and applying an unbiased estimator to sample data for estimation of area and map accuracy (analysis):

- **Sampling design**: support for four designs: simple random, simple systematic stratified random and stratified systematic. For stratified designs, a map should provided where the map classes correspond to strata. Currently, the assessment unit is a 30 m × 30 m pixel and the output a shapefile that contains the locations of the units in the sample. Users can arbitrarily set or determine the sample size and the allocation of sample units to strata according to the literature recommendations.
- **Response design**: support for visualization of time series of Landsat data and display of Landsat and Sentinel-2 for sample locations.
- **Analysis**: support for use of the stratified estimator<sup>1</sup>,<sup>4</sup> and the model-assisted regression estimator<sup>2</sup>,<sup>5</sup>. Both estimator provide estimates of the area of each category in the map provided; user’s and producer’s accuracy of each category; overall map accuracy; and confidence intervals for each estimate. 

1. Olofsson P, et al. (2013). Making better use of accuracy data in land change studies: Estimating accuracy and area... *Remote Sensing of Environment*, 129, 122-131.
2. McRoberts R E (2011). Satellite image-based maps: Scientific inference or pretty pictures? *Remote Sensing of Environment*, 115, 715-724.
3. Olofsson P, et al. (2014). Good practices for estimating area and assessing accuracy of land change. *Remote Sensing of Environment*, 148, 42-57.
4. Cochran W G (1977). *Sampling Techniques: 3d Ed.* Wiley.
5. Särndal C E, et al. (1992). *Model assisted survey sampling.* Springer.
6. GFOI (2016). *Integration of remote-sensing and ground-based observations for estimation of emissions and removals of greenhouse gases in forests: Methods and Guidance from the Global Forest Observations Initiative, Edition 2.0.* UN-FAO, Rome.

