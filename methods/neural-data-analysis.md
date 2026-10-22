# Neural data analysis

[Collection](../README.md) · [Learn](../learn/README.md) · [Topics](../topics/README.md) · [Methods](README.md) · [Resources](../resources/README.md) · [Community](../community/README.md)

Use this workflow when a scientific question depends on measurements from neural or behavioral recordings. The analysis should preserve the meaning and limitations of the measurement while turning it into quantities that can answer the question. Processing is not neutral: filtering, sorting, alignment, exclusion, and aggregation can change what remains visible.

## When to use this workflow

- You need to characterize signal quality before testing a hypothesis.
- You need to extract spikes, events, behavioral variables, or population activity from recordings.
- You need to relate neural activity to stimuli, actions, internal states, or behavior.
- You need to evaluate a model against measurements or compare recording conditions.

Choose procedures by modality and question. Extracellular spikes, calcium imaging, EEG/MEG, fMRI, and video have different measurement models and failure modes.

## Prerequisites

Know the acquisition modality, units, sampling rate, trial or session structure, and relevant experimental design. Use descriptive statistics and visualization before complex inference. Consult modality-specific tutorials and [data standards](../resources/standards.md) as needed. Coding is useful for large or repeatable analyses, though hand inspection and analytic work can be part of a valid early-stage investigation.

## Inputs and outputs

**Inputs:** raw or minimally processed data; metadata and acquisition details; experimental events and behavioral annotations; quality criteria; and a stated question with a target measurement.

**Outputs:** quality-control summaries; documented preprocessing and exclusions; analysis-ready signals or features; estimates with uncertainty; and a record of the data versions and transformations.

## Decision sequence

1. **Translate the question into measurements.** Decide what neural or behavioral quantity could support or challenge the claim, at what temporal and spatial scale.
2. **Inventory data and metadata.** Confirm sampling rates, channels, units, trial boundaries, missing values, synchronization, subject/session identifiers, and permissions. Record the data source and version.
3. **Plot before transforming.** Inspect raw traces, events, image fields, or behavior. Look for saturation, drift, movement, missing segments, misalignment, and unusual channels or trials.
4. **Define exclusions in advance.** Set criteria tied to acquisition or analysis quality. Summarize how many channels, trials, units, or sessions each rule removes, and check whether exclusions track condition or behavior.
5. **Choose preprocessing for the target.** Apply filtering, artifact handling, spike sorting, motion correction, or image preprocessing only when the measurement model and target justify it. Preserve an unprocessed path and document parameters.
6. **Align measurements to events.** Verify synchronization and event definitions. Decide whether analysis uses fixed windows, continuous time, trials, or sessions, and guard against leakage across these units.
7. **Build interpretable summaries.** Use units and uncertainty, inspect distributions and individual subjects, and retain within-subject structure. Choose a model appropriate to repeated measures, counts, signals, or latent variables.
8. **Evaluate against controls or references.** Use known labels, synthetic data, repeated measurements, or negative controls when available. Check that the pipeline recovers expected signals and does not create them under a null condition.
9. **Check sensitivity.** Test reasonable preprocessing settings, exclusion thresholds, time windows, and aggregation choices. A conclusion that changes under a small defensible choice should be reported as sensitive.
10. **Interpret at the measurement level.** State what the processed quantity represents and what it cannot establish. Route explicit parameter estimation or competing generative accounts to [fitting and model comparison](fitting-and-model-comparison.md).

## Evaluation

Quality control asks whether the data and transformations support the intended measurement; inference asks whether the measured pattern supports the scientific claim. Keep those questions distinct. Plot distributions and example traces alongside group summaries. Report uncertainty and variation across relevant experimental units, not only the number of samples or time points.

For decoding, compare with a baseline and keep held-out data separated at the level relevant to generalization, such as trials, sessions, or subjects. For spike sorting or signal extraction, use ground truth, synthetic recordings, or manual curation where available. For imaging and electrophysiology, inspect alignment and artifact sensitivity before treating derived events as neural activity.

## Limitations

Recorded signals are indirect and may mix biological activity with instrumentation, preprocessing, and behavior. A statistical association does not establish a causal mechanism. Large sample counts can overstate precision when trials are nested within a small number of subjects or sessions. Performance on a benchmark does not guarantee validity for a different modality or acquisition protocol.

## Selected resources

- [Neural data science: accelerating the experiment-analysis-theory cycle](../resources/papers-and-reviews.md#neural-data-science-accelerating-the-experiment-analysis-theory-cycle-in-large-scale-neuroscience) — frames signal extraction and modeling around the questions recordings can answer.
- [Neural Data Science in Python](../resources/books.md#neural-data-science-in-python) — worked analysis examples across single-unit recordings, EEG, and fMRI.
- [NiPraxis](../resources/books.md#nipraxis-practice-and-theory-of-brain-imaging) — connects imaging data structure, regression, and reproducibility.
- [SpikeInterface](../resources/software.md#spikeinterface) — tools and documentation for extracellular recording, preprocessing, sorting, and validation.
- [Neural Latents Benchmark](../resources/datasets-and-benchmarks.md#neural-latents-benchmark) — datasets and evaluation tasks for latent-variable methods on population recordings.
- [Neurodata Without Borders](../resources/standards.md#neurodata-without-borders-nwb) — a data standard for sharing and organizing neurophysiology recordings.

## Continue

Select a setting from [topics](../topics/README.md), then use [reproducible research](reproducible-research.md) to keep transformations traceable. For a theoretical interpretation, see [theory and model building](theory-and-model-building.md); for parameter estimation and predictions, see [fitting and model comparison](fitting-and-model-comparison.md).

To connect analysis assumptions with acquisition, inspect the [Open Ephys GUI](../resources/software.md#open-ephys-gui) documentation for recording configuration and platform requirements. [Connectomics](../topics/connectomics.md) and [computational psychiatry](../topics/computational-psychiatry.md) add data-specific questions about graph construction, sampling, sites, and individual variation.
