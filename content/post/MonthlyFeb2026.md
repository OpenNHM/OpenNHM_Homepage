---
Title: "This month in AvaFrame - February 2026 edition"

Date: 2026-03-01T00:00:00+01:00
author: "Felix"
Draft: false

Tags:
- avaframe
- monthly

Description: "Multi-layer result support across AIMEC, statistics, and probability analysis. Expert configuration override folders.
 DebrisFrame improvements for time dependent release and topography plotting. Read more..."

---

Welcome to the February 2026 update:

February was a busy month with multi-layer result support landing across the code base, a new intermediate configuration
system, and continued DebrisFrame development including time dependent release improvements and debris-flow topography
plotting.

**Multi-Layer Result Support**

Two PRs brought multi-layer result support to the full analysis pipeline. PR #1236
(https://github.com/OpenNHM/AvaFrame/pull/1236) added layer detection to `parseSimName()` and layer-aware columns
(ppr_l1, ppr_l2) to `makeSimFromResDF()`. It also refactored com8MoTPSA postprocessing to use L1/L2 layer naming
instead of the previous dfa/psa modelType workaround, and added a `runoutLayer` config parameter to AIMEC for explicit
layer selection. **This is a breaking change** for com8MoTPSA - output filenames changed from the old modelType naming
to layer-based naming.

PR #1242 (https://github.com/OpenNHM/AvaFrame/pull/1242) then extended multi-layer awareness to ana4Stats, probAna, and
downstream tools. The com8MoTPSA module was further refactored, replacing `MoTGenerateConfigs` with `com1DFAPreprocess`
and adding `modName` for simulation filtering.

**Intermediate (Expert) Configuration Override**

PR #1230 (https://github.com/OpenNHM/AvaFrame/pull/1230) added an intermediate configuration override system. A new
`Inputs/CFGs/` directory in avalanche projects takes priority over local config files. The PR also refactored
`cfgUtils.getModuleConfig()` to use explicit `fileOverride` and `avalancheDir` arguments instead of positional
parameters, and removed the deprecated `rewriteLocalCfgs` and `_removeCfgItemsNotInOverride` functions.

**Windows Multiprocessing Fix**

PR #1234 (https://github.com/OpenNHM/AvaFrame/pull/1234) removed Windows-specific conditional imports for
`multiprocessing` across com1DFA, com4FlowPy, com8MoTPSA, and com9MoTVoellmy. Recent Python versions no longer need
this distinction on Windows, and the old code was causing simulations to run multiple processes but only on a single
core. Parallel execution now works correctly on all platforms.

**Documentation**

PR #1233 (https://github.com/OpenNHM/AvaFrame/pull/1233) updated the configuration documentation with a graph
illustrating the configuration hierarchy.

**Module Updates**

PR #1222 (https://github.com/OpenNHM/AvaFrame/pull/1222) finalized the com6 Scarp module with minor changes to
attribute names and meanings.

**Note**

We are currently working on a new release of AvaFrame, which will upgrade the major version number from 1.0 to 2.0.
This will include breaking changes! We will also switch the AvaFrame QGis Connector to an OpenNHM QGis Connector, this
includes, for example, the new intermediate configuration override system.

See you in March!

Felix

---

Summary of PRs merged in February 2026:

1. PR #1230 - Add expert configuration override folder (merged Feb 3)
2. PR #1234 - Fix Windows multiprocessing to use multiple cores (merged Feb 5)
3. PR #1233 - Update configuration documentation with graph (merged Feb 9)
4. PR #1236 - Add multi-layer result support; breaking change in com8 (merged Feb 17)
5. PR #1239 - Include time dependent release values in simulation hash (merged Feb 18)
6. PR #1241 - Add debris-flow topography plotting (merged Feb 18)
7. PR #1222 - Finalize com6 Scarp module (merged Feb 19)
8. PR #1240 - Add time dependent release info to reports (merged Feb 19)
9. PR #1242 - Extend multi-layer support to analysis and probability tools (merged Feb 19)
10. PR #1246 - Add timeDependentRelease configuration to com9MoTVoellmy (merged Feb 27)

Total: 10 pull requests merged