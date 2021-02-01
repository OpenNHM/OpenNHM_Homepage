---
title: "This month in AvaFrame - January 2021 edition"
date: 2021-01-30T19:08:58+01:00
draft: false
slug: "monthlyjan2021" 
---

Welcome to the first instalment of our monthly update of 2021. This month we
started getting into the nitty-gritty of our dense flow module's numerical
implementation:

+ To facilitate and improve our development we added new test cases. This time
they are more geared towards testing specific numerical issues and more *targeted*
issues, concentrating for now on the dense flow module com1DFAPy.

    * flat plane: a *pile of sand* (i.e. particles with coulomb friction)
    on a flat plane. The pile should or should not move depending on the
    steepness of the sides of the pile

    * inclined slope: similar to the previous, a *pile of sand* (coulomb
    friction again) flowing down an inclined plane. This test enables comparison
    to a solution described in
    [Savage-Hutter 1993](https://link.springer.com/article/10.1007/BF01176861) 
    in which the depth and velocity profiles can be determined in an analytical
    form.
    
    * (rotated) pyramid: generation routines to produce a, potentially rotated
    and/or shifted, pyramid with a release area at the top of the pyramid. This
    allows for checking of rotational symmetry, among others. 
    
    
+ We are currently looking at and analysing how to place the initial particles
and what effect this has further along the simulation. 

+ Getting into the numerical development also means the compute times start to
play a role. We moved some parts of the code over to Python to improve the
computation efficiency of the python dense flow kernel. We are starting to
profile our python code (pudb and cProfile for those interested). 

+ For general analysing with ana3AIMEC: after some deliberation we decided to
  move the (arbitrary) starting point of our runout calculation to the top of
  the main avalanche profile (instead of some point further down the profile).
  See our definitions for this in the [glossary](https://docs.avaframe.org/en/latest/glossary.html).
  If this makes you internally scream in agony because we got it all wrong, feel
  free to contact us!
  
+ We have a ton of minor changes which however improve usability quite a lot. That means
  mundane (some might say boring) things like enabling underscores in input names,
  consistent naming of result variables, extended export capabilities (more
  time steps), and many more. 

+ Bringing AvaFrame to the Windows world is also currently high on our
  priority list. We explored options on the best ways to install and maintain an
  AvaFrame installation on as many Windows versions as possible. Expect some
  exciting news on this one in the next few weeks. 
  
As you can see, we are off to a good start this year! As always please contact
us with any questions or issues you have!

Felix
  
