---
layout: page
title: phot2lc
subtitle: A pure-Python Light Curve Extraction Suite
---
[Github Page](https://github.com/zvanderbosch/phot2lc)      
[![PyPI](https://img.shields.io/pypi/v/phot2lc.svg)](https://pypi.org/project/phot2lc/)      
[![Docs](https://readthedocs.org/projects/phot2lc/badge/?version=latest)](https://phot2lc.readthedocs.io/en/latest/?badge=latest)

Throughout my time as an observational astronomy PhD student, I have obtained and reduced enough data to fill up my computer hard drive several times over. My data typically come in the form of time-series photometry, meaning that when I'm at the telescope I will observe a single star for several hours at a time, taking one image after another in 5-10 second intervals, often resulting in hundreds or even thousands of images per night (about 1 GB). Ultimately, these images will need to be converted into light curves, which are the final data product indicating a star's brightness versus time, typically in units of percent change relative to the average brightness. To get from raw images to light curves, the following steps are performed:

* Image Calibrations (Dark, Flat, and Bias corrections)
* Circular Aperture Photometry
* Light Curve Extraction

*phot2lc* handles the light curve extraction step, and is a pure-Python interactive program inspired largely by WQED ([Thompson & Mullally 2009](https://ui.adsabs.harvard.edu/abs/2009JPhCS.172a2081T/abstract), [2013](https://ui.adsabs.harvard.edu/abs/2013ascl.soft04004T/abstract)). While not nearly as extensive in its scope as WQED, *phot2lc* has several key features which make it a much more efficient and user-friendly tool for light curve extraction. The first such feature is its ease of installation. *phot2lc* is a Python package and can be installed with:

pip install phot2lc

Detailed documentation for *phot2lc* can be found at 

For each step, one or more software tools are needed. When I first started obtaining and reducing data, the tools which I was taught to use were [IRAF (Image Reduction and Aalysis Facility)](https://iraf.net/) for image reductions, [*ccd_hsp*](https://ui.adsabs.harvard.edu/abs/2002A%26A...389..896K/abstract) (an IRAF package) for aperture photometry, and [WQED](https://ui.adsabs.harvard.edu/abs/2009JPhCS.172a2081T/abstract) for light curve extraction. While these are all powerful tools, the primary challenge they pose to new users is their ease of installation. For me, it took several weeks to get everything working properly. IRAF has been around since the 1980s and has been so fundamentally important to astronomers, people still try to install it on new computers despite the pain they know is waiting for them. This process can be so painful at times that once astronomers finally get IRAF working, many will then refuse to ever update their operating systems for fear of breaking something. Actually, installation isn't always difficult thanks to [the efforts of the Space Telescope Science Institute (STScI)](https://astroconda.readthedocs.io/en/latest/installation.html), but many IRAF tasks have 32-bit dependencies that are no longer supported on some modern machines and OS's ([MacOS Catalina for example](https://medium.com/@krisastern/installing-iraf-pyraf-on-mac-with-linux-vm-767fb99ec757)), and STScI no longer provides institutional support for IRAF. A full replacement for IRAF in modern coding languages still doesn't exist, though small pieces have been re-written in Astropy and various other Python packages.

So, IRAF is one issue, but it's such a monumental piece of software, no one person could hope to re-write the whole thing. WQED poses another problem. WQED is a software suite designed for light curve extaction and on its own is not hard to install. The difficulty comes with its dependency on PGPLOT, a library of plotting routines that are necessary for WQED's GUI. This [PGPLOT installation guide](http://mingus.as.arizona.edu/~bjw/software/pgplot_fix.html) hints at some of the potential issues

**phot2lc is a pure-Python interactive tool for extracting light curves from time-series photometric data.** 

**phot2lc** is largely inspired by WQED ([Thompson & Mullally 2009](https://ui.adsabs.harvard.edu/abs/2009JPhCS.172a2081T/abstract), [2013](https://ui.adsabs.harvard.edu/abs/2013ascl.soft04004T/abstract)), and is designed to work with the output photometry from both MAESTRO ([Dalessio 2010](https://ui.adsabs.harvard.edu/abs/2010AAS...21545209D/abstract), [2013](https://ui.adsabs.harvard.edu/abs/2013PhDT.......170D/abstract)) and ccd_hsp ([Kanaan et al. 2002](https://ui.adsabs.harvard.edu/abs/2002A%26A...389..896K/abstract)).

While not nearly as extensive in its scope as WQED, **phot2lc** has several key features which make it a much more efficient and user-friendly tool for light curve extraction. The first such feature is its ease of installation. **phot2lc** is a Python package and can be installed with:

    pip install phot2lc

Detailed documentation for **phot2lc** can be found at 
