---
title: "This month in AvaFrame - July 2025 edition"
date: 2025-08-01T00:00:00+01:00
draft: false
tags:
  - avaframe
  - monthly
description: "Major integration of NGI's MoT-Voellmy simulation tool as new com9MoTVoellmy module.
Enhanced com1DFA with raster export capabilities and expanded documentation infrastructure. Read more..."
---

Welcome to the July 2025 update:

July was an exciting month with major expansion of AvaFrame's capabilities! We successfully integrated the Norwegian
Geotechnical Institute's MoT-Voellmy simulation tool, extended our core DFA module with better data export features,
and improved our documentation infrastructure.

## Major New Module Integration

The biggest highlight this month was **PR #1154** ([link](https://github.com/avaframe/AvaFrame/pull/1154)), which
introduced the complete new computational module `com9MoTVoellmy`. This represents a milestone in expanding
AvaFrame's simulation capabilities by integrating NGI's MoT with Voellmy friction approach.

## Com1DFA Improvements 

We improved our core com1DFA module with **PR #1153** ([link](https://github.com/avaframe/AvaFrame/pull/1153)), adding
raster export capabilities for release and entrainment data. Users can now export intermediate raster data to
`Outputs/internalRasters/`, significantly improving workflow transparency and making debugging much easier.

Our analysis tools also got more flexible with **PR #1155** ([link](https://github.com/avaframe/AvaFrame/pull/1155)),
which enhanced the range-time analysis script to work without configuration files and support results from multiple
computational modules.

## Documentation Expansion

July saw a major push in documentation quality. We added comprehensive documentation for both new MoT modules through *
*PR #1157** ([link](https://github.com/avaframe/AvaFrame/pull/1157)) and **PR #1158** ([link](https://github.com/avaframe/AvaFrame/pull/1158)).

**PR #1156** ([link](https://github.com/avaframe/AvaFrame/pull/1156)) enhanced our cross-module analysis documentation,
providing clear guidelines for using range-time analysis with external modules.

## Looking Forward

The MoT-Voellmy integration represents a significant step forward in making AvaFrame a comprehensive platform for
different avalanche simulation approaches. As mentioned in our June update, we're continuing to work on full calibration
and optimization of these new methods.

See you in August!

Felix