---
title: "This month in AvaFrame - May 2021 edition"
date: 2021-06-05T17:08:58+01:00
draft: false
---

Welcome to the May 2021 edition of our monthly update. Our main goal was the
preparation for the switch of the dense flow model com1DFA from a C code to
python (cython) code. This meant to check every little detail and difference that
we found as well as:

+ updated the documentation for the new python com1DFAP: algorithm, workflow and description
  
+ updated the re-projection method of particles. Now particles are re-projected
  normal to the surface and not vertically. This is especially important at
  sharp drops. We also added a test case for this.  

+ restructured the com1DFA run workflow 

  - now everything is controlled in model configuration via ini (the previous
    com1DFA had a lot of internal setup)
  
  - allow for parameter variation runs right from python

  - new naming of simulations which provides easy filtering options

+ restructured the benchmark workflow and updated run scripts for standard tests 

  - added simple functions to fetch benchmarks

  - simplify plotting and AIMEC path functions according to new structure based 
  on simulation name and configuration

+ com2AB (Alpha Beta) now allows for running with custom parameters

+ added an export function to visualise particle properties with Paraview

+ started the development of the QGis Connection. See this
  [repository](https://github.com/avaframe/QGisAF) for the development. 

Since we are now nearing the milestone of our first public prototype, I guess we
will have to start posting some nice graphics as well... So watch this space for
upcoming posts! :-) 

Felix
