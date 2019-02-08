.. include:: <isopub.txt> 


.. image:: _nolinesoftext.png
   :width: 175pt

  
------------

Two-stage Sampling |check|
==========================

Selecting a sample by two-stage sampling requires you to specify a stratification of the study area, a shapefile that defines the population of Primary Sampling Units (PSUs), and a sample size of both Primary and Secondary  Sampling Units (PSUs and SSUs). The sampling is limited to simple random selection of SSUs in PSUs, and to selection of PSUs in strata based on the proportion of a single class of interest.  

1. Start by running the Sampling Design script in the Scripts pane > click *Two-stage sampling*. 
2. In the first entry box *Specify stratification of the study area*, specify a map that defines the study area. 
3. Under *Specify the band values in the stratification that correspond to the class of interest*, list the band values in stratification that correspond to the class of interest. For example, if the forest is the class of interest, specify all band values separated by comma that correspond to the forest strata.
4. If the map has a no-data value or if you want to exclude a certain value in the map when defining the study area, specify the value in *Specify no data value*.
5. Under *Specify vector asset that defines PSU population*, specify a GEE vector asset that outlines the population of PSUs. If shapefile exist, import into GEE from the Assets tab > New > Table upload.
6. Click *Load image* -- the map should be displayed in the image pane with all PSUs draped on top.
7. Optional: click *Display Class of Interest in PSUs* to calculate and display the proportion of the class of interest in each PSU as a proportion between zero and one.
8. In order to create the strata, you need specify a threshold or thresholds to divide the population of PSUs based on the proportion of the class of interest. For example, a threshold of 0.3 would create one stratum corresponding to the PSUs that contain the top 30% of the class of interest, and one stratum corresponding to the remaining PSUs. Specifying three thresholds of "0.25, 0.50, 0.75" would create four strata, one stratum that contains the top 25% PSUs, one that contains 25-50% of the top PSUs, one that contains 50-75% of the top PSUs and one with the remaining PSU. To understand what "Top x% PSUs" measn in this case. Think of a list of all the PSUs ranked by how much they contain the class of interest from 0 to 1. Specify the threshold under *Select proportion for dividing strata (0-1)* and click *Divide into strata*.
9. Specify the number of 30 PSUs to be included in the sample under *Specify desired number of Primary Sampling Units*, and click *Select PSUs*.
10. Specify the number of SSUs to selected in each of PSUs under *Specify desired number of SSUs in each PSU*. The total sample size will the number of selected PSUs times the number of selected SSUs. 
11. Optional: export the PSUs by clicking *Export PSUs* -- note that this is not necessarily for collecting sample data. 
12. Export the total sample for interpretation, click *Export sample* and select the desired file format.












