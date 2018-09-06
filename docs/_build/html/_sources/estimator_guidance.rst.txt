.. include:: <isopub.txt> 

Choosing an estimator |check|
=============================

We provide support for five different estimators. Consider the following when choosing between estimators:

**Stratified estimator**. The stratified estimator is recommended for estimating population parameters from sample data obtained by stratified random sampling. The estimator is expressed as the sum of the means of the simple random samples within strata weighted by stratum weights calculated as relative proportions of the population within strata.

**Post-stratified estimator**. We recommend the use of a post-stratified estimator when sample data has been collected by *simple random* or *simple systematic* designs, and when a stratification has been applied to the study area subsequent to the sampling. Consider the following example: if a systematic sample of field plots has been collected for estimation of forest area, post-stratifying the study area by a forest/non-forest map and using a post-stratified estimator is likely to increase precision in area estimates compared to just simply applying a simple random estimator (i.e. the mean value). Note that the post-stratified estimator is a stratified estimator applied to sample data collected to simple random/systematic designs. 

**Model-assisted regression estimator**.  The model-assisted regression estimator is, just as the stratified estimator, recommended for estimating population parameters from sample data collected by stratified random sampling. But while the stratified estimator has been shown to provide more precise estimates when the map and the reference observations represent classes of a categorical variable (such as deforestation, forest, non-forest), model-assisted regression is likely to provide more precise estimates when the sample data contains continuous reference observations such as proportion of forest or proportion of deforestation.

**Model-assisted difference estimator**. The difference estimator has been used to estimate net forest change when no reference observations or maps of change exist. For example,  the difference estimator can be used for estimating the area of forest loss and gain if forest inventory data have been collected of the same area at times 1 and 2, and two forest/non-forest representing conditions at times 1 and 2 exist. The difference estimator require the sample data have been collected by simple random or systematic sampling or stratified random sampling if the sample size is proportionally allocated to strata. 

**Ratio estimator**. If sample data have been collected by stratified random sampling for estimation of area and map accuracy but the strata are different from the map classes, we recommend using a ratio estimator. For example, a sample that was collected by stratified random sampling using version 1 of certain land cover map as stratification, can still be used to estimate the accuracy of an updated map of the same area, if using the ratio estimator.


More information about the use of various estimator for area estimation is provided in: Stehman, S. V. (2013). Estimating area from an accuracy assessment error matrix. *Remote Sensing of Environment*, 132, 202-211.