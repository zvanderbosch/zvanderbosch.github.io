---
layout: page
title: phot2lc
subtitle: A pure-Python Light Curve Extraction Suite
---

Throghout my time as an observational astronomy PhD student, I have obtained and reduced enough data to fill up my computer hard drive several times over. My data typically come in the form of time-series photometry, meaning that when I'm at the telescope I will often observe a single star for several hours at a time, taking one image after another in 5-10 second intervals. Each night I end up with hundreds or even thousands of images. 

The final product from these images will ultimately be a light curve, which is a measurement of a star's brightness versus time. To get from raw images to light curves, the following steps are typically performed:

* Image Calibrations (Dark, Flat, and Bias corrections)
* Circular Aperture Photometry
* Light Curve Extraction

**phot2lc is a pure-Python interactive tool for extracting light curves from time-series photometric data.** 

**phot2lc** is largely inspired by WQED ([Thompson & Mullally 2009](https://ui.adsabs.harvard.edu/abs/2009JPhCS.172a2081T/abstract), [2013](https://ui.adsabs.harvard.edu/abs/2013ascl.soft04004T/abstract)), and is designed to work with the output photometry from both MAESTRO ([Dalessio 2010](https://ui.adsabs.harvard.edu/abs/2010AAS...21545209D/abstract), [2013](https://ui.adsabs.harvard.edu/abs/2013PhDT.......170D/abstract)) and ccd_hsp ([Kanaan et al. 2002](https://ui.adsabs.harvard.edu/abs/2002A%26A...389..896K/abstract)).

While not nearly as extensive in its scope as WQED, **phot2lc** has several key features which make it a much more efficient and user-friendly tool for light curve extraction. The first such feature is its ease of installation. **phot2lc** is a Python package and can be installed with:

    pip install phot2lc

Detailed documentation for **phot2lc** can be found at 
