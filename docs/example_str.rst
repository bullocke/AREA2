.. include:: <isopub.txt> 

Stratified Estimation |cir|
===========================

An example is provided here to illustrate the estimation of the area of forest loss for the country of Cambodia between 2000 and 2010 using stratified estimation. The example has three different parts: 1) sampling design -- a sample is selected by stratified random sampling; 2) response design which involves observing the reference conditions at sample unit in  various satellite data available in Google Earth Engine; and 3) the analysis which is based on the application of a stratified estimator to the sample data.

**Note that the sample data are made-up and do not reflect actual conditions in Cambodia!** 

1. Sampling Design
------------------

1. Because the area of forest loss is small relative the total study area, using non-stratified designs would require a very large sample size to ensure a sufficient number of observations of forest loss in the sample data. To use a stratified design, we will first need to define a stratification. In this case, we will extract a map of Cambodia from a global map [1]_ of forest, non-forest, forest loss, and forest gain. The map will serve a stratification of study area. (A tutorial from BEEODA illustrating the creation of a local stratification from the global map is provided here: https://github.com/beeoda/tutorials/blob/master/Use_of_global_tree_cover_and_change_datasets/2_extract_map.pdf)

2. Once you have identified a stratification, highlight the script "1_sampling_design" in the Script Manager and click *Run*. (Check `Overview <https://gee-assessment-tools.readthedocs.io/en/latest/overview.html>`_ to familiarize yourself with GEE interface.)

3. Text


2. Response Design
------------------

Text

3. Analysis
------------------

Text


.. [1] Hansen, M. C., Potapov, P. V., Moore, R., Hancher, M., Turubanova, S. A. A., Tyukavina, A., ... & Kommareddy, A. (2013). High-resolution global maps of 21st-century forest cover change. *Science*, 342(6160), 850-853.