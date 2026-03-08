---
title: "LLM Evaluation — A Researcher's Framework"
date: 2025-08-01
draft: false
tags: ["AI", "LLM", "evaluation", "measurement"]
---

Evaluating large language models requires thinking beyond benchmark accuracy. Here's a measurement-informed framework.

## The Evaluation Stack

### Level 1: Capability (Can it do the task?)

| What to test | Method | Metrics |
|---|---|---|
| Task accuracy | Benchmark datasets, held-out test sets | Accuracy, F1, BLEU, ROUGE |
| Instruction following | Structured prompts with expected outputs | Compliance rate, format accuracy |
| Reasoning | Chain-of-thought problems, logic puzzles | Correct reasoning steps, final answer accuracy |
| Knowledge | Fact-based Q&A, domain-specific tests | Factual accuracy, hallucination rate |

### Level 2: Reliability (Does it do it consistently?)

| What to test | Method | Metrics |
|---|---|---|
| Output stability | Same prompt multiple times | Semantic similarity across outputs |
| Paraphrase robustness | Equivalent prompts, different wording | Response consistency |
| Sensitivity to ordering | Reorder few-shot examples | Variance in output quality |
| Edge case behavior | Adversarial inputs, ambiguous prompts | Graceful degradation |

### Level 3: Validity (Does the benchmark reflect real-world value?)

| What to test | Method | Metrics |
|---|---|---|
| Ecological validity | Real user tasks vs. benchmark tasks | Correlation between benchmark and real performance |
| Construct validity | Multiple measures of the same capability | Convergent/discriminant validity |
| Distribution shift | Test on data unlike training data | Performance degradation |

### Level 4: Human Experience (Do users benefit?)

| What to test | Method | Metrics |
|---|---|---|
| Perceived quality | User ratings, preference studies | Satisfaction, usefulness, trust |
| Task completion | User studies with real tasks | Success rate, efficiency, error rate |
| Fairness | Performance across demographic groups | Disparity metrics, demographic parity |
| Safety | Red-teaming, adversarial testing | Harm rate, refusal accuracy |

## Key Concepts

### Hallucination Measurement
- **Intrinsic hallucination**: Output contradicts the source material
- **Extrinsic hallucination**: Output contains claims not in any source
- Measurement: fact-checking pipelines, human evaluation, model-based detection
- Key metric: hallucination rate by domain and task type

### Human Evaluation Design
- **Side-by-side comparison**: Show outputs from two models, ask which is better
- **Likert rating**: Rate individual outputs on quality dimensions
- **Task-based**: Give users a task, measure success with/without AI assistance
- **Key principle**: Define clear rubrics before evaluation begins
- **Inter-rater reliability**: Use Cohen's kappa or Krippendorff's alpha

### Evaluation Contamination
- Test data may be in the training set → inflated benchmark scores
- Mitigations: use held-out data, temporal splits, adversarial variants
- Always pair benchmarks with human evaluation on novel tasks

## Emerging Evaluation Approaches

### LLM-as-Judge
- Use a strong model to evaluate a weaker model's outputs
- Faster and cheaper than human evaluation
- Limitations: bias toward verbose/confident responses, model blind spots
- Best practice: calibrate against human judgments, use structured rubrics

### Arena-Style Evaluation
- Users interact with two anonymous models, choose which is better
- Produces Elo ratings (like chess)
- High ecological validity but expensive and slow
- Example: Chatbot Arena (LMSYS)

### Agentic Evaluation
- For AI agents: evaluate multi-step task completion, not just single outputs
- Metrics: task success rate, steps taken, error recovery, tool use accuracy
- New frontier: evaluating planning, self-correction, and tool chaining

## What UX Researchers Bring to AI Evaluation

UXR expertise directly applies:

| UXR Skill | AI Evaluation Application |
|---|---|
| Survey design | Human evaluation rubric development |
| Psychometrics | Scale development for perceived quality |
| Experimental design | A/B testing of model versions |
| Mixed methods | Combining benchmarks with human studies |
| Measurement validity | Questioning whether benchmarks measure what matters |
