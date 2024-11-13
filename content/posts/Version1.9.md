---
title: "Release Version 1.9"
date: 2024-11-12T00:00:00+01:00
draft: false
slug: "version1_9"
---

**We released [Version 1.9](https://github.com/avaframe/AvaFrame/releases/tag/1.9)** 

**QGis users please note (after updating the plugin): do not forget to run Admin -> Update AvaFrame from within the 
toolbox to receive the updated core as well.** 

As is obvious by the long list below, this release contains plenty of bug fixes and internal improvements. 
The highlights are:
- changes for small avalanche calibration in com2AB (in relation to the QGis Connector)
- advanced installation instructions for Windows
- functions to create probability maps from non-com1DFA results
- plenty of com4FlowPy improvements and additional functionalities
- option for detrainment (in resistance areas) for com1DFA
- changes default range for propAna analysis

## What's Changed
* com4FlowPy bug-fixes/added functionality [com4] by @ahuber-bfw in https://github.com/avaframe/AvaFrame/pull/974
* adjust extent of plots and add tests by @awirb in https://github.com/avaframe/AvaFrame/pull/982
* functionality to create probMaps for peakfiles from different modules [ana4; out3] by @awirb in https://github.com/avaframe/AvaFrame/pull/976
* Fix various admin doc by @fso42 in https://github.com/avaframe/AvaFrame/pull/983
* fix typo in docs by @awirb in https://github.com/avaframe/AvaFrame/pull/984
* fix masking array for plot by @awirb in https://github.com/avaframe/AvaFrame/pull/985
* Hotfix for installation problem (script install) by @fso42 in https://github.com/avaframe/AvaFrame/pull/988
* issue936 com4FlowPy documentation [doc] by @ahuber-bfw in https://github.com/avaframe/AvaFrame/pull/987
* [com4FlowPy]: add travel length to output-files by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/990
* Immediate bugFixes to com4FlowPy and minor mode enhancement [com4] by @ahuber-bfw in https://github.com/avaframe/AvaFrame/pull/989
* [com4FlowPy] cell_counts BUG FIX and code simplification by @ahuber-bfw in https://github.com/avaframe/AvaFrame/pull/996
* Add ref to aimec [ana3; in3; out3] by @awirb in https://github.com/avaframe/AvaFrame/pull/992
* [com4FlowPy]: Add additional output: ForestInteraction Layer by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/997
* add docu for aimec reference [ana3] by @awirb in https://github.com/avaframe/AvaFrame/pull/999
* Add info about samosATAuto to doc [doc] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1000
* [com1DFA]: add detrainment by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/991
* change to array by @awirb in https://github.com/avaframe/AvaFrame/pull/1008
* [com4FlowPy]: option for dynamic max_z_delta by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/995
* Make syntax compatible with NumPy 2.0 by @ninsbl in https://github.com/avaframe/AvaFrame/pull/1007
* [doc]: Docu for detrainment by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1004
* Add aimec summary fig [out3] by @awirb in https://github.com/avaframe/AvaFrame/pull/1011
* add max velocity option to rangeTime diagram [ana5;out3] by @awirb in https://github.com/avaframe/AvaFrame/pull/1013
* fix issue with entrainment from shapefile; fixes #1009 by @fso42 in https://github.com/avaframe/AvaFrame/pull/1012
* Restructure com2AB parameter setup [com2] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1015
* change python version in test action by @fso42 in https://github.com/avaframe/AvaFrame/pull/1018
* [com4FlowPy] added support for .tif and .asc input/output, output files configurable via .ini by @ahuber-bfw in https://github.com/avaframe/AvaFrame/pull/1001
* add release volume info into report [com1] by @awirb in https://github.com/avaframe/AvaFrame/pull/1014
* use returned array in probAna [ana4] by @awirb in https://github.com/avaframe/AvaFrame/pull/1021
* add pytest for non-matching nrows and ncols of files for probAnalysis by @awirb in https://github.com/avaframe/AvaFrame/pull/1022
* Handle bug about simName / scenario mismatch in report (Windows QGis GUI); issue #872 [com1] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1024
* Start adding gallery in visualisation documentation by @fso42 in https://github.com/avaframe/AvaFrame/pull/1020
* [com4FlowPy]: minor modification for log-file by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1028
* fix runtime cython error on windows with current libs [com1] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1029
* Add units to parameters in ini file; update com5 resistance [com1; com5] by @leon-wagner in https://github.com/avaframe/AvaFrame/pull/1023
* Update Advanced Usage chapter in docs [doc] by @leon-wagner in https://github.com/avaframe/AvaFrame/pull/1031
* Add small indicator to com2AB outputs [com2] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1032
* Change default probAna range; fixes #967 [ana4] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1033
* Change runout info altitude for friction adjustment (request by WLV) [doc] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1034
* Adds a try except for cmcrameri lipari colormap (missing in older versions)[out3] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1035
* Adjust releaseWithManyLinux, start switching to cibuildwheel by @fso42 in https://github.com/avaframe/AvaFrame/pull/1036
* revers long long vs long again; adjust setup.py and releaseMany [com1] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1041

## New Contributors
* @ahuber-bfw made their first contribution in https://github.com/avaframe/AvaFrame/pull/974
* @leon-wagner made their first contribution in https://github.com/avaframe/AvaFrame/pull/1023

**Full Changelog**: https://github.com/avaframe/AvaFrame/compare/1.8.3...1.9

Felix
