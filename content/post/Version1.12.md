---
#type: post
#layout: "post"
title: Release Version 1.12
author: Felix
subtitle: ""
publishDate: 2025-04-28
#date: 2025-05-18T10:36:44+02:00
#highlight: true
draft: false
#slug: "version1_12"
image: "img/FZGL_PFD.jpg"
#image: "https://i.imgur.com/prPLcUi.jpg"
tags:
  - avaframe
  - version
categories: ["whatever"]
---

**We released [Version 1.12](https://github.com/avaframe/AvaFrame/releases/tag/1.12)** 

**QGis users please note (after updating the plugin): do not forget to run Admin -> Update AvaFrame from within the 
toolbox to receive the updated core as well.** 

There are many small fixes and improvements in this release, but two main points:
- for com1DFA, output is now constantly saved during a run, allowing to resume computation if the run was interrupted. Previously the results were only written at the end.
- If a release thickness raster is provided for com1DFA, this in now also remeshed in case of a mismatched cellsize. Previously com1DFA expected the DEM and release thickness raster cellsize to already match. However we still recommend to remesh the input data in advance. 

## What's Changed
* add info of DAM file by @awirb in https://github.com/avaframe/AvaFrame/pull/1093
* [com4] Further mass redistribution/correction modifications by @theweathermanda in https://github.com/avaframe/AvaFrame/pull/1084
* [com4FlowPy] minor Bugfix, documentation update and added feature for "forestFriciton", "forestDetrainment" and "forestFrictionLayer" model options by @ahuber-bfw in https://github.com/avaframe/AvaFrame/pull/1087
* fix SyntaxWarning by @leon-wagner in https://github.com/avaframe/AvaFrame/pull/1097
* [in2;in3] fix problem with -9999 not interpreted correctly py rasterio on remeshing by @fso42 in https://github.com/avaframe/AvaFrame/pull/1098
* [com1] add note to thickness by @awirb in https://github.com/avaframe/AvaFrame/pull/1099
* [com1;out3] add info on secrel, ent, res, and dam in releaseScenario plot by @awirb in https://github.com/avaframe/AvaFrame/pull/1096
* [in2;out3] Add profile plot by @awirb in https://github.com/avaframe/AvaFrame/pull/1100
* [ana3AIMEC]: correct comments by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1102
* [in3] Problem with non-closed shape polygons  by @awirb in https://github.com/avaframe/AvaFrame/pull/1103
* [com1]: changed a function call by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1106
* [doc]: fixed minor bugs in representation by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1107
* [com1] fix bug in plot that shows release thickness in release scenario of read from relTh file by @awirb in https://github.com/avaframe/AvaFrame/pull/1109
* [com5; com6]: rename functions to be consistent with com1DFA by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/1108
* [sys] Add Qlty (codeclimate replacement) and remove Codecov integration by @fso42 in https://github.com/avaframe/AvaFrame/pull/1111
* [com1; in3] save files during run;  enable to resume computation if interrupted  by @awirb in https://github.com/avaframe/AvaFrame/pull/1078
* Changed docu about windows install [doc] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1117
* Add remeshing of relth raster file [com1] by @fso42 in https://github.com/avaframe/AvaFrame/pull/1116
* chore(release): add support for `python 3.13` by @fso42 in https://github.com/avaframe/AvaFrame/pull/1118
* Revert source dist python  by @fso42 in https://github.com/avaframe/AvaFrame/pull/1119
* docs(visualization): add profile plot to gallery; fixes #1101 by @fso42 in https://github.com/avaframe/AvaFrame/pull/1120

## New Contributors
* @theweathermanda made their first contribution in https://github.com/avaframe/AvaFrame/pull/1084

Felix
