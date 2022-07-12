---
title: "Release Version 1.2"
date: 2022-07-07T00:00:00+01:00
draft: false
slug: "version1_2"
---

**Today we released [Version 1.2](https://github.com/avaframe/AvaFrame/releases/tag/1.2)** 

The main changes are the automatic split point generation and optional computation of fields 
inside the calculation loop. Furthermore, renaming functions used for the QGis AvaFrameconnector are included.

ENHANCEMENTS

- Add function for renaming simulations, i.e. adding info to the simName. Used for AvaFrameConnector
- Split cfgUtils: Utils contain all reading and writing; cfghandling has functions that do 
  something with the cfgInfos
- Make computation of ppr, pta, P, TA and pke optional within the calculation loop. Only compute them 
  if they are required as output
- Add automatic split point generation: - First run a DFA simulation, either using the runDFAModule flag 
  in runComputeDFAPath.py or yourself
  - Do not forget that you need to save particles or FD, FM, FV for multiple time steps
  - What DFA parameters to use is not yet clear. I would use the BenMoussa time stepping and particles parameters, 
    sphOption 2, explicit friction option 1, some artificial viscosity, and maybe activate curvature 
    (with all this and a mu=0.42, I get ok results)
  - Then runComputeDFAPath computes the mass average path, extends it and defines a splitPoint

FIX
- Particle exiting domain was not working properly with the new cython flag (wraparound boundcheck…)
- Correct hybrid Path ini file
- Update fields is too slow #455
- Automatic split point or beta point finding #706
- Add pfe to output files #694
- Make cflTime and sphKernelRadius a common option #668
- Change benchmarks not read particles from file (particles files still exist)
- Add consistency check for com1DFA configuration
- Fix problems with filtering of simulations
-  Aimec comparison checks
- Add missing mass files to benchmarks

Felix
