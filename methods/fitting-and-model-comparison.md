# Fitting and model comparison

[Collection](../README.md) · [Learn](../learn/README.md) · [Topics](../topics/README.md) · [Methods](README.md) · [Resources](../resources/README.md) · [Community](../community/README.md)

Use this workflow when a model has unknown parameters, when you need to quantify uncertainty about them, or when competing accounts make different predictions for observed data. Fitting asks which parameter values are compatible with data under a model; comparison asks how candidate models perform under a defined criterion and evaluation design.

## When to use this workflow

- A mechanistic, statistical, or normative model makes quantitative predictions but contains unknown parameters.
- You need to test whether parameters are identifiable from the available observations.
- Several models explain the same data, and you need a principled comparison.
- You want to evaluate generalization to new trials, sessions, subjects, or conditions.

If the model itself is not yet clear, begin with [theory and model building](theory-and-model-building.md). For preprocessing and measurement construction, use [neural data analysis](neural-data-analysis.md).

Do not fit more parameters than the data and intended claim can support.

## Prerequisites

Specify the observation model, likelihood or loss, parameter meanings and constraints, data hierarchy, and candidate models. Understand the experimental sampling unit and which observations are independent. Probability, statistics, and optimization are common tools; the right fitting approach depends on noise, missingness, parameter geometry, and data volume.

## Inputs and outputs

**Inputs:** analysis-ready observations with metadata; model predictions or likelihood; parameter bounds or priors; an optimization or inference method; baseline models; and a validation plan.

**Outputs:** parameter estimates or posterior distributions; uncertainty and identifiability diagnostics; comparative scores on training and evaluation data; and predictive checks that reveal systematic mismatch.

## Decision sequence

1. **Define the prediction target.** State whether the goal is parameter interpretation, prediction on held-out observations, explanation across conditions, or model discrimination. These goals can favor different criteria.
2. **Specify the data unit.** Identify trials, sessions, subjects, or time bins and how they nest. Choose train/test separation at the level matching the intended generalization claim.
3. **Write the observation model.** Specify what is observed, the assumed noise or sampling distribution, missing-data treatment, and how repeated observations relate. A squared-error objective implies assumptions; make them visible.
4. **Check identifiability before optimization.** Ask whether different parameter combinations can produce nearly the same predictions. Use analytic reasoning, simulated parameter recovery, profile likelihood, or posterior correlations as appropriate.
5. **Select fitting methods.** Match optimizer or inference method to the objective, constraints, and uncertainty goal. Use multiple initializations or chains when local optima or multimodality are plausible.
6. **Fit a simple baseline.** Establish a reference such as a mean, null, linear, or reduced model using training data only. Check that a complex candidate improves on a relevant alternative.
7. **Fit candidate models consistently.** Use the same observations, preprocessing, evaluation split, and comparable tuning effort. Document model-specific parameters and any regularization or prior choices.
8. **Check fit quality and recovery.** Plot residuals or posterior predictive summaries against time, condition, subject, and relevant covariates. Where possible, simulate data with known parameters and verify that the pipeline can recover them.
9. **Compare on the intended criterion.** Use held-out predictive performance for generalization claims; information criteria or Bayes factors only when their assumptions and interpretation fit the design. Report uncertainty in score differences.
10. **Challenge the conclusion.** Vary plausible preprocessing, prior or regularization strength, split strategy, and candidate set. Report where rankings or parameter interpretations change.

## Evaluation

A good score is not enough. Check residual patterns, calibration or predictive coverage where relevant, parameter recovery, and stability across data splits. Compare the fitted model with a simpler baseline and report the exact evaluation unit. If observations are temporally or hierarchically dependent, random pointwise splitting can exaggerate generalization. For small samples, show individual split scores or uncertainty rather than a single aggregate rank.

For a mechanistic claim, ask whether distinct models make testable predictions under an intervention or novel condition, not only whether they fit existing observations. For parameter claims, report uncertainty and distinguish a broad compatible range from a precisely identified value. Model rankings depend on the candidates and score chosen.

## Limitations

Optimization can find a best fit even when every candidate is wrong. Parameter values may be non-identifiable or strongly dependent on priors, constraints, and preprocessing. In-sample fit rewards flexibility. A held-out score estimates performance for its sampling design, not universal biological validity. Information criteria and Bayesian evidence answer different questions and should not be treated as interchangeable rankings.

## Selected resources

- [Statistical Models for Neural Data](../resources/courses-and-lectures.md#statistical-models-for-neural-data-cosyne--incf-trainingspace) — course materials connecting neural measurements with statistical model choices.
- [Neuromatch Academy: Computational Neuroscience](../resources/courses-and-lectures.md#neuromatch-academy-computational-neuroscience) — practical modules on model fitting, GLMs, and related analysis.
- [Neural Latents Benchmark](../resources/datasets-and-benchmarks.md#neural-latents-benchmark) — a shared setting for comparing latent population models and evaluation choices.
- [Probabilistic Machine Learning: Advanced Topics](../resources/books.md#probabilistic-machine-learning-advanced-topics) — reference material for latent-variable models and approximate inference.
- [Statistical Thinking for the 21st Century](../resources/books.md#statistical-thinking-for-the-21st-century) — accessible coverage of uncertainty, model checking, and statistical reasoning.

## Continue

Use the [topic guides](../topics/README.md) to ground candidates in a scientific question. Return to [theory and model building](theory-and-model-building.md) when candidate assumptions or predictions need clarification, [neural data analysis](neural-data-analysis.md) when measurements need review, and [reproducible research](reproducible-research.md) to record data splits and fit settings.

When the simulator has no practical likelihood, use [simulation-based inference](simulation-based-inference.md) and its [sbi resource](../resources/software.md#sbi). [PCNtoolkit](../resources/software.md#pcntoolkit) provides a reference-distribution route for individual variation; [hBayesDM](../resources/software.md#hbayesdm) provides task-based hierarchical models. For intervention claims, use [causal inference and experimental design](causal-inference-and-experimental-design.md) to examine what the comparison identifies.
