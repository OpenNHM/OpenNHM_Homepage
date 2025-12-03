---
Title: "This month in DebrisFrame - November 2025 edition"

Date: 2025-12-02T00:00:00+01:00
author: "Paula, Julian"
Draft: false

Tags:
- debrisframe 
- monthly

Description: "First DebrisFrame kickoff meeting establishes project goals including case study processing, input
hydrograph development, and PyTopRun module integration. PR #1167 introduces initial hydrograph input functionality to
com1DFA for debris flow simulations."

---

In November, we held the first DebrisFrame - KickOff Meeting with the main project members from BOKU University, the
Austrian Avalanche and Torrent Service (WLV) and the Austrian Research Centre for Forests (BFW) in November. In summary,
we agreed on the general goals of the DebrisFrame project and the next steps. These are as follows:

- Processing of case studies for the GitHub repository
- Development of generic input hydrographs
- Definition of the right location for the input hydrograph
- Development of a generic topography for debris flows
- Evaluation of possible approaches to consider buildings and obstructions in the simulation domain
- Integration of module PyTopRun

Starting conditions

PR #1167 (https://github.com/OpenNHM/AvaFrame/pull/1167) introduced initial hydrograph input functionality to com1DFA
for debris flow simulations. Users can now provide a polygon defining the input area and a CSV table with timesteps,
thickness values, and optional velocity values in the Inputs/HYDR directory. Particles are initialized at defined time
steps within the polygon location with the specified thickness and initial velocity. This is an initial implementation
with further improvements planned - see DebrisFrame Issue #13 for ongoing development. It is also possible that the
process will be reworked…

Paula, Julian