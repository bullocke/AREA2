Overview
========

As explained in the `Theoretical Background <https://gee-assessment-tools.readthedocs.io/en/latest/background.html>`_, areas of map categories should not be obtained by counting pixels in maps because of classification errors. Instead, a sample of reference observations need to be collected to which an unbiased estimator is applied to obtain an area estimate with confidence intervals. The tools provided here lend support for each step the estimation workflow.

The first step is selecting the sample locations where to observe reference conditions. Support for several sampling designs are provided. If land change is of interest, which is often a small part of the study area, `stratified sampling <https://gee-assessment-tools.readthedocs.io/en/latest/str_sample.html>`_ is recommended with the categories of change map are used to define strata. `Simple random <https://gee-assessment-tools.readthedocs.io/en/latest/srs_sample.html>`_ sampling is also supported, as are `stratified <https://gee-assessment-tools.readthedocs.io/en/latest/sys_sample.html>`_ and `simple systematic <https://gee-assessment-tools.readthedocs.io/en/latest/sys_str_sample.html>`_ sampling. 

The big benefit of Google Earth Engine is that the data needed to observe the reference conditions on the land surface are available without having to download the data. A couple of different applications are available to users to collect the reference observations 


`Timeseries Viewer <https://gee-assessment-tools.readthedocs.io/en/latest/tsviewer.html>`_

`Collection Earth <https://gee-assessment-tools.readthedocs.io/en/latest/colearth.html>`_

`TimeSync <https://gee-assessment-tools.readthedocs.io/en/latest/timesync.html>`_
