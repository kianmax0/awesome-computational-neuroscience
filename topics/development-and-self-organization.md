# Development and self-organization

[Collection overview](../README.md) · [All topics](README.md) · [Learn](../learn/README.md) · [Methods](../methods/README.md) · [Resource library](../resources/README.md)

This guide asks how neural structure emerges through growth, local interactions, and constraints, and how computational models can make those assumptions testable. It connects single-cell arbor formation to early circuit assembly and developmental measurements; it does not treat a mature morphology or atlas as a direct record of the developmental process that produced it.

## Questions to bring

- What changes over simulated time: neurite tips, branches, cell positions, synapses, activity, or some combination?
- Which rules are intrinsic to the cell, and which depend on local cues, neighboring cells, geometry, or activity?
- What measured outcome constrains the model: branch statistics, spatial distributions, connectivity, gene expression, or developmental timing?
- Can competing growth rules produce the same final pattern, and which time-resolved observation would distinguish them?
- Does the model represent physical development, or is it a phenomenological generator of plausible structures?

## Prerequisites

Useful background includes basic graph theory, probability, differential equations, and neuronal morphology. Python is helpful for agent-based growth simulations and data analysis; MATLAB is needed to use the TREES toolbox. Readers new to neural branching can begin with the open-access [Cuntz et al. paper](../resources/papers-and-reviews.md#one-rule-to-grow-them-all-a-general-theory-of-neuronal-branching-and-its-practical-application), which develops an optimization account of neuronal trees.

## A short start route

1. Choose a level and observable: one arbor's branch topology, a population's spatial organization, or a region's developmental expression profile.
2. Write the growth or organization rule explicitly, including what each simulated agent can sense and what it cannot.
3. Identify the observation that constrains the rule and the assumptions connecting that observation to a developmental mechanism.
4. Compare a baseline rule with one changed constraint, then test whether the difference survives parameter variation and replicate runs.

## Research threads

### Neuronal morphology as constrained growth

An arbor can be represented as a rooted graph embedded in space. Growth models can ask how branch placement follows from local exploration, target density, wiring cost, conduction distance, or competition. The [TREES toolbox](../resources/software.md#trees-toolbox) supports graph-based analysis and generation of neuronal morphologies, while [NeuroDevSim](../resources/software.md#neurodevsim) models growing fronts, cell migration, environmental interactions, and emerging microcircuits. These tools work at different levels: TREES emphasizes tree structure and morphology operations, and NeuroDevSim provides a phenomenological developmental simulation framework.

### Self-organization and circuit assembly

Local interaction rules can generate population-level arrangements without specifying a final circuit in advance. Ask whether the apparent order follows from attraction or repulsion, collision avoidance, shared resources, activity-dependent selection, or boundary conditions. A match to a mature pattern alone cannot identify which mechanism operated; trajectories, perturbations, or intermediate developmental stages are needed to discriminate causes.

### Developmental measurements as model constraints

Developmental expression and anatomy provide time- and region-dependent constraints, not growth rules by themselves. The [BrainSpan Atlas of the Developing Human Brain](../resources/datasets-and-benchmarks.md#brainspan-atlas-of-the-developing-human-brain) provides developmental transcriptome datasets and associated anatomical annotations. Use the atlas to define a measured temporal or regional pattern, then be explicit about how molecular or anatomical measurements relate to the state variables in a computational model. Stages, samples, and historical normalization choices matter when comparing profiles.

## Small project: a branching rule under a changed cue

Build or adapt a minimal 2D branching simulation with a root, growing tips, a boundary, and one spatial cue. Compare cue-free growth with attraction or repulsion while holding the number of initial tips, simulation steps, and random seed set fixed; repeat across several seeds. Deliver the rule in pseudocode, a plot of the resulting arbors, and a table of branch count, total length, and endpoint distance to the cue. State what the experiment can distinguish and what remains ambiguous. The exercise is a proposed model comparison, not a claim that the chosen cue reproduces biological development. This is a suggested exercise and has not been run by the repository.

## Limits and deeper evidence

Phenomenological growth rules are useful for testing consequences of local interactions, but a visually plausible arbor does not validate a cellular mechanism. Conversely, an optimization account can summarize mature morphology without specifying the developmental sequence that produced it. Atlas expression data are sampled observations rather than continuous trajectories, and species, region, stage, and measurement protocol constrain what can be inferred. Prefer time-resolved and perturbation evidence when making causal claims, and report stochastic variation and sensitivity to initialization.

## Where to go next

Move to [neurons and dendrites](neurons-and-dendrites.md) when the question is how mature morphology affects cellular computation; to [circuits and dynamics](circuits-and-dynamics.md) when the target is emergent population activity; or to [learning and plasticity](learning-and-plasticity.md) when activity-dependent change is central. Methods: [theory and model building](../methods/theory-and-model-building.md), [simulation](../methods/simulation.md), and [neural data analysis](../methods/neural-data-analysis.md). Learning: [prerequisites](../learn/prerequisites.md), [projects](../learn/projects.md), and [teaching](../learn/teaching.md). Browse [all topics](README.md) and the [resource library](../resources/README.md).
