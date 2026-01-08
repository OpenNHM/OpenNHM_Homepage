---
Title: "This month in AvaFrame - December 2025 edition"

Date: 2026-01-01T00:00:00+01:00
author: "Felix"
Draft: false

Tags:
- avaframe
- monthly

Description: "Timestep export control and time information tracking in com1DFA. GitHub repository migration to OpenNHM
organization. Documentation corrections and raster input improvements. Read more..."

---

Welcome to the December 2025 update:

December brought important changes to simulation output control and time tracking, along with the official migration of
AvaFrame to the OpenNHM organization. We also improved documentation and refined raster input handling.

**Timestep Export Control**

PR #1219 (https://github.com/OpenNHM/AvaFrame/pull/1219) introduced a breaking change to how timestep exports work in
com1DFA. By default, t=0 is no longer exported - only the final timestep is exported when `tSteps` is empty. To export
the initial timestep, you must now explicitly specify it in the `tSteps` parameter. The default configuration changed
from `tSteps = 1` to an empty value, making the export behavior more intentional and reducing unnecessary output.

**Time Information Tracking**

PR #1217 (https://github.com/OpenNHM/AvaFrame/pull/1217) added `timeInfo` as a new result type in com1DFA and out1Peak.
This enhancement provides better tracking of temporal simulation data and adds units to `outPlotAllPeak` plots used in
com1DFA reports, improving result interpretation.

**AIMEC Analysis Enhancement**

PR #1224 (https://github.com/OpenNHM/AvaFrame/pull/1224) added writing of reference DataFrame in ana3AIMEC, improving
the analysis module's ability to track and compare reference simulation data.

**GitHub Repository Migration**

PR #1223 (https://github.com/OpenNHM/AvaFrame/pull/1223) updated all repository references following AvaFrame's
migration to the OpenNHM organization. The repository path changed from `https://github.com/avaframe/AvaFrame.git` to
`https://github.com/OpenNHM/AvaFrame.git`. If you have local clones, you'll need to update your remote URLs.

**Documentation Improvements**

Two documentation-focused PRs improved accuracy and clarity:

PR #1218 (https://github.com/OpenNHM/AvaFrame/pull/1218) fixed the thalweg computation equation in the documentation,
correcting a display error in the mathematical formula.

PR #1214 (https://github.com/OpenNHM/AvaFrame/pull/1214) corrected the documentation for raster inputs in com1DFA. The
update removes references to the deprecated `thicknessFromShp` flag and clarifies the process for using release
thickness files. The code changes also improved handling of no-data values in raster input files, allowing them when
matching no-data locations in the DEM, and properly ignoring NaN values that result from remeshing to match DEM cell
size.

**Configuration Cleanup**

PR #1220 (https://github.com/OpenNHM/AvaFrame/pull/1220) corrected a comment in the com4FlowPy configuration file for
the forestFrictionLayer module, improving configuration clarity.

As we close out 2025, we're excited about the progress on DebrisFrame and the migration to OpenNHM marks an important 
step in organizing natural hazard modeling tools under a unified organization.

See you in January!

Felix

---

Summary of PRs merged in December 2025:

1. PR #1218 - Fix thalweg computation equation in documentation (merged Dec 9)
2. PR #1214 - Correct documentation for raster inputs and improve no-data handling (merged Dec 9)
3. PR #1220 - Correct comment in com4FlowPy configuration file (merged Dec 12)
4. PR #1217 - Add timeInfo result type and units to peak plots (merged Dec 15)
5. PR #1219 - Change default timestep export behavior [breaking change] (merged Dec 16)
6. PR #1223 - Update repository path to OpenNHM organization (merged Dec 17)
7. PR #1224 - Add reference DataFrame writing in AIMEC analysis (merged Dec 22)

Total: 7 pull requests merged