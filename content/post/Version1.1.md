---
title: "Release Version 1.1"
date: 2022-05-19T00:00:00+01:00
draft: false
slug: "version1_1"
---

**Today we released [Version 1.1](https://github.com/avaframe/AvaFrame/releases/tag/1.1)** 

The benchmark and thickness release. There are two main changes:

- The benchmarks (i.e. reference results) are updated and originate from com1DFA now. 
  Previously these were produced by com1DFAOrig.  
- All references to *depth* are now switched to *thickness*. This is done to be more consistent
  and precise. It also means result types switch from *pfd / fd* (peak flow depth / flow depth) to 
  *pft / ft* (peak flow thickness / flow thickness). Note that this is purely a *naming* change; nothing 
  changed regarding the computation!

ENHANCEMENTS

- benchmarks originate from com1DFA
- change all depth variables to thickness
- change the order of simHash within the result names; fixes Move simHash in filename #690
- path finding added; see issue #610. This will be fully introduced in version 1.2, including
  automatic split point generation
    - refactor path computation functions
    - allow computing path from particles or fields (if *from fields*: needs the FM=FlowMass)
    - runscript to compute a path from com1DFA results (requires that one saves some time steps)
- automate the benchmark updating process
- improve energy line plot
- set deleteOutput to False in runOperational; addresses User Feedback (CT) #715. This means
  it is possible to reuse the same directory in the QGis Connector, adding results to existing 
  ones
- add real area to aimec analysis #695
- update hybrid and energy test
- add com3Hybrid documentation #618

FIX

- hybrid model #611
- refactor com2AB for clarity and readability #446
- address savefigFormat TODO in outAB #560
- only one makeDomainTransfo #700

Felix
