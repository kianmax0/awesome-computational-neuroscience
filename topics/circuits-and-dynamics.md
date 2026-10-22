# Circuits and dynamics

[Collection overview](../README.md) · [All topics](README.md) · [Learn](../learn/README.md) · [Methods](../methods/README.md) · [Resource library](../resources/README.md)

Circuit models ask how populations of neurons interact over time. Depending on scale, a circuit may be represented by coupled rate variables, spiking cells, neural fields, or a whole-brain network. The central task is to connect assumptions about interactions and timescales to measurable activity and behavior.

## Questions to bring

- Which population variables are modeled: rates, spikes, membrane states, or latent activity?
- What dynamical feature is at issue: stability, oscillation, synchrony, waves, switching, or computation through trajectories?
- Which connections are known from anatomy, inferred from data, or introduced as simplifying assumptions?
- Does the model predict a perturbation response, or only reproduce activity it was fit to?

## Prerequisites

Review ordinary differential equations, fixed points, linear stability, and basic probability. For spiking networks, know how synaptic currents, delays, and event-based simulation work. Neural data analysis requires careful alignment of sampling, event times, and behavioral epochs; familiarity with matrices and numerical integration is useful.

## A short start route

1. Choose a dynamical signature and define how it will be measured.
2. Begin with a two-population or small rate model, draw its interaction graph, and state sign and timescale assumptions.
3. Analyze equilibria or simulate trajectories, then change one parameter or connection at a time.
4. Compare with neural data or a more detailed model, making clear which quantities were fit and which were predicted.

## Research threads

### E–I balance, oscillations, and stability

Coupled excitation and inhibition can generate asynchronous activity, oscillatory regimes, and transitions as gain or connectivity changes. [Dynamical Neural Systems](../resources/courses-and-lectures.md#dynamical-neural-systems) offers a structured route through stability, oscillations, bursting, and waves. The [Cajal Course in Computational Neuroscience](../resources/courses-and-lectures.md#cajal-course-in-computational-neuroscience) connects balanced network dynamics with analysis and computation. Neither a qualitative match nor a reproduced spectrum uniquely identifies circuit wiring.

### Computation through trajectories

Some tasks may be solved by transient population trajectories rather than a fixed activity code. The [Computation-through-Dynamics benchmark and toolkit](../resources/datasets-and-benchmarks.md#computation-through-dynamics-benchmark-and-toolkit) supplies task models, synthetic datasets, and comparison metrics for examining this idea. Use it to separate dynamical prediction from task accuracy: a network can solve a task without matching the biological trajectory.

### Spatially extended populations and brain-scale models

Neural fields describe activity varying over space; neural masses compress a region into a few state variables. [Neural Fields: Theory and Applications](../resources/books.md#neural-fields-theory-and-applications) is a deeper theory route. The hands-on [Large-Scale Modeling of Brain Dynamics](../resources/courses-and-lectures.md#large-scale-modeling-of-brain-dynamics) course models Wilson–Cowan populations coupled through structural connectivity. Such couplings depend on parcellation, tractography, delays, and observation models; BOLD agreement alone does not establish the underlying neural mechanism.

### Microcircuits and scale reduction

Detailed spiking networks can test how cellular and synaptic assumptions affect emergent activity, but often require many parameters and compute. The [Potjans–Diesmann cortical microcircuit in NetPyNE](../resources/tutorials-and-examples.md#potjansdiesmann-cortical-microcircuit-model-in-netpyne) is a concrete layered-network implementation. [Modeling Neural Circuits Made Simple with Python](../resources/books.md#modeling-neural-circuits-made-simple-with-python) provides a lighter route to circuit models and data.

## Small project: locate a stability transition

Build a two-population E–I rate model. Deliver its equations, interaction diagram, fixed-point calculation, and a plot of trajectories across a one-dimensional parameter sweep. Compare the stability prediction with simulation and identify where the linear approximation fails. Evaluate by checking that trajectories from multiple initial states approach the predicted fixed point or diverge as expected. State how adding delays, heterogeneity, or spiking would alter the interpretation; do not claim the chosen parameter values describe a particular brain circuit unless independently constrained.

## Limits and deeper evidence

Many different networks produce similar low-dimensional activity. Correlation does not determine direction of influence, and a fitted effective connection need not equal an anatomical synapse. Model reduction can preserve selected observables while discarding mechanisms. Stronger claims need interventions, held-out conditions, explicit observation models, sensitivity analyses, and comparison to plausible alternatives. Scaling a microcircuit or fitting a neural field does not automatically preserve the biological constraints of the original system.

## Where to go next

Go to [neurons and dendrites](neurons-and-dendrites.md) for cellular assumptions, [coding and representations](coding-and-representations.md) for population readouts, or [action and control](action-and-control.md) for closed-loop dynamics. Methods: [theory and model building](../methods/theory-and-model-building.md), [simulation](../methods/simulation.md), [neural data analysis](../methods/neural-data-analysis.md), [fitting and model comparison](../methods/fitting-and-model-comparison.md), [reproducible research](../methods/reproducible-research.md). Learning: [prerequisites](../learn/prerequisites.md), [learning paths](../learn/learning-paths.md), [projects](../learn/projects.md), [teaching](../learn/teaching.md). See [all topics](README.md), the [collection overview](../README.md), and [resources](../resources/README.md).

For connections used to constrain a circuit model, see [connectomics](connectomics.md). For rules that generate structure, see [development and self-organization](development-and-self-organization.md).
