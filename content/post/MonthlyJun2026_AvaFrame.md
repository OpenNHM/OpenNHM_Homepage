---
title: "This month in AvaFrame - June 2026 edition"
date: 2026-07-01T00:00:00+01:00
draft: false
author: "Felix"
tags:
  - avaframe
  - monthly

Description: "Dense flow module improvements, com9 integrated compilation, parallel simulation
runs with time-dependent release, analysis tool extensions, and Voellmy friction rasters."
---

Welcome to the June 2026 edition of the AvaFrame monthly update:

This month brought improvements across the dense flow module, a new compilation
approach for com9, and several documentation updates. An external contribution
from @NUForever extended the DFA path generation in the analysis tools, allowing
runout analysis all the way to the deposit front. The com9 module now compiles
automatically as part of the build process, removing the need for a separately
maintained executable. A new shapefile-to-raster function enables spatially
variable Voellmy friction configurations for com6. The developer guide received
a section on LLM/AI usage to help contributors to apply these tools responsibly
in relation to our codebase.

## Features

**Dense Flow Module (com1DFA)**

- **PR #1300** ([link](https://github.com/OpenNHM/AvaFrame/pull/1300))
  consolidated TIF validity checks into a reusable function.
- **PR #1290** ([link](https://github.com/OpenNHM/AvaFrame/pull/1290))
  added a saving option for resistance fields.

**Analysis Tools**

- **PR #1296** ([link](https://github.com/OpenNHM/AvaFrame/pull/1296))
  added `extBottomOption` to ana5, extending DFA path generation to the
  deposit front for more complete runout analysis.
- **PR #1299** ([link](https://github.com/OpenNHM/AvaFrame/pull/1299))
  introduced collection and summary of comparison warnings in the
  logging module, making it easier to spot discrepancies across
  simulation runs.

**com9 Compilation**

- **PR #1281** ([link](https://github.com/OpenNHM/AvaFrame/pull/1281))
  replaced the previously hardcoded com9 executable with an integrated
  compilation step, bringing it in line with how other computational
  modules are built.

**Spatial Friction (com6)**

- **PR #1074** ([link](https://github.com/OpenNHM/AvaFrame/pull/1074))
  added `VariableVoellmyShapeToRaster` to generate Voellmy friction
  rasters from shapefile features, enabling spatially variable friction
  configurations.

**Other Enhancements**

- **PR #1297** ([link](https://github.com/OpenNHM/AvaFrame/pull/1297))
  added a new configuration parameter shared between com1 and com8.
- **PR #1280** ([link](https://github.com/OpenNHM/AvaFrame/pull/1280))
  added a raster-to-NetCDF conversion function in in2Trans.
- **PR #1213** ([link](https://github.com/OpenNHM/AvaFrame/pull/1213))
  added release area information output to com4FlowPy.

## Bug Fixes

**Particle Analysis**

- **PR #1302** ([link](https://github.com/OpenNHM/AvaFrame/pull/1302))
  fixed a problem with the runscript for particle analysis in out3Plot.

**Testing and CI**

- **PR #1288** ([link](https://github.com/OpenNHM/AvaFrame/pull/1288))
  fixed a path bug in the com4 tests.
- **PR #1289** ([link](https://github.com/OpenNHM/AvaFrame/pull/1289))
  updated the Pixi setup GitHub Action to v0.9.6.

**Documentation Fix**

- **PR #1286** ([link](https://github.com/OpenNHM/AvaFrame/pull/1286))
  clarified the time-stepping configuration in both the com1DFA
  documentation and the config file, resolving a common point of
  confusion.

## Documentation

**Developer Guide**

- **PR #1284** ([link](https://github.com/OpenNHM/AvaFrame/pull/1284))
  added a section on LLM/AI usage to the developer guide.

**Config Descriptions**

- **PR #1283** ([link](https://github.com/OpenNHM/AvaFrame/pull/1283))
  improved the entrainment description in the com1DFA config file to
  explicitly mention frontal entrainment.

See you next month!

Felix
