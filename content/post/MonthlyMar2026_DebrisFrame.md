---
Title: "This month in DebrisFrame - March 2026 edition"

Date: 2026-04-02T00:00:00+01:00
author: "Paula, Julian"
Draft: false

Tags:
- debrisframe
- monthly

Description: "DebrisFrame monthly update for March 2026: module renaming, rheological model improvements, and default parameter sets."

---

# Monthly Summary: DebrisFrame
--------------

## March 2026

PR #60 (https://github.com/OpenNHM/DebrisFrame/pull/60) renames the computational module c1Ti into c1Tif that shortens
Thickness Integrated Flow.

**Rheological models**

PR #1252 (https://github.com/OpenNHM/AvaFrame/pull/1252)
replaces the bulk dynamic viscosity by the consistency factor K in the Herschel-Bulkley rheological model. The former
implementation of the Herschel-Bulkley rheological model assumed that the consistency factor K from the original
formulation is equal to the bulk dynamic viscosity. This was not true, so the bulk dynamic viscosity was replaced by
the consistency factor K.

PR #1254 (https://github.com/OpenNHM/AvaFrame/pull/1254) introduces an additional parameter input option for the
Bingham, Herschel-Bulkley and O'Brien and Julien rheological models, making it possible to define the yield shear stress
`tauy` and the dynamic viscosity `eta` directly in the configuration file. By default, ```tauy``` and ```eta``` are used
directly from the configuration file. If either of these two parameters is set to 0, the quantities are computed using
```alpha```, ```beta``` and ```cv```.

PR #62 (https://github.com/OpenNHM/DebrisFrame/pull/62) provides a default parameter set for the rheological models that
are based on literature research.

**Ongoing Work**
- The time dependent release and the different debris-flow friction models will be tested on the generic topography
- Sensitivity analysis of friction parameters
- Option to run Debrisframe simulation tools from QGIS
- Literature research and creating a database of friction parameters of back-calculated debris-flow events

Paula, Julian