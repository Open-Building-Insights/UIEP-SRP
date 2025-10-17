.. UIEP-SRP documentation master file, created by
   sphinx-quickstart on Fri Oct 17 10:54:07 2025.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to UIEP-SRP's documentation!
====================================
As cities continue to grow, so does their demand for energy. Harnessing local, 
renewable resources can help meet this need sustainably. Solar energy is a key ally in
decarbonizing the electricity sector, and rooftop solar plays a pivotal role in powering up urban areas.
The assessment of Solar Rooftop Potential with GIS is not new. Several methodologies and platforms are available.
However, below are a few of the limitations we have observed:

* Some are high-level (e.g., focusing just on incoming solar radiation, not taking into account urban morphology)
* More comprehensive methods exist, but are only available in a few locations (e.g., selected cities)
* Even when available, many of those are proprietary, limiting the availability of granular information to the general public, especially where it is most needed (e.g., vulnerable geographies).

**There is a lack of open-access, granular solar rooftop potential data in geographies that mostly need it.**

The combination of open-access & open-source remote sensing data & machine learning pipelines, 
presents a transformative opportunity in the energy access, energy modelling domain. With their use, we aim to “democratize” high granularity (building level)
and good accuracy Solar Rooftop Potential information at scale, and in geographies that need it the most, at a significantly lower cost. 

.. image:: /_static/Methodology.png

**Our approach:**
* Estimating the solar potential of rooftops in granular manner is a costly and time-consuming process. It requires high-granularity data, such as Digital Surface Models (DSMs), to accurately map urban morphology and accurately estimate the yield of incoming solar radiation. This data-intensive approach is typically limited to selected geographies (e.g., capital cities, wealthy neighbourhoods) leaving other areas unmapped.
* To address this, this project aims to train a U-Net convolutional neural network. This network is used to develop a normalized Digital Surface Models (nDSM) from open-source Sentinel-2 satellite imagery, resampling – in the process – the data from 10 meters to 50-centimeter spatial resolution.
* The resulting nDSM is then used in GRASS GIS, a powerful open-source geospatial processing engine. Using its advanced modelling and time series analysis capabilities, the annual solar potential is then extracted for all rooftops in any area of interest, enabling access to this information across all geographies Sentinel-2 data is available at.
* Solar Rooftop Potential results are then integrated to the Open Building Insights (OBI) platform, making the output easy to understand for non-technical users, and empowering stakeholders to make informed decisions about sustainable urban development.


.. toctree::
   :maxdepth: 2
   :caption: Contents:

Indices and tables
==================
* :ref:`Step 1: nDSM generation.`
* :ref:`modindex`
* :ref:`search`

