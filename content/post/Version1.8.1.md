---
title: "Release Version 1.8.1"
date: 2024-04-04T00:00:00+01:00
draft: false
slug: "version1_8_1"
---

**Today we released [Version 1.8.1](https://github.com/avaframe/AvaFrame/releases/tag/1.8.1)** 

**QGis users please note: do not forget to run Admin -> Update AvaFrame from within the toolbox to receive the updated core as well.** 

This release fixes a bug/problem with com2AB in which the chosen interpolation method led to points being offset from the original profile. (Thanks @CT for reporting this)

## What's Changed
* add convert to th from depth [in2; out3] by @awirb in https://github.com/avaframe/AvaFrame/pull/959
* add option to use discrete colorbar [out3] by @awirb in https://github.com/avaframe/AvaFrame/pull/961
* fix bug in color aimec plot by @awirb in https://github.com/avaframe/AvaFrame/pull/964
* Add +1SD point in com2AB plots; change prepareLine [com2AB; geoTrans] by @fso42 in https://github.com/avaframe/AvaFrame/pull/966


**Full Changelog**: https://github.com/avaframe/AvaFrame/compare/1.8...1.8.1


Felix
