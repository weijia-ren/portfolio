---
title: "Technical Interview — Statistics & Methods"
date: 2025-04-01
draft: false
tags: ["interview", "technical", "statistics", "methods"]
---

Common technical questions in quantitative UXR and data science interviews.

## Experimentation & A/B Testing

**Q: How do you determine sample size for an A/B test?**
- Power analysis: need effect size (MDE), significance level (α), power (1-β), baseline rate
- Formula depends on metric type (proportion vs. continuous)
- Key: the smaller the effect you want to detect, the larger the sample needed
- Mention practical significance vs. statistical significance

**Q: Your A/B test shows a significant p-value but tiny effect size. What do you do?**
- Statistical significance ≠ practical significance
- With large N, even trivial effects are "significant"
- Focus on effect size and confidence interval
- Ask: "Is this effect large enough to matter for the business?"

**Q: How do you handle multiple comparisons?**
- Bonferroni, Holm, Benjamini-Hochberg (FDR)
- Pre-registration of primary metrics
- Distinguish exploratory vs. confirmatory analyses

**Q: What's the difference between Type I and Type II error? Which is worse?**
- Type I: false positive (α) — you think there's an effect but there isn't
- Type II: false negative (β) — you miss a real effect
- Which is worse depends on context (launching a bad feature vs. missing a good one)

## Survey Methodology

**Q: How do you handle non-response bias?**
- Compare respondents vs. non-respondents on observable characteristics
- Use weighting (post-stratification, raking) to adjust
- Report response rate and discuss potential bias direction
- Consider non-response follow-up for critical studies

**Q: What's the difference between reliability and validity?**
- Reliability: consistency of measurement (test-retest, internal consistency)
- Validity: accuracy of measurement (does it measure what it claims to?)
- A measure can be reliable but not valid (consistently wrong)
- A measure cannot be valid without being reliable

**Q: How do you decide between a 5-point and 7-point scale?**
- 5-point: simpler, lower cognitive load, good for general populations
- 7-point: more discrimination, better for research contexts
- Evidence shows diminishing returns beyond 7 points
- Key: label ALL scale points, not just endpoints

## Causal Inference

**Q: When can't you run an A/B test? What do you do instead?**
- Can't randomize: ethical concerns, technical constraints, policy changes
- Alternatives: DiD, RDD, matching, ITS, synthetic control
- Key: articulate the assumptions each method requires

**Q: Explain difference-in-differences to a non-technical person.**
- "We compare the change over time in the treated group to the change over time in a similar untreated group. If the treated group changed MORE than we'd expect based on the control group's trend, we attribute the extra change to the treatment."
- Key assumption: parallel trends — both groups would have changed similarly without the intervention

## Regression & Modeling

**Q: When would you use logistic vs. linear regression?**
- Linear: continuous outcome (satisfaction score, time on task)
- Logistic: binary outcome (converted yes/no, clicked yes/no)
- Key: logistic coefficients are log-odds; report odds ratios for interpretability

**Q: How do you check for multicollinearity?**
- VIF (Variance Inflation Factor) — flag if > 5, worried if > 10
- Correlation matrix for obvious pairs
- Solutions: drop one variable, combine into composite, use regularization (ridge/lasso)

**Q: What's an interaction effect and when do you test for one?**
- "The effect of X on Y depends on the level of Z"
- Test when theory suggests moderation (e.g., feature impact differs by user segment)
- Always visualize interactions — don't just report coefficients
- Example from my work: video format × relevance interaction in search results

## General Tips

- **Think out loud** — interviewers want to see your reasoning process
- **Start with the simplest approach** — then add complexity as needed
- **Connect to real work** — "In a recent project, I used this approach when..."
- **It's okay to say "I don't know"** — then reason through it
- **Ask clarifying questions** — "What's the sample size? Is this an observational study or an experiment?"
