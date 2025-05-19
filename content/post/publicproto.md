---
title: "Public prototype and monthly update"
date: 2021-07-14T07:08:58+01:00
draft: false
---

In case you wondered where your beloved monthly update is, it was delayed due to
us working on a big announcement:

We released [version 0.5](https://github.com/avaframe/AvaFrame/releases/tag/v0.5), 
our so called **public prototype**. 

So now why is this big? (Apart from being a project milestone, which you couldn't
care less about I guess) 

**This is the first release that is being tested for
application in operational hazard mapping.**

To achieve this, quite a few things changed:

- Version 0.4 saw us switching to our own code for the dense flow module
com1DFA. The original module is still available, but our development efforts
will now focus on the new one. 

- With version 0.5 we completely overhauled and updated the documentation to include things
  like:
  - updated descriptions of the modules
  - installation instructions for Windows
  - new DFA algorithm [description page](https://docs.avaframe.org/en/latest/com1DFAAlgorithm.html)
  - and many more changes...

- We created a [new repository](https://github.com/avaframe/QGisAF) for the
  connection between QGis and AvaFrame. This means you can run our operational
  workflow from inside QGis. It is a setup for running com1DFA (dense flow) and
  com2AB (alpha beta), in which you can change
  release thicknesses and run multiple scenarios, but the rest of the setup is
  according to our current default setup. 
  
- and many more functional changes under the hood, see the main ones in our 
 [release notes](https://docs.avaframe.org/en/latest/releaseNotes.html).

- Together with C. Tollinger (Fachzentrum f. Geologie und Lawinen, WLV) we
 developed a visualisation of the main peak variables based on colormaps that
 works better for people with vision deficiencies (e.g. red/green blindness).
 These plots now work for normal vision, red/green deficiency and in grayscale.
 See examples for the test case ALR at the end of this post. 

We invite you to give this version a try, but expect some rough edges. 
But whatever you do, enjoy your summer (or your winter for the southern
hemisphere people out there)! 

Signing out for summer, 

Felix
 
 
 Peak flow depth
![Peak flow depth](/img/FZGL_PFD.jpg)

 Peak flow pressure
![Peak pressure](/img/FZGL_PPR.jpg)

 Peak flow velocity
![Peak flow velocity](/img/FZGL_PFV.jpg)

