# Inference and prediction

[Collection overview](../README.md) · [All topics](README.md) · [Learn](../learn/README.md) · [Methods](../methods/README.md) · [Resource library](../resources/README.md)

Inference models ask how neural systems estimate hidden causes from noisy observations and update expectations over time. Predictive coding is one family of proposals among several; a useful guide keeps mathematical claims, algorithmic implementations, and neural mechanism claims distinct.

## Questions to bring

- What is hidden, what is observed, and how are likelihoods and priors represented?
- Does the model explain perception, learning, neural activity, or all three with separate assumptions?
- What does “prediction error” denote in the specific model, and how is it computed?
- Which perturbation or behavioral manipulation could discriminate inference from alternative accounts?

## Prerequisites

Know conditional probability, Bayes’ rule, latent-variable models, and basic optimization. Familiarity with graphical models and state-space models helps. For neural-data work, distinguish measurement noise from variability in the latent process and from model misspecification.

## A short start route

1. Draw the generative model and label observations, latent states, and parameters.
2. Derive or identify the inference objective and the update procedure.
3. Simulate data from the model, infer hidden variables, and check calibration or recovery.
4. Construct an alternative model that makes a different prediction on a targeted condition.

## Research threads

### Bayesian perception and integration

Bayesian models formalize how prior expectations combine with uncertain sensory evidence. [Bayesian Brain: Probabilistic Approaches to Neural Coding](../resources/books.md#bayesian-brain-probabilistic-approaches-to-neural-coding) introduces probabilistic accounts; [Bayesian Models of Learning and Integration of Neuroimaging Data](../resources/courses-and-lectures.md#bayesian-models-of-learning-and-integration-of-neuroimaging-data) connects latent beliefs with learning and imaging analyses. A behavior that looks Bayesian may arise from other strategies; assess predictions across uncertainty and prior manipulations.

### Prediction error and predictive coding

Predictive-coding formulations vary in their variables, objective, message passing, and learning assumptions. The [theoretical and experimental review](../resources/papers-and-reviews.md#predictive-coding-a-theoretical-and-experimental-review) maps these questions; [Predictive Coding Networks and Inference Learning](../resources/papers-and-reviews.md#predictive-coding-networks-and-inference-learning-tutorial-and-survey) surveys computational constructions; the [Predictive Coding](../resources/software.md#predictive-coding) resource provides a focused entry. Agreement between a model’s predictions and brain measurements does not prove that the brain implements that model’s inference procedure.

### Learning structured beliefs over time

Hierarchical Gaussian filter (HGF) models track changing uncertainty and volatility. The [HGF Toolbox](../resources/software.md#hgf-toolbox) offers a route to fitting and examining hierarchical belief updates. The [pymdp toolkit](../resources/software.md#pymdp) supports active-inference-style discrete generative models. These frameworks encode particular assumptions; parameter recovery and comparison with simpler alternatives are essential before interpreting fitted latent beliefs.

## Small project: test prior-weighted perception

Simulate a one-dimensional sensory estimate with controllable sensory variance and a prior whose mean can shift. Compare a Bayesian estimator with a fixed-weight or stimulus-only baseline. Deliver the generative model, predicted estimates across variance and prior conditions, parameter recovery results, and one plot of model comparison on simulated held-out data. Evaluate calibration and whether the models make separable predictions at the extremes. This is a proposed exercise, not a validated experiment. Do not infer neural implementation from behavioral fit alone.

## A useful comparison

Check parameter recovery before interpreting fitted latent beliefs, and include data generated outside the candidate model when possible. Examine whether rivals differ on a specific manipulation rather than relying only on aggregate fit. Keep computational and neural implementation claims in separate sentences.

## Limits and deeper evidence

Latent variables are not directly observed, and different generative models can fit the same behavior. Model comparison depends on priors, parameter constraints, and task structure; recovery on simulated data checks the analysis under the assumed model but cannot validate the assumption itself. Neural correlates of prediction error are also measurement- and region-dependent. Separate evidence for computation from evidence for a particular circuit implementation.

## Where to go next

Continue to [perception and decision](perception-and-decision.md) for choices under uncertainty, [learning and plasticity](learning-and-plasticity.md) for changes to beliefs or synapses, and [NeuroAI](neuroai.md) for comparisons of inference algorithms. Methods: [theory and model building](../methods/theory-and-model-building.md), [neural data analysis](../methods/neural-data-analysis.md), [fitting and model comparison](../methods/fitting-and-model-comparison.md), [reproducible research](../methods/reproducible-research.md). Learning: [prerequisites](../learn/prerequisites.md), [learning paths](../learn/learning-paths.md), [projects](../learn/projects.md), [teaching](../learn/teaching.md). Browse [all topics](README.md), the [collection overview](../README.md), and [resources](../resources/README.md).

For parameter inference about a generative simulator, use [simulation-based inference](../methods/simulation-based-inference.md). [Computational psychiatry](computational-psychiatry.md) connects inference models and statistical reference distributions to individual variation.
