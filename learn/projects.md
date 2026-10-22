# Suggested projects

[Collection](../README.md) · [Learn](README.md) · [Topics](../topics/README.md) · [Methods](../methods/README.md) · [Resources](../resources/README.md) · [Community](../community/README.md)

These are project prompts, not completed analyses or claims about expected results. The repository has not run them or checked the current instructions of linked software and datasets. Before using an external tool, data release, or example, consult its catalog entry and documentation for current versions, access terms, and requirements. Keep the question small enough that assumptions, controls, and output can be inspected.

For each project, make a note of the scientific question, data or model, settings, output, control, and limitation. Label axes and units, and record software versions and random seeds when applicable. A convincing plot alone does not establish a biological explanation.

## Single neuron or small circuit

**Question:** How does a simple cell or small circuit respond as input changes?

**Suggested exercise:** Implement or adapt a leaky integrate-and-fire neuron, or use a documented small network example from [software for spiking network simulation](../resources/software.md#brian-2). Plot membrane voltage or a spike raster at several input levels. State time step, duration, parameters, and units; for a stochastic circuit, include repeated seeds.

**Control:** Compare with a no-input condition or an analytically expected limiting case, and change one parameter at a time.

**Limit:** A model's spike pattern does not identify the mechanism used by a biological neuron. The point-neuron model also omits morphology and other mechanisms.

**Continue:** [Neuron models](../topics/neurons-and-dendrites.md), [circuits and dynamics](../topics/circuits-and-dynamics.md), and [simulation](../methods/simulation.md).

## Recording quality control

**Question:** What can be learned from an initial inspection of a neural recording, before inference?

**Suggested exercise:** Select a short interval from an accessible dataset in [datasets and benchmarks](../resources/datasets-and-benchmarks.md). Plot a few channels and report the interval, units, and per-channel RMS amplitude or robust percentile range. If using synthetic data with known events, add a comparison to those known events.

**Control:** Compare channels with an appropriate reference or known-good segment, if the dataset provides one, and check whether units and sampling are consistent.

**Limit:** These summaries can flag conspicuous differences. They do not establish unit quality, spike identity, absence of artifacts, or experimental validity.

**Continue:** [Neural data analysis](../methods/neural-data-analysis.md), [recording software](../resources/software.md), and the modality-specific tools in the [software catalog](../resources/software.md#neural-data-analysis).

## Fit a model to behavior

**Question:** Which simple model captures a behavioral pattern, and which comparison would challenge that account?

**Suggested exercise:** Choose a decision or memory task from [datasets and benchmarks](../resources/datasets-and-benchmarks.md), or define a small simulated task. Fit or simulate one candidate model and compare its predictions with a simple baseline on trials held out according to the question. Report performance by condition rather than only one aggregate score.

**Control:** Estimate any preprocessing or baseline parameters from training data only. Consider whether the split tests generalization to trials, sessions, or subjects.

**Limit:** Better predictive performance on a selected split does not alone identify a cognitive or neural mechanism. Parameter estimates may be weakly constrained or non-unique.

**Continue:** [Perception and decision](../topics/perception-and-decision.md), [memory and navigation](../topics/memory-and-navigation.md), and [fitting and model comparison](../methods/fitting-and-model-comparison.md).

## Derive a theoretical result

**Question:** What follows from a set of explicit assumptions about a neural model?

**Suggested exercise:** Select a claim from a relevant [topic guide](../topics/README.md) or a paper in [papers and reviews](../resources/papers-and-reviews.md). Define variables, assumptions, and a nearby alternative. Derive one consequence or steady state, then test a limiting case by hand. Use a numerical check only if it is useful to verify the algebra.

**Control:** Check dimensions, signs, a limiting case, or an independently derived special case.

**Limit:** A valid derivation establishes a consequence of the assumptions; biological relevance depends on whether the assumptions and predictions match evidence.

**Continue:** [Theory and model building](../methods/theory-and-model-building.md), [mathematical foundations](../resources/books.md#mathematics-for-machine-learning), and the [advanced theory books](../resources/books.md#biophysics-searching-for-principles).

## Compare a model with brain measurements

**Question:** Does an artificial or theoretical model capture a neural or behavioral pattern beyond a simple alternative?

**Suggested exercise:** Choose a model and comparison task from [NeuroAI resources](../topics/neuroai.md) and a suitable evaluation from [datasets and benchmarks](../resources/datasets-and-benchmarks.md#brain-score). State the predicted observable, fit or tune on one portion, and evaluate on a separately held-out condition or dataset as appropriate.

**Control:** Include a baseline, report uncertainty or variability when possible, and document the exact preprocessing and comparison metric.

**Limit:** Similarity under a chosen metric does not prove identical representations, mechanisms, or causal organization. Interpret the comparison at the level supported by its data and design.

**Continue:** [NeuroAI](../topics/neuroai.md), [fitting and model comparison](../methods/fitting-and-model-comparison.md), and [reproducible research](../methods/reproducible-research.md).

## Adapt the scope

Each prompt can be done as a paper discussion or hand derivation, a small notebook, or a larger implementation. For a no-code version, sketch expected outcomes and compare them with a figure or documented output. For a coding version, retain the same question and control, and add implementation details rather than expanding the scientific claim.

## Domain-specific project routes

| Question | Suggested output | Full prompt |
| --- | --- | --- |
| What does a wiring graph preserve or omit? | A declared adjacency construction, a baseline graph comparison, and a statement of scale and sampling limits. | [Connectomics](../topics/connectomics.md). |
| How does a local cue affect a growing arbor? | Growth-rule pseudocode, morphology plots, and branching statistics across seeds. | [Development](../topics/development-and-self-organization.md). |
| What can a model say about individual variation? | A reference or behavioral model, held-out diagnostics, and a comparison that respects participants and sites. | [Computational psychiatry](../topics/computational-psychiatry.md). |
| How does hardware mapping change a model? | Conversion settings and output agreement; physical latency or power only if measured. | [Neuromorphic computing](../topics/neuromorphic-computing.md). |
| What remains uncertain after fitting a simulator? | Parameter recovery, predictive checks, and a comparison across observation summaries. | [Simulation-based inference](../methods/simulation-based-inference.md). |
| Does an association estimate an intervention effect? | A graph with defined semantics and a synthetic adjusted/unadjusted comparison. | [Causal inference and design](../methods/causal-inference-and-experimental-design.md). |
