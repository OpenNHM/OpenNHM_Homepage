---
title: "This month in AvaFrame - August 2020 edition"
date: 2020-08-21T12:28:05+02:00
draft: false
slug: "monthlyaug2020" 
---

Welcome to this months monthly update (try to say this really fast :-) ) :

+ The computational module for AlphaBeta is coming along nicely. We cleaned
  quite a lot of code and are starting the testing / comparing to reference results
  (Matthias is working on this).
  
+ Creation of idealised (test) topographies hit our public code base 
  (see [github](https://github.com/avaframe/AvaFrame)). With these functions the
  creation of various types of topographies is a breeze (thanks Anna). Matching release areas
  can also be automatically created for some topographies. Additionally we started
  putting these topographies and matching release / entrainment areas into the
  data folder (in case you don't want to run the code yourself).

+ The comparison tools/routines for AIMEC are on github now. This is the first
  transfer of existing code, so Matthias is heavily working on this one. Expect a lot
  of changes to happen here. 

+ The first functions for the computational module com1DFA (main dense flow
  module) are public now. As of now the necessary executable is not yet
  available, but expect it to hit the repository sometime around end of September. 

+ Various helper routines are included now:
    + Configuration file reading and handling
    + Log file creation and handling
    + Project initialiser 
    + Input data transfer scripts
    + ...
    
+ Documentation ([docs.avaframe.org](https://docs.avaframe.org)) is constantly 
  being updated, current new additions / updates are
  the AlphaBeta module, AIMEC module and generateTopo module. 
  
Thanks for following our project, 
signing off for summer :-) 

Felix

If you have any questions and/or want to contact us, visit our matrix
 room at:
[#public:matrix.avaframe.org](https://matrix.to/#/!qmUrKSNurDoVuKAtRU:matrix.avaframe.org?via=matrix.avaframe.org)
