---
title: "Survey Weighting — When and How"
date: 2025-01-15
draft: false
tags: ["weighting", "statistics", "survey methodology"]
---

A practical guide to when and how to weight survey data.

## Why Weight?

Weighting corrects for differences between your sample and the target population. Three main reasons:

1. **Unequal selection probabilities** — some units were more likely to be sampled (design weights)
2. **Non-response** — certain groups responded at lower rates (non-response adjustment)
3. **Coverage gaps** — the sampling frame doesn't cover the full population (post-stratification)

## Types of Weights

### 1. Design Weights (Base Weights)
```
w_i = 1 / P(selection_i)
```
- Inverse of the probability of selection
- Always needed for complex survey designs
- For SRS: all weights are equal (N/n)

### 2. Non-Response Adjustment
- Model the probability of response using available covariates
- Adjust design weights: `w_adjusted = w_design / P(response)`
- Use logistic regression or response propensity modeling
- Variables: demographics, behavior, timing, device

### 3. Post-Stratification / Raking
- Adjust so weighted sample margins match known population margins
- **Post-stratification**: one variable at a time, exact cell matching
- **Raking (iterative proportional fitting)**: multiple variables simultaneously, matches marginals
- Common targets: age, gender, region, education, platform usage

### 4. Calibration Weights
- Generalization of raking — can match means and totals, not just proportions
- Methods: linear calibration, GREG (generalized regression estimator)
- More flexible but more complex

## Practical Steps

1. **Start with design weights** based on sampling design
2. **Adjust for non-response** using response propensity model
3. **Rake or post-stratify** to known population benchmarks
4. **Trim extreme weights** — cap at a reasonable range (common rule: weight < 5× median weight)
5. **Validate** — check weighted distributions against known benchmarks

## Weight Trimming

Extreme weights increase variance. Common approaches:

| Method | Rule |
|--------|------|
| **Cap at multiple of median** | Trim weights > 5× median weight |
| **Winsorization** | Cap at 1st/99th percentile |
| **Weight efficiency** | Target ≥ 70% weight efficiency |

Weight efficiency = `(sum(w))² / (n × sum(w²))` — 100% means equal weights.

## When NOT to Weight

- Descriptive/exploratory analysis where representativeness isn't the goal
- When the sample IS the population (census)
- When weights are so extreme they introduce more variance than they reduce bias
- When you don't have reliable population benchmarks to weight to

## Common Mistakes

- Weighting to a benchmark that's itself biased
- Not using weights in variance estimation (standard errors are wrong without them)
- Over-weighting: too many dimensions → extreme weights → high variance
- Forgetting to use weighted analyses in statistical software (R: `survey` package; Python: `statsmodels` WLS)

## Tools

| Language | Package | Notes |
|----------|---------|-------|
| R | `survey` | Gold standard for complex survey analysis |
| R | `anesrake` | Raking implementation |
| R | `autumn` | Calibration weighting |
| Python | `ipfn` | Iterative proportional fitting |
| Python | `statsmodels` | WLS, GEE with weights |
