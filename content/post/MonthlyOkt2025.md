---
Title: "This month in AvaFrame - October 2025 edition"

Date: 2025-11-01T00:00:00+01:00

Draft: false

Tags:
- avaframe
- monthly

Description: "New rheological models for debris-flow simulations in com1DFA. Updated com9MoTVoellmy
documentation and improved AIMEC analysis handling. Read more..."

---
Welcome to the October 2025 update:

October brought new friction models to com1DFA, better documentation for our MoT-Voellmy module, and several
improvements to configuration and analysis tools.

**New Rheological Models**

PR #1169 (https://github.com/avaframe/AvaFrame/pull/1169) added rheological models for debris-flow
simulations to com1DFA. This extends AvaFrame's capabilities from snow avalanches to debris flows. The
implementation updates the Cython force computation functions, adds new configuration parameters, and
includes documentation at https://docs.avaframe.org/en/rheologicalmodels/theoryCom1DFA.html#rheological-models. 

**Documentation Updates**

PR #1196 (https://github.com/avaframe/AvaFrame/pull/1196) expanded the com9MoTVoellmy documentation with
details on input/output specifications and setup instructions. The update also fixed the autodoc
configuration (replacing autosummary_mock_imports with autodoc_mock_imports) and improved API references.

**Configuration Changes**

PR #1197 (https://github.com/avaframe/AvaFrame/pull/1197) and PR #1198
(https://github.com/avaframe/AvaFrame/pull/1198) renamed "FromShp" to "FromFiles" in the INI configuration
files. This better reflects that AvaFrame reads various file formats, not just shapefiles.

**Analysis Tools**

PR #1190 (https://github.com/avaframe/AvaFrame/pull/1190) updated ana3AIMEC to handle cases where reference
or comparison data contains only zero values. The module now skips plot generation in these scenarios instead
of creating empty or misleading plots.

**Dependencies**

PR #1194 (https://github.com/avaframe/AvaFrame/pull/1194) added explicit temporary dependencies (gdal,
libgdal, geos, proj) to pyproject.toml to address installation compatibility issues.

Furthermore we took part in the [Snow.is](https://snow2025.is/) conference in Iceland. 
Have a look at O3.1 in the [proceedings](https://snow2025.is/wp-content/uploads/2025/09/SNOW2025_Abstract_Book-Lokautgafa.pdf) for our contribution. 

And another huge development we are quite happy about is the inclusion of NGI's MoT-Voellmy in the QGis Connector plugin. This 
is currently still in experimental mode, but we are looking forward to get feedback and improve the plugin. We are in close
communication with people from the NGI and SLF regarding the calibration of the MoT modules. 

And last, but in now way least, we contributed to a paper which finally got published in [NHESS](https://nhess.copernicus.org/articles/25/4185/2025/). 
Thanks at Michael Neuhauser for the great work!

See you in November!

Felix

---
Summary of PRs merged in October 2025:

1. PR #1169 - Rheological models for debris-flow simulations in com1DFA (merged Oct 15)
2. PR #1190 - Skip plotting when data contains only zeros in ana3AIMEC (merged Oct 13)
3. PR #1194 - Add temporary GDAL dependencies to pyproject.toml (merged Oct 13)
4. PR #1196 - Update and expand com9MoTVoellmy documentation (merged Oct 21)
5. PR #1197 - Rename FromShp to FromFiles in INI files (merged Oct 16)
6. PR #1198 - Rename FromShp to FromFiles in INI files (part 2) (merged Oct 16)

Total: 6 pull requests merged
