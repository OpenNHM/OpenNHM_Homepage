---
title: "This month in AvaFrame - December 2020 edition"
date: 2020-12-29T20:19:18+01:00
draft: false
slug: "monthlydec2020" 
---

Welcome to this years last monthly update. 

+ This month we concentrated on getting more tests into our repository. We now
  have included all 6 realistic topographies with release areas and benchmark
  results in our test scripts. We also expanded our routine testing with pytest
  to more functions/modules. And those testing DEM's, as well as the release
  areas,  are freely available in the repository, see the *data* directory. 
  
+ The availability of these test cases lead to the release of **version 0.2**.
  Read our last [post](https://avaframe.org/posts/version0_2/) to get to know
  more about it. 

+ We started including tools and functions regarding the generation of probability
  maps. These range from basic functions for sample generation with different
  distribution all the way to kernel distribution plots. 
  
+ Fixing a few niggles, like consistent ASCII writing, updating of docstrings
  for the documentation and other documentation improvements (i.e. *how to add
  test cases*).
  
+ One big thing to be filled in future: we started a glossary where we define
  commonly used terms. We want to use these terms consistently throughout all
  modules. And yes: we are aware this will lead to tons of discussions :-) .

+ For our python version of the dense flow kernel, we looked into particle
  distribution, mesh generation and the (potential) application of SPH on a 3d
  surface. 

We wish you all a happy new year 2021! On to an exciting next year!
 
Felix
