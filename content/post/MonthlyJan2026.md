---
Title: "This month in AvaFrame - January 2026 edition"

Date: 2026-02-01T00:00:00+01:00
author: "Felix"
Draft: false

Tags:
- avaframe
- monthly

Description: "Module name added to simulation names for multi-module workflows. Time dependent release improvements for
DebrisFrame. AIMEC coordinate system validation and build system updates. Read more..."

---

Welcome to the January 2026 update:

January brought changes to simulation naming, improved time dependent release handling for debris flow simulations,
and added validation checks for AIMEC coordinate system transformations.

**Module Name in Simulation Names**

PR #1226 (https://github.com/OpenNHM/AvaFrame/pull/1226) added the computational module name as a component of the
simulation name. The format changed from `relNameSim_simHash_defID_frictIndi_simType_modelType` to
`relNameSim_simHash_modName_defID_frictIndi_simType_modelType`. For example, a simulation previously named
`release1_a1b2c3_C_S_ent_dfa` now becomes `release1_a1b2c3_com1DFA_C_S_ent_dfa`. This makes it easier to track and
distinguish simulations from different modules. A centralized parser handles both old and new formats for backward
compatibility.

**Time Dependent Release for Timestep 0**

PR #1215 (https://github.com/OpenNHM/AvaFrame/pull/1215) improved the time dependent release option (formerly called
"hydrograph") in com1DFA. The feature now works at timestep 0 and no longer requires a separate release area in the REL
folder. The terminology was renamed from "hydrograph" to "time dependent release" throughout the codebase. Input polygon
and CSV files are now located in the REL folder, and time dependent values are saved in the configurationFiles folder. A
new example data setup and standard test were added. This PR closes several DebrisFrame issues related to debris flow
input handling.

**AIMEC Coordinate System Validation**

PR #1225 (https://github.com/OpenNHM/AvaFrame/pull/1225) added validation checks for the AIMEC coordinate system
transformation in ana3AIMEC. When defining a new coordinate system along the thalweg, excessive curvature can cause
overlapping regions in the transformed coordinates. The new checks detect self-intersecting domain boundaries and
overlapping coordinate lines, issuing warnings when problems are found. Standard tests show no differences with this
change.

**Build System and Dependency Updates**

PR #1229 (https://github.com/OpenNHM/AvaFrame/pull/1229) updated version pinning in pyproject.toml. Cython was updated
to >=3.0.10 (needed for Python 3.12/3.13 support), pyshp was updated to >=3.0.3, and the salib version pin was removed.
The pixi clean task was rewritten to avoid platform-dependent shell commands, and the documentation was updated to
reflect that pixi handles the Python installation, so a separate Python install is no longer required.

**MacOS Multiprocessing Fix**

PR #1231 (https://github.com/OpenNHM/AvaFrame/pull/1231) removed the MacOS-specific workaround that forced ThreadPool
usage instead of the standard multiprocessing Pool. Both com1DFA and com4FlowPy now use the same multiprocessing
approach on MacOS as on Linux, based on feedback from MacOS users. The PR also includes minor code formatting changes in
com4FlowPy.

In other news we took part in the "BFW-Praxistag Innsbruck" with a "Marktstand" and our ISeeSnow Paper finally found an editor
and can be viewed here: https://egusphere.copernicus.org/preprints/2026/egusphere-2025-6053/

See you in February!

Felix

---

