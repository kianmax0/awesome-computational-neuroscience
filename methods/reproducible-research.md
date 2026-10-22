# Reproducible research

[Collection](../README.md) · [Learn](../learn/README.md) · [Topics](../topics/README.md) · [Methods](README.md) · [Resources](../resources/README.md) · [Community](../community/README.md)

Use this workflow whenever a result depends on data processing, code, model configuration, or human decisions that another researcher would need to inspect or repeat. Reproducibility is part of the method: preserve enough provenance to understand how the reported result came from its inputs.

## When to use this workflow

- You run an analysis or simulation that may need to be checked, extended, or rerun.
- You combine data, code, software packages, or model files from several sources.
- You plan to share a dataset, model, notebook, or computational result.
- You need to distinguish a successful run from a reproducible result.

Apply the steps early. Adding provenance after a complex project can be costly and incomplete.

## Prerequisites

Know the question, data source, analysis or simulation steps, and outputs that support the claim. For coding projects, use version control and a documented environment. For data, confirm access rights, consent limits, and any sharing restrictions before copying or publishing files.

## Inputs and outputs

**Inputs:** source data and metadata; code, notebooks, model definitions, and configurations; software and hardware dependencies; and decisions made during curation or analysis.

**Outputs:** an organized project with provenance; an environment or dependency record; documented commands or workflow steps; quality-control evidence; and an access or sharing plan appropriate to the data.

## Decision sequence

1. **Define the result to reproduce.** Identify the figure, statistic, prediction, or simulation outcome and the exact inputs that generated it.
2. **Track data provenance.** Record original source, version or release, download date, identifiers, metadata, and transformations. Keep raw data distinct from derived data when permissions allow.
3. **Organize the project.** Use stable paths and separate source data, derived data, code, configuration, results, and documentation. Avoid relying on machine-specific absolute paths.
4. **Version code and model choices.** Commit meaningful source changes and configuration, including parameter values, random seeds, and data-selection rules. Do not commit secrets or restricted data.
5. **Record the environment.** Capture language, package versions, operating system or container image, simulator version, and hardware details when numerical behavior may depend on them.
6. **Make the run executable.** Provide a documented command or ordered steps from prepared inputs to outputs. A clean-session rerun is a useful check; interactive notebooks should state execution order and required files.
7. **Preserve intermediate evidence.** Save quality-control plots, exclusions, logs, convergence checks, and data dictionaries that help diagnose the result without exposing restricted observations.
8. **Check determinism and variability.** Fix and record seeds when appropriate, but also repeat stochastic analyses to quantify variation. Record nondeterministic hardware or parallel behavior where it affects outputs.
9. **Verify the rerun.** Recreate key outputs from documented inputs in a fresh environment or session. Compare numerical results within an explicit tolerance and inspect plots or tables for meaningful differences.
10. **Prepare sharing and citation.** Choose a repository or archive, cite data and software, include licenses and access terms, and state what is unavailable and why.

## Evaluation

A useful reproducibility check allows another person to identify the source data, understand transformations, and recover the key reported outputs. Check file paths from a clean clone or copy, document software versions, and include expected output names. For simulations, preserve seeds and configurations; for empirical analyses, record data versions, exclusions, and split assignments.

Use established data formats where they fit the modality. [NWB](../resources/standards.md#neurodata-without-borders-nwb) supports neurophysiology data organization; [BIDS](../resources/standards.md#brain-imaging-data-structure-bids) organizes neuroimaging and related datasets; [NeuroML](../resources/standards.md#neuroml) describes computational neuroscience models. A standard helps interoperability but does not replace documentation or validation.

## Limitations

Reproducibility does not guarantee correctness, strong inference, or biological validity. Exact bitwise reproduction may be impossible across hardware, software versions, or nondeterministic operations. Data access terms may prevent redistribution; document the route to access rather than sharing files without authorization. A notebook that runs once on its author's machine is not sufficient evidence that others can reproduce the result.

## Selected resources

- [Neurodata Without Borders](../resources/standards.md#neurodata-without-borders-nwb) — a standard for organizing and sharing neurophysiology data.
- [Brain Imaging Data Structure](../resources/standards.md#brain-imaging-data-structure-bids) — conventions that make imaging datasets and derivatives more portable.
- [NeuroML](../resources/standards.md#neuroml) — standardized descriptions for sharing computational neuroscience models.
- [DANDI Archive](../resources/datasets-and-benchmarks.md#dandi-archive) — an archive for sharing neurophysiology datasets and related resources.
- [OpenNeuro](../resources/datasets-and-benchmarks.md#openneuro) — a repository for public neuroimaging datasets.
- [INCF](../resources/community.md#incf) — community resources and standards supporting interoperable neuroscience research.

## Continue

Use the relevant [topic](../topics/README.md) and [resource](../resources/README.md) pages to find data, software, and standards for a project. Pair this guide with [simulation](simulation.md), [neural data analysis](neural-data-analysis.md), or [fitting and model comparison](fitting-and-model-comparison.md) to capture the details that affect each result.

For concrete infrastructure, [DataLad](../resources/software.md#datalad) connects data versions and computational provenance, while [Neurodesk](../resources/software.md#neurodesk) provides versioned analysis environments. A reproducible environment still needs documented data access, analysis choices, and result checks.
