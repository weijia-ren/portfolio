---
title: "Why Most A/B Tests Answer the Wrong Question"
date: 2025-09-15
draft: false
tags: ["experimentation", "A/B testing", "methodology"]
categories: ["Methods"]
---

Most A/B tests are designed to answer "Is version B better than version A?" But that's rarely the question that matters most for product decisions.

<!--more-->

## The real questions

What product teams actually need to know:

1. **For whom** is B better? (heterogeneous effects)
2. **Why** is B better? (mechanism, not just outcome)
3. **How much better** — is the effect practically meaningful? (effect size, not just significance)
4. **How durable** is the effect? (novelty vs. sustained impact)

A p-value alone answers none of these.

## The "average treatment effect" trap

Standard A/B tests report an Average Treatment Effect (ATE). But averages hide critical variation:

- A redesign might hurt power users (-5%) while helping new users (+15%)
- The ATE shows +5%, everyone celebrates, and the most valuable segment churns

This is why heterogeneous treatment effect analysis matters. Tools like causal forests or simple interaction models can reveal segment-level effects that the ATE obscures.

## What I recommend instead

Design your experiments to answer layered questions:

| Layer | Question | Method |
|-------|----------|--------|
| 1 | Is there an overall effect? | Standard ATE |
| 2 | Who benefits most/least? | CATE / subgroup analysis |
| 3 | What drives the effect? | Mediation analysis |
| 4 | Is it durable? | Time-series decomposition |

This takes more planning upfront but prevents the "we shipped it and engagement dropped three months later" problem.

## Key takeaway

> An experiment that only tells you "B won" is a wasted experiment. The goal is to understand *why* and *for whom*, so you can make better decisions next time too.

---

*Related: [Data-Driven Optimization of Video Placement](/case-studies/video-placement-optimization/)*
