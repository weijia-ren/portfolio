---
title: "Diagnosing Root Causes of Search Dissatisfaction"
date: 2025-04-01
draft: false
tags: ["root cause analysis", "user segmentation", "expectation mapping", "mixed methods", "quality framework"]
categories: ["Product Research"]
icon: "🔬"
weight: 3
---

## Context

Tracking surveys measured whether searches were useful, but the team needed to understand *why* results failed — what specific pain points drove dissatisfaction, and how quality expectations varied by search context. A single quality score couldn't tell the team where to focus product improvements.

## Question

What are the distinct reasons search results fail for users, and do different search motivations require fundamentally different quality attributes?

## Approach

Designed a detailed quality survey with layered follow-up questions probing the reasons behind useful and unuseful ratings:

- **Layered follow-up design**: After rating usefulness, users answered context-specific follow-up questions about *why* — including evaluation of individual search results, not just the overall page
- **Motivation-based segmentation**: Used hierarchical clustering to segment users by search motivation (building on the motivation taxonomy from prior research)
- **Expectation mapping**: Mapped distinct quality expectations per motivation segment to identify what "good" looks like for different types of searches
- **Triangulation with behavioral data**: Cross-referenced stated dissatisfaction reasons with behavioral signals (dwell time, scroll depth, reformulation) to separate real quality problems from measurement artifacts

## Key Findings

1. **Quality expectations are motivation-dependent**: Different search types demanded fundamentally different result attributes — high precision for people searches, variety and freshness for discovery searches, exact-match accuracy for refinding
2. **True problems vs. measurement problems**: Distinguished between scenarios where both satisfaction and engagement were low (true quality problem requiring product fixes) versus scenarios where satisfaction was high but engagement was low (measurement problem requiring metric improvement) — a critical distinction for resource allocation
3. **Intent-specific quality gaps**: Identified specific intents where quality was systematically weak, enabling targeted optimization rather than one-size-fits-all approaches
4. **Actionable pain point categories**: Top failure reasons mapped to concrete product levers: relevance model tuning, content type diversification, freshness signals, and personalization improvements

## Impact

- **Shifted from global to targeted optimization**: The motivation-based quality framework moved the team from optimizing a single quality score to addressing intent-specific gaps
- **Clarified the metric vs. product investment question**: By distinguishing true quality problems from measurement problems, helped the team allocate resources between "fix the product" and "fix the metric"
- **Created a reusable diagnostic methodology**: The layered survey approach became the standard template for investigating quality drops
- **Directly informed the product roadmap**: Intent-specific quality gaps were prioritized as distinct workstreams

## Methods & Tools

`Survey-Based Root Cause Analysis` · `User Segmentation` · `Expectation Mapping` · `Mixed-Methods Triangulation` · `Quality Framework Development` · `Hierarchical Clustering` · `SQL` · `R`

## What This Demonstrates

This project shows the ability to move from "what's the score?" to "what's actually broken and for whom?" The key intellectual contribution — distinguishing true quality problems from measurement problems — required thinking simultaneously about product quality and metric design. It demonstrates how rigorous qualitative-quantitative integration can produce frameworks that change how a team thinks about their problem.
