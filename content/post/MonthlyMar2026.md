---
Title: "This month in AvaFrame - March 2026 edition"

Date: 2026-04-01T00:00:00+01:00
author: "Felix"
Draft: false

Tags:
- avaframe
- monthly

Description: "Rheological model improvements for Herschel-Bulkley and Bingham models, restructured usage documentation,
 and QGis compatibility fixes. Read more..."

---

Welcome to the March 2026 update:

March focused on improving the rheological models in com1DFA, restructuring the documentation for better usability,
and fixing compatibility issues for the upcoming QGis 4.0 release.

**Rheological Model Improvements**

Two PRs improved the rheological models in com1DFA. PR #1252
(https://github.com/OpenNHM/AvaFrame/pull/1252) corrected the Herschel-Bulkley implementation by replacing the bulk
dynamic viscosity with the consistency factor K. The previous implementation incorrectly assumed these were equivalent,
which is not the case. The theory documentation was updated accordingly.

PR #1254 (https://github.com/OpenNHM/AvaFrame/pull/1254) then added direct input options for yield shear stress
(`tauy`) and dynamic viscosity (`eta`) in the Bingham, Herschel-Bulkley, and O'Brien-Julien rheological models. By
default, these values are used directly from the configuration file. 

**Documentation Restructuring**

PR #1257 (https://github.com/OpenNHM/AvaFrame/pull/1257) restructured the usage documentation by splitting and
merging existing pages into a clearer hierarchy. The old `advancedUsage.rst` was reorganised, and two new pages
(`standardUsage.rst` and `complexUsage.rst`) were added. Redundant content from `expertConfiguration.rst` was removed.
The installation and connector pages were also updated for consistency.

PR #1248 (https://github.com/OpenNHM/AvaFrame/pull/1248) added documentation for the time dependent release feature
in the com1DFA algorithm description.

**Bug Fixes**

PR #1255 (https://github.com/OpenNHM/AvaFrame/pull/1255) fixed the handling of `nan` values and special character
checks in `cfgUtils.simDFTest()`, addressing a compatibility issue with pyarrow on QGis 4.0 on Windows.

PR #1256 (https://github.com/OpenNHM/AvaFrame/pull/1256) updated the energy line test configuration to also save `pfv`
fields. A recent change in how timestep exports work meant the velocity peak field was no longer available with the
default settings, which broke figure generation.

**CI/Build**

PR #1249 (https://github.com/OpenNHM/AvaFrame/pull/1249) updated GitHub Actions versions in the build and upload
workflow, along with minor dependency version updates in pyproject.toml.

In other news, we have another small sideproject running regarding snow slides and their handling for hazard mapping (SRPrax).
This will not directly lead to changes in AvaFrame, but will result in Austrian guildlines for snow slides being published.
Furthermore, the work in relation to a master thesis about PSA is coming along nicely. There's an ongoing PR at the moment, feel
free to comment on it / check it out.

See you in April!

Felix

---

Summary of PRs merged in March 2026:

1. PR #1248 - Add documentation for time dependent release (merged Mar 11)
2. PR #1249 - Update GitHub Actions versions for dependencies (merged Mar 13)
3. PR #1252 - Replace viscosity by consistency factor for Herschel-Bulkley rheology (merged Mar 17)
4. PR #1255 - Fix nan and special character handling in cfgUtils for QGis 4.0 (merged Mar 18)
5. PR #1256 - Update energy line test config to save pfv fields (merged Mar 19)
6. PR #1257 - Restructure and merge usage documentation (merged Mar 25)
7. PR #1254 - Add direct input options for rheological model parameters (merged Mar 26)

Total: 7 pull requests merged
