---
draft: false
publishDate: 2026-05-04
author: Felix
subtitle: ""
title: AvaFrame Version 2.0
tags:
  - avaframe
  - version
  - release
image: img/FZGL_PFD.jpg
categories:
  - whatever  
description: "AvaFrame 2.0: simulation naming changes, expert configuration, new OpenNHM QGis Connector, 
and breaking changes"
---

**We released [AvaFrame Version 2.0 (full changelog)](https://github.com/OpenNHM/AvaFrame/releases/tag/2.0)** (and 
the obligatory 2.0.1 due to a problem in the release pipeline)

**QGis users please note: uninstall the previous AvaFrameConnector plugin, install the new
OpenNHMConnector (Plugins -> Manage and Install Plugins -> search for OpenNHMConnector),
and then run Admin -> Update AvaFrame from within the toolbox to receive the updated core.**

This is a major release with several user-facing changes and breaking updates. Please read carefully before upgrading.

**Key changes:**

- **Simulation names now include the module name** as part of their identifier (e.g. `release1PF_4ab57f8760_com1_C_L_null_dfa` instead of `release1PF_4ab57f8760_C_L_null_dfa`). Existing scripts or workflows that parse simulation names will need to be updated.

- **Expert configuration (advanced usage)** is now available. Module default parameters can be overridden via expert configuration files, either through the QGis Connector or by placing ini files in the project's `Inputs/CFGs/` directory. See the [Advanced Usage documentation](https://docs.avaframe.org/en/latest/advancedUsage.html) for details.

- The **AvaFrame QGis Connector has been superseded by the OpenNHM QGis Connector**. See the [Connector
  documentation](https://docs.avaframe.org/en/latest/connector.html).

- **Com9MoTVoellmy** received an update with a new configuration version (incompatible with 1.13.2 ini files).

**Breaking changes since 1.13.2:**

Config/API:
- `getModuleConfig` signature changed — `fileOverride` and `modInfo` parameters removed
- `rewriteLocalCfgs`, `_removeCfgItemsNotInOverride`, `checkCfgInfoType`, and `MoTGenerateConfigs` removed
- `plotFields` config key removed from com1DFA — `resType` now controls all output fields
- Com9MoTVoellmy config version updated (incompatible with 1.13.2 ini files)

Renames:
- `THICKNESSThFromShp` renamed to `THICKNESSThFromFile`
- `findAvaDirs` (com7) moved to in3Utils as `findAvaDirsBasedOnInputsDir`
- `splitInputsFlag` renamed to `splitInputs` in com7Regional

Output changes:
- Not-affected cells now use -9999 instead of 0 in all output rasters; a new config parameter defines the no-data value
- Output rasters compressed by default when written as .tif
- Multi-layer suffix (L1, L2, ...) added to filenames (at the moment only relevant for com9MoTPSA)

Removed:
- `runSplitInputs.py` — functionality integrated into `runCom7Regional.py` via `--split-inputs` flag
- Windows-OS-specific conditional imports for multiprocessing removed

Join the [discussion for this release](https://github.com/OpenNHM/AvaFrame/discussions/1269) — feedback and questions welcome!

Felix
