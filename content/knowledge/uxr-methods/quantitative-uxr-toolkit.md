---
title: "Quantitative UXR — The Expanding Toolkit"
date: 2025-06-01
draft: false
tags: ["quantitative UXR", "methods", "analytics", "measurement"]
---

Quantitative UXR is evolving beyond surveys and A/B tests. Here's the full modern toolkit.

## The Quant UXR Stack

### Layer 1: Descriptive Analytics (What's happening?)
- **Behavioral log analysis** — funnels, flows, feature adoption curves
- **Segmentation** — clustering users by behavior, needs, or outcomes
- **Cohort analysis** — retention, adoption, and engagement over time
- **Journey mapping from data** — reconstructing user flows from event logs

### Layer 2: Measurement (How much? How well?)
- **Survey programs** — tracking satisfaction, usefulness, NPS, task success
- **In-product measurement** — inline surveys, experience sampling
- **Psychometric instruments** — validated scales for trust, effort, satisfaction
- **Metric design** — creating product metrics grounded in user outcomes

### Layer 3: Causal Inference (What caused it?)
- **Experimentation** — A/B testing, multivariate testing
- **Quasi-experiments** — DiD, RDD, ITS when randomization isn't possible
- **Mediation analysis** — what's the mechanism behind the effect?
- **Heterogeneous treatment effects** — who benefits most/least?

### Layer 4: Prediction & Modeling (What will happen?)
- **Churn/retention modeling** — predicting who will leave and why
- **Propensity scoring** — matching treated and control groups
- **Text analytics / NLP** — analyzing open-text feedback at scale
- **Latent variable modeling** — factor analysis, SEM, latent class analysis

## Emerging Quant UXR Methods

### Log-Linked Surveys
Connect survey responses to behavioral logs for the same users. Enables:
- Validating survey responses against behavior
- Understanding when stated preferences diverge from actions
- Building richer models that combine attitudinal and behavioral data

### Experience Sampling Method (ESM)
- Random in-context prompts asking about current experience
- Higher ecological validity than retrospective surveys
- Captures moment-to-moment experience, not just summary judgments

### Bayesian Analysis for UXR
- Better for small samples (common in UXR)
- Incorporates prior knowledge
- Produces probability statements ("there's a 95% probability the effect is between X and Y") instead of reject/fail-to-reject
- Practical tools: `brms` in R, PyMC in Python

### MaxDiff and Conjoint Analysis
- **MaxDiff**: Rank-order preferences without scale bias (best-worst scaling)
- **Conjoint**: Understand trade-offs between features/attributes
- Both force choices, reducing acquiescence and satisficing bias

## Key Metrics Every Quant UXR Should Know

| Metric | What it measures | Watch out for |
|--------|-----------------|---------------|
| **Task Success Rate** | Can users complete the task? | Binary — misses partial success |
| **Time on Task** | Efficiency | Longer isn't always worse (engagement) |
| **SUS (System Usability Scale)** | Overall usability | 10-item validated scale, score ranges 0–100 |
| **CSAT** | Satisfaction | Susceptible to ceiling effects |
| **NPS** | Loyalty/advocacy | Controversial validity, useful as a trend |
| **CES (Customer Effort Score)** | Ease of experience | Good predictor of churn |
| **UMUX-Lite** | Usability (2 items) | Ultra-short, validated against SUS |
