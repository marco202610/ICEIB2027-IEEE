# AIOT-DIC3 — AI Fitness Coach

Research project exploring smartphone-based outdoor activity tracking and GIS point-of-interest (POI) interaction. The repository currently contains an IEEE conference manuscript and supporting research documents; it is not the deployed mobile application.

## Current research focus

The broader A–F concept proposes an AI-assisted fitness workflow that coordinates phone sensing, GIS route and POI information, food queries through MCP, and consent-based data management. The current manuscript narrows the first research phase to smartphone-sensed outdoor trajectories, distance and speed estimates, GIS/POI interaction, and a plan for evaluating accuracy and resource use.

The intended workflow is:

1. A user describes an outdoor activity goal through a mobile web interface.
2. An AI avatar coordinates GIS queries for candidate routes and nearby POIs; the user reviews and confirms a route.
3. The phone collects permitted location and available motion data. Quality checks mark missing or unreliable intervals before activity estimates are shown.
4. Food MCP queries and dietary records are a separate, user-confirmed workflow.
5. With consent, activity data are intended to be encrypted for cloud storage. Digest anchoring requires separate consent; raw personal data are not intended to be placed on-chain.

These are proposed system capabilities, not claims that the complete workflow is implemented or validated.

## Scope and current status

- The paper uses the IEEEtran conference format. The author details remain a placeholder until confirmed.
- Phase one does not measure heart rate or infer cardiac workload from phone movement. Those topics require a separate method and validation phase.
- Real blockchain writes are disabled in the documented prototype. GPS integration, production deployment, and the complete coaching workflow have not been verified end to end.
- No complete experimental results for trajectory accuracy, GIS interaction, battery use, food MCP, or exercise outcomes are reported. The paper describes a planned evaluation.
- A related development record reports 56 local and simulated tests. These results were not independently rerun for this manuscript and do not validate GPS, GIS, real-device sensing, real blockchain transactions, or the integrated workflow.

## Repository map

- `main.tex` — IEEEtran conference root document and title/author block.
- `sections/` — abstract, introduction, related work, proposed scheme, evaluation plan, and conclusion.
- `tables/comparison.tex` — planned evaluation measures; it contains no experimental results.
- `references.bib` — bibliography used by the manuscript.
- `docs/A_to_F.md` — concise A–F research concept and motivation.
- `docs/A2Z.md` — expanded proposal, system flow, evaluation plan, and limitations.
- `docs/blockchain-development.md` — source-project notes for the related data-management prototype; not evidence that the full fitness workflow has been validated.
- `docs/AIOT-DIC3.jpg` — original concept illustration.

## Build the manuscript

In Overleaf, set `main.tex` as the root document and use pdfLaTeX. For a local build, install a TeX distribution with IEEEtran and the packages used in `main.tex`, then run:

```bash
latexmk -pdf main.tex
```

Confirm the final conference-specific submission requirements with the event organizers; the IEEEtran conference class alone does not establish every venue requirement.

## Research and evidence notes

The 2025 Taiwan exercise-participation survey cited in the manuscript is background motivation only; it does not establish that this system improves exercise adherence. Distance, speed, cadence, energy expenditure, and POI accessibility must be evaluated against appropriate references. A data digest can check consistency with a trusted reference, but it cannot prove that the original sensor measurements were true.
