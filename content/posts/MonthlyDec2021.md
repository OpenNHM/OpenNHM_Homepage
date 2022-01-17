---
title: "This month in AvaFrame - December 2021 edition"
date: 2022-01-03T00:00:00+01:00
draft: false
---

Welcome to our last monthly update for 2021. 

This month so a broad development across all modules:

- A new module `ana4Stats/probAna` is available and is concerned with all things related to probability runs 
  and it therefore includes a lot of tools for parameter variations as well. This lead to some general improvements
  regarding filtering and ordering of simulations, both before any simulations are run, as well as for sorting 
  and filtering results for postprocessing. 

- Some more initial particle distribution stuff was tackled, mainly experimenting on new ideas / improvements.

- One big improvement is related to our unique ID, the so called `simHash`. It now includes input data info 
  about the DEM, release/entrainment/secondary release scenario names. This avoids a previous issue in which 
  it was possible to get the same hash for different input values, if those values originated in the input 
  shape files. Glad this is off the table now...

- In the same area of the code, the process of getting thickness values from configuration or shape file is 
  now fully documented and fully reproducible.

- The documentation received some substantial update regarding the splitting and merging of particles, as well
  as an extensive documentation for our bottom friction and operator splitting algorithm.

- The data format for AIMEC inputs and outputs is refactored to use pandas dataframes. This is to make it easier to use,
  filter, order the outputs of AIMEC.

- We introduced the concept of the `travel angle`, expect some more development/output in this regard. 

- Work is still going on regarding the similarity solution convergence test.

Some fixes that are included now:

- Fix com2AB documentation with ambiguous symbols

- Fix bug in ordering simulation files inside AIMEC

Hope you all had a nice end of the year, and are are excited for the new year to come (at least I am :-) )

Felix

