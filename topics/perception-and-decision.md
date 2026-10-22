# Perception and decision

[Collection overview](../README.md) · [All topics](README.md) · [Learn](../learn/README.md) · [Methods](../methods/README.md) · [Resource library](../resources/README.md)

This topic links sensory evidence to choices, confidence, and response time. Computational models can formalize how evidence accumulates or how actions are selected, but the same behavior can often be explained by multiple processes.

## Questions to bring

- Is the target perceptual sensitivity, choice, response time, confidence, or their joint pattern?
- How do noise, bias, urgency, reward, and prior experience enter the model?
- Does a model describe a decision variable or identify a neural implementation?
- Which task condition gives rival models different predictions?

## Prerequisites

Review probability, regression, likelihoods, and basic stochastic processes. Understand trial structure, response-time distributions, and the difference between accuracy and calibration. Coding in Python is useful for fitting and simulating behavioral models.

## A short start route

1. Plot choice and response-time distributions by condition before fitting.
2. Fit a simple baseline, such as logistic regression, alongside a mechanistic candidate.
3. Check parameter recovery and posterior/predictive behavior on simulated data.
4. Compare models on held-out trials or conditions and inspect systematic residuals.

## Research threads

### Evidence accumulation and choice dynamics

Sequential sampling models explain choices and response times through noisy evidence accumulation, boundaries, and non-decision components. [Computational Models of Decision Making](../resources/papers-and-reviews.md#computational-models-of-decision-making) introduces these model families; [PyDDM](../resources/software.md#pyddm) and [HSSM](../resources/software.md#hssm) provide tools for building and fitting decision models. Good fit is not unique evidence for accumulation; compare plausible alternatives and parameter identifiability.

### Confidence and hierarchical choice

Confidence can depend on accumulated evidence, post-decision processing, or metacognitive access. The broad [Computational Cognitive Neuroscience](../resources/books.md#computational-cognitive-neuroscience) text and [Edinburgh computational cognitive neuroscience course](../resources/courses-and-lectures.md#computational-cognitive-neuroscience-edinburgh) provide wider cognitive-model context. Fit joint choice and confidence patterns where possible rather than adding verbal interpretations after fitting choices alone.

### Behavior tasks and model-based data

Task structure shapes the inference problem. [IBL decision-making behavior data](../resources/datasets-and-benchmarks.md#ibl-decision-making-behavior-data) offers trial-level behavior for studying decision variables; [NeuroGym](../resources/software.md#neurogym) provides task environments for model and agent comparisons. A simulated task simplifies the experimental and behavioral context, so identify which features the environment omits.

## Small project: compare accumulation with a baseline

Generate synthetic two-choice trials under a drift-diffusion model, then fit it and a logistic choice model to the same training set. Deliver simulation code, parameter recovery plots, held-out choice and response-time predictions, and a short account of when model parameters become hard to distinguish. Evaluate recovery across trial counts and noise levels, and include posterior predictive checks. This suggested exercise has not been run by the repository; conclusions apply to the simulated assumptions, not to a biological decision circuit.

## A useful comparison

Plot the full response-time distributions and choice proportions by condition. Compare candidate models on held-out conditions where stimulus strength, reward, or deadline changes. A difference in mean accuracy alone may leave important model predictions untested.

## Limits and deeper evidence

Choice and reaction time jointly constrain models more than accuracy alone, yet non-decision time, lapses, urgency, and stimulus history can still confound interpretation. Flexible hierarchical models need enough trials and careful prior checks. Neural correlates of a decision variable do not prove that variable causes the choice. Stronger inference combines behavioral model comparison with neural recordings, perturbations, and task designs that separate candidate mechanisms.

## Where to go next

Explore [inference and prediction](inference-and-prediction.md) for belief formation, [coding and representations](coding-and-representations.md) for sensory and choice signals, or [action and control](action-and-control.md) when decisions feed continuous movement. Methods: [theory and model building](../methods/theory-and-model-building.md), [neural data analysis](../methods/neural-data-analysis.md), [fitting and model comparison](../methods/fitting-and-model-comparison.md), [reproducible research](../methods/reproducible-research.md). Learning: [prerequisites](../learn/prerequisites.md), [learning paths](../learn/learning-paths.md), [projects](../learn/projects.md), [teaching](../learn/teaching.md). Browse [all topics](README.md), the [collection overview](../README.md), and [resources](../resources/README.md).

For model-based behavior and individual variation, see [computational psychiatry](computational-psychiatry.md) and the [causal-design workflow](../methods/causal-inference-and-experimental-design.md).
