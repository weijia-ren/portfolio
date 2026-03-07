---
title: "Impact of Rich Content Formats on Search Experience"
date: 2025-02-01
draft: false
tags: ["mixed methods", "causal analysis", "content strategy", "user experience"]
categories: ["Product Research"]
icon: "🎬"
weight: 3
---

## Context

A search product team was considering increasing the presence of rich content formats (particularly video) in search results. The hypothesis was that richer content would improve engagement and user satisfaction. However, there was no evidence about *how* users actually experienced these richer results — whether they were helpful, distracting, or fundamentally changed how people evaluated search quality.

Simply measuring engagement lift wouldn't be enough. Users might click on video results out of novelty or visual salience without actually finding them useful for their search task.

## Question

How does the presence of rich content formats (video) in search results affect the overall search experience — and does increased engagement translate to genuine user value?

## Approach

### Behavioral Analysis

- Analyzed behavioral differences between search sessions with and without video results present
- Compared engagement patterns: click-through rate, dwell time, return-to-results rate, and session-level task completion
- Controlled for query type, user segment, and content relevance to isolate the format effect

### User Perception Study

- Designed a controlled study where users evaluated search result pages with varying levels of video presence
- Measured perceived relevance, helpfulness, visual overwhelm, and trust
- Used conjoint-style design to separate the effect of *content format* from *content quality*

### Integration

- Cross-referenced behavioral signals with perception data to identify alignment and gaps
- Built a framework distinguishing "engagement driven by value" from "engagement driven by visual salience"

## Key Findings

1. **Engagement ≠ satisfaction**: Video results increased click-through by 18%, but user-reported helpfulness showed no significant improvement — users were drawn to video visually but didn't consistently find it more useful
2. **Context dependence**: Video presence improved experience for certain query types (how-to, experiential) but degraded it for others (factual, navigational) where users wanted quick answers
3. **Cognitive load trade-off**: Above a threshold of video density, users reported feeling overwhelmed and had lower overall satisfaction with the results page, even while individual video clicks increased
4. **The "displacement effect"**: When video results displaced text results, users who needed text-based answers took longer to complete their task — the richer format helped some users at the cost of others

## Impact

- **Nuanced product strategy**: Instead of a blanket increase in video presence, the team adopted an intent-aware approach — showing video results selectively based on query type
- **New evaluation framework**: Created a "value vs. salience" diagnostic that the team now uses when evaluating any new content format
- **Prevented a false positive**: Without the perception study, the team would have scaled video presence based on engagement lift alone — which would have degraded experience for a significant user segment
- **Cross-functional influence**: Findings were shared with content ranking and content creation teams, influencing both how results were ranked and what content was prioritized

## Methods & Tools

`Quasi-Experimental Design` · `Behavioral Log Analysis` · `Controlled Perception Study` · `Conjoint-Style Design` · `Mixed-Methods Integration` · `SQL` · `R` · `Python`

## What This Demonstrates

This project shows the value of going beyond surface metrics to understand *why* users behave the way they do. It required integrating behavioral data with perception research, designing studies that could separate confounded factors, and communicating nuanced findings (not just "it works" or "it doesn't") to a product team eager for a simple answer.
