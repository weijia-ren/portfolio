---
title: "Data-Driven Optimization of Video Placement in Search Results"
date: 2025-02-01
draft: false
tags: ["logistic regression", "interaction effects", "content strategy", "log-linked survey analysis", "intent segmentation"]
categories: ["Product Research"]
icon: "🎬"
weight: 5
---

## Context

The platform was pursuing a video-first strategy for search, but needed evidence on when, where, and how many videos to surface to improve — rather than degrade — perceived quality. Simply boosting video presence across all searches risked harming the experience for users who didn't want video results.

## Question

What is the relationship between video presence in search results and perceived usefulness, and how does this vary by relevance, ranking position, density, and search intent?

## Approach

Linked large-scale inline survey data (N=230,000+) with search log data to analyze the relationship between video presence and user-perceived usefulness:

- **Log-linked survey analysis**: Connected usefulness ratings to detailed session-level features including video count, ranking position, video density, and query intent classification
- **Logistic regression modeling**: Built models to disentangle the independent effect of video format from content relevance, controlling for confounders
- **Interaction effect analysis**: Tested whether video impact depended on the relevance context — specifically, whether video amplified or degraded perceived quality at different relevance levels
- **Intent-level mapping**: Analyzed video impact across 30+ search intent categories to identify where video helped and where it harmed

## Key Findings

1. **Relevance dominates format**: Relevance — not content format — was the primary driver of perceived usefulness, with format having a very weak independent effect. A relevant text result consistently outperformed an irrelevant video result
2. **Critical interaction effect**: Video presence amplified usefulness in high-relevance sessions but actively harmed it in low-relevance sessions — the same video could help or hurt depending on context
3. **Optimal density and position identified**: Determined the video density threshold beyond which usefulness declined, and identified the riskiest ranking position for video placement (where irrelevant video was most damaging)
4. **Intent-specific impact map**: Identified which search categories benefited from video (how-to, entertainment, events) and which were harmed by it (people search, navigational queries, factual lookups)

## Impact

- **Prevented a blanket video-boosting approach**: Without this evidence, the team would have increased video presence uniformly — degrading quality for a significant share of searches
- **Enabled intent-aware video ranking**: Findings led to a strategy of selectively surfacing video based on intent and relevance signals, rather than boosting video universally
- **Provided specific optimization parameters**: The optimal density and position findings gave the ranking team concrete engineering targets
- **Established an evidence template**: The log-linked survey methodology became the standard approach for evaluating any new content format in search results

## Methods & Tools

`Log-Linked Survey Analysis` · `Logistic Regression Modeling` · `Interaction Effect Analysis` · `Content Strategy Research` · `Intent-Based Segmentation` · `SQL` · `R` · `Python`

## What This Demonstrates

This project shows the ability to use large-scale data to answer nuanced product strategy questions — not just "does video help?" but "when, where, how much, and for whom?" The critical contribution was identifying the relevance × format interaction, which transformed the product recommendation from a binary yes/no to a context-dependent strategy. It required both statistical modeling sophistication and the communication skill to make interaction effects actionable for a product team.
