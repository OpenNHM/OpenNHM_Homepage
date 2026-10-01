---
title: "This month in AvaFrame - August 2026 edition"
date: 2026-09-01T00:00:00+01:00
draft: false
author: "Felix"
tags:
  - avaframe
  - monthly

Description: "FlowPy acceleration, a new optimisation module, spatial Voellmy
friction, and extended time-dependent release inputs."
---

Welcome to the August 2026 edition of the AvaFrame monthly update:

This month brought an optional faster compute engine for FlowPy, a new
optimisation module for com8MoTPSA, and spatially variable friction for rock
avalanche simulations. We also extended time-dependent release inputs and
adapted shared functions for DebrisFrame development.

## Features

**FlowPy Performance**

- **PR #1319** ([link](https://github.com/OpenNHM/AvaFrame/pull/1319))
  added an optional Numba compute engine for FlowPy. The contribution
  reported speedups of around 30–45 times in selected benchmarks.
  Python remains the default engine and the fallback for unsupported
  options or installations without Numba. Results matched exactly on
  tested single-tile domains, though small numerical differences were
  observed on fine-resolution flat runout terrain.

**Optimisation and MoT-PSA**

- **PR #1245** ([link](https://github.com/OpenNHM/AvaFrame/pull/1245))
  introduced ana6Optimisation for com8MoTPSA, with a combined runout
  and Tversky loss function, Morris sensitivity analysis, and
  surrogate-based optimisation. The com8 workflow now checks for
  existing simulations and processes simulation batches in chunks.
- **PR #1306** ([link](https://github.com/OpenNHM/AvaFrame/pull/1306))
  updated the com8 configuration file for the new format.

**Rock Avalanche Friction**

- **PR #1312** ([link](https://github.com/OpenNHM/AvaFrame/pull/1312))
  added support for spatially variable Voellmy friction in com6.
  Friction rasters can be generated from a single shapefile containing
  both friction parameters. Ambiguous inputs containing both rasters
  and a friction shapefile are rejected.

**Release Inputs and Shared Functions**

- **PR #1334** ([link](https://github.com/OpenNHM/AvaFrame/pull/1334))
  added a CSV input option for time-dependent release, specifying
  coordinates, time steps, thickness, and velocity components.
  This allows the initial movement direction to be defined explicitly,
  alongside the existing polygon-based release option.
- **PR #1331** ([link](https://github.com/OpenNHM/AvaFrame/pull/1331))
  adapted shared input and dense flow functions for use in
  DebrisFrame module development.

**Assets and Scarp Tools**

- **PR #1324** ([link](https://github.com/OpenNHM/AvaFrame/pull/1324))
  made the value representing locations without assets configurable.
- **PR #1325** ([link](https://github.com/OpenNHM/AvaFrame/pull/1325))
  corrected the scarp azimuth calculation, updated configuration and
  attribute names, and added documentation.

## Bug Fixes

- **PR #1326** ([link](https://github.com/OpenNHM/AvaFrame/pull/1326))
  fixed FlowPy parameter handling when an input file contains an
  invalid value. The default is now restored instead of reusing
  the previous value, which could affect simulation results.
- **PR #1329** ([link](https://github.com/OpenNHM/AvaFrame/pull/1329))
  corrected forest-effect handling involving remeshing and disabled
  forest effects for simulations without resistance.

## Testing and Benchmarks

- **PR #1321** ([link](https://github.com/OpenNHM/AvaFrame/pull/1321))
  added FlowPy benchmarks for a channelled parabola and the Arzler Alm
  avalanche. A new comparison script checks simulation rasters
  against reference data pixel by pixel and writes a test report.

**AvaFrameData** - **PR #6** ([link](https://github.com/OpenNHM/AvaFrameData/pull/6))
completed author attribution and Zenodo metadata for our data repository,
now released as 1.1 and fully citable.

Welcome to first-time contributors **@jmasseysykes** (PR #1319) and
**@MunsMan** (PR #1326). Thanks for the contributions!

See you in September!

Felix
