---
title: "This month in AvaFrame - January 2022 edition"
date: 2022-02-05T00:00:00+01:00
draft: false
---

Welcome to the January 2022 update.

Our focus this month was the preparation for our upcoming version 1.0 release. We finished the month by publishing 
the first release candidate. See [github releases](https://github.com/avaframe/AvaFrame/releases) for a full changelog. 

- For the final release of version 1.0 we worked on a difference report, investigating our numerics and comparing it
to com1DFAOrig.

- We streamlined and improved the way release thickness is being set in the DFA module *com1DFA* 
  - it is possible now to add variations if release thickness is read from shapefile.
  - add percent and range variation options.

- A new probability runscript is now in its final development stages.

- On the numerics side *convergence* of com1DFA for the similarity solution test case was the topic of the month. 
  - The aim is to extract a criterion between the time and space discretization parameters that leads to convergence 
  of the numerical method towards the solution of the depth integrated equations.
  - We are now trying to do the same analysis on more test cases. Starting with idealized topographies and coulomb friction, 
  but also real topographies.

- Further minor improvements here and there, including:
  - cleaning up runscripts.
  - cleaning benchmarks.
  - explore plotting options for uncertainty visualisation.

That's it for this month, have a good start into this year!

Felix

