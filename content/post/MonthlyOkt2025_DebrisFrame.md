---
Title: "This month in DebrisFrame - October (and before) 2025 edition"

Date: 2025-11-02T00:00:00+01:00

Draft: false
author: "Paula,Julian"
Tags:
- debrisframe
- monthly

Description: "The first monthly update of DebrisFrame. Stuff that happened this year already..."

---

Welcome to the October 2025 (and before) update:

This is the first installment of the monthly update of DebrisFrame. Some things where already mentioned in the monthly 
Avaframe updates. Here we will focus on the DebrisFrame specific stuff. So lets get started!

First functions relevant for simulating debris flows have been implemented in AvaFrame.

The DebrisFrame repository now contains a c1Ti module that executes AvaFrame's com1DFA with overwritten
parameters (https://github.com/OpenNHM/DebrisFrame/tree/master/debrisframe).
Until now DebrisFrame's c1Ti module is only excecutable from a
terminal (https://docs.debrisframe.org/en/latest/installation.html).

**Adaptive Topography** 

PR #1112 (https://github.com/avaframe/AvaFrame/pull/1112) provides the opportunity to adapt the surface when
entrainment, detrainment or stopping takes place. The documentation can be found
here: https://docs.avaframe.org/en/latest/theoryCom1DFA.html#adaptive-surface

**New Rheological Models**

PR #1169 (https://github.com/avaframe/AvaFrame/pull/1169 ) added rheological models for debris-flow simulations to
com1DFA. This extends AvaFrame’s capabilities from snow avalanches to debris flows. The implementation updates the
Cython force computation functions, adds new configuration parameters, and includes documentation
at https://docs.avaframe.org/en/rheologicalmodels/theoryCom1DFA.html#rheological-models .

**Data**
A repository was created (https://github.com/OpenNHM/DebrisFrameData) where you can find prepared reference scenarios
for debris-flow simulations.

We continue to work:
* on enabling hydrographs to be used as input,
* on implementing alternative formulations for material entrainment (erosion),
* model testing.

Paula, Julian



