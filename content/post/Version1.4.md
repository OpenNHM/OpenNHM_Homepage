---
title: "Release Version 1.4"
date: 2023-01-23T00:00:00+01:00
draft: false
slug: "version1_4"
---

**Today we released [Version 1.4](https://github.com/avaframe/AvaFrame/releases/tag/1.4)** 

(and version 1.4.1; and this is totally not because I made the same mistake as before and
forgot to add some files...)

Version 1.4 

This version adds a new computiational module com5GlideSnow for glide snow avalanches, 
based on com1DFA.  It also adds an (untested) wetSnow friction type to com1DFA and gives an indication 
about the used parameterset in the simulation names of com1DFA. 

ENHANCEMENTS

- Glide snow [com5GlideSnow]
    - GlideSnow run script
    - glide snow standard tests
- SphKernelRadius setting option [com1DFA] 
- Wet snow friction type [com1DFA]
    - Wet snow standard tests
    - Docu paragraph for wetSnow
- Remove unused location option in addColorBar [out3Plot]
- Add avalanche coordinate system to particle properties [ana3AIMEC]
- Triangular initialization method [com1DFA]
- Indicator of default/changed to simulationname and report [com1DFA] #780 
    - Adds D/C to indicate default/changed parameter set in simulation name
    - Also adds info and changed parameters to report
- New workflow com1DFA:
    - com1DFAPreprocess
    - com1DFAMain
    - com1DFAPostprocess
- Add the dam tool [com1DFA]
    - Update com1DFA dam documentation
- Add reference simulation to contour plot
- Add contour plot to aimec
- Split cython files [com1DFA]
- Add filtering for greater or smaller than
- Add resDF to be saved for com1DFA results that can be used for statistical analysis [com1DFA]
- Match code to  the description in the theory paper. Added com1DFA options:
    - add the curvature in the pressure gradient computation
    - to add the curvature in the friction force
    - to add the curvature in the tangential equation

FIX

- Bug simName modelType [com1DFA]
- Saving plots and report generation [out3Plots][out1Peak] 
- Handle two deprecated warnings; test black formatter
- Approach velocity for rangeTimeDiagram; Issue #782
- Allow for string in search for resType #776 
- Bug for filtering function
- Bug in aimec warning Avatar

Felix
