---
Title: "This month in AvaFrame - September 2025 edition"

Date: 2025-10-01T00:00:00+01:00
author: "Felix"
Draft: false

Tags:
- avaframe
- monthly

Description: "Regional avalanche modeling workflow integration and stability improvements to
com1DFA. Improved AIMEC analysis capabilities, configuration updates and com8MoTPSA module. Read more..."

---

Welcome to the September 2025 update:

September brought improvements to AvaFrame's regional modeling capabilities and important
stability improvements to our core simulation modules. We completed a long-awaited regional workflow
integration and addressed critical particle handling issues.

Major Workflow Integration

The highlight of this month was PR #1053 (https://github.com/avaframe/AvaFrame/pull/1053), which added a
complete regional modeling workflow for com1DFA. This substantial contribution by Leon Wagner
introduces the new in4 module and expands com7Regional to enable large-scale avalanche simulations across
regional terrain datasets. The integration includes comprehensive documentation available at
https://docs.avaframe.org/en/regional/moduleCom7Regional.html.

Com1DFA Stability

PR #1180 (https://github.com/avaframe/AvaFrame/pull/1180) fixed a critical issue where particles with zero
mass (due to detrainment) could cause division-by-zero errors, leading to invalid velocities and cell
positions. The module now checks for zero-mass particles and removes them before computational
operations, preventing potential crashes in long-running simulations.

Analysis Tools Enhancement

Our AIMEC analysis tool became more robust with PR #1189 (https://github.com/avaframe/AvaFrame/pull/1189),
which now gracefully handles scenarios with zero result rasters. This affects ana3AIMEC, ana4Stats, and
out3Plot modules, making analysis workflows more reliable when dealing with incomplete simulation datasets.

Module Refinements

Several focused improvements enhanced specific modules:

Com7Regional Streamlining - PR #1181 (https://github.com/avaframe/AvaFrame/pull/1181) consolidated the
regional workflow by integrating runSplitInputs.py functionality directly into runCom7Regional.py,
simplifying the regional modeling pipeline for QGIS connector scripts.

Com8MoTPSA Enhancement - PR #1187 (https://github.com/avaframe/AvaFrame/pull/1187) extended file renaming
functionality to entrainment simulation types, improving consistency in output file naming conventions.

Configuration Cleanup - PR #1191 (https://github.com/avaframe/AvaFrame/pull/1191) removed unused parameters
from the com7Regional configuration file, reducing configuration complexity.

Infrastructure

PR #1186 (https://github.com/avaframe/AvaFrame/pull/1186) added new log helper scripts for probabilistic run
analysis while removing the deprecated .codeclimate.yml configuration.

Also of note  is the ProBE - Project, which in parts uses AvaFrame and has some ongoing Webinars which we highly recommend. 
For more, see 
[ProBE Website](https://www.naturgefahren.sites.be.ch/de/start/themen/informationen-gemeinden-fachpersonen/neue-beurteilungsgrundlagen-fuer-hangmuren-.html).

See you in October!

Felix

---

Summary of PRs merged in September 2025:

1. PR #1053 - Regional modeling workflow for com1DFA (merged Sep 9)
2. PR #1180 - Zero-mass particle handling fix in com1DFA (merged Sep 10)
3. PR #1181 - Consolidate com7Regional run scripts (merged Sep 16)
4. PR #1186 - Add log helper scripts, remove CodeClimate config (merged Sep 18)
5. PR #1187 - Extend renaming for entrainment simType in com8 (merged Sep 25)
6. PR #1189 - Allow zero result rasters in AIMEC analysis (merged Sep 24)
7. PR #1191 - Remove unused parameters from com7Regional config (merged Sep 25)

Total: 7 pull requests merged




