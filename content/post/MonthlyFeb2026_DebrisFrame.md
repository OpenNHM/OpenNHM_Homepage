---
Title: "This month in DebrisFrame - January and February 2026 edition"

Date: 2026-03-02T00:00:00+01:00
author: "Paula, Julian"
Draft: false

Tags:
- debrisframe
- monthly

Description: "DebrisFrame monthly update for January and February 2026: friction models, generic topography, time dependent release."

---

# February 2026

**Friction model**

PR #53 (https://github.com/OpenNHM/DebrisFrame/pull/53) allows choosing a friction model and modifying
respective parameters when executing c1Ti.

**Generic topography**

PR #54 (https://github.com/OpenNHM/DebrisFrame/pull/54) and PR #1241
(https://github.com/OpenNHM/AvaFrame/pull/1241) provide a generic topography for debris flows and its
generation script.
The generic topography is based on real longitudinal profiles from 19 different catchment areas in the
Pitztal and Paltental valleys (Austrian Alps, Kessler 2019). An average longitudinal profile was derived
from this natural data.
In the upper section, the topography begins with a semicircular channel with a radius of 20 m. At the
fan apex, the channel begins to widen and then runs out into the terrain. The transverse curvature of
the fan apex was not taken into account. In the last section, the topography is transformed into a flat
plane.
With the default parameter settings following morphometric features of the topography are achieved:
 horizontal length of the whole domain: 2000 m
 total fall height: 709 m
 horizontal length of channel (beginning channel - start widening): 703 m
 inclination channel: 34°
 horizontal length fan (start widening - end widening): 677 m
 inclination fan: 19°

*Reference: Kessler, M. (2019): "Morphometrische Untersuchung von Mur- und Schwemmkegeln in den
österreichischen Alpen unter Berücksichtigung des Prozessregimes", master thesis, BOKU University,
Vienna.*


**Time dependent release**

PR #1240 (https://github.com/OpenNHM/AvaFrame/pull/1240) writes time dependent release parameters to
the simulation output report, such as the model release volume at timestep 0 and summed over all release
timesteps.

PR #1239 (https://github.com/OpenNHM/AvaFrame/pull/1239) adds the time dependent release values
(timesteps and corresponding thickness and velocity) to the configuration, which is considered when
creating the simhash. This leads to a modified simulation-hash when the time dependent values within the
csv file are modified.

**Ongoing work**

* We are working on integrating the DebrisFrame simulation models into the OpenNHM-QGIS-Connector so
that they can be executed from QGIS. But be aware that they are still experimental!

* The time dependent release and the different debris-flow friction models will be tested on the generic
topography

----

# January 2026

**Time Dependent Release for Timestep 0**

PR #1215 (https://github.com/OpenNHM/AvaFrame/pull/1215) improved the time dependent release option
(formerly called "hydrograph") in com1DFA. The feature now works at timestep 0 and no longer requires a
separate folder for hydrograph options. The terminology was renamed from "hydrograph" to "time dependent
release" throughout the codebase. Input polygon and CSV files are now located in the REL folder, and time
dependent values are saved in the configurationFiles folder. A new example data setup and standard test
were added. This PR closes several DebrisFrame issues related to debris flow input handling, but there
are still some open issues on what we will work on in the next months.

**Ongoing work**

We are working on integrating existing simulation tools into DebrisFrame, for example pyTopRunDF
(https://github.com/schidli/pyTopRunDF).

Additionally, we will provide a generic topography that represents a typical debris flow topography soon.

Paula, Julian