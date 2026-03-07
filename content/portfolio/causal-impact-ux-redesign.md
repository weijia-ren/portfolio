---
title: "Causal Impact of a UX Redesign on Conversion"
date: 2024-11-01
draft: false
tags: ["causal inference", "A/B testing", "experiment design", "conversion"]
categories: ["Quantitative UXR"]
icon: "🔬"
weight: 3
---

## Context

<!-- Replace with your actual project -->

A major UX redesign was launched for a key conversion flow. The team ran a standard A/B test but faced challenges: the redesign affected multiple steps in the funnel, there were carry-over effects from the old design, and different user segments responded differently.

## Question

What is the true causal effect of the redesign on conversion, and how does the effect vary across user segments and funnel stages?

## Method

- Designed a stratified experiment with pre-registered hypotheses and power analysis
- Used difference-in-differences (DiD) to account for pre-existing trends
- Applied heterogeneous treatment effect analysis (CATE) to identify segment-specific responses
- Built a funnel decomposition model to isolate where in the flow the redesign had the most impact
- Conducted sensitivity analysis for multiple comparisons and novelty effects

## Key Findings

1. **Overall lift**: The redesign increased end-to-end conversion by 8.2% (95% CI: [5.1%, 11.4%])
2. **Funnel decomposition**: 70% of the lift came from the first step (simplified form), while the final step (confirmation) showed no change
3. **Segment heterogeneity**: Power users showed minimal lift (+2%), while new users showed +14% — the redesign primarily removed barriers for less experienced users
4. **Novelty effect**: After controlling for novelty, the sustained effect was 6.8% — still significant and durable

## Impact

- Provided rigorous evidence to fully ship the redesign (previously debated)
- Identified that further optimization should focus on the confirmation step (untapped potential)
- Established a template for how the team evaluates major UX changes going forward

## Methods Used

`A/B Testing` · `Difference-in-Differences` · `Heterogeneous Treatment Effects` · `Power Analysis` · `Python` · `SQL`
