---
title: "This month in AvaFrame - September 2020 edition"
date: 2020-09-30T12:28:05+02:00
draft: false
slug: "monthlysep2020" 
---

Winter is slowly creeping up on us, so here is the next AvaFrame update:


+ We heavily worked on the dense flow avalanche module com1DFA, bringing
functionality from its native code over to python functions. Now there is 
the option to do parameter variations on friction parameters and release thickness automatically.
Besides this new option, more and more simulation parameters can now be set in python.

+ Regarding the necessary executable for the com1DFA (dense flow) module: we
  discovered some discrepancy which we currently work on to resolve. The
  differences to our reference results are minuscule, but we would like to
  understand the source of it. Once this is resolved, we will release the
  executable as a first step to bringing it fully open source. 

+ We created a new results folder structure for com1DFA, now simulation files
  can be addressed according to their name and characteristics such as
  simulation type, name of release area and many more via a dictionary.

+ The full documentation for com1DFA (dense flow) took a big step forward, you
  can see it here
  [docs.avaframe.org](https://docs.avaframe.org/en/latest/appendixCom1DFA.html).
  Please be aware, this is currently not reviewed yet and still heavily being
  worked on. 

+ The AlphaBeta and AIMEC modules also received improved documentation, but
  again, not completely done yet. 
  
+ The AIMEC computation and plotting routines are now a lot cleaner and easier
  to read.

+ The plotting routines are developed/improved with styling of the plots and
new colormaps. To use a modern visualisation, we are working in the HCL color
space wherever possible. For more information about this see [hclwizard](http://hclwizard.org).

**Quarterly Outlook** 

We are currently working towards version 0.1, a bare bones first version
including the main modules com1DFA, com2AB (AlphaBeta) and the necessary support
modules, like logging, input/output and report generation. With this experienced
users will be able to run avalanche simulations. This will also include
our dense flow executable mentioned above. Towards the end of the year
we will concentrate on testing, improving our code-coverage and documentation.
The development of the interface to QGis, i.e. triggering simulations right out
of QGis, will also start around this time.

Excited to see the first simulation results, 

Felix

