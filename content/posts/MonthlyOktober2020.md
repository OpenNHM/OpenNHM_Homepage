---
title: "This month in AvaFrame - October 2020 edition"
date: 2020-10-29T20:19:18+01:00
draft: false
slug: "monthlyoct2020" 
---


Winter has arrived here, so this is basically the first winter update:

This month focused on getting our code base ready for the upcoming release of
version 0.1.

+ The documentation got a lot of attention with updates and improvements
  basically everywhere. Most notably we started to include installation and
  quick start sections for you to follow. 
  
+ Testing took a big step forward. We expanded out standard tests, generated more
  benchmarks and created scripts to run these tests on demand as well as within
  our continuous integration. 

+ Related to the testing as well as the operational script (see below), plotting
  routines got improved and report generation was heavily developed. This means the results
  and some crucial information of the execution are now presented in an easy
  readable manner. 

+ We started to include a *runOperational* script which will contain the core
  of AvaFrame and will be used to execute the most stable, well tested modules
  in operational settings (who would have guessed with this name...)

+ A minor bug in com2AB (Alpha Beta) was found and fixed. Furthermore we improved the quality
  of other parts of the code with added checks and more automatic tests with
  pytest. 

+ In the new [com1DFA_Exe repository](https://github.com/avaframe/com1DFA_Exe) a
  first (linux) executable for the com1DFA module (dense flow kernel) and necessary files can be found. 
  
**All this will lead to the release of version 0.1 within the next few days, so please
watch this space. Exciting times are ahead!**

