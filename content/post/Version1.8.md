---
title: "Release Version 1.8"
date: 2024-02-15T00:00:00+01:00
draft: false
slug: "version1_8"
---

**Today we released [Version 1.8](https://github.com/avaframe/AvaFrame/releases/tag/1.8)** 

**Please note: the QGis AvaFrame Connector also received an update. Please do not forget to run Admin -> Update 
AvaFrame from within the toolbox to receive the updated core as well.** 

The new computational module release. 

We've added two new (experimental) computational modules, com4FlowPy and com6RockAvalanche. Com4FlowPy integrates the development already done in the FlowPy project, and aims to be the target for flowpy development from now on. 
com6RockAvalanche is a highly experimental extension of com1DFA, aiming to find a parameterset/adjustments needed to simulate rock avalanches. It also allows the AvaFrame QGis Connector to set the release-thickness, which is done via a release-thickness raster file. This also necessitated a change in remeshing: now, the release thickness files are meshed analogous to the topography file (if necessary).

One important change in regards to the operational application of com1dfa: now the release volume of secondary release areas is considered when choosing the correct friction settings for samosATAuto friction model. Important: it does not matter whether the secondary release areas are actually triggered or not, their volume is included in the decision. 

## Breaking change

There's one breaking change in this release: If you used the override function from within one of the ini configuration files, this changes now. It is necessary to include the module collection as well, ie. instead of [com1dfa_override], you have to use [com1dfa_com1dfa_override].


## What's Changed
* Add result types and info about entTh to documentation [doc] by @awirb in https://github.com/avaframe/AvaFrame/pull/934
* Add sec release to relVolume computation for samosATAuto by @awirb in https://github.com/avaframe/AvaFrame/pull/932
* Include flowpy development in com4FlowPy [com4]  by @Iceman-bfw in https://github.com/avaframe/AvaFrame/pull/933
* add coulomb min shear friction by @awirb in https://github.com/avaframe/AvaFrame/pull/942
* Add L to simName for samosAT; fixes #930 [com1] by @fso42 in https://github.com/avaframe/AvaFrame/pull/940
* Set exists_ok on creation of dirs (for parallel computing) [in3] by @awirb in https://github.com/avaframe/AvaFrame/pull/946
* Add com6 rock avalanche [com6] by @fso42 in https://github.com/avaframe/AvaFrame/pull/939
* Add new functions to analyze deepDiff results in parameter variation cases [com1] by @fso42 in https://github.com/avaframe/AvaFrame/pull/945
* add aimec functionality to color parameters of type string [ana3; out3] by @awirb in https://github.com/avaframe/AvaFrame/pull/947
* check warnings in pytest update adding a new column to dfs by @awirb in https://github.com/avaframe/AvaFrame/pull/949
* Extend Kot topography [data] by @fso42 in https://github.com/avaframe/AvaFrame/pull/948
* change finding of velocity threshold indices in aimec for thalweg plots [ana3] by @awirb in https://github.com/avaframe/AvaFrame/pull/950
* Fixed avaKot pathAB projection [data] by @fso42 in https://github.com/avaframe/AvaFrame/pull/956
* fix bug in labelling in legend by @awirb in https://github.com/avaframe/AvaFrame/pull/957
* add runscript for prob analysis for existing sims within ava directory [ana4; in3] by @awirb in https://github.com/avaframe/AvaFrame/pull/955
* Add contour line plot [com1; ana5; out3; breaking change] by @awirb in https://github.com/avaframe/AvaFrame/pull/953
* fix bug in figure legend by @awirb in https://github.com/avaframe/AvaFrame/pull/958
* In case of relThFile = True, remesh the thickness file if needed [com1DFA] by @fso42 in https://github.com/avaframe/AvaFrame/pull/954
* Update docu; add init for com4 by @fso42 in https://github.com/avaframe/AvaFrame/pull/960

## New Contributors
* @Iceman-bfw made their first contribution in https://github.com/avaframe/AvaFrame/pull/933

**Full Changelog**: https://github.com/avaframe/AvaFrame/compare/1.7.2...1.8

Felix
