---
layout: page
title: ZTF Analysis
subtitle: Tools for Visualization and Analysis of ZTF Data
---

Over the years I have worked with Zwicky Transient Facility (ZTF) data, I have developed and made public several tools that aid in the visualization and analysis of ZTF photometry and imagery. These tools can be found on [My Github Site](https://github.com/zvanderbosch/ZTF_tools), with brief descriptions given below.

* [LC Interact](https://github.com/zvanderbosch/ZTF_tools/tree/main/LC_Interact)
	-  A Bokeh-based light curve and image inspection tool for ZTF data. Useful for inspecting the quality of light curve data points and visually assessing whether any outliers may be associated with image artifacts.
* [ZTF Quicklook](https://github.com/zvanderbosch/ZTF_tools/tree/main/ZTF_quicklook)
	- A python notebook for quick visualization and periodicity analysis of ZTF light curves. By default performs a 3.0 arcsecond radius query of the latest ZTF data release around the provided R.A. and Declination coordinates.
* [Bokeh Web Plot](https://github.com/zvanderbosch/ZTF_tools/tree/main/bokeh_web_plot)
	- A script for generating an HTML-embeddable interactive Bokeh plot. I use this code to embed two interactive plots on my wesbite (see [Debris Monitoring page](https://zvanderbosch.com/debris_monitoring/)) containing both ZTF data and Las Cumbres Observatory monitoring data.


