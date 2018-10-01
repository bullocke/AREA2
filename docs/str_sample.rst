.. include:: <isopub.txt> 

Stratified Random Sample |check|
================================

Selecting a sample by stratified random sampling requires you to specify a map to define strata,  a total sample size, and an allocation of sample units to strata. 

1. Start by running the Sampling Design script in the Scripts pane. 
2. In the first entry box *Specify an image ID and sampling scheme*, specify a map that defines the study area. Because you are not using strata or clusters, the contents of the map does not matter.
3. Under *Specify band if a multi-band map (if not, specify 1)*: if you are using a map that contains multiple bands, specify which band you want to use to define the study area.  Otherwise, just specify "1".
4. If the map has a no-data value or if you want to exclude a certain value in the map when defining the study area, specify the value in *Specify no data value*.
5. Click *Load image* -- the map should be displayed in the image pane.
6. Under *Select a sampling scheme*, select *Stratified Random* 
7. Under *Determine sample size*, you can either specify an arbitrary sample size or determine the sample size by specifying a target standard error of the anticipated overall accuracy of the map that is being assessed.

If specifying arbitrary sample size
 I. If choosing to specify an arbitrary sample size, simply specify the sample size in each stratum. 
 II. Click *Create sample*. 
 
 
If specifying a target precision of the overall accuracy
 I. To determine the sample size required to meet a certain target standard error of the overall accuracy require you to specify the anticipated user's accuracy of each of the map classes used as strata under *Specify anticipated user's accuracies (0-1)*
 II. Then *Specify target standard error of overall accuracy (0-1)* and click *Calculate sample size* -- the sample size is calculated using Equation 13 in [1]_ which is derived from Equation 5.25 in [2]_.
 III. Click *Create sample*. 
 
  
If specifying a target precision of an area estimate 
 I. [Coming soon]
  
 
8. To view, the sample in the Display pane, click *Add to map*
9. To export the sample, click *Export sample* and select the desired file format.


.. [1] Olofsson, P., Foody, G. M., Herold, M., Stehman, S. V., Woodcock, C. E., & Wulder, M. A. (2014). Good practices for estimating area and assessing accuracy of land change. *Remote Sensing of Environment*, 148, 42-57.
.. [2] Cochran, W. G. (1977). *Sampling techniques*. John Wiley & Sons.



