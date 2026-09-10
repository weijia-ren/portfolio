---
title: "Regression Model Selection"
date: 2026-09-09
draft: false
layout: "poster"
posterPdf: "posters/interview-prep/regression-model-selection-visual-memory-posters.pdf"
tags: ["regression", "model selection", "interview prep", "quantitative research", "visual learning"]
categories: ["Interview prep series"]
summary: "A visual memory poster deck for choosing regression models based on outcome type, estimand, data structure, and interpretation scale."
---

## What this poster covers

- How to start model selection from the outcome, research goal, estimand, and data structure
- Linear regression for continuous outcomes and residual/functional-form diagnosis
- Logistic regression for binary outcomes, with interpretation on odds and probability scales
- Count models, including Poisson and Negative Binomial regression
- Ordinal, multinomial, survival, mixed, and multilevel models
- Functional form choices, interactions, confounding, regularization, and prediction vs. explanation
- Common interview traps and a practical model-selection flow

## Why it matters for Quant UXR

Regression is most useful when the model choice follows the product or research question. A good answer explains what outcome is being modeled, what estimand matters, how dependence or clustering enters the data, and how the result should be communicated to stakeholders.

## 30-second interview framing

I choose a regression model by starting with the outcome type and the estimand, not by defaulting to a familiar method. For a continuous outcome, linear regression may be appropriate if the conditional mean and residual structure are reasonable. For binary outcomes, logistic regression models log-odds, but I usually translate results into predicted probabilities or marginal effects. For counts, ordinal outcomes, survival data, or clustered observations, I choose a model family that matches the data-generating process and then check assumptions, functional form, and interpretation scale.

## Common traps this poster helps prevent

- Choosing a model based only on software defaults
- Treating odds ratios as probability differences
- Using Poisson regression without checking overdispersion or exposure time
- Ignoring repeated measures, clustering, or nested data structures
- Optimizing prediction accuracy when the real question is explanatory or causal
- Reporting coefficients without translating them into stakeholder-relevant quantities
