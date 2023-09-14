---
title: "Release Version 1.5"
date: 2023-02-28T00:00:00+01:00
draft: false
slug: "version1_5"
---

**Today we released [Version 1.5](https://github.com/avaframe/AvaFrame/releases/tag/1.5)** 

The parallel release.  This adds parallel computation for com1DFA, meaning
multiple simulations are run in parallel. For more information see [our
documentation](https://docs.avaframe.org/en/latest/moduleCom1DFA.html?highlight=parallel#parallel-computation).
**Be aware, there is a breaking change** in case you call com1DFA functions
directly: the calls to com1DFAMain changed; there is one less argument to give.

- Add info about parallel computation in doc [com1DFA]
- rename s to travelLengthXY [ana4AIMEC] 
- particle properties renaming:
   - s -> travelLengthXY
   -  l -> travelLengthXYZ
- set kernelradius to cellsize for default settings [com1DFA]
- Add parallel computation of com1DFACore [com1DFA]
- Remove redundant argument from com1DFA functions [com1DFA] !Breaking change!!
- Drop log to debug in pyx files; problem with QGIS!
-  Add run from multiple cfg
- Turned off writing of damfootline since it is not threadsafe
- update probrun with drawing from full sample
- Fix mac parallel; fixes https://github.com/avaframe/AvaFrame/issues/819
- Change the main of runOperational and runcom5glide snow in preparation for next connector release
- Add a latestSims.csv to com1DFA configuration output; needed for the qgis connector

Felix
