# Coding and representations

[Collection overview](../README.md) · [All topics](README.md) · [Learn](../learn/README.md) · [Methods](../methods/README.md) · [Resource library](../resources/README.md)

Neural coding asks how activity relates to stimuli, actions, internal variables, and downstream use. A response that predicts a label is not automatically a complete account of representation: the result depends on the measurement, task, sampled population, and assumed observer.

## Questions to bring

- What variable is represented, for whom, and over what time window?
- Is the claim about information, a decodable signal, a geometrical structure, or a causal readout?
- How do tuning, noise correlations, population geometry, and task demands change the answer?
- Does the analysis generalize across stimuli, sessions, subjects, or behavioral states?

## Prerequisites

Know basic probability, conditional distributions, regression, and classification. Be able to distinguish training and test data and recognize dependence among repeated observations. For spike trains, understand binning choices and temporal precision; for imaging data, know that the measured signal is an indirect, filtered observation of neural activity.

## A short start route

1. State the candidate represented variable and the competing null or alternative.
2. Plot single-unit responses before fitting a decoder; inspect stimulus and behavioral sampling.
3. Fit a simple encoding or decoding model with held-out evaluation and a meaningful baseline.
4. Ask what the decoder accesses that a biological downstream circuit could plausibly use.

## Research threads

### Tuning and population readout

Single-neuron tuning curves summarize response dependence, while population decoders ask whether a variable can be recovered from joint activity. [Coding and Vision 101](../resources/courses-and-lectures.md#coding-and-vision-101) offers a practical route into coding analyses; [The Neural Code (UCL Cortexlab)](../resources/courses-and-lectures.md#the-neural-code-ucl-cortexlab) connects neural responses to coding questions. A statistically successful decoder may exploit artifacts, correlations, or information inaccessible to the actual downstream system.

### Information and task relevance

Information-theoretic quantities can compare responses to stimuli, but finite samples, continuous variables, and estimator choices matter. The resource [Information Theory and Neural Coding](../resources/papers-and-reviews.md#information-theory-and-neural-coding) is a theoretical entry point; [Statistical Models for Neural Data](../resources/courses-and-lectures.md#statistical-models-for-neural-data-cosyne--incf-trainingspace) helps connect distributions to practical data analysis. Information about a variable is not proof that the brain uses it for a specific computation.

### Representational geometry and dynamics

Population geometry can expose shared structure across tasks, brain areas, or artificial networks. [SPIKY](../resources/software.md#spiky) supports analysis and visualization of spike-train timing relations. When activity evolves rapidly, analyses should preserve temporal structure rather than treating each bin as independent. For cross-system comparisons, see [NeuroAI](neuroai.md) and the [Computation-through-Dynamics benchmark and toolkit](../resources/datasets-and-benchmarks.md#computation-through-dynamics-benchmark-and-toolkit).

## Small project: test a code under changed sampling

Choose a public dataset or a simulated population with a known stimulus variable. Deliver (a) a response visualization, (b) a simple encoding model and a decoder, (c) cross-validated performance under random splits, and (d) performance under a split that holds out stimulus conditions or sessions. Compare a rate representation with a timing-sensitive summary if the data support it. Evaluate whether conclusions survive the harder split, whether a baseline captures the effect, and whether uncertainty is reported. The exercise has not been run by this repository; do not interpret decodability as causal use.

## A useful comparison

Report at least one baseline matched to the data structure, plus uncertainty across folds or sessions. Separate stimulus decoding from behavioral prediction and specify whether the readout is biologically motivated or simply optimized for accuracy. Preserve the stimulus identity in the split design.

## Limits and deeper evidence

Population analyses are sensitive to unit sampling, behavioral covariates, temporal binning, and preprocessing. Flexible models can capitalize on leakage or nonstationarity. A linear readout demonstrates sufficiency under its assumptions, while a failure can reflect limited data or a poor readout rather than absence of signal. Claims about a neural code become stronger when the task manipulation, neural perturbation, and behavioral consequence align.

## Where to go next

For plasticity and changing representations see [learning and plasticity](learning-and-plasticity.md); for hidden-variable accounts see [inference and prediction](inference-and-prediction.md); for brain-model comparisons see [NeuroAI](neuroai.md). Methods: [neural data analysis](../methods/neural-data-analysis.md), [fitting and model comparison](../methods/fitting-and-model-comparison.md), [reproducible research](../methods/reproducible-research.md). Learning: [prerequisites](../learn/prerequisites.md), [learning paths](../learn/learning-paths.md), [projects](../learn/projects.md), [teaching](../learn/teaching.md). Browse [all topics](README.md), the [collection overview](../README.md), and [resources](../resources/README.md).
