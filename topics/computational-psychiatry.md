# Computational psychiatry

[Collection overview](../README.md) · [All topics](README.md) · [Learn](../learn/README.md) · [Methods](../methods/README.md) · [Resource library](../resources/README.md)

Computational psychiatry applies formal models of learning, decision-making, inference, and brain dynamics to questions about mental-health-related behavior and brain function. It is a research program with several distinct model families, not one unified theory: fitted parameters and brain deviations are model-dependent measurements whose meaning must be established for each task, sample, and analysis.

## Questions to bring

- Which observable is the model intended to explain: trial-by-trial choices, response times, symptoms, brain measurements, or change over time?
- What generative or statistical assumptions connect that observable to a latent process or reference distribution?
- Which simpler model, alternative mechanism, or measurement explanation could produce similar data?
- Does the analysis estimate group differences, participant-level predictions, or both, and what independent evidence would support the intended interpretation?

## Prerequisites

Be comfortable with probability, regression, optimization, and basic programming. For behavioral models, learn the task structure and choice/response-time likelihood before interpreting latent parameters. For neuroimaging, understand preprocessing, measurement reliability, covariates, and site effects. Bayesian computation, cross-validation, and hierarchical models are useful for the practical routes below.

## A short start route

1. State a narrow research question and identify the measured outcome and its sampling unit.
2. Draw the model's data-generating assumptions and define the parameters that can be recovered from the task or measurements.
3. Simulate from the candidate and rival models; test parameter recovery and predictive checks before fitting real data.
4. Plan participant- and site-aware validation, and decide in advance what evidence would change the interpretation.
5. Report uncertainty, missingness, model failures, and the population or task conditions to which the result may transfer.

## Readings and tools

The [Zurich Computational Psychiatry Course](../resources/courses-and-lectures.md#computational-psychiatry-course) connects computational methods with behavioral and brain physiology examples; the 2026 edition has ended, and the page says to look for next year's course. For reinforcement-learning and decision-making models, [hBayesDM](../resources/software.md#hbayesdm) provides hierarchical Bayesian implementations in R and Python. The [HGF Toolbox](../resources/software.md#hgf-toolbox) is an existing MATLAB route for hierarchical belief-update models; [HSSM](../resources/software.md#hssm) covers hierarchical Bayesian sequential-sampling models for choice and response times.

For brain-measurement heterogeneity, [PCNtoolkit](../resources/software.md#pcntoolkit) provides documented normative-model workflows; its linked [normative modeling protocol](https://pmc.ncbi.nlm.nih.gov/articles/PMC7613648/) covers data selection, training and test sets, evaluation, and interpretation. The protocol predates the current 1.x package interface, so use current PCNtoolkit documentation for executable steps. Compare its participant-level framing with the broader [computational psychiatry review](../resources/papers-and-reviews.md#computational-psychiatry-towards-a-mathematically-informed-understanding-of-mental-illness). The [Transdiagnostic Connectome Project](../resources/datasets-and-benchmarks.md#transdiagnostic-connectome-project) shares behavioral, questionnaire, and MRI data for cross-domain research; it is a modest sample for high-dimensional prediction and should not be treated as a stand-alone validation cohort.

## Research threads

### Learning and decision processes

Reinforcement-learning models can formalize how action values or prediction errors change over trials. Compare models that differ in update rule or choice policy, and ask whether the task has enough informative trials to distinguish them. Hierarchical estimates partially pool information across participants; this changes uncertainty and can stabilize estimates, but it does not make a parameter a direct measure of a psychiatric mechanism. Before connecting a latent variable to fMRI or EEG, check its recovery and its timing and scaling assumptions.

### Belief updating and uncertainty

Hierarchical belief models describe how estimates and uncertainty change when observations are noisy or the environment changes. The [HGF Toolbox](../resources/software.md#hgf-toolbox) supplies one established model family, but an HGF parameter is conditional on its update equations, response model, and task design. Simulate plausible alternatives and check whether the data distinguish volatility learning from simpler recency or sensitivity accounts. For broader inference questions, continue to [inference and prediction](inference-and-prediction.md).

### Normative models and population variation

Normative models estimate a conditional reference distribution, often for brain measurements given age, sex, or site, and express observations relative to that fitted distribution. A deviation score is statistical relative position under a selected reference sample; it is not a diagnosis, a causal explanation, or a prescription to move an individual toward the sample average. Inspect how reference-sample composition, scanner/site, measurement quality, covariate range, and model misspecification affect the score. The [PCNtoolkit guide](../resources/software.md#pcntoolkit) and its linked protocol provide practical model and evaluation routes; use current PCNtoolkit documentation for executable instructions.

### Prediction, mechanism, and translation

Prediction asks whether a model forecasts held-out observations under a specified sampling scheme. Mechanistic interpretation asks whether the proposed process is identifiable and discriminates from alternatives. Individual utility requires a further link between a prediction and a decision or outcome that matters, evaluated in the relevant population and setting. Good in-sample fit, a statistically unusual deviation, or an accurate held-out group label does not establish either mechanistic specificity or individual benefit.

## Small project: separate participant and site generalization

Using the public [Transdiagnostic Connectome Project](../resources/datasets-and-benchmarks.md#transdiagnostic-connectome-project), draft or run a preregistered prediction of one continuous questionnaire measure from a small, specified set of behavioral or imaging features. First inspect the sample's site-by-diagnosis and missing-data structure. Compare a demographics-only baseline with a feature model using participant-grouped, site-stratified nested cross-validation; repeated runs from a person must stay in one fold. Evaluate transfer to a held-out site only if outcome distributions overlap and the analysis has a prespecified strategy for a site unseen during training; if not, report transfer as not estimable. Report uncertainty and performance by site, and include a participant-level permutation control. The output is a reproducible analysis plan or held-out prediction report, not a clinical classifier. With only 241 participants, many predictors, site-linked sampling, noisy imaging, and limited external validation, apparent prediction may be unstable and cannot establish cause, mechanism, or individual utility.

## Evidence and interpretation checks

- Keep participants, sessions, runs, and trials distinct when splitting data; group repeated observations from one person within the same fold.
- Inspect whether diagnostic composition, acquisition site, demographic variables, medication, task completion, or data quality are entangled. A model can exploit these patterns without learning the proposed process.
- Report posterior uncertainty, recovery, calibration, and predictive checks alongside parameter or deviation estimates; group-average fit does not establish participant-level reliability.
- Test transfer to held-out sites or samples and describe where the reference distribution or task is poorly represented.
- Treat diagnoses and questionnaire scores as measured variables with their own reliability and sampling limits, not as direct readouts of a single biological mechanism.

## Where to go next

Continue to [perception and decision](perception-and-decision.md) for choice and response-time models, [inference and prediction](inference-and-prediction.md) for latent belief updates, and [neural data analysis](../resources/neural-data-analysis.md) for measurement and preprocessing methods. Browse [fitting and model comparison](../methods/fitting-and-model-comparison.md), [reproducible research](../methods/reproducible-research.md), and the [resource library](../resources/README.md) for adjacent methods.
