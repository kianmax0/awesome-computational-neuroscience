# Modular prerequisites

[Collection](../README.md) · [Learn](README.md) · [Topics](../topics/README.md) · [Methods](../methods/README.md) · [Resources](../resources/README.md) · [Community](../community/README.md)

Use these checks to decide what would help with a particular question. They are independent skill areas, not stages in one universal beginner-to-expert sequence. You can begin with concepts or theory before programming; you can also learn a tool while filling a biology or mathematics gap.

Each self-check has three useful responses: **ready** (continue), **review** (use a linked resource and repeat the check), or **defer** (choose a route that does not require this skill yet).

## Biology and neural systems

| Capability | Self-check | If you want a bridge |
| --- | --- | --- |
| Cells, synapses, and circuits | Sketch a neuron, label input, output, and synapse, and name one feature a point-neuron model omits. | Start with [biological background](../resources/books.md#brain-facts-a-primer-on-the-brain-and-nervous-system) or the [neurons and dendrites guide](../topics/neurons-and-dendrites.md). |
| Neural signals and measurement | Distinguish a spike train, a calcium trace, and an EEG signal by what is measured and at what scale. | Use the introductory neural-signal materials in [Neuromatch](../resources/courses-and-lectures.md#neuromatch-academy-computational-neuroscience) and connect them to the [measurement workflow](../methods/neural-data-analysis.md). |
| Linking a model to biology | Given a model variable, state which observation could constrain it and one alternative explanation for the same observation. | Use a [topic guide](../topics/README.md) to situate the question, then the [NeuroAI guide](../topics/neuroai.md). |

For a longer biological bridge, [Neuroscience Online](../resources/books.md#neuroscience-online) connects membrane mechanisms, synapses, sensory and motor systems, and higher functions. Choose the chapters relevant to the model you want to understand.

You do not need a complete survey of neuroscience before studying a model. Learn the biological detail needed to interpret the quantities and claims in front of you.

## Mathematics and quantitative reasoning

| Capability | Self-check | If you want a bridge |
| --- | --- | --- |
| Algebra, functions, and units | Rearrange a linear equation, plot a function, and check whether both sides of a physical equation have compatible units. | Browse [mathematical foundations](../resources/books.md#mathematics-for-machine-learning). |
| Calculus and differential equations | Explain how a derivative describes change and interpret the steady state of a first-order differential equation. | Use [Notes on Diffy Qs](../resources/books.md#notes-on-diffy-qs-differential-equations-for-engineers) alongside [neuron models](../topics/neurons-and-dendrites.md). Calculus is not needed for every introductory route. |
| Linear algebra | Interpret a vector of neural activity and describe what multiplying it by a matrix does. | Review [Interactive Linear Algebra](../resources/books.md#interactive-linear-algebra) and connect it to [population coding](../topics/coding-and-representations.md). |
| Probability and statistics | Explain a probability distribution, distinguish a mean from variability, and say why independent held-out data are useful. | Start with [Statistical Thinking for the 21st Century](../resources/books.md#statistical-thinking-for-the-21st-century) or [statistical modeling and inference](../methods/fitting-and-model-comparison.md). |

## Programming and scientific computing

| Capability | Self-check | If you want a bridge |
| --- | --- | --- |
| Read and change a short program | Change one input, run the program again, and identify which output changed. | Begin with [Software Carpentry: Programming with Python](../resources/courses-and-lectures.md#software-carpentry-programming-with-python). |
| Arrays, plotting, and file formats | Load a small array, describe its dimensions and sampling interval, and plot it with labeled axes and units. | Use [NumPy: the absolute basics](../resources/tutorials-and-examples.md#numpy-the-absolute-basics-for-beginners), then a modality in [neural data analysis](../methods/neural-data-analysis.md). |
| Reproducible computation | Record the data identifier, key settings, software version, and random seed for a result that uses randomness. | Read [reproducible research](../methods/reproducible-research.md) and the relevant [standards](../resources/standards.md). |

Choose a route that matches your current access and interests. [Simulation](../methods/simulation.md) is a way to explore a model; it is not required to understand every theoretical argument.

## Experimental measurement and study design

| Capability | Self-check | If you want a bridge |
| --- | --- | --- |
| Modality and sampling | State what is measured, the unit, sampling interval, and one limitation for a chosen recording type. | Use [neural data analysis](../methods/neural-data-analysis.md) to connect a modality to its units, preprocessing, and interpretation; consult the corresponding package documentation for a concrete recording example. |
| Controls and comparisons | Name a baseline or control that would help distinguish the proposed explanation from a simpler one. | Use [fitting and model comparison](../methods/fitting-and-model-comparison.md) or a related [topic guide](../topics/README.md). |
| Data and provenance | Identify whether a dataset is public, synthetic, or restricted, and what provenance or consent information travels with it. | Begin with [datasets and benchmarks](../resources/datasets-and-benchmarks.md) and [data standards](../resources/standards.md). |

## Pick only the next useful check

For a first neuron simulation, algebra and the ability to inspect a simple program may be enough. For a derivation, start with the mathematical ideas the derivation uses; you can defer coding. For recording analysis, add modality, units, sampling, and basic statistics. For a model-to-brain comparison, also ask whether the measurement and comparison metric can support the biological claim being made.

When a gap becomes concrete, use the corresponding [learning path](learning-paths.md) or [suggested project](projects.md). For a method-specific sequence, see [theory and model building](../methods/theory-and-model-building.md), [simulation](../methods/simulation.md), [neural data analysis](../methods/neural-data-analysis.md), or [fitting and model comparison](../methods/fitting-and-model-comparison.md).
