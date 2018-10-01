.. include:: <isopub.txt> 

Simple Random Sample |check|
==========================

Selecting a sample by simple random sampling requires you to specify the study area and a sample size. 

1. Start by running the Sampling Design script in the Scripts pane. 
2. In the first entry box *Specify an image ID and sampling scheme*, specify a map that defines the study area. Because you are not using strata or clusters, the contents of the map does not matter.
3. Under *Specify band if a multi-band map (if not, specify 1)*: if you are using a map that contains multiple bands, specify which band you want to use to define the study area.  Otherwise, just specify "1".
4. If the map has a no-data value or if you want to exclude a certain value in the map when defining the study area, specify the value in *Specify no data value*.
5. Click *Load image* -- the map should be displayed in the image pane.
6. Under *Select a sampling scheme*, select *Simple Random* 
7. Under *Determine sample size*, you can either specify an arbitrary sample size or determine the sample size by specifying a target standard error of the anticipated overall accuracy of the map that is being assessed.
8. If choosing to specify an arbitrary sample size, simply add a number under *Specify sample size*, and click *Create sample*.
9. To view, the sample in the Display pane, click *Add to map*
10. To export the sample, click *Export sample* and select the desired file format.