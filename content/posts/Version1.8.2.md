---
title: "Release Version 1.8.2"
date: 2024-05-17T00:00:00+01:00
draft: false
slug: "version1_8_2"
---

**Today we released [Version 1.8.2](https://github.com/avaframe/AvaFrame/releases/tag/1.8.2)** 

**QGis users please note: do not forget to run Admin -> Update AvaFrame from within the toolbox to receive the updated core as well.** 

This version adds Python 3.12 to the release script. 

If you used and changed resistance parameters (not the outlines/shapes in QGis), this version includes a breaking change! See #970 for more information.


## What's Changed
* add runscript by @awirb in https://github.com/avaframe/AvaFrame/pull/968
* Reduce resistance parameters to one parameter [com1] by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/970
* adjust format of saving particle csv files by @awirb in https://github.com/avaframe/AvaFrame/pull/971
* Modified documentation: resistance parameter [doc] by @PaulaSp3 in https://github.com/avaframe/AvaFrame/pull/972
* add option to write parameter variation config files through ana4Prob… [ana4] by @awirb in https://github.com/avaframe/AvaFrame/pull/973
* Include py 3.12; add psutil requirement by @fso42 in https://github.com/avaframe/AvaFrame/pull/977


**Full Changelog**: https://github.com/avaframe/AvaFrame/compare/1.8.1...1.8.2

Felix
