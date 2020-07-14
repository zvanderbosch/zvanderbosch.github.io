---
layout: page
title: phot2lc
subtitle: A pure-Python Light Curve Extraction Suite
---
[![PyPI](https://img.shields.io/pypi/v/phot2lc.svg)](https://pypi.org/project/phot2lc/)

[![Github Link](img/GitHub-Mark-64px.png#center)](https://github.com/zvanderbosch/phot2lc)

[![Docs](https://readthedocs.org/projects/phot2lc/badge/?version=latest)](https://phot2lc.readthedocs.io/en/latest/?badge=latest)<-

![phot2lc Screenshot](/img/phot2lc_screenshot.png)

Throughout my time as an observational astronomy PhD student, I have obtained and reduced enough data to fill up my computer hard drive several times over. My data typically come in the form of time-series photometry, meaning that when I'm at the telescope I will observe a single star for several hours at a time, taking one image after another in 5-10 second intervals, often resulting in hundreds or even thousands of images per night (about 1 GB). Ultimately, these images will need to be converted into light curves, which are the final data product indicating a star's brightness versus time, typically in units of percent change relative to the average brightness. To get from raw images to light curves, the following steps are performed:

* Image Calibrations (Dark, Flat, and Bias corrections)
* Circular Aperture Photometry
* Light Curve Extraction

*phot2lc* handles the light curve extraction step, and is a pure-Python interactive program inspired largely by WQED ([Thompson & Mullally 2009](https://ui.adsabs.harvard.edu/abs/2009JPhCS.172a2081T/abstract), [2013](https://ui.adsabs.harvard.edu/abs/2013ascl.soft04004T/abstract)). While not nearly as extensive in its scope as WQED, *phot2lc* has several key features which make it a much more efficient and user-friendly tool for light curve extraction. The first such feature is its ease of installation. *phot2lc* is a Python package and can be installed with:

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

