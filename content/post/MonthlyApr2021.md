---
title: "This month in AvaFrame - April 2021 edition"
date: 2021-05-05T17:08:58+01:00
draft: false
---

Welcome to the April 2021 edition of our monthly update. 

Apart from the release of version 0.3, we put a lot of effort into our
python/cython dense flow avalanche module *com1DFAPy*, targeting a swap with
*com1DFA* within the next month:

+ com1DFAPy now includes:
  
  - an additional particle initialisation method: the *per depth* method

  - the option to use secondary release areas. They are being triggered if
  particles enter the area of a secondary release area.

  - split simulation types for entrainment and resistance. So far only a
    combined type existed. This allows for more granular and easier control of
    different simulation setups.

  - distinguish grid size used for the normal computation and for interpolating
  the fields from the grid used for neighbour search (kernel smoothing length).

  - an option to remesh the input DEM

  - better output options to reduce computational costs (mainly RAM usage)

  - proper handling of overlapping release areas 
   
The second big block tackles reporting and visualisation:

+ output options for visualisation in *Paraview*

+ introduce constraining plots to data plus a buffer zone

+ generate report and plots to validate the entrainment

+ update benchmark files, ini files and run scripts to new options

+ improve Aimec plots (add some statistical information about the error)

And last but not least, this month also saw us also focusing on getting things ready for the EGU:

+ a new page was introduced in our docu about
  [testing](https://docs.avaframe.org/en/latest/testing.html) including an
  example of a full report of our standard tests. There you'll also find all
  available test topographies. 

+ we presented these tests and our strategy at EGU21, see
  [abstract](https://doi.org/10.5194/egusphere-egu21-6560) and [publicly
  available video](https://www.youtube.com/watch?v=GS7zdlByLQE).

Felix
