.. include:: <isopub.txt> 

.. image:: _nolinesoftext.png
   :width: 175pt
   
------------

What is AREA :superscript:`2`? |check|
======================================

AREA :superscript:`2` ("area squared"), short for *Area Estimation & Accuracy Assessment*, is a Google Earth Engine application that provides comprehensive support for sampling and estimation in a design-based inference framework. Several sampling designs and estimators are supported. The aim of AREA :superscript:`2` is to provide users the tools necessary to comply with recommended practices and international guidance for estimation areas of land categories and land change, and to assess the accuracy of maps.

As explained in the `Theoretical Background <https://gee-assessment-tools.readthedocs.io/en/latest/background.html>`_, areas of map categories should not be obtained by counting pixels in maps because of classification errors. Instead, a sample of reference observations need to be collected to which an unbiased estimator is applied. AREA :superscript:`2` allows users to design a sample according to various design criteria and objectives. 

A big benefit of Google Earth Engine is that the data needed to observe the reference conditions on the land surface are available without having to download the data. `Time Series Viewer <https://gee-assessment-tools.readthedocs.io/en/latest/tsviewer.html>`_ is a part of AREA :superscript:`2` it extracts time series of all available Landsat and Sentinel-2 observations for reconstruction of changes on the land surface. `Collect Earth Online <https://gee-assessment-tools.readthedocs.io/en/latest/colearth.html>`_  and  `TimeSync <https://gee-assessment-tools.readthedocs.io/en/latest/timesync.html>`_ are other applications that provide direct access to reference data using Google Earth Engine.

Once the sample data have been collected, an estimator that corresponds to the sampling design provide an estimate or area or accuracy with confidence intervals when applied to the sample data. Different estimator are more or less efficient Support for various estimators are provided in addition to guidance for choosing an appropriate estimator.