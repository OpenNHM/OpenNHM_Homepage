---
title: "This month in AvaFrame - March 2022 edition"
date: 2022-04-03T00:00:00+01:00
draft: false 
---

Welcome to the March 2022 update.

As you might have noticed from all the other posts, this month saw our 1st public workshop. In case you missed it, see the
previous post for a link to its recording. Big thanks to all participants, it is nice to know the interest in our
project! And also, a big thanks for all the feedback we got, it is always very much appreciated.

We are still working on the first release, which is expected to be released within the next few weeks (probably beginning of
April). 

- Add the version to all logs, including full info about the commit / tag the current code is on. You are on modified
code if you see a `+dirty` in the version. This means this code is not reproducible! If you need reproducibility, please
make sure you are on a clean commit. 

- Add date to log name to be able to find the latest log and not overwriting any logs. 

- We have a new *ana5utils* module with thalweg-time diagrams and simulograms, i.e. figures and methods related to radar
measurements and a new way to display temporal evolution of simulations results. We will adequately introduce this in an
upcoming publication.

- A few plots were improved. Most notably is adding hillshade and contours to the standard peak plots. 

- Update documentation, especially by adding info about ata viscosity.

- An improvement regarding the AvaFrameConnector (for QGis): Alpha-Beta is now optional in the operational runscript,
  i.e. profiles and split points are not mandatory anymore. 

- We fixed the missing `tau0` in the friction relation `SamosAT`. It is by default set to 0, so there is no impact on already
calculated standard runs. 

We had a few release candidates, for a full changelog see [github releases](https://github.com/avaframe/AvaFrame/releases).

Felix
