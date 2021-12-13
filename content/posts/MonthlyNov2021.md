---
title: "This month in AvaFrame - November 2021 edition"
date: 2021-12-03T00:00:00+01:00
draft: false
---

Welcome to our monthly update for November. 

There are some changes especially for those wanting to try and test AvaFrame:

- the AvaFrame QGis Connector is now out of the experimental state, so it is easily installable via the QGis plugins
manager. No more need to enable experimental plugins. See 
[QGis plugin directory](https://plugins.qgis.org/plugins/avaframeConnector/). 

- We had our first webinar with about 15 test users. This group is testing AvaFrame from an operational point of view.
The first feedback is already rolling in, and we already discovered some more snags. However, so far nothing too serious.
Some, as yet to be solved, problems concern file access rights on windows machines. If you hit a similar problem, we'd
be happy to hear from you! (e.g. via a github bug report...) 

- For those working on MacOS: there are successful installations on current MacOS versions. The safest way seems to be
to install QGis via conda (anaconda; conda-forge). 

- We are investing more effort into the improvement of our testing. Both unit testing and model testing are tackled.
  This is applied right away for current developments like the ongoing investigation into initial particle distribution
  methods. 

- Work is also being done on the  similarity solution test, comparing DFA results to an analytic solution.

- As mentioned last month, a, what we call *hybrid model* is being developed.  This includes automatic path finding 
  from a combination of  DFA simulations (com1DFA) and alpha beta results (com2AB). Expect the full module hitting our
  code base soon. 

- The documentation now includes information about an extended method to split and/or merge particles during computation
of the com1DFA module. See [here](https://docs.avaframe.org/en/latest/DFAnumerics.html?highlight=merge#particle-splitting-and-merging) 
for more information. 

We plan on offering a  **public webinar** for everyone interested. It is currently set for the beginning of February, 
watch this space for an announcement soon!

That's it for this month, happy skiing, snowboarding or whatever satisfies your winter-y needs!

Felix

