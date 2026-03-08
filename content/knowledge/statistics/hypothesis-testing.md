---
title: "Hypothesis Testing — Decision Framework"
date: 2025-01-20
draft: false
tags: ["hypothesis testing", "statistics", "p-values", "effect sizes"]
---

A practical framework for statistical testing that goes beyond p-values.

## The Testing Decision Framework

Before running any test, answer these:

1. **What's the research question?** (not "is there a difference?" but "how big is the difference and does it matter?")
2. **What's the outcome type?** (continuous, binary, count, ordinal)
3. **How many groups?** (1, 2, 3+)
4. **Are observations independent or paired?**
5. **What's the sample size?** (determines parametric vs. non-parametric choice)

## Test Selection Guide

### Comparing Means

| Scenario | Parametric | Non-Parametric |
|----------|-----------|----------------|
| 1 sample vs. known value | One-sample t-test | Wilcoxon signed-rank |
| 2 independent groups | Independent t-test | Mann-Whitney U |
| 2 paired/matched groups | Paired t-test | Wilcoxon signed-rank |
| 3+ independent groups | One-way ANOVA | Kruskal-Wallis |
| 3+ groups, repeated measures | Repeated measures ANOVA | Friedman test |

### Comparing Proportions

| Scenario | Test |
|----------|------|
| 1 proportion vs. known value | Binomial test / Z-test for proportions |
| 2 independent proportions | Chi-square / Fisher's exact |
| 2+ groups × 2+ categories | Chi-square test of independence |
| Paired proportions | McNemar's test |

### Relationships

| Scenario | Method |
|----------|--------|
| 2 continuous variables | Pearson r (linear) / Spearman ρ (monotonic) |
| Outcome ~ multiple predictors | Linear regression / logistic regression |
| Ordinal outcome | Ordinal logistic regression |
| Count outcome | Poisson / negative binomial regression |

## Beyond P-Values: What to Always Report

| Metric | What it tells you | Why it matters |
|--------|------------------|---------------|
| **Effect size** | Magnitude of the difference | P-value tells you "is it real?"; effect size tells you "is it meaningful?" |
| **Confidence interval** | Range of plausible values | More informative than a point estimate + p-value |
| **Power** | Probability of detecting a real effect | Low power means negative results are inconclusive |

### Common Effect Size Benchmarks

| Measure | Small | Medium | Large |
|---------|-------|--------|-------|
| Cohen's d (means) | 0.2 | 0.5 | 0.8 |
| Pearson r (correlation) | 0.1 | 0.3 | 0.5 |
| η² (ANOVA) | 0.01 | 0.06 | 0.14 |
| Odds ratio | 1.5 | 2.5 | 4.0 |

## Multiple Comparisons

When running multiple tests, adjust for inflated false positive rates:

| Method | When to use | How |
|--------|------------|-----|
| **Bonferroni** | Few tests, need strict control | α / k |
| **Holm-Bonferroni** | Few tests, less conservative | Step-down procedure |
| **Benjamini-Hochberg** | Many tests, control FDR | Rank-based adjustment |
| **Tukey's HSD** | All pairwise comparisons after ANOVA | Family-wise error rate |

## Practical Rules

- **N < 30 per group**: Consider non-parametric tests or bootstrap
- **Skewed data**: Log-transform, use non-parametric tests, or use robust methods
- **Unequal variances**: Use Welch's t-test (not Student's) — just default to Welch
- **Large N**: Everything will be "significant" — focus on effect sizes
- **Pre-register**: Decide your analysis plan before looking at data
