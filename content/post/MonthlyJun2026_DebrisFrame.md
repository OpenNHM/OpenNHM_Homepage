---
Title: "This month in DebrisFrame - May and June 2026 edition"

Date: 2026-07-02T00:00:00+01:00
author: "Paula, Julian"
Draft: false

Tags:
- debrisframe
- monthly

Description: "DebrisFrame monthly update for May and June 2026: EGU poster, project meeting, c1TIF renaming, time
dependent release improvements, and adaptive topography."

---

# Monthly Summary: DebrisFrame
--------------

## June 2026

**EGU General Assembly 2026**

We presented a poster about the DebrisFrame concept at the EGU General Assembly in Vienna
(https://meetingorganizer.copernicus.org/EGU26/EGU26-12647.html).

**Project meeting**

In a project meeting between BOKU, BFW and WLV we discussed our previous work and the next steps, from input
hydrographs to adaptive topography.

**Time dependent release**

PR #1267 (https://github.com/OpenNHM/AvaFrame/pull/1267) allows multiple features within one time dependent
release scenario.

PR #1278 (https://github.com/OpenNHM/AvaFrame/pull/1278) enables a parallel run with multiple time dependent
release scenarios (multiple csv files).

**Adaptive topography**

PR #1292 (https://github.com/OpenNHM/AvaFrame/pull/1292) enables deposition (mass that has velocity = 0 m/s) to
be eroded. In this initial version, we assume that parts of the topography (DEM) are eroded. There are still open
issues.

**Ongoing work**

- We are still working on solutions for using a hydrograph as a starting condition
- Addressing open issues with the adaptive topography implementation

----

## May 2026

**c1TIF renaming**

PR #78 (https://github.com/OpenNHM/DebrisFrame/pull/78) renamed the computational module c1Tif into c1TIF
(thickness integrated flow) and added a short documentation for this module.

Paula, Julian
