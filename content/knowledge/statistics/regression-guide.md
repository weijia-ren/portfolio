---
title: "Regression — Practical Guide"
date: 2025-01-25
draft: false
tags: ["regression", "statistics", "modeling"]
---

When to use which regression and what to watch out for.

## Choosing the Right Model

| Outcome Type | Model | R function | Python |
|-------------|-------|------------|--------|
| Continuous | Linear regression | `lm()` | `statsmodels.OLS` |
| Binary (0/1) | Logistic regression | `glm(family=binomial)` | `LogisticRegression` |
| Count | Poisson regression | `glm(family=poisson)` | `statsmodels.Poisson` |
| Overdispersed count | Negative binomial | `MASS::glm.nb()` | `statsmodels.NegativeBinomial` |
| Ordinal | Ordinal logistic | `MASS::polr()` | `mord` |
| Time-to-event | Cox proportional hazards | `survival::coxph()` | `lifelines.CoxPH` |
| Nested/grouped data | Mixed-effects model | `lme4::lmer()` | `statsmodels.MixedLM` |

## Linear Regression Assumptions (CHECK THESE)

1. **Linearity** — residuals vs. fitted plot should show no pattern
2. **Independence** — observations are independent (not clustered, not time-series)
3. **Normality of residuals** — Q-Q plot, matters mainly for small samples
4. **Homoscedasticity** — constant variance of residuals (check residual plot)
5. **No multicollinearity** — VIF < 5 for all predictors (VIF > 10 is a problem)

## Interpreting Coefficients

### Linear Regression
- β = "a 1-unit increase in X is associated with a β-unit change in Y, holding other predictors constant"
- Standardized β: compare relative importance across predictors

### Logistic Regression
- β is a log-odds change — not directly interpretable
- **exp(β) = odds ratio** — this is what you report
- OR = 1.5 means "50% higher odds"
- For probabilities: use marginal effects or predicted probability plots

### Interaction Terms
- `X1 * X2`: the effect of X1 depends on the level of X2
- Always plot interactions — don't just report coefficients
- Center continuous variables before creating interactions

## Model Building Strategy

1. **Start with theory** — include predictors that make substantive sense
2. **Check bivariate relationships** first
3. **Build incrementally** — base model → add predictors → check improvement
4. **Compare models** — AIC (lower is better), likelihood ratio test, adjusted R²
5. **Don't overfit** — rule of thumb: ≥ 10-20 observations per predictor

## Diagnostics Checklist

- [ ] Residual vs. fitted plot (linearity + homoscedasticity)
- [ ] Q-Q plot of residuals (normality)
- [ ] VIF for all predictors (multicollinearity)
- [ ] Cook's distance (influential observations — investigate any > 1)
- [ ] For logistic: ROC curve + AUC, Hosmer-Lemeshow test
- [ ] For count models: check for overdispersion (variance >> mean → negative binomial)

## Common Mistakes

- Using stepwise selection (data-dredging — use theory-driven model building)
- Interpreting R² as "the model explains X% of the outcome" without caveats
- Including mediators as controls (blocks the causal path you're trying to measure)
- Not checking for non-linear relationships (try adding polynomial or spline terms)
- Reporting "no effect" when you had low power (absence of evidence ≠ evidence of absence)
