# Google Earth Engine Assessment Tools
This repository provides tools for estimating map accuracy and area on the Google Earth Engine. Additionally, this repository aims to provide guidance for all components of the assessment process including the:

- Sampling design
- Response design
- Estimation of accuracy and area 

The tools provided in this repository should be seen an non-exhaustive and relying on existing tools as much as possible (such as [TimeSync](http://timesync.forestry.oregonstate.edu/) or [Collect Earth](http://www.openforis.org/tools/collect-earth.html). This is an ongoing project and community involvement is welcomed. 

## Background
Remote sensing data allows for wall-to-wall mapping of land and atmospheric processes. The open data policies of agencies such as the USGS, NASA, and ESA, in addition to scientific advancements in the fields of machine learning and image processing have allowed for significant advancements in the quality of analysis that can be performed with remote sensing data. Utilizing the power of the Google Earth Engine, these new methods can be applied at spatial scales that never used to be technical infeasible. However, no maps will ever be perfect. Without proper estimation of the errors associated with a map it can only be seen as a "pretty picture" (McRoberts 2011). It is therefore necessary that proper statistical inference is performed on mapped datasets in order to:

- Assess the accuracy of the dataset
- Adjust for biases
- Utimately, give legitimacy to the dataset and the tools used to create it

   
