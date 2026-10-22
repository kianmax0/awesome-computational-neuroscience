# Connectomics

[Collection overview](../README.md) · [All topics](README.md) · [Learn](../learn/README.md) · [Methods](../methods/README.md) · [Resource library](../resources/README.md)

Connectomics studies how neural elements are connected and how those maps relate to activity, computation, and behavior. The word covers several scales and measurements: synapses between reconstructed cells, projections among regions, diffusion MRI streamlines, and statistical dependence between signals. Each produces a different kind of network and supports different claims.

## Questions to bring

- What are the nodes: synapses, neurons, parcels, or recorded signals?
- What observation produced each edge, and what does its weight mean?
- Is the network directed, signed, weighted, incomplete, or versioned?
- Which conclusion concerns anatomy, statistical association, causal influence, or model assumption?
- What uncertainty comes from segmentation, proofreading, parcellation, tractography, sampling, or thresholding?

## Prerequisites

Basic graph concepts help: adjacency matrices, degree, paths, and connected components. For cellular connectomes, be comfortable reading neuron morphology and interpreting synapse annotations; programming is useful for querying large datasets. Human MRI connectomics also assumes familiarity with image preprocessing, brain parcellations, and diffusion or functional MRI. The [Brain Connectivity Toolbox](../resources/software.md#brain-connectivity-toolbox) expects square network matrices and MATLAB or a compatible environment; its measures require matching the graph type to the function.

## A short start route

1. State the biological scale and the operational definition of a node and edge.
2. Inspect the acquisition, reconstruction, annotation, and release-version documentation before choosing a graph measure.
3. Draw or query a small subgraph and verify that its identifiers and edge weights mean what you think they mean.
4. Compare the result with an explicit null or alternative construction, and report which evidence cannot be recovered from the graph.

## Structural, functional, and inferred connectivity

Structural connectivity is a claim about anatomical pathways. At cellular scale, electron microscopy can support synapse-level contacts after segmentation and annotation, but a reconstruction may be partial, proofread to different levels, or bounded by a volume. At human macroscale, diffusion MRI and tractography estimate likely white-matter pathways between chosen regions; streamlines are not axons and depend on acquisition, reconstruction, parcellation, and tracking choices.

Functional connectivity usually describes statistical dependence between measured signals, such as correlations among fMRI time series or tuning-related activity. It does not by itself establish a direct anatomical edge or the direction of influence. Effective connectivity refers to a model-based account of directed interactions, conditional on its assumptions and observations. These terms answer different questions; a correlation matrix, tractography matrix, and synapse table should not be combined as if they were the same measurement.

## Research threads

### Cellular wiring and neuron morphology

The [MICrONS functional connectomics dataset](../resources/datasets-and-benchmarks.md#microns-functional-connectomics-dataset) links dense calcium imaging with co-registered electron-microscopy reconstructions in a bounded mouse visual-cortex volume. Its matching activity and anatomy invite questions about whether cell morphology, response properties, and local connectivity covary. For a distinct species and reconstruction, [FlyWire Codex](../resources/datasets-and-benchmarks.md#flywire-codex-connectome-explorer) provides versioned adult-fly connectome snapshots and interactive query tools. Neither volume is a complete mammalian brain map.

Use [navis](../resources/software.md#navis) to inspect, transform, measure, and visualize neuron skeletons or meshes. Its morphology operations can characterize reconstructed arbors; they do not validate the underlying segmentation or prove that a geometric feature causes a connection. The [neuprint-python client](../resources/software.md#neuprint-python-client) supports programmatic queries over FlyEM-style neuron and synapse graphs, with a server, dataset choice, and authorization token required.

### Human regional connectomes and network measures

The [WU-Minn Human Connectome Project 1200 Subjects Release](../resources/datasets-and-benchmarks.md#wu-minn-human-connectome-project-1200-subjects-release) offers multimodal MRI and related data, including diffusion and functional imaging, for regional network analyses. Its broad coverage enables population-level questions but uses a very different measurement and node scale from cellular reconstruction; access requires a ConnectomeDB account and acceptance of the applicable data-use terms. Begin with the review [Imaging human connectomes at the macroscale](../resources/papers-and-reviews.md#imaging-human-connectomes-at-the-macroscale) for the choices involved in parcellation, mapping, and analysis.

The [Brain Connectivity Toolbox](../resources/software.md#brain-connectivity-toolbox) provides established graph measures for structural and functional brain-connectivity matrices. It is most useful after the matrix construction is justified: its documentation emphasizes that it offers limited network construction, different functions support different directed/weighted graph types, and measures should often be compared with suitable null networks. Its release page lists 2019 as the latest dated update, so check the function-level documentation and release notes for a specific analysis.

## Small project: test whether a graph statistic survives construction choices

Choose a small, already released connectome table or an HCP-derived regional matrix; do not mix the two. Define nodes, edge inclusion, direction, and weight before analysis. Produce a graph summary and a comparison across at least two defensible edge thresholds or parcellation choices, then compare the observed measure with a degree- or weight-aware null model appropriate to that graph. Deliver the construction rule, a diagram or matrix, summary plots, and a short account of changes across choices. Evaluate whether the claimed pattern survives those changes and whether the null preserves the relevant constraints. This is a suggested exercise, not a repository-run analysis; threshold and null choices can change results, and a stable graph statistic still does not establish function or causality.

## Limits and deeper evidence

Connectomes are measurements and reconstructions with explicit sampling boundaries. A missing edge may mean no detected connection, an unannotated segment, an omitted region, or an algorithmic false negative. A present edge may encode synapse count, estimated fiber probability, or signal dependence, each with different uncertainty. Graph statistics compress those choices further; check sensitivity to node definition, edge construction, missingness, and null model before interpreting a hub, motif, or community biologically. To claim a circuit mechanism, combine wiring with cell identity, physiology, perturbation, or behavior and test predictions that distinguish alternatives.

## Where to go next

Go to [circuits and dynamics](circuits-and-dynamics.md) to ask how interactions generate activity, [neurons and dendrites](neurons-and-dendrites.md) for cell morphology and mechanisms, and [coding and representations](coding-and-representations.md) for links between population activity and task variables. Methods: [neural data analysis](../methods/neural-data-analysis.md), [fitting and model comparison](../methods/fitting-and-model-comparison.md), [simulation](../methods/simulation.md), and [reproducible research](../methods/reproducible-research.md). Learning: [prerequisites](../learn/prerequisites.md), [learning paths](../learn/learning-paths.md), and [projects](../learn/projects.md). See [all topics](README.md) and the [resource library](../resources/README.md).
