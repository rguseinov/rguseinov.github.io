---
layout: archive
title: "Software"
permalink: /software/
author_profile: true
---

<div style="display:flex; gap:24px; align-items:flex-start; flex-wrap:wrap; margin-bottom:1.5em;">
  <img src="/images/publications/guseinov2026contentiousr.webp" alt="contentiousR logo" style="width:160px; flex-shrink:0;">
  <div style="flex:1; min-width:240px;">
    <h2 style="margin-top:0;">contentiousR</h2>
    <p>An R package that provides tools and datasets for contentious politics and civil conflict research. It offers a flexible workflow for building state panels and enriching them with socioeconomic, political, and conflict indicators, using either the Correlates of War (COW) or Gleditsch-Ward (GW) country coding schemes.</p>
    <div style="display:flex; gap:8px; flex-wrap:wrap;">
      <a href="https://rguseinov.github.io/contentiousR/" target="_blank" style="font-size:0.85em; padding:4px 12px; background:#4a8; color:#fff; border-radius:4px; text-decoration:none;">🌐 Website</a>
      <a href="https://github.com/rguseinov/contentiousR" target="_blank" style="font-size:0.85em; padding:4px 12px; background:#333; color:#fff; border-radius:4px; text-decoration:none;">💻 GitHub</a>
      <a href="https://doi.org/10.2139/ssrn.7506799" target="_blank" style="font-size:0.85em; padding:4px 12px; background:#555; color:#fff; border-radius:4px; text-decoration:none;">📄 Paper (SSRN)</a>
    </div>
  </div>
</div>

### Installation

```r
# install.packages("remotes")
remotes::install_github("rguseinov/contentiousR")
```

### Example

```r
library(contentiousR)

panel <- build_states_panel(start_year = 1990, end_year = 2015, coding_system = "cow") |>
  add_gdp() |>
  add_vdem(vars = c("v2x_polyarchy", "v2x_libdem")) |>
  add_conflict(dataset = "navco2.1") |>
  add_leader_data(dataset = "archigos")
```

### Citation

Guseinov, R. (2026). contentiousR: An R package for contentious politics and civil conflict research [Preprint]. SSRN. [https://doi.org/10.2139/ssrn.7506799](https://doi.org/10.2139/ssrn.7506799)
