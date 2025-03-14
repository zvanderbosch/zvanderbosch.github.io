---
layout: page
title: phot2lc
subtitle: A pure-Python Light Curve Extraction Suite
---
<p align="middle">
    <a href="https://pypi.org/project/phot2lc/">
        <img src="https://img.shields.io/pypi/v/phot2lc.svg" width="100" />
    </a>
    <a href="https://github.com/zvanderbosch/phot2lc">
        <img src="/img/GitHub-Mark-120px-plus.png" width="60" /> 
    </a>
    <a href="https://phot2lc.readthedocs.io/en/latest/?badge=latest">
        <img src="https://readthedocs.org/projects/phot2lc/badge/?version=latest" width="100" />
    </a>
</p>

![phot2lc Screenshot](/img/phot2lc_screenshot.png#center)

Throughout my time as an observational astronomer, I have obtained and reduced many hundreds of gigabytes of data. Much of this data comes in the form of time-series photometry, meaning hudreds of consecutive images taken in intervals of a few seconds over the course of minutes to hours fpr single stars. Ultimately these images need to be converted into light curves indicating the brightness of the star versus time. To get from raw images to light curves, the following steps are performed:

* Image Calibrations (Dark, Flat, and Bias corrections)
* Circular Aperture Photometry
* Light Curve Extraction

*phot2lc* was born from the desire to have a more efficient tool for light curve extraction from time-series photometry, especially in the event that light curves from multiple aperture sizes need to be analyzed to determine the optimal size. 

*phot2lc* is a pure-Python interactive program for light curve extraction inspired largely by WQED ([Thompson & Mullally 2009](https://ui.adsabs.harvard.edu/abs/2009JPhCS.172a2081T/abstract), [2013](https://ui.adsabs.harvard.edu/abs/2013ascl.soft04004T/abstract)). While not nearly as extensive in its scope as WQED, *phot2lc* has several key features which make it a much more efficient and user-friendly tool for light curve extraction. The first such feature is its ease of installation. *phot2lc* is a Python package and can be installed with:

    pip install phot2lc

Detailed documentation for *phot2lc* can be found at [phot2lc.readthedocs.io](https://phot2lc.readthedocs.io/en/latest/?badge=latest)

### List of Features

* Standard Light Curve Manipulation Tools:
    - Delete/Add single points
    - Delete points inside and outside a drawn box
    - Divide by a polynomial of chosen order
    - Delete outliers with a sigma clipping routine
    - Comparison star selection
* Analyzes photometry for all apertures sizes at once
* Automated determination of optimal aperture size
* Automated determination of optimal comparison star combination
* Barycentric time corrections with Astropy accounting for:
    - Object RA and Dec Coordinates
    - Observatory Location
    - Leap Seconds
* Additional tools for post-processing:
    - **weldlc** for combining light curves
    - **quicklook** for quick analysis of light curves and their periodograms
* Automatically loads previous changes made to a light curve (i.e. same deleted points, polynomial, and comparison stars) when *phot2lc* is re-run for an object.

