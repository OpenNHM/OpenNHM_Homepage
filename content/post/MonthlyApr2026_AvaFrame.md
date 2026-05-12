---
title: "This month in AvaFrame and DebrisFrame- April 2026 edition"
date: 2026-05-01T00:00:00+01:00
draft: false
tags:
  - avaframe
  - debrisframe
  - monthly

Description: "AvaFrame 2.0 preview, hillshade contrast, snow slide detrainment, remeshing NaN fix, and more."

---

Welcome to the April 2026 update for AvaFrame and DebrisFrame:

Prepare for version **AvaFrame 2.0** in May. This will be a major milestone bringing breaking
changes and new capabilities. Key changes include simulation names now including
the module name, an expert configuration setup with override files in
`Inputs/CFGs/`, the new OpenNHM QGIS Connector replacing the previous
AvaFrame-only version, compressed TIF output by default, and many API cleanups.

This month we closed **6 PRs**: a configurable hillshade contrast enhancement,
a fix for edge NaNs during raster remeshing, documentation standardization of pixi 
commands and equation references, and updated test data for scarp analysis.

For DebrisFrame, we did not close and merge any pull requests. We prepared for the 
EGU conference, where we will present a poster about DebrisFrame (see
the abstract here: https://meetingorganizer.copernicus.org/EGU26/EGU26-12647.html). Additionally, we prepare for the
project meeting during this EGU - week.

## Enhancements

**Hillshade Contrast** - **PR #1262**
([link](https://github.com/OpenNHM/AvaFrame/pull/1262)) added an option for
increased contrast in hillshade plots, controlled by a new config parameter.
The default setting preserves the existing appearance.

**Snow Slide Module** - **PR #1259**
([link](https://github.com/OpenNHM/AvaFrame/pull/1259)) set detrainment to
`False` in com5, aligning the default behavior with expected usage.

## Bug Fixes

**Remeshing Edge NaNs** - **PR #1266**
([link](https://github.com/OpenNHM/AvaFrame/pull/1266)) fixed a bug where
bilinear interpolation during raster remeshing left NaNs at grid borders,
triggering validation errors in `deriveParameterSet`. The fix adds a
nearest-neighbor fallback for edge pixels and enforces stricter NaN validation
on non-DEM input rasters.

**Run Script Guards** - **PR #1258**
([link](https://github.com/OpenNHM/AvaFrame/pull/1258)) wrapped top-level
execution code in `runStandardTestsCom1DFA.py` and
`runUpdateBenchmarkTestsCom1DFA.py` in `if __name__ == "__main__"` guards.
This prevents unintended execution during imports (e.g. test collection or
parallel processing forks), fixing issue #1247.

## Documentation

**Pixi Command Standardization** - **PR #1264**
([link](https://github.com/OpenNHM/AvaFrame/pull/1264)) updated all
documentation to consistently use `pixi run python ...` instead of bare
`python ...` commands, and replaced manual Cython build instructions with
`pixi run build`.

**Equation Reference Fix** - **PR #1260**
([link](https://github.com/OpenNHM/AvaFrame/pull/1260)) corrected incorrect
equation references (31 and 32) in the Rheological Models section of
`docs/theoryCom1DFA.rst`.

## Testing Infrastructure

**Scarp Test Data** - **PR #1265**
([link](https://github.com/OpenNHM/AvaFrame/pull/1265)) updated scarpExample
test inputs with new point and polygon shapefiles for the EllipsoidMethod and
PlaneMethod tests, replacing the old generic coordinate files.

In other news we had a successfull AvaFrame Steering Meeting, and we are currently starting
 a new master thesis about entrainment, more info to come. 

See you next month!

Felix
