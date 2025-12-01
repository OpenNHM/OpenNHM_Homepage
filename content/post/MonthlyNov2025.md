---
Title: "This month in AvaFrame - November 2025 edition"

Date: 2025-12-01T00:00:00+01:00
author: "Felix"
Draft: false

Tags:
- avaframe
- monthly

Description: "Input handling improvements with raster file support. New hydrograph input functionality for DebrisFrame. Parallel test execution and output standardization. Read more..."

---

Welcome to the November 2025 update:

November brought important improvements to AvaFrame's input handling, with raster files now supported across multiple
modules. We also added initial hydrograph input functionality for debris flow simulations and improved testing
infrastructure with parallel execution.

**Major Input Handling Enhancement**

PR #1193 (https://github.com/OpenNHM/AvaFrame/pull/1193) added the ability to read input data directly from raster files
without requiring shapefiles. This affects release areas, secondary release areas, entrainment zones, resistance areas,
and friction parameters across com1DFA, com8MoTPSA, com9MoTVoellmy, and the in1Data, in2Trans, and in3Utils modules. For
thickness files (release, secondary release, entrainment), values are taken directly from the raster where non-zero. For
resistance areas, non-zero values define resistance zones with parameters from the configuration file. 

**DebrisFrame Development**

PR #1167 (https://github.com/OpenNHM/AvaFrame/pull/1167) introduced initial hydrograph input functionality to com1DFA
for debris flow simulations. Users can now provide a polygon defining the input area and a CSV table with timesteps,
thickness values, and optional velocity values in the `Inputs/HYDR` directory. Particles are initialized at defined time
steps within the polygon location with the specified thickness and initial velocity. This is an initial implementation
with further improvements planned - see [DebrisFrame Issue #13](https://github.com/OpenNHM/DebrisFrame/issues/13) for
ongoing development. It is also possible that the process will be reworked...

**Testing Infrastructure**

PR #1211 (https://github.com/OpenNHM/AvaFrame/pull/1211) parallelized the test loop in runStandardTestsCom1DFA.py to
reduce wall-clock time for running standard tests. 

**Output Standardization and Compression**

PR #1164 (https://github.com/OpenNHM/AvaFrame/pull/1164) standardized output raster handling in com4FlowPy. A new
parameter `outputNoDataValue` (default: -9999) ensures all output rasters use the same value in cells not affected by
the process. All rasters saved as TIFF files are now LZW compressed by default, with an option to disable compression in
the configuration file.

PR #1173 (https://github.com/OpenNHM/AvaFrame/pull/1173) refined particle export logic in com1DFA and added TIFF
compression. Particles are now only exported if they are in the result type or if trackParticles is enabled. Each module
can implement a `useCompression` parameter in their configuration to control compression when using TIFF files, with
compression enabled by default.

PR #1216 (https://github.com/OpenNHM/AvaFrame/pull/1216) fixed a bug in com1DFA where remeshed files failed to write
correctly due to compression settings.

**Visualization Improvements**

PR #1210 (https://github.com/OpenNHM/AvaFrame/pull/1210) improved plot extent calculation in out3Plot. For fields that
can have negative values (like surface change), the plot extent now includes all non-zero values rather than just
positive values, since zero values represent cells not affected by the process.

**Module Enhancements**

PR #1209 (https://github.com/OpenNHM/AvaFrame/pull/1209) added command-line argument support to runCom6Scarp.py for
overriding the scarp analysis method. Users can now switch between plane and ellipsoid methods using `--method plane` or
`--method ellipsoid` without modifying configuration files. The default `--method ini` uses the configuration file
setting.

In other news, we are starting a small project related to developing snow slide guidelines in close cooperation between
the WLV and the BFW. Stay tuned for more details! Furthermore, the whole AvaFrame Team took part in the DebrisFrame
project kick-off in Vienna, you'll see more of that in the DebrisFrame monthly update. 

See you in December!

Felix

---

Summary of PRs merged in November 2025:

1. PR #1193 - Read input data from raster files (merged Nov 13)
2. PR #1209 - Add method override functionality for scarp analysis (merged Nov 18)
3. PR #1173 - Add TIFF compression and adjust particle export logic (merged Nov 18)
4. PR #1210 - Improve plot extent for fields with negative values (merged Nov 19)
5. PR #1211 - Enable parallel execution for standard tests (merged Nov 19)
6. PR #1167 - Add input hydrograph functionality for DebrisFrame (merged Nov 19)
7. PR #1164 - Standardize nodata values in com4FlowPy output rasters (merged Nov 19)
8. PR #1216 - Fix compression bug in remeshed file writing (merged Nov 25)

Total: 8 pull requests merged