---
title: "Release Version 1.7"
date: 2023-10-12T00:00:00+01:00
draft: false
slug: "version1_7"
---

**Today we released [Version 1.7](https://github.com/avaframe/AvaFrame/releases/tag/1.7)** 

This is a benchmark release.
We are updating the benchmarks that changed due to the introduction of the samosATAuto friction model. This release
contains all necessary configuration changes. The actual result files will be pushed in the next version 1.7.1.
We also updated and cleaned all AIMEC plotting, including new plots and removing/consolidating some others.

## What's Changed
* Add pdf output to readthedocs by @fso42 in https://github.com/avaframe/AvaFrame/pull/903
* change location of plot / deprecated libs pytest  by @awirb in https://github.com/avaframe/AvaFrame/pull/904
* allow to pass dem [ana3] by @awirb in https://github.com/avaframe/AvaFrame/pull/905
* Add new AIMEC plot; add flag for in depth plots; change readASCheader [ana3] by @awirb in https://github.com/avaframe/AvaFrame/pull/908
* fix bug in checking for matplotlibversion by @awirb in https://github.com/avaframe/AvaFrame/pull/916
* changes topo gen to move topo in z direction [in3Utils] by @chhesselbach in https://github.com/avaframe/AvaFrame/pull/911
* update thalweg plot to compute average for bars by @awirb in https://github.com/avaframe/AvaFrame/pull/917
* Update py versions in GitHub workflows by @fso42 in https://github.com/avaframe/AvaFrame/pull/912
* Clarify input information and requirements in documentation by @fso42 in https://github.com/avaframe/AvaFrame/pull/914
* add ax object to aimec contour plot colorbar by @awirb in https://github.com/avaframe/AvaFrame/pull/918
* make name dependent on input in plot [out3Plot] by @awirb in https://github.com/avaframe/AvaFrame/pull/919
* Change aimec [ana3,ana5,out3] by @awirb in https://github.com/avaframe/AvaFrame/pull/921
* Adjust aimec min mean values with added zero mask [ana3] by @awirb in https://github.com/avaframe/AvaFrame/pull/923
* Add documentation for particle plots [out3] by @awirb in https://github.com/avaframe/AvaFrame/pull/922
* Adjust float format of ReleaseStat to avoid Excel Problem by @fso42 in https://github.com/avaframe/AvaFrame/pull/924
* add updated aimec cfg for benchmarks by @awirb in https://github.com/avaframe/AvaFrame/pull/925

## New Contributors
* @chhesselbach made their first contribution in https://github.com/avaframe/AvaFrame/pull/911

**Full Changelog**: https://github.com/avaframe/AvaFrame/compare/1.6.1...1.7

Felix
