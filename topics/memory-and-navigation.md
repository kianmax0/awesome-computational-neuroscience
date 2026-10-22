# Memory and navigation

[Collection overview](../README.md) · [All topics](README.md) · [Learn](../learn/README.md) · [Methods](../methods/README.md) · [Resource library](../resources/README.md)

Memory and navigation research asks how neural activity supports spatial maps, routes, associations, and the retention of experience. Models range from simplified place and grid-cell networks to agents moving through environments; connecting a model’s internal state to recorded activity requires explicit observables and task assumptions.

## Questions to bring

- What is remembered: location, trajectory, context, sequence, or a learned association?
- Which neural or behavioral signatures distinguish candidate spatial representations?
- How do movement, sensory cues, and internal dynamics interact?
- Does the model generalize when the environment, route, or sensory context changes?

## Prerequisites

Understand vectors, coordinate frames, basic dynamical systems, and time-series data. For neural recordings, know how to align spikes or imaging signals with position and behavior. For navigation simulations, understand state, action, reward, and how the environment’s geometry constrains possible paths.

## A short start route

1. Define the behavioral quantity, such as position error, path choice, or recall accuracy.
2. Visualize trajectories and neural activity in the same coordinate system.
3. Choose a simple baseline map or memory model before adding recurrent or learned structure.
4. Evaluate on new paths or environmental changes, and separate interpolation from true generalization.

## Research threads

### Hippocampal microcircuits and spatial codes

Place and grid cells provide complementary empirical and theoretical targets. [Hippocampal Microcircuits: A Computational Modeler's Resource Book](../resources/books.md#hippocampal-microcircuits-a-computational-modelers-resource-book) is a focused entrance to hippocampal modeling. The review [Grid Cells and Spatial Maps in Entorhinal Cortex and Hippocampus](../resources/papers-and-reviews.md#grid-cells-and-spatial-maps-in-entorhinal-cortex-and-hippocampus) connects spatially periodic codes with mapping and remapping questions. Reproducing a spatial firing pattern does not by itself explain how animals use it.

### Navigation models and environment structure

[RatInABox](../resources/software.md#ratinabox) provides simulated movement and neural activity for spatial modeling. [NeuralPlayground](../resources/software.md#neuralplayground) supports experiments on neural representations in embodied environments. These tools make it easier to test controlled conditions, but their built-in movement statistics and sensory assumptions shape the data. The [Models of Vector Navigation with Grid Cells](../resources/tutorials-and-examples.md#models-of-vector-navigation-with-grid-cells-modeldb) and [Place and Grid Cells in a Loop](../resources/tutorials-and-examples.md#place-and-grid-cells-in-a-loop-modeldb) offer specific model implementations for inspection.

### Experience, association, and neural evidence

Associative memory can link sensory cues, places, and outcomes; the resulting code may change with context. The [Odor-Place Spatial Association Task](../resources/datasets-and-benchmarks.md#odor-place-spatial-association-task-dandi001539) supplies a dataset route for relating recorded activity to a learned spatial association. Its task design and recording coverage constrain which learning or memory claims the data can support.

## Small project: test a spatial code across environments

Simulate an agent moving through a two-dimensional arena and construct a simple place-like or grid-like population code. Deliver the movement generator, activity maps, a position decoder, and a comparison between familiar and altered trajectories. Evaluate error as a function of training coverage and test whether the code still decodes after a controlled cue or route change. Include a non-neural baseline based on recent position. This is a proposed project, not a repo-run analysis; simulated maps do not establish that biological circuits use the same code or learning process.

## A useful comparison

Split spatial data by contiguous trajectory, route, or session to reduce leakage from neighboring positions. Compare against a behavior-only or recent-position baseline. Report occupancy maps so apparent neural fields can be interpreted against where the animal actually sampled.

## Limits and deeper evidence

Spatial data contain strong autocorrelation: random train/test splits can leak nearby positions across partitions. Occupancy, speed, head direction, and sensory cues can mimic or modulate apparent spatial tuning. Report sampling coverage and use splits by trajectory or session. ModelDB implementations are valuable for reproducibility and extension, but inspect the original question and assumptions; a successful recreation is not independent evidence for mechanism.

## Where to go next

See [coding and representations](coding-and-representations.md) for population geometry, [learning and plasticity](learning-and-plasticity.md) for experience-dependent change, and [circuits and dynamics](circuits-and-dynamics.md) for recurrent population behavior. Methods: [simulation](../methods/simulation.md), [neural data analysis](../methods/neural-data-analysis.md), [fitting and model comparison](../methods/fitting-and-model-comparison.md), [reproducible research](../methods/reproducible-research.md). Learning: [prerequisites](../learn/prerequisites.md), [learning paths](../learn/learning-paths.md), [projects](../learn/projects.md), [teaching](../learn/teaching.md). See [all topics](README.md), the [collection overview](../README.md), and [resources](../resources/README.md).
