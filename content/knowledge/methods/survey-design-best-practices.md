---
title: "Survey Design — Best Practices"
date: 2025-04-05
draft: false
tags: ["survey design", "methods", "UXR"]
---

Practical notes on designing surveys that produce reliable, valid data.

## Question Writing Rules

1. **One concept per question** — never "double-barreled" questions
2. **Avoid leading language** — "How much do you enjoy..." assumes enjoyment
3. **Concrete > abstract** — "In the past 7 days, how often..." beats "How often do you usually..."
4. **Exhaustive and mutually exclusive** response options
5. **Include "Not applicable" / "I don't know"** when relevant — forced responses create noise

## Scale Design

### Likert Scales
- 5-point for simple agreement: Strongly disagree → Strongly agree
- 7-point for finer discrimination (research shows diminishing returns beyond 7)
- **Always label all points**, not just endpoints
- Consider unipolar (Not at all → Extremely) vs. bipolar (Strongly disagree → Strongly agree)

### Frequency Scales
- Use concrete anchors: "Never / Once / 2-3 times / 4+ times" > "Never / Rarely / Sometimes / Often"
- Match the time frame to actual behavior patterns

## Structure & Flow

1. Start with easy, engaging questions (not demographics)
2. Group by topic
3. Put sensitive questions later (after rapport is built)
4. Demographics at the end
5. **Target < 10 minutes** — completion rates drop sharply after that

## Sample Size Planning

| Analysis | Minimum N (rough guide) |
|----------|------------------------|
| Descriptive stats | 100-200 |
| Group comparisons (2 groups) | 200-400 |
| Factor analysis | 300+ (or 5-10x number of items) |
| Regression with 5+ predictors | 200+ |
| Segmentation / clustering | 500+ |

## Bias Checklist

- [ ] Acquiescence bias — mix positively and negatively worded items
- [ ] Social desirability — use indirect questions for sensitive topics
- [ ] Order effects — randomize question order within blocks
- [ ] Satisficing — include attention checks
- [ ] Self-selection — track and report response rates
