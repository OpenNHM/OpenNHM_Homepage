---
title: "This month in AvaFrame - May 2026 edition"
date: 2026-06-01T00:00:00+01:00
author: "Felix"
draft: false
tags:
  - avaframe
  - monthly

Description: "AvaFrame 2.0 released with breaking changes, first 2.1 release candidates, com5/com1DFA fixes, 
time-dependent release, selective particle output, and MoT-Voellmy updates."

---

Welcome to the May 2026 update for AvaFrame:

The big news this month is the **[release of AvaFrame 2.0](/post/version2.0/)**, which brings several breaking
changes and new capabilities. We also shipped the first 2.1 release candidates by the end of
the month.

## Changes in May 

### Bug Fixes

**com5 / com1DFA consistency fixes** -- **PR #1274**
([link](https://github.com/OpenNHM/AvaFrame/pull/1274)) fixed several bugs
discovered during simulations: a circular reference in stopped particles
that swapped flowing and stopped mass in output rasters, stale bond indices
after particle removal causing data corruption, a division-by-zero guard in
reprojection, and memory ownership issues that caused dangling references.

**cfgUtils string handling** -- **PR #1279**
([link](https://github.com/OpenNHM/AvaFrame/pull/1279)) fixed handling of
`none` strings in numeric conversion checks, a Windows-specific issue.

### Features

**Time-dependent release** -- **PR #1267**
([link](https://github.com/OpenNHM/AvaFrame/pull/1267)) extended the
time-dependent release option in com1DFA to support multiple release
features and updated the corresponding standard tests.

**Selective particle output** -- **PR #1273**
([link](https://github.com/OpenNHM/AvaFrame/pull/1273)) added an option to
save only selected particle properties, reducing disk usage. **PR #1275**
([link](https://github.com/OpenNHM/AvaFrame/pull/1275)) consolidated
particle property definitions into a single location to make them easier to
maintain.

### Model Updates

**com9 MoT-Voellmy** -- **PR #1268**
([link](https://github.com/OpenNHM/AvaFrame/pull/1268)) updated the model
configuration and executables to the 2026-04-20 version, replacing the
momentum threshold with a minimum momentum fraction parameter and adjusting
friction coefficients.

### Analysis & Tools

**Scarp** -- **PR #1263**
([link](https://github.com/OpenNHM/AvaFrame/pull/1263)) updated the scarp
script to prevent negative values in generated raster files.

## 2.1 Release Candidates

The first 2.1 release candidates landed on May 28th:
[2.1rc1](https://github.com/OpenNHM/AvaFrame/releases/tag/2.1rc1),
[2.1rc4](https://github.com/OpenNHM/AvaFrame/releases/tag/2.1rc4), and
[2.1rc5](https://github.com/OpenNHM/AvaFrame/releases/tag/2.1rc5).

In other news: we welcome our new master student Michael Pallua, he'll look into entrainment for com1 and com9.

See you in June!

Felix
