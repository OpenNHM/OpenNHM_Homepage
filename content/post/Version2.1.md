---
draft: false
publishDate: 2026-06-11
author: Felix
subtitle: ""
title: AvaFrame Version 2.1
tags:
  - avaframe
  - version
  - release
categories:
  - whatever
description: "AvaFrame 2.1: build-on-release for com9MoTVoellmy, com1DFA particle property selection,
com4FlowPy per-cell output, and various fixes"
---

**We released [AvaFrame Version 2.1 (full changelog)](https://github.com/OpenNHM/AvaFrame/releases/tag/2.1)**

This release focuses on stability fixes in com1DFA, major changes to the com9MoTVoellmy build pipeline, and new output
features across com4FlowPy and com6RockAvalanche.

**Key changes:**

- **com9MoTVoellmy build-on-release:** The C binary is now compiled at release time (or on demand) instead of shipping
  precompiled binaries. Source is fetched automatically from the latest upstream MoT-Voellmy release. This release
  includes MoT-Voellmy [v2026-05-04](https://github.com/norwegian-geotechnical-institute/MoT-Voellmy/releases/tag/v20260504),
  which fixes a bug in the AvaFrame-entrainment model (entrainment energy now correctly read from file).

- **com1DFA fixes and features:** A long-standing memory corruption bug affecting com5SnowSlide is fixed — arrays
  returned by `updateFieldsC` are now properly owned copies. Particle property saving is now selective: you can
  configure which properties to save, reducing output file sizes. Time-dependent release handling now supports
  multiple files for parallel simulations and more release features.

- **com4FlowPy output improvements:** Computes `startCellID` per cell and generates output polygons for each process
  path.

- **com6RockAvalanche fixes:** `scarp.py` no longer produces negative values in raster output. The config file
  (`com6RockAvalancheCfg.ini`) now exposes all adjustable parameters.

- **in2Trans raster-to-NetCDF:** New `rasterUtils` functions to convert rasters to NetCDF files.

- **Documentation updates:** Time-stepping configuration in com1DFA is now clearer (fixes
  [#1285](https://github.com/avaframe/AvaFrame/issues/1285)). An AI/LLM usage section has been added to the developer
  guide.



Felix
