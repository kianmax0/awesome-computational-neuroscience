# Theory and model building

[Collection](../README.md) · [Learn](../learn/README.md) · [Topics](../topics/README.md) · [Methods](README.md) · [Resources](../resources/README.md) · [Community](../community/README.md)

Use this guide when the main goal is to explain a neural or behavioral phenomenon with a compact formal account, derive consequences from assumptions, or distinguish candidate mechanisms. A theory can be analytic, computational, or partly verbal; coding is useful for many models but is not a prerequisite for every theoretical contribution.

## When to use this approach

- The question asks what mechanism or computation could produce a measured pattern.
- Several plausible accounts fit the broad observation, and you need predictions that separate them.
- You need to state what a model represents and what it leaves outside its scope.
- A mathematical framework such as dynamics, probability, information theory, control, or optimization offers tools for a specific part of the question.

Do not begin by choosing a fashionable framework. Begin with the observation, task, biological constraints, and alternatives that matter for the claim.

## Prerequisites

Requirements depend on the model. Differential equations and linear algebra support dynamical models; probability and statistics support stochastic or latent-variable accounts; optimization supports normative models and parameter learning. Read enough biology to interpret the represented units, timescales, and interventions. See [mathematical foundations](../resources/books.md#mathematics-for-machine-learning) and [books](../resources/books.md).

The [learning paths](../learn/README.md) can help fill a background gap before choosing a formalism.

Programming is useful when equations lack closed forms, when simulations expose behavior, or when fitting requires computation. A derivation, conceptual model, or analytic limiting case can still be valuable without a software implementation.

## Inputs and outputs

**Inputs:** a sharply stated phenomenon or task; empirical constraints and relevant alternative explanations; a defined system boundary; and assumptions about observables, hidden variables, noise, and time or space scales.

**Outputs:** a formal model or derivation; an account of its assumptions and scope; results or predictions that follow from it; and a clear statement of evidence that could challenge it.

## Decision sequence

1. **State the target.** Define the observation to explain, the experimental or behavioral conditions, and what counts as success for an explanation.
2. **Name the represented objects.** Specify cells, populations, synapses, stimuli, actions, latent states, or other entities. Identify which are measured and which are model constructs.
3. **Define quantities and units.** List state variables, parameters, inputs, outputs, probability distributions, and units where applicable. Say whether quantities describe individual trials, averages, distributions, or population summaries.
4. **Fix model semantics.** For graphs, say whether nodes denote variables, mechanisms, anatomical units, or computational operations. Say what an edge means: causal influence, statistical dependence, message flow, connectivity, or a constraint. Do not infer causal direction from statistical association alone.
5. **State assumptions before deriving.** Include boundary conditions, stationarity or independence assumptions, approximations, noise model, constraints, and omitted mechanisms that affect interpretation.
6. **Derive consequences.** Show how the assumptions lead to the claimed behavior. Separate mathematical identities from additional modeling choices and approximations.
7. **Check special and limiting cases.** Test zero input, weak coupling, no noise, extreme parameter values, small populations, or other limits that expose sign errors, degeneracies, or hidden commitments.
8. **Make discriminating predictions.** Identify an intervention, context, timescale, or measurement for which competing models predict different outcomes. Prefer predictions not used to construct or tune the model.
9. **Choose an evaluation route.** Compare analytic predictions with data, use a simulation if behavior is not tractable, or derive a measurement plan. Route parameter estimation to [fitting and model comparison](fitting-and-model-comparison.md).

## Evaluate the account

Check internal consistency, units, identifiability of key quantities, robustness to plausible assumption changes, and whether the model reproduces the target without being over-tuned to it. A model that fits one curve may have weak explanatory value if several mechanisms make the same prediction there. State in advance which result would count against the proposed account.

For fitted models, reserve observations or conditions for evaluation and inspect residual structure. For mechanistic claims, test perturbations or contexts that expose the proposed mechanism. For normative accounts, state the objective and constraints explicitly; an objective that reproduces an outcome does not by itself establish that the brain optimizes it.

## Limits and interpretation

Every model is selective. A result is conditional on its representation, assumptions, data, and evaluation conditions. Mathematical elegance, biological detail, predictive accuracy, and causal identification are different virtues; report which one the work establishes. Avoid treating one formal language as a universal description of nervous systems.

## Selected resources

- [Theoretical Neuroscience](../resources/books.md#theoretical-neuroscience-computational-and-mathematical-modeling-of-neural-systems) — broad examples connecting coding, neurons, circuits, and learning; useful for identifying established model forms.
- [Dynamical Systems in Neuroscience](../resources/books.md#dynamical-systems-in-neuroscience-the-geometry-of-excitability-and-bursting) — a focused route from phase-plane geometry to excitability and bursting.
- [Neuromatch Academy: Computational Neuroscience](../resources/courses-and-lectures.md#neuromatch-academy-computational-neuroscience) — guided tutorials that connect mathematical models to computational exercises.
- [Neural population dynamics during reaching](../resources/papers-and-reviews.md#neural-population-dynamics-during-reaching) — a concrete population-level account to examine for represented quantities, timescales, and empirical predictions.

## Continue

Choose the relevant [topic guide](../topics/README.md), then use [simulation](simulation.md) if model behavior needs computation, [neural data analysis](neural-data-analysis.md) to define measurements, or [fitting and model comparison](fitting-and-model-comparison.md) to estimate and test parameters.

When the account concerns an intervention, connect its assumptions to [causal inference and experimental design](causal-inference-and-experimental-design.md). When mechanistic parameters must be constrained through a simulator, use [simulation-based inference](simulation-based-inference.md) and retain the distinction between model assumptions and information supplied by observations.
