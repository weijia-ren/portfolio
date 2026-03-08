---
title: "Sampling Methods — Quick Reference"
date: 2025-01-10
draft: false
tags: ["sampling", "statistics", "survey design"]
---

A reference guide for choosing the right sampling approach.

## Probability Sampling Methods

| Method | How it works | Best for | Watch out for |
|--------|-------------|----------|---------------|
| **Simple Random** | Every unit has equal probability of selection | Homogeneous populations, baseline studies | Inefficient for rare subgroups |
| **Stratified** | Divide population into strata, sample within each | Ensuring subgroup representation, reducing variance | Need to know strata in advance |
| **Cluster** | Randomly select clusters, then sample within | Geographically dispersed populations, cost reduction | Higher variance than SRS (design effect) |
| **Systematic** | Select every k-th unit from a list | Operational simplicity | Risky if list has periodic patterns |
| **Multi-Stage** | Combine methods across stages | Large-scale national surveys, complex populations | Complex variance estimation |

## Non-Probability Sampling Methods

| Method | Use case | Limitation |
|--------|----------|-----------|
| **Convenience** | Pilot testing, early exploration | No generalizability claims |
| **Quota** | Ensuring demographic mix without a frame | Selection bias within quotas |
| **Snowball** | Hard-to-reach populations | Network bias |
| **Purposive** | Expert selection for qualitative research | Researcher bias |

## Key Formulas

### Sample Size for Proportions
```
n = (Z² × p × (1-p)) / E²
```
- Z = Z-score (1.96 for 95% CI)
- p = expected proportion (use 0.5 if unknown)
- E = margin of error

### Design Effect (DEFF)
```
DEFF = Var(complex design) / Var(SRS of same size)
```
- Effective sample size = n / DEFF
- Clustering increases DEFF; stratification decreases it
- Rule of thumb for cluster sampling: DEFF ≈ 1 + (m-1) × ICC, where m = cluster size, ICC = intraclass correlation

### Finite Population Correction
```
FPC = sqrt((N - n) / (N - 1))
```
Apply when sampling > 5% of the population.

## Practical Decision Guide

1. **Do you have a sampling frame?** No → non-probability methods only
2. **Do you need subgroup estimates?** Yes → stratified sampling
3. **Is the population geographically dispersed?** Yes → cluster or multi-stage
4. **Is the population homogeneous?** Yes → simple random is fine
5. **Budget constraints?** Cluster sampling reduces field costs but requires larger n

## Common Mistakes

- Treating a convenience sample as representative
- Ignoring the design effect when calculating confidence intervals from cluster samples
- Not accounting for non-response when planning sample size (inflate by expected non-response rate)
- Using unweighted estimates from a stratified design with disproportionate allocation
