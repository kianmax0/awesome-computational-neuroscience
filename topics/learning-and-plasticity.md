# Learning and plasticity

[Collection overview](../README.md) · [All topics](README.md) · [Learn](../learn/README.md) · [Methods](../methods/README.md) · [Resource library](../resources/README.md)

Learning models connect experience, internal state, objectives, and parameter change. A local synaptic update rule is one part of this account; it does not by itself specify how useful teaching signals arise or how delayed outcomes receive credit.

## Questions to bring

- What changes with experience: synaptic efficacy, intrinsic excitability, latent state, or a policy?
- Which signals are available locally, and how are global outcomes linked to synapses and time?
- Is the rule descriptive, normative, mechanistic, or an engineering approximation?
- Which intervention or task manipulation distinguishes candidate learning rules?

## Prerequisites

Review probability, gradients, dynamical systems, and basic synaptic physiology. Be able to derive a simple Hebbian or error-driven update and simulate it. For reinforcement learning, understand reward prediction error, eligibility traces, and temporal credit assignment as related but distinct components.

## A short start route

1. Specify the task, observable, objective, model state, and allowed update signals.
2. Write the update rule and identify which quantities must be stored locally or transmitted.
3. Simulate a minimal task with a baseline rule and one alternative.
4. Test learning and stability on held-out conditions, then examine biological assumptions separately from performance.

## Research threads

### Plasticity windows and synaptic state

Spike-timing-dependent plasticity describes timing-dependent change under particular protocols, while voltage, rate, neuromodulatory, and metaplastic variables can change the rule. [Computational Modeling of Neuronal Plasticity](../resources/courses-and-lectures.md#computational-modeling-of-neuronal-plasticity) and the [Brian 2 Clopath voltage-based STDP example](../resources/tutorials-and-examples.md#brian-2-clopath-voltage-based-stdp-example) provide practical model routes. [Synaptic Plasticity Forms and Functions](../resources/papers-and-reviews.md#synaptic-plasticity-forms-and-functions) surveys functional interpretations. A fitted plasticity window is protocol-dependent evidence, not a universal rule.

### Reward and neuromodulation

Three-factor rules combine pre/post activity with a modulatory signal. The [NESTML dopamine-modulated STDP tutorial](../resources/tutorials-and-examples.md#nestml-dopamine-modulated-stdp-tutorial) supports implementation; [A Simple Model of Neuromodulatory State-Dependent Synaptic Plasticity](../resources/tutorials-and-examples.md#a-simple-model-of-neuromodulatory-state-dependent-synaptic-plasticity) links modulatory state to plasticity. An eligibility trace can preserve recent local activity, but trace plus reward is not automatically exact task-dependent credit assignment; examine delays, competing synapses, and the objective.

### Normative and computational accounts

Optimization can explain why an update improves an objective, yet the resulting algorithm may require nonlocal information or biologically unavailable operations. The review [Spike Timing-Dependent Plasticity: A Consequence of More Fundamental Learning Rules](../resources/papers-and-reviews.md#spike-timing-dependent-plasticity-a-consequence-of-more-fundamental-learning-rules) motivates comparing phenomenological plasticity with broader learning principles. Distinguish algorithmic performance, implementation constraints, and evidence for a mechanism.

## Small project: delayed reward and local traces

Implement a two-choice toy task where a synapse receives a pre/post event and a delayed scalar reward. Compare immediate correlation-based change with a rule using an eligibility trace. Deliver the task specification, update equations, learning curves across delay, and a table of required signals and memory. Evaluate across multiple random seeds and compare against a simple supervised or policy-gradient baseline. Include a case where reward is unrelated to the earlier event. The goal is to expose what the trace solves and what it does not; do not claim the toy rule is a complete biological learning mechanism.

## A useful comparison

For every candidate rule, list the state variables, information sources, and update timescale it requires. Compare these requirements with the experimental preparation and with the task’s feedback structure. A biologically local update can still depend on a difficult global signal.

## Limits and deeper evidence

Behavioral improvement does not establish the synaptic mechanism. Normative derivations can rely on assumptions about objective, feedback, and state that experiments do not directly verify. Plasticity protocols isolate components but may omit behavioral context and interacting modulators. Stronger accounts relate measured synaptic changes to learning behavior, perturb the proposed signals, and test predictions across conditions. When comparing rules, make the task and module dependencies explicit rather than assuming a universal dependency graph.

## Where to go next

See [inference and prediction](inference-and-prediction.md) for learning about hidden causes, [coding and representations](coding-and-representations.md) for changing population codes, and [action and control](action-and-control.md) for learning in closed-loop behavior. Methods: [theory and model building](../methods/theory-and-model-building.md), [simulation](../methods/simulation.md), [fitting and model comparison](../methods/fitting-and-model-comparison.md), [reproducible research](../methods/reproducible-research.md). Learning: [prerequisites](../learn/prerequisites.md), [learning paths](../learn/learning-paths.md), [projects](../learn/projects.md), [teaching](../learn/teaching.md). See [all topics](README.md), the [collection overview](../README.md), and [resources](../resources/README.md).

For developmental changes in structure, see [development](development-and-self-organization.md). For on-device learning and implementation constraints, see [neuromorphic computing](neuromorphic-computing.md).
