# Learning paths

[Collection](../README.md) · [Learn](README.md) · [Topics](../topics/README.md) · [Methods](../methods/README.md) · [Resources](../resources/README.md) · [Community](../community/README.md)

Choose among orientation, neuron and circuit models, recordings, brain–AI comparisons, theory, and cross-background transitions. Each route is a suggested sequence through catalog entries, with a capability to check before moving on. It does not require following every route or programming from the outset.

| Route | A useful starting point | Observable outcome |
| --- | --- | --- |
| [Get oriented and explore a first model](#get-oriented-and-explore-a-first-model) | Basic algebra; coding can be learned alongside the route | Explain the assumptions in a small neuron model and predict how one change affects its output |
| [Model neurons and circuits](#model-neurons-and-circuits) | Basic programming and differential equations | Compare activity across input conditions while recording settings and seeds |
| [Work with neural recordings](#work-with-neural-recordings) | Arrays, plots, units, and descriptive statistics | Produce a quality-control summary and describe what it does not establish |
| [Connect brain and AI models](#connect-brain-and-ai-models) | One concrete behavior or representation question | Compare a model and baseline on a stated held-out condition |
| [Build a theoretical account](#build-a-theoretical-account) | Algebra; add calculus, probability, or linear algebra as needed | Write assumptions, derive a result, and identify a distinguishing prediction |
| [Bridge from a different background](#bridge-from-a-different-background) | A strength in at least one field and a question to carry across | Translate one concept between disciplines without claiming unsupported equivalence |

## Keep a short project record

For any route, keep a short note with the question, linked resource, data or model, settings, output, and one limitation. State units and relevant sampling intervals. If randomness or parameter choices affect the result, record the seed or sensitivity. Project ideas below are suggested exercises; this repository has not run them. Check the linked catalog entry for current instructions and requirements.

## Get oriented and explore a first model

**Before starting:** Basic algebra is useful. Programming is optional for the conceptual steps and can be learned as part of the exercise.

**Sequence:**

1. Choose a question in the [neuron and dendrite topic guide](../topics/neurons-and-dendrites.md) or [coding and representations](../topics/coding-and-representations.md).
2. Work through one item in [computational neuroscience courses](../resources/courses-and-lectures.md#neuromatch-academy-computational-neuroscience), or read a relevant section of [Neuronal Dynamics](../resources/books.md#neuronal-dynamics-from-single-neurons-to-networks-and-models-of-cognition).
3. Identify the model's variables, parameters, inputs, predicted observables, and at least one biological detail it leaves out. Use [prerequisite self-checks](prerequisites.md) only where you encounter a gap.

**Outcome:** Draw or describe the model and explain what each variable means. If you want a first computational exercise, plot a leaky integrate-and-fire neuron's voltage for three constant input levels and report the chosen inputs and spike counts over a fixed interval.

**Next step:** Continue to [neuron and circuit modeling](#model-neurons-and-circuits) or take a [theory route](#build-a-theoretical-account). Find concepts in the [topic guides](../topics/README.md) and learning material in [books](../resources/books.md).

## Model neurons and circuits

**Before starting:** Python fundamentals, arrays and plotting, and introductory differential equations are helpful. Check [mathematics](prerequisites.md#mathematics-and-quantitative-reasoning) and [programming](prerequisites.md#programming-and-scientific-computing) separately; neither assessment determines the other.

**Sequence:**

1. Read about [neuron and dendrite models](../topics/neurons-and-dendrites.md), then name the state variables, parameters, and predicted observables in the example you choose.
2. Choose a simulator in [software for cellular or network models](../resources/software.md#brian-2) and follow a documented example before adapting it.
3. Compare the model with [circuits and dynamics](../topics/circuits-and-dynamics.md) and the [simulation workflow](../methods/simulation.md) to make the question, controls, and outputs explicit.

**Outcome:** Adapt a small network model to compare activity under at least three input levels. Plot a raster or population rate, state the simulation duration and parameters, and repeat stochastic runs with recorded seeds. Interpret the pattern as behavior of the specified model, not evidence that the biological circuit behaves identically.

**Next step:** Use [fitting and model comparison](../methods/fitting-and-model-comparison.md) to ask which alternatives the simulation distinguishes, or visit [learning and plasticity](../topics/learning-and-plasticity.md).

## Work with neural recordings

**Before starting:** Familiarity with arrays, plots, units, sampling, and basic descriptive statistics. Choose a modality you can access or work with a synthetic example.

**Sequence:**

1. Select a measurement type in [neural data analysis](../methods/neural-data-analysis.md) and note its units, sampling, and preprocessing needs.
2. Find a suitable [dataset or benchmark](../resources/datasets-and-benchmarks.md) and read its provenance and access terms.
3. Make a quality-control summary before doing inference or spike sorting. Use the modality-specific [analysis software](../resources/software.md) and the [reproducible research workflow](../methods/reproducible-research.md) as needed.

**Outcome:** Plot raw traces or signal summaries for several channels, report the selected units and time interval, and explain why these checks flag conspicuous issues but do not establish neuron identity, signal quality in all respects, or a biological conclusion.

**Next step:** Choose a specific [neural data analysis method](../methods/neural-data-analysis.md), then define a held-out comparison appropriate to new trials, sessions, or subjects.

## Connect brain and AI models

**Before starting:** One task, neural representation, or learning question. Basic programming and neural-network knowledge help with implementations but are not prerequisites for reading and comparing claims.

**Sequence:**

1. State the question in terms of a behavior or measurement. Start from [coding](../topics/coding-and-representations.md), [learning](../topics/learning-and-plasticity.md), [perception and decision](../topics/perception-and-decision.md), or [NeuroAI](../topics/neuroai.md).
2. Read one entry in [NeuroAI model comparison](../topics/neuroai.md) and write down what a simpler account predicts.
3. Choose an evaluation in [datasets and benchmarks](../resources/datasets-and-benchmarks.md#brain-score) or model performance on an explicit behavioral condition.

**Outcome:** Compare a model with a baseline on held-out conditions, report performance by condition, and say what the metric supports. Success on a task or agreement under one metric alone does not establish shared biological computation.

**Next step:** Study the assumptions of the metric and data split using [fitting and model comparison](../methods/fitting-and-model-comparison.md), or follow a specific [topic](../topics/README.md).

## Build a theoretical account

**Before starting:** Algebra and the ability to follow definitions. Identify the mathematical technique required by the question; some routes need calculus, probability, linear algebra, dynamical systems, information theory, or control, but few require all of them at once.

**Sequence:**

1. Choose a question in [a topic guide](../topics/README.md) and write the phenomenon or data pattern that motivates it.
2. Read an appropriate source in [advanced theory](../resources/books.md#biophysics-searching-for-principles) or [papers and reviews](../resources/papers-and-reviews.md), tracking definitions and assumptions.
3. Follow [theory and model building](../methods/theory-and-model-building.md) to state the model, derive one consequence, and compare it with a nearby alternative.

**Outcome:** A short derivation with variables and assumptions defined, at least one limiting case or sanity check, and a prediction that could distinguish the account from a competitor. Code is optional unless the derivation's claim depends on a numerical result.

**Next step:** Find what measurement could constrain the prediction and use [model-to-brain comparison resources](../topics/neuroai.md) or a relevant [topic's evidence section](../topics/README.md).

## Bridge from a different background

Bring one idea from your previous training and test how far it carries. A biologist or experimentalist might connect measurement choices to model observables; a mathematician or physicist might translate a formal result into a neural prediction; a computer scientist or machine-learning learner might ask what biological claim a benchmark can support. These are entry points, not job-title tracks.

**Sequence:** Choose one cross-field pair—measurement and model, equation and mechanism, task and behavior, or representation and brain data. Read one relevant [topic guide](../topics/README.md), the associated [method](../methods/README.md), and one resource from [the catalog](../resources/README.md). Then use a prerequisite self-check only for the missing bridge.

**Outcome:** A short comparison that defines the terms on both sides, states one useful connection, and names one place the analogy breaks down.

**Next step:** Make the comparison concrete with one [suggested project](projects.md) or facilitate it as a [reading-group activity](teaching.md).

## Continue toward a specialist question

After a first model or analysis, choose a question rather than taking every advanced route. [Connectomics](../topics/connectomics.md) pairs wiring data with graph interpretation; [development](../topics/development-and-self-organization.md) examines how structure can emerge from rules. [Computational psychiatry](../topics/computational-psychiatry.md) connects model-based behavior and reference distributions to individual variation. [Neuromorphic computing](../topics/neuromorphic-computing.md) connects event models to implementation and measurement.

For research training with theory–experiment collaboration, inspect the [MBL course](../resources/courses-and-lectures.md#mbl-methods-in-computational-neuroscience). For a focused model-based behavioral route, inspect the [Computational Psychiatry Course](../resources/courses-and-lectures.md#computational-psychiatry-course). Participation and material access vary; use the catalog entries and official course pages to check conditions.
