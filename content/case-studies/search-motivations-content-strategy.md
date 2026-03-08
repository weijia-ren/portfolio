---
title: "Understanding Search Motivations to Inform Content Strategy"
date: 2025-05-01
draft: false
tags: ["JTBD", "clustering analysis", "cross-market research", "content strategy", "search intent"]
categories: ["Strategic Research"]
icon: "🔎"
weight: 2
---

## Context

A platform's search team was pursuing a content-first product strategy but lacked a clear understanding of *why* users search — what motivations drive searches and what content formats users expect for different types of queries. Without this understanding, content ranking and surfacing decisions were based on assumed user intent rather than measured motivation.

## Question

What are the distinct motivations that drive users to search on the platform, and how do content format expectations differ across motivation types, demographics, and global markets?

## Approach

Designed and fielded a large-scale on-platform survey tied to users' actual search queries across multiple global markets (N=15,000+):

- **Real-query linkage**: Each survey response was linked to the specific query the user had just performed, grounding motivations in actual behavior rather than hypothetical scenarios
- **Hierarchical clustering**: Applied clustering analysis to identify distinct search motivation segments from the survey data
- **Content format mapping**: Mapped each motivation cluster to preferred content formats (video, text, images, profiles) and analyzed how preferences varied by age group and region
- **Intent classifier audit**: Compared discovered motivation segments against the platform's existing search intent classifier to identify coverage gaps

## Key Findings

1. **Four distinct motivation clusters emerged**: Interpersonal connection (finding people/groups), information-seeking (news, answers), discovery/entertainment (browsing, exploring), and refinding (retrieving previously seen content)
2. **Refinding was under-recognized**: Retrieving previously seen content was a top motivation across all markets — but was severely under-represented in the platform's search intent classifier, surfacing a major improvement opportunity
3. **Format expectations varied by motivation**: Entertainment-driven searches expected video content; information-seeking searches expected text and articles; people-finding searches expected profiles — validating a motivation-aware content ranking approach
4. **Cross-market and demographic patterns**: Younger users skewed toward discovery/entertainment motivations while older users skewed toward refinding and interpersonal connection, with meaningful regional variations

## Impact

- **Informed content ranking strategy**: Motivation-to-format mappings directly guided how search results were ranked and presented for different query types
- **Identified a classifier gap**: The discovery that "refinding" was under-classified led to improvements in the search intent classification system
- **Enabled segmented quality tracking**: Motivation segments became a standard analysis dimension for ongoing quality measurement
- **Shaped cross-market product decisions**: Regional motivation differences informed market-specific search optimization priorities

## Methods & Tools

`On-Platform Survey Design` · `Hierarchical Clustering Analysis` · `Jobs-to-Be-Done Framework` · `Cross-Market Research` · `Search Intent Taxonomy Development` · `SQL` · `R` · `Python`

## What This Demonstrates

This project shows the ability to connect user motivation research directly to product architecture — specifically, to an intent classification system. It goes beyond surface-level persona work by grounding motivation segments in actual search behavior and mapping them to concrete product implications (content format ranking, classifier improvement, market-specific strategy).
