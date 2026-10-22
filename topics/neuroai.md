# NeuroAI

[Collection overview](../README.md) · [All topics](README.md) · [Learn](../learn/README.md) · [Methods](../methods/README.md) · [Resource library](../resources/README.md)

NeuroAI connects neuroscience and artificial intelligence through shared questions about learning, perception, memory, action, and generalization. The comparison is scientifically useful when the target, measurements, and evaluation are explicit; resemblance between a model and brain data alone does not establish a shared mechanism.

## Questions to bring

- Which phenomenon or computation motivates the model, and what observation would count as a match?
- Are brain and model compared at comparable levels, such as behavior, representations, dynamics, or learning trajectories?
- Does the artificial system generalize in a way that makes a biological prediction, or merely score well on a benchmark?
- Which assumptions about architecture, training data, objective, and optimization shape the result?

## Prerequisites

Know basic machine learning evaluation, neural data analysis, and the distinction between training objective and test behavior. Learn representational similarity, encoding models, and cross-validation. For spiking systems, understand event-based computation and the difference between a model’s local update and a complete learning algorithm.

## A short start route

1. Choose a domain and align the model and brain stimulus/task conditions.
2. Specify a measurable comparison: behavior, neural responses, representational geometry, or dynamics.
3. Use held-out data and appropriate baselines; document model training data and weights.
4. Interpret similarity as evidence about the chosen measurement, then identify a discriminating experiment.

## Research threads

### Visual representations and brain prediction

Artificial vision systems can be compared with neural responses and behavior at several stages. [Neuroscience-Inspired Artificial Intelligence](../resources/papers-and-reviews.md#neuroscience-inspired-artificial-intelligence) provides a broad review context. [Net2Brain](../resources/software.md#net2brain) supports feature extraction and representational comparisons; [CORnet](../resources/software.md#cornet) provides recurrent visual-system model variants. [Brain-Score](../resources/datasets-and-benchmarks.md#brain-score) offers task-specific model-to-brain and behavior evaluation. The [Natural Scenes Dataset](../resources/datasets-and-benchmarks.md#natural-scenes-dataset) and [THINGS-data](../resources/datasets-and-benchmarks.md#things-data) provide human measurements and stimulus resources; [The Algonauts Project](../resources/datasets-and-benchmarks.md#the-algonauts-project) organizes brain-response prediction challenges. Benchmark success depends on split design, preprocessing, and metric choice, and does not establish biological identity.

### Spiking systems and event-based learning

Spiking networks explore computation with discrete events and alternative dynamics. [snnTorch](../resources/software.md#snntorch), [Norse](../resources/software.md#norse), [SpikingJelly](../resources/software.md#spikingjelly), and [Rockpool](../resources/software.md#rockpool) support different development workflows; [Tonic](../resources/software.md#tonic) provides event data tools. [Spiking Heidelberg Digits and Spiking Speech Commands](../resources/datasets-and-benchmarks.md#spiking-heidelberg-digits-and-spiking-speech-commands) supply auditory spike benchmarks. [Neuromatch Academy: NeuroAI](../resources/courses-and-lectures.md#neuromatch-academy-neuroai) and [Brains, Minds and Machines](../resources/courses-and-lectures.md#brains-minds-and-machines-summer-course-mit-ocw) connect methods with broader neuroscience questions. Efficiency on event data alone does not establish energy efficiency or biological plausibility in a deployed system.

### Generalization, mechanisms, and evaluation

Cross-domain comparison asks whether a model captures useful constraints, not whether neuroscience can be reduced to a model score. Design evaluations that vary stimuli, context, training exposure, or task rules. Distinguish predictive adequacy from causal explanation, and inspect whether representation metrics are stable across layers, preprocessing, and dataset splits. Read the [NeuroAI review](../resources/papers-and-reviews.md#neuroscience-inspired-artificial-intelligence) alongside benchmark documentation before making broad claims.

## Small project: compare representations under a controlled shift

Choose a pretrained vision model and a public neural-response dataset. Define one stimulus feature and compare a linear encoding model using model features against a simple pixel or low-level baseline. Deliver a documented stimulus split, feature extraction settings, held-out prediction scores with uncertainty, and a representational similarity plot. Evaluate performance under a shift such as held-out image identities or categories. If access terms or data size prevent a local run, use a small synthetic dataset and label it clearly. This proposal has not been run by the repository; a higher score is evidence about prediction under this analysis, not proof of a brain-like mechanism.

## A useful comparison

Keep training data, objectives, and model selection procedures in the comparison record. Use a baseline with similar input access and a split that tests a meaningful shift. Check whether representational conclusions survive reasonable metric and layer choices.

## Limits and deeper evidence

Model comparisons can confound architecture, training data, objective, and optimization. Neural datasets differ in coverage and measurement; correlations in representational spaces can be insensitive to important mechanistic differences. Benchmarks are task-bound and can encourage overfitting to metrics. For claims about shared computation, combine predictive comparisons with interventions, learning dynamics, out-of-distribution tests, and explicit alternatives. In spiking-learning work, eligibility traces or local plasticity rules alone do not establish exact credit assignment or whole-system biological plausibility.

## Where to go next

Follow the domain-specific guides for [coding and representations](coding-and-representations.md), [learning and plasticity](learning-and-plasticity.md), [perception and decision](perception-and-decision.md), [memory and navigation](memory-and-navigation.md), or [action and control](action-and-control.md). Methods: [theory and model building](../methods/theory-and-model-building.md), [simulation](../methods/simulation.md), [neural data analysis](../methods/neural-data-analysis.md), [fitting and model comparison](../methods/fitting-and-model-comparison.md), [reproducible research](../methods/reproducible-research.md). Learning: [prerequisites](../learn/prerequisites.md), [learning paths](../learn/learning-paths.md), [projects](../learn/projects.md), [teaching](../learn/teaching.md). Browse [all topics](README.md), the [collection overview](../README.md), and [resources](../resources/README.md).

For physical implementation, conversion, and measured efficiency, continue to [neuromorphic computing](neuromorphic-computing.md). For structural constraints and individual variation, see [connectomics](connectomics.md) and [computational psychiatry](computational-psychiatry.md).
