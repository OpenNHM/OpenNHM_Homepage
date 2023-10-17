---
title: "Release Version 1.6"
date: 2023-08-29T00:00:00+01:00
draft: false
slug: "version1_6"
---

**Today we released [Version 1.6](https://github.com/avaframe/AvaFrame/releases/tag/1.6)** 

The samosATAuto release:
The biggest, most obvious change in this release is the introduction of a samosATAuto friction relation (set as
default). It decides the friction calibration for samosAT friction relation based on release volume (small, medium,
large). This also means that some of our benchmarks show differences (see attached zip) for those avalanches that are
now in the categories small or medium. We will update our benchmark results with the next release. It also means that we
now have moved away from a single mu setting (in com1DFACfg.ini) for all friction relations and gave each friction model
its own mu setting. Also, the simulation names indicate the friction calibration if small or medium was used.

Other changes include:
* separate runscripts for  com1 and com2 (instead of using the runOperational with options)
* runscript for probabilityMaps (needed for the QGis connector)
* functions for release area statistics
* functions for particle tracking 

There is one breaking change regarding the function `cleanSingleAvaDir`:
Remove keep log parameter from cleanSingleAvaDir

## Relevant PRs:
* Prepare ana4ProbAna for QGis connector by @fso42 in https://github.com/avaframe/AvaFrame/pull/829
* Refactor glossary  by @jtfisch in https://github.com/avaframe/AvaFrame/pull/830
* add remeshing result files for probMap [ana4Prop][out3plot] by @awirb in https://github.com/avaframe/AvaFrame/pull/835
* Make error on features outside DEM clearer [in2Trans] by @fso42 in https://github.com/avaframe/AvaFrame/pull/836
* Add modelType to com5 cfg; remove kernel radius setting [com5] by @fso42 in https://github.com/avaframe/AvaFrame/pull/838
* add optional argument for general config by @awirb in https://github.com/avaframe/AvaFrame/pull/839
* Fix boundary bug in plotUtils [ou3Plot]; add missing ini parameter [ana4] by @fso42 in https://github.com/avaframe/AvaFrame/pull/840
* split and add line point snapping distance functions by @awirb in https://github.com/avaframe/AvaFrame/pull/841
* add snap point to line and analysis plots [in3Utils] [out3Plots] by @awirb in https://github.com/avaframe/AvaFrame/pull/843
* add flag for exports and create contour line plot [com1DFA] by @awirb in https://github.com/avaframe/AvaFrame/pull/844
* add creating rel info file [com1DFA] by @awirb in https://github.com/avaframe/AvaFrame/pull/845
* remove unused check for contourType [out3Plot] by @awirb in https://github.com/avaframe/AvaFrame/pull/850
* Fix failing doc  by @fso42 in https://github.com/avaframe/AvaFrame/pull/853
* add acceleration to particle info [com1DFA] by @awirb in https://github.com/avaframe/AvaFrame/pull/851
* rename frict model parameters to include model name [com1DFA] by @awirb in https://github.com/avaframe/AvaFrame/pull/849
* fix bug in adding dem in probmap plot [ana4Stats] by @awirb in https://github.com/avaframe/AvaFrame/pull/855
* rename travelAngle of particles to trajectoryAngle [com1DFA] by @awirb in https://github.com/avaframe/AvaFrame/pull/856
* Update probAna run script example by @awirb in https://github.com/avaframe/AvaFrame/pull/861
* add capability of adding small and medium size calibration values [com1DFA] by @fso42 in https://github.com/avaframe/AvaFrame/pull/857
* add RELTH to folderstruct [in3Utils] by @fso42 in https://github.com/avaframe/AvaFrame/pull/864
* Rename glidesnow to snowslide [com5] by @fso42 in https://github.com/avaframe/AvaFrame/pull/865
* Fix graphvix on rtd by @fso42 in https://github.com/avaframe/AvaFrame/pull/867
* Prepare RelInfo for the connector [in1Data] by @fso42 in https://github.com/avaframe/AvaFrame/pull/869
* remove unused filter option, change input for ana4Prob run script [ana4Prop] by @awirb in https://github.com/avaframe/AvaFrame/pull/862
* fix line in docu by @awirb in https://github.com/avaframe/AvaFrame/pull/871
* address change in scipy libraries [in1Data] by @awirb in https://github.com/avaframe/AvaFrame/pull/878
* Add Friction model option that chooses L/M/S based on release volume [com1DFA] by @awirb in https://github.com/avaframe/AvaFrame/pull/874
* add ci95 to HelixChannel and Mal releases by @fso42 in https://github.com/avaframe/AvaFrame/pull/882
* remove : from path for amaP by @awirb in https://github.com/avaframe/AvaFrame/pull/883
* only use relthFile if relThFromFile true [com1] by @awirb in https://github.com/avaframe/AvaFrame/pull/888
* RelTh file check for nans [com1] by @awirb in https://github.com/avaframe/AvaFrame/pull/887
* Prob plots [com1; out3; ana4] by @awirb in https://github.com/avaframe/AvaFrame/pull/886
* add input read function [com1] by @awirb in https://github.com/avaframe/AvaFrame/pull/892
* Include particle plots and comparisons [com1;ana5;out3;in1;ana3;in3;out3] by @fso42 in https://github.com/avaframe/AvaFrame/pull/880
* add flag for label in contourplots [out3] by @awirb in https://github.com/avaframe/AvaFrame/pull/895
* Add plot of release scenario [com1] by @awirb in https://github.com/avaframe/AvaFrame/pull/894
* add optional input dir for aimec analysis by @awirb in https://github.com/avaframe/AvaFrame/pull/896
* Fix docu by @awirb in https://github.com/avaframe/AvaFrame/pull/897
* Prepare com1dfa com2AB runscripts for QGis_AF; add size indicator to simname [com1] by @fso42 in https://github.com/avaframe/AvaFrame/pull/870
* Fix name problems in runStandardTests by @fso42 in https://github.com/avaframe/AvaFrame/pull/900


**Full Changelog**: https://github.com/avaframe/AvaFrame/compare/1.5.2...1.6

Felix
