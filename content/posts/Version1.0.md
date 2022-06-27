---
title: "Release Version 1.0"
date: 2022-05-06T00:00:00+01:00
draft: false
slug: "version1_0"
---

So this is a big one:

**On April 6. we released [Version 1.0](https://github.com/avaframe/AvaFrame/releases/tag/1.0)!** 

As you might guess, this is very exciting for us, but what does this mean?

- First of all, you can find all changes in our [documentation release notes](https://docs.avaframe.org/en/latest/releaseNotes.html#id1). 
  As one might expect with a first full release, the list is long! 

- Version 1.0 means we can partly fulfil a vital topic of our [mission](/about), namely the *replicating ...
  current simulation procedures...* part. The core computation module com1DFA for dense flow computations is in a state
  that allows it to be used in operational settings. In this regard, we published a report detailing differences between 
  the currently operationally used com1DFAOrig (i.e. SamosAT) results and our rewritten com1DFA results. See
  [reports](/reports) for a link to the report (or head over to 
  [the assets of the version 1.0 release on Github](https://github.com/avaframe/AvaFrame/releases/tag/1.0)). In this
  document, we detail the steps taken to ensure the similarity of the results, highlight the differences we found, the 
  investigations into numerical issues and our recommendations for operational application. 

- After testing this release by the WLV's operational team, AvaFrame is now included in the operational
  guidelines for avalanche simulations, see the 
  [Praxisleitfaden](https://info.bmlrt.gv.at/dam/jcr:edebd872-2a86-4edf-ac5e-635ef11e35fe/Praxisleitfaden%20LawSim%20WLV%202022%20Gr%C3%BCn.pdf)
  (unfortunately only available in German). Integrating AvaFrame into current procedures is recommended, but running
  current models in parallel to catch any possible issues not yet discovered. 

Of course, many features and modules are still missing since we are only halfway through the first project
phase. But we are confident Version 1.0 already provides a benefit for avalanche simulations! And we are working on 
quite a few interesting new features, so watch out for the next releases. 

Felix
