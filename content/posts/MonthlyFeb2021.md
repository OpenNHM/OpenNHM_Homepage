---
title: "This month in AvaFrame - February 2021 edition"
date: 2021-03-05T19:08:58+01:00
draft: false
---

A short month with a lot of progress! It went over so quickly, even this post
missed the end of the month...

+ The big focus this month was the implementation of our dense flow kernel
  (com1DFAPy) in  python/cython. The aim is to replicate the results of our
  current com1DFA module to be able to swap them. 
  This meant diving deep into every numerical/model detail, things like
  * artificial viscosity
  * friction forces 
  * particle initialisation
  * and many more. 
  
  Alongside this development a lot of *supporting* work was needed,
  i.e. making things easier for us, as one example: being able to read and export
  particle positions.

+ While using our tests we came across some areas to improve on:
  * the module *ana1Tests* was introduced, where we collect code related to
    testing, analytical solutions and similar (however not stuff related to code
    testing, i.e. pytest)
  * a helpful new feature is the possibility to filter benchmark tests by tags, i.e.
    one only wants to run tests including entrainment, or only idealised
    topographies, or some other combination
  * the similarity solution was improved, with added run script and setup
    reading from ini file.

+ Then we have a lot of minor improvements:
  * global plotting flags, options to save outputs and plots
  * rename Velocity to FlowVelocity, rename the *hockey* test case to *parabola*
  * update topographies with channels
  * functions for 3D topography plots 
  * more flexible cleaning routines 
  * code coverage for cython files
  * documentation updates

And last but not least: our 2nd Scientific Meeting took place at the beginning
of the month. Thanks again to all participants for your helpful and much
appreciated input!

That's it for this update, thanks for reading! 

Felix
