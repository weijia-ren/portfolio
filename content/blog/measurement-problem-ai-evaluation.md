---
title: "The Measurement Problem in AI Evaluation"
date: 2025-07-10
draft: false
tags: ["AI evaluation", "measurement", "psychometrics"]
categories: ["AI & Measurement"]
---

We're building increasingly powerful AI systems, but our methods for evaluating them haven't kept up. Most AI evaluation still relies on benchmark accuracy — the equivalent of grading a student only on multiple-choice tests.

<!--more-->

## What's missing

Benchmark accuracy tells you whether a model can produce correct outputs on a fixed set of problems. It doesn't tell you:

- **Reliability**: Does the model give consistent outputs for equivalent inputs?
- **Validity**: Does the benchmark actually measure what we care about in real use?
- **Fairness**: Does performance vary systematically across user groups?
- **User perception**: Do users trust, understand, and find value in the outputs?

These are measurement science problems, and the field of psychometrics has been solving them for decades.

## What psychometrics can teach AI evaluation

| Psychometric concept | AI evaluation equivalent |
|---------------------|------------------------|
| Test-retest reliability | Output consistency across equivalent prompts |
| Content validity | Does the benchmark represent real-world use cases? |
| Construct validity | Are we measuring the right capability? |
| Differential item functioning | Does the model perform differently for different user groups? |
| Item response theory | Difficulty-calibrated evaluation (not all test items are equal) |

## A practical framework

I've been thinking about a layered evaluation approach:

1. **Capability layer**: Can the system do the task? (benchmarks)
2. **Reliability layer**: Does it do the task consistently? (stability testing)
3. **Validity layer**: Does performance on the benchmark predict real-world value? (ecological validity)
4. **Human layer**: Do users trust, use, and benefit from it? (UXR)

Each layer builds on the previous one. Skipping to layer 4 without layer 1 is premature; stopping at layer 1 is insufficient.

## Why this matters for UX researchers

UX researchers are uniquely positioned to contribute to AI evaluation because we already:

- Know how to measure subjective constructs (satisfaction, trust, perceived quality)
- Understand validity and reliability in measurement
- Can design studies that connect system behavior to user outcomes
- Think about the full user experience, not just task accuracy

> The gap isn't in AI capability. It's in our ability to measure whether that capability translates to real human value.

---

*Related: [Evolving Engagement Metrics Through User Feedback Calibration]({{< ref "/case-studies/evolving-engagement-metrics" >}})*
