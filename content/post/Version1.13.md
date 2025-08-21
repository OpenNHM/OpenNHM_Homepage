---
draft: false
publishDate: 2025-08-21
author: Felix
subtitle: ""
title: Release Version 1.13
tags:
  - avaframe
  - version
image: img/FZGL_PFD.jpg
categories:
  - whatever
description: "New release version 1.13: com1DFA resistance change and move to pixi"
---

**We released [Version 1.13](https://github.com/avaframe/AvaFrame/releases/tag/1.13)** 

The resistance and pixi release. 

**QGis users please note (after updating the plugin): do not forget to run Admin -> Update AvaFrame from within the 
toolbox to receive the updated core as well.** 

**IMPORTANT NOTE:: This release has a noticeable difference in the way com1DFA treats resistance areas! With the new
default setup, the resistance has a much stronger effect, including removal of mass. Please
see https://doi.org/10.5281/zenodo.16893215 for more information on differences (German only) and/or investigate the
effects for your application. Our resistance benchmarks show the difference as well, we will include the report and
updated benchmarks in the next minor release.**

Additional modifications of note:

- We moved to using pixi as our development environment, see the documentation for more information
- Added scarp tools for com6Rockavalanche (will also show up in the QGis Connector)
- Added two new modules: com8PSA and com9MoTVoellmy; this is in a purely development stage yet.  
- Added particle stopping and surface adaptation according to deposition and erosion in com1DFA 
- Added faster backtracking for com4FlowPy


## What's Changed
* docs(com1DFA, com2AB): clarify optional files and output naming by @fso42 in https://github.com/avaframe/AvaFrame/pull/1121
* [com1] Add comment, fix small bug by @RolandFischbacher in https://github.com/avaframe/AvaFrame/pull/1123
* [sys]: switch to pixi and hatchling build backend by @fso42 in https://github.com/avaframe/AvaFrame/pull/1124
* [doc] update documentation build instructions and dependencies by @fso42 in https://github.com/avaframe/AvaFrame/pull/1125
* [sys] add .gitattributes file to configure github linguist detection by @fso42 in https://github.com/avaframe/AvaFrame/pull/1127
* [com4] use custom path only for DEM (for CAIROS) by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1129
* [runscripts] adjust log handling in project initialization by @fso42 in https://github.com/avaframe/AvaFrame/pull/1130
* [in2]: improve error messages for shape file validation by @fso42 in https://github.com/avaframe/AvaFrame/pull/1131
* [com4] use raster functions (for .asc and .tif) from AvaFrame by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1095
* [com4]: delete rasterIo by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1133
* [com4FlowPy] faster backTracking, previewMode and minor improvs by @ahuber-bfw in https://github.com/avaframe/AvaFrame/pull/1138
* [com1] add option for resistance by @awirb in https://github.com/avaframe/AvaFrame/pull/1105
* add old info from computations of already performed sims by @awirb in https://github.com/avaframe/AvaFrame/pull/1141
* [doc] Add new resistance setup to doc by @fso42 in https://github.com/avaframe/AvaFrame/pull/1137
* [sys] Fix deployment via github actions and pypi by @fso42 in https://github.com/avaframe/AvaFrame/pull/1144
* [sys] Adjust deployment for smaller wheel sizes by @fso42 in https://github.com/avaframe/AvaFrame/pull/1145
* [sys] enable `include-package-data` in setuptools configuration by @fso42 in https://github.com/avaframe/AvaFrame/pull/1146
* com6RockAvalanche: add scarp.py, runCom6Scarp.py & scarpCfg.ini [com6] by @dwolfsch in https://github.com/avaframe/AvaFrame/pull/1042
* [com1;sys] Clean log output; update Readme badges by @fso42 in https://github.com/avaframe/AvaFrame/pull/1150
* docs(moduleCom6RockAvalanche): improve input/output and naming clarifications by @fso42 in https://github.com/avaframe/AvaFrame/pull/1151
* [com1] exporting of release and entrainment raster produced from shp files by @awirb in https://github.com/avaframe/AvaFrame/pull/1153
* [runscript] adjust ranteTime to allow for reading result files without config file by @awirb in https://github.com/avaframe/AvaFrame/pull/1155
* add docu for range time with inputs from another module by @awirb in https://github.com/avaframe/AvaFrame/pull/1156
* [com8] Add initial com8MotPSA and com9MoTVoellmy  by @fso42 in https://github.com/avaframe/AvaFrame/pull/1149
* [com1]: option to delete stopped particles, and adapt surface according to deposition & erosion by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1112
* chore(config): remove `.pep8speaks.yml` and update `pyproject.toml` Python support; docu com8 and coom9 by @fso42 in https://github.com/avaframe/AvaFrame/pull/1157
* docs(index): add documentation for `com8MoTPSA` and `com9MoTVoellmy` modules by @fso42 in https://github.com/avaframe/AvaFrame/pull/1158
* [doc]: add adapt surface by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1140
* [com4]: Add result file: minimum of travel length and travel angle by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1159
* [out1] add compute area indicators based on real area not transformed into thalweg following by @awirb in https://github.com/avaframe/AvaFrame/pull/1166

## New Contributors
* @dwolfsch made their first contribution in https://github.com/avaframe/AvaFrame/pull/1042

Felix
