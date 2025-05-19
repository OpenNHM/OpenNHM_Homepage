---
title: "Release Version 1.3"
date: 2022-10-12T00:00:00+01:00
draft: false
slug: "version1_3"
---

**Today we released [Version 1.3](https://github.com/avaframe/AvaFrame/releases/tag/1.3)** 

The main change is the change of logic for secondary release areas. This was done to be able
to expose these functions in the AvaFrameConnecter. So it is now possible to include secondary 
release areas in dense flow simulations done via QGis.
Please also make sure you read the new [installation instructions](https://docs.avaframe.org/en/latest/installation.html).

ENHANCEMENTS

- Change logic for secondary release areas:
  - Check for release and secondary release shapefiles
  - If only release available -> just run release
  - If both release and secondary release are available -> run with secondary release 
    UNLESS secRelArea = False 
  - ALL scenarios in release get the secondary release areas!
- Add  rotational energy line test: helps to check eg. for numerical grid independence
- Update ini file procedure for the energy line test and the rotation test
- Additional statistical plots
- New three-panel plot of tt-diagram (plus animation)
- Add variation option for thickness settings and probrun based on normal distribution derived from ci and mean
- Add filtering option to aimec
- Add scenario name to configuration to be used for plotting example #757 
- Add surface parallel coordinate computation to Aimec
- Improve operational installation instructions
- Add a german version of the operational installation

FIX
- Contour legend bug with matplotlib 3.5.2
- Update installation instructions; fixes #764
- Bugs in deriving variation
- Remeshing issue that lead to standard test differences (originated in commit 419c11f)
- No calls to matplotlib for plotting purposes in com1DFA
- Removes multiple printouts of config during run in, e.g. com1DFA
- CompareConfig always honours the toPrint flag

Contributors:

Code: core team 

Felix
