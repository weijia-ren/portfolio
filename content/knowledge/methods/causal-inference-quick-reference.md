---
title: "Causal Inference Methods — Quick Reference"
date: 2025-03-10
draft: false
tags: ["causal inference", "methods", "reference"]
---

A quick-reference guide for choosing the right causal inference method when a randomized experiment isn't possible.

## Decision Guide

| Method | Use when... | Key assumption |
|--------|-------------|---------------|
| **Randomized Experiment (RCT)** | You can randomly assign treatment | Random assignment eliminates confounders |
| **Difference-in-Differences (DiD)** | You have a treatment/control group with pre/post data | Parallel trends (groups would have trended similarly without treatment) |
| **Regression Discontinuity (RDD)** | Treatment assigned by a threshold (score, date, etc.) | Units just above/below threshold are comparable |
| **Instrumental Variables (IV)** | You have a variable that affects treatment but not outcome directly | Exclusion restriction holds |
| **Matching / Propensity Score** | You have observational data with rich covariates | No unobserved confounders (conditional ignorability) |
| **Interrupted Time Series** | You have a time series with a clear intervention point | No other events at the same time |
| **Synthetic Control** | One treated unit, multiple control units, pre/post data | Weighted controls can reproduce pre-treatment trend |

## Key Questions Before Choosing

1. **Can you randomize?** If yes, do it. Everything else is second-best.
2. **What does your data look like?** Panel data → DiD. Cross-section → matching. Time series → ITS.
3. **Is there a threshold?** → RDD.
4. **What's the biggest threat to validity?** Design around it.

## Common Mistakes

- Using matching without checking covariate balance
- Applying DiD without testing parallel trends
- Ignoring SUTVA (Stable Unit Treatment Value Assumption) in network settings
- Reporting only statistical significance without effect sizes
- Not doing sensitivity analysis for unmeasured confounding

## Resources

- Angrist & Pischke, *Mostly Harmless Econometrics*
- Cunningham, *Causal Inference: The Mixtape* (free online)
- Hernán & Robins, *Causal Inference: What If* (free online)
