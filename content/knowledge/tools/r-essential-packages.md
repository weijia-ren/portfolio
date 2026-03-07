---
title: "R — Essential Packages for Quantitative UXR"
date: 2025-05-01
draft: false
tags: ["R", "tools", "packages"]
---

My go-to R packages organized by task.

## Data Wrangling & Exploration

| Package | Use |
|---------|-----|
| `dplyr` | Data manipulation (filter, mutate, summarize) |
| `tidyr` | Reshaping data (pivot_longer, pivot_wider) |
| `readr` | Fast CSV/TSV reading |
| `janitor` | Clean column names, tabyl() for quick cross-tabs |
| `skimr` | Quick data summaries |

## Statistical Modeling

| Package | Use |
|---------|-----|
| `lme4` | Linear/generalized mixed-effects models |
| `brms` | Bayesian regression (Stan backend, formula syntax like lme4) |
| `survival` | Survival analysis (Kaplan-Meier, Cox PH) |
| `lavaan` | Structural equation modeling, CFA, path analysis |
| `psych` | Psychometrics, EFA, reliability analysis |
| `emmeans` | Estimated marginal means and contrasts |
| `effectsize` | Cohen's d, eta-squared, etc. |

## Causal Inference

| Package | Use |
|---------|-----|
| `MatchIt` | Propensity score matching |
| `did` | Difference-in-differences with staggered treatment |
| `rdrobust` | Regression discontinuity |
| `CausalImpact` | Bayesian structural time series (Google) |
| `grf` | Generalized random forests for CATE |

## Visualization

| Package | Use |
|---------|-----|
| `ggplot2` | Everything |
| `patchwork` | Combining multiple plots |
| `scales` | Axis formatting |
| `ggdist` | Uncertainty visualization |
| `gt` | Publication-quality tables |

## Survey Analysis

| Package | Use |
|---------|-----|
| `survey` | Complex survey designs (weights, strata) |
| `likert` | Likert scale visualization |
| `ltm` | Item response theory |

## Tips

- Use `renv` for reproducible package management
- Create an `.Rprofile` with your common library loads
- `tidymodels` is great for ML workflows but overkill for most UXR analysis
