---
title: "Release Version 1.10"
date: 2025-02-10T00:00:00+01:00
draft: false
slug: "version1_10"
---

**We released [Version 1.10](https://github.com/avaframe/AvaFrame/releases/tag/1.10)** 

**QGis users please note (after updating the plugin): do not forget to run Admin -> Update AvaFrame from within the 
toolbox to receive the updated core as well.** 

The path generation and geotiff release. So the main changes are:
* The raster reading routines now accept geotiff files as well 
* we updated the automatic path generation, this will also end up in the QGis connector
* added a new spatialVoellmy friction setup, to read mu/xi values from raster during initialization. 
* fix a long/long Windows bug (again...)
* some plot can include a (online) background map

Please be aware: the module ascUtils is being deprecated. Please use rasterUtils which has the same functions in it. ascUtils will be removed in a future version. 

**Also be aware: The benchmarks give slightly changed results!** The differences are well within accepted ranges. They originate from the new interpolation during remeshing (using rasterio) and / or the slight changes during conversion from asc to tif topography (see avaAlr). We will update the benchmarks in the next release and add the difference report there. 

## What's Changed
* add underscore in file name search using resType by @leon-wagner in https://github.com/avaframe/AvaFrame/pull/1040
* [out3]: Fix bugin AIMEC plot  by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1043
* Fix no points in shp reading routines [in2] by @awirb in https://github.com/avaframe/AvaFrame/pull/1045
* [doc]: Adapt Docu (W. Fellin suggestions) by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1047
* add new friction model spatialVoellmy [com1] by @awirb in https://github.com/avaframe/AvaFrame/pull/1046
* change default input and add in ini in probAnalysis [ana4] by @awirb in https://github.com/avaframe/AvaFrame/pull/1049
* Update glossary.rst [doc] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1026
* fix wrong indents in glossary by @awirb in https://github.com/avaframe/AvaFrame/pull/1050
* update DFA path runscript [ana5; runscripts] by @leon-wagner in https://github.com/avaframe/AvaFrame/pull/1039
* Set dtypes for integer, Windows Long Long problem again [com1] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1052
* [doc]: update links to packages for com4FlowPy  by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1054
* [doc]: update (again) com4FlowPy docu by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1055
* [com1DFA]: Add options for computing resistance (especially dealing with hEff) by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/993
* fix com2AB multiple lines issue [com2] by @leon-wagner in https://github.com/avaframe/AvaFrame/pull/1060
* update check for extent of mu, xi fields [com1] by @awirb in https://github.com/avaframe/AvaFrame/pull/1056
* Add an output raster: sum of flux [com4] by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1048
* disable overlap checking for secrels; fixes #1065 [com1] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1066
* [com4FlowPy]: new computation of zDeltaSum by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1067
* remove setting label for contourline at collections [out3] by @awirb in https://github.com/avaframe/AvaFrame/pull/1077
* update documentation with changes to DFAPath script [doc] by @leon-wagner in https://github.com/avaframe/AvaFrame/pull/1051
* Include rasterio for geotiff and wmts plotting  by @fso42 in https://github.com/avaframe/AvaFrame/pull/1059


**Full Changelog**: https://github.com/avaframe/AvaFrame/compare/1.9...1.10


Felix
