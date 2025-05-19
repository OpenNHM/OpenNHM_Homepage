---
title: "This month in AvaFrame - March 2021 edition"
date: 2021-04-04T19:08:58+01:00
draft: false
---

Welcome to the March 2021 edition of our monthly update. 

+ One big focus this months was a refactor of our AIMEC routines. We realised
  that our functions were still too complex, so we decided to
 
  * split it into more atomic function to make it easier to access only certain
    parts of the AIMEC functionalities. 
  * make sure no special folder structure is needed anymore.
  * add an option to compare results from two different com modules.
  * improve and develop the AIMEC plots some more.
  * showcase how to use it by including it in the standard tests.
  
  All this is especially important in light of our submission to the vEGU 2021.
  See [here](https://meetingorganizer.copernicus.org/EGU21/EGU21-6560.html) for more information.

+ Our Windows side is progressing: the windows executable for the com1DFA module
  has landed. If you want to try it, you can follow our
  [installation](https://docs.avaframe.org/en/latest/installation.html) and
  adapt it for windows paths. The documentation will be updated as soon as a
  simpler installation method is available. This will (hopefully) be possible
  via *pypi*, first tests look promising, but some kinks need to be ironed out
  first. 

+ We started an in depth comparison between com1DFA and the python version
  com1DFAPy. Since the python version is getting closer to reproduce the com1DFA
  results we want to make sure we are covering all the bases. To finally being
  able to switch over to the python version, we are now working on adding
  entrainment and resistance areas.
  
+ And as always plenty of smaller issues and tasks were tackled:

  * writing theory and numerics documentation.
  * update idealised topos and naming.
  * add description dict/json file for the tests, with an option to filter them using tags.
  * update benchmark tests (ini files, particles, benchmark results also regarding com1DFAPy, damBreak).
  * add option to change entrainment thickness for com1DFA
  * update quickplot with histogram plot insert and 0 values not shown anymore

Since the beginning of the month our team got a bit bigger: we welcome Marie and
Michael, 2 master thesis students, on board. We are looking forward to AvaFrame being
put to the test!

Hope to see you at the EGU21, 

Felix
