.. include:: <isopub.txt> 

Stratified Random Sampling |check|
==================================

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
 I. To determine the sample size required to meet a certain target standard error of the area estimate of a  certain class, you first need to specify which class to target. When loading the stratification in Step 5., console will print the strata weights -- the stratification used in Examples: Stratified estimation has the following strata and weights::
 
   >>> Area weights of strata:
       List (6 elements)
       1: 0.41211
       2: 0.49320
       3: 0.02195
       4: 0.06674
       5: 0.00365
       6: 0.00234


 Where 1 is Non-forest, 2 is Forest, 3 is Water, 4 is Forest loss, 5 is Forest gain, and 6 is Forest gain/loss. 
 II. Assume that we want to estimate stratum 4 (Forest loss) -- simply select "4" under *Select target class*
 III. The second step is to specify how much Forest loss according to the reference data is present in the other strata. The amount of actual Forest loss present in the Forest loss stratum, equals the user's accuracy of the *Forest loss* map class. Specify the anticipated user's accuracy of the Forest loss map class.
 IV. Then specify the anticipated proportion of forest loss present in the other strata. These proportions equals the anticipated omission of forest loss in each of the map classes.
 V. Finally, specify the target standard error of the class of interest. In my case, the area of forest loss was mapped at 0.066 of the total map area. While the area of forest loss is unknown, the mapped area is best "guesstimate". If trying to achieve a 95% confidence interval of \pm 0.01, we would need to specify a target standard error of 0.005 of the study area.
 VI. Click calculate sample size to use Equation 13 in [1]_  but with the overall accuracy substituted for the area of a map class. The equation is derived from Equation 5.25 in [2]_.
 
 
8. To view, the sample in the Display pane, click *Add to map*
9. To export the sample, click *Export sample* and select the desired file format.


.. [1] Olofsson, P., Foody, G. M., Herold, M., Stehman, S. V., Woodcock, C. E., & Wulder, M. A. (2014). Good practices for estimating area and assessing accuracy of land change. *Remote Sensing of Environment*, 148, 42-57.
.. [2] Cochran, W. G. (1977). *Sampling techniques*. John Wiley & Sons.



