.. include:: <isopub.txt> 

Stratified Estimation |cir|
===========================

An example is provided here to illustrate the estimation of the area of forest loss for the country of Cambodia between 2000 and 2010 using stratified estimation. The example has three different parts: 1) sampling design -- a sample is selected by stratified random sampling; 2) response design which involves observing the reference conditions at sample unit in  various satellite data available in Google Earth Engine; and 3) the analysis which is based on the application of a stratified estimator to the sample data.

**Note that the sample data are made-up and do not reflect actual conditions in Cambodia!** 

1. Sampling Design
------------------

1. Because the area of forest loss is small relative the total study area, using non-stratified designs would require a very large sample size to ensure a sufficient number of observations of forest loss in the sample data. To use a stratified design, we will first need to define a stratification. In this case, we will extract a map of Cambodia from a global map [1]_ of forest, non-forest, forest loss, and forest gain. The map will serve a stratification of study area. Preferably, use the GeoTIFF format. (A tutorial from BEEODA illustrating the creation of a local stratification from the global map is provided `here <https://github.com/beeoda/tutorials/tree/master/Use_of_global_tree_cover_and_change_datasets>`_)

2. You can download the stratification of Cambodia `here <https://drive.google.com/open?id=1XYzslxY0F7X0Dum58-4_KTEBGqm2EEe3>`_. Once downloaded to your local computer, click the *Assets* tab next to the *Scripts* tab and *NEW* > *Image upload* > *SELECT*; click *Advanced* > *Masking mode* > and set *No-data value* to "0". Click *OK* to upload the stratification as an image file. You can check the progress in the *Tasks* tab (the upload will take several minutes).

3. Once the stratification has been added to *Assets*, highlight the script "1_sampling_design" in the *Scripts* tab and click *Run*. (Check `Overview <https://gee-assessment-tools.readthedocs.io/en/latest/overview.html>`_ to familiarize yourself with GEE interface if you have done so already.)

4. In Sampling Design dialog, add the path to the stratification under *Specify an image to define study area*. The path is likely something like "users/[your name]/stratification_cambodia_utm_small". Set the band to "1" and mask value to "0" and click *Load image*. 

5. Because the objective of the exercise is to estimate the area forest loss which is a small part of the study area, the sample will be selected by stratified random sampling -- under *Select a sampling scheme* select *Stratified random*. 

6. Further, we will *Determine sample size* by setting a *Target SE of a class*, in this case, class number 4, Forest loss. The application will print in the Dialog and Console the area proportion of class 4::
   >>> Area weights of strata:
       0.0667431639819303 


	   
7. Text 


2. Response Design
------------------

Text

3. Analysis
------------------

Text


.. [1] Hansen, M. C., Potapov, P. V., Moore, R., Hancher, M., Turubanova, S. A. A., Tyukavina, A., ... & Kommareddy, A. (2013). High-resolution global maps of 21st-century forest cover change. *Science*, 342(6160), 850-853.