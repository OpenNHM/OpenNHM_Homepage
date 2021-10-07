---
title: "This month in AvaFrame - September 2021 edition"
date: 2021-10-05T00:00:00+01:00
draft: false
---

We're back from summer! And with some exciting news too!

[Version 0.6](https://github.com/avaframe/AvaFrame/releases/tag/v0.6), 
the **QGis/pypi and testing** - release, was published.

So what is included in this release?

- The installation process was completely changed and (hopefully) made a lot easier for you:
  - installation of AvaFrame is now working via [pypi](https://pypi.org/project/avaframe/), 
  i.e. through *pip install avaframe*. 
  - the *pip* install is provided for Windows, Linux and MacOS for python versions *> 3.6*. Note that
  we did not test MacOS (anyone got a free Macbook lying around?! :-); seriously: if you work on MacOS
  we'd be happy about some feedback!)
  - the QGis connector plugin is now in the public
  [QGis plugin directory](https://plugins.qgis.org/plugins/avaframeConnector/) 
  and installable via the QGis plugin manager. This allows you to run the standard operational 
  workflow from within QGis.
  - see our [installation instructions](https://docs.avaframe.org/en/latest/installation.html) for more information

- Our testing / code coverage has improved considerably. We are still long ways away from perfect, but this is an 
  ongoing process. As a side-note: we switched from codecoverage to codeclimate as service provider, since we felt we
  gain more insights this way. 
 
- Modules with the most substantial changes are:
  - *com1DFA*:
    - any resolution is possible (also see the new [FAQ](https://docs.avaframe.org/en/latest/FAQ.html))
    - option to track particles by ID and know which parent particle they originate from. 
    - include entrainment thickness from shapefiles
    - new option for the initialisation of particle mass
  - *ana3AIMEC*: adjust raster cellsize (for different resolutions) and mass analysis plots

- And as always: many more functional changes under the hood, see the main ones in our 
 [release notes](https://docs.avaframe.org/en/latest/releaseNotes.html).
 
We invite you to give this version a try, especially the *standard installation using QGis*. Please let us know
if you run into problems (which you will...). We are looking forward to your feedback!

And since I can see fresh snow up on the mountains from where I'm writing this: let the next avalanche season begin...

Till next month, 

Felix
 
    

<!--  LocalWords:  QGis pypi avaframe MacOS
 -->
