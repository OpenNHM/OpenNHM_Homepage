---
title: "This month in AvaFrame - September 2026 edition"
date: 2026-10-01T00:00:00+01:00
draft: false
author: "Felix"
tags:
  - avaframe
  - monthly

Description: "General thalweg preparation, FlowPy input validation,
and fixes for polygon rasterisation and optimisation."
---

Welcome to the September 2026 edition of the AvaFrame monthly update:

This month brought tools for preparing thalweg profiles from coordinate
data and additional input checks for FlowPy. We also corrected polygon
winding detection, which could cause rasterised areas to shrink
incorrectly, and fixed simulation-name handling in the optimisation module.

## Features

**Thalweg Preparation**

- **PR #1323** ([link](https://github.com/OpenNHM/AvaFrame/pull/1323))
  added tools to prepare thalweg profiles from x and y coordinates.
  Paths can be extended at both ends, resampled with a configurable
  spline degree, and with elevations from a DEM and distances
  along the path.

**FlowPy Input Validation**

- **PR #1328** ([link](https://github.com/OpenNHM/AvaFrame/pull/1328))
  added checks for variable alpha and maximum-velocity input rasters
  before running a FlowPy simulation, helping identify invalid
  parameter values earlier.

## Bug Fixes

**Polygon Rasterisation**

- **PR #1338** ([link](https://github.com/OpenNHM/AvaFrame/pull/1338))
  replaced the polygon winding heuristic with a signed-area calculation.
  Winding detection no longer depends on the starting vertex or the
  polygon's orientation. The previous method could incorrectly shrink
  release, entrainment, or resistance areas during rasterisation,
  excluding cells that should have been included.

**Optimisation**

- **PR #1336** ([link](https://github.com/OpenNHM/AvaFrame/pull/1336))
  corrected simulation-name retrieval in ana6Optimisation by removing
  an incorrect indexing operation.

Thanks to first-time contributor **@bskerlak** for the polygon winding
fix (PR #1338).

In other news: a smaller side project related to snow slides (SRPrax) came 
to a close this month, expect the report on zenodo and on this homepage soon.  


See you in October!

Felix
