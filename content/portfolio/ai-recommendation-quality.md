---
title: "Evaluating AI Recommendation Quality Through User Perception Studies"
date: 2025-03-01
draft: false
tags: ["AI evaluation", "survey design", "psychometrics", "mixed methods"]
categories: ["AI & Decision Systems"]
icon: "🤖"
weight: 2
---

## Context

<!-- Replace with your actual project -->

An AI-powered recommendation system was optimized for engagement metrics, but the team had no systematic way to assess whether users actually found the recommendations *useful* or *trustworthy*. High click rates could mask low satisfaction.

## Question

How do users perceive AI recommendation quality, and can we build a scalable measurement instrument that captures dimensions beyond engagement?

## Method

- Conducted qualitative interviews (N=20) to identify dimensions of perceived recommendation quality
- Developed a multi-item survey instrument measuring: **Relevance**, **Novelty**, **Trustworthiness**, and **Control**
- Ran psychometric validation: exploratory factor analysis (EFA), confirmatory factor analysis (CFA), reliability analysis
- Deployed the validated scale in a large-scale survey (N=3,000) across user segments
- Correlated perception scores with behavioral log data to identify gaps between behavior and satisfaction

## Key Findings

1. **Relevance and trust are distinct**: Users can find recommendations relevant but not trustworthy — and trust predicts long-term engagement better
2. **The novelty paradox**: Users say they want novel recommendations but behaviorally prefer familiar ones — the gap is largest for new users
3. **Control as a moderator**: Users with high perceived control over the algorithm rate recommendations 23% higher on trust

## Impact

- Created a reusable "Recommendation Quality Index" (RQI) adopted as a quarterly tracking metric
- Informed the team's decision to add user control features (filters, "not interested" feedback)
- Provided evidence that optimizing for click-through alone was masking declining user trust

## Methods Used

`Psychometric Scale Development` · `Factor Analysis (EFA/CFA)` · `Survey Design` · `Mixed Methods` · `R` · `Python`
