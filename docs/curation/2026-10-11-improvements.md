# Navigation and maintenance improvements — 2026-10-11

This pass builds on the [2026-10-05 coverage audit](2026-10-05-expansion.md). That audit remains a dated snapshot. The current catalog adds two independent resources, bringing the total from 136 to 138; learning-path references and companion documentation do not count as additional resources.

## Reader navigation

The [learning paths](../learning-paths.md) turn the four README starting points into prerequisites, ordered steps, and small projects with observable outputs. These are editorial suggestions, not a claim that every linked tutorial has been executed. README also links directly to the recording-modality subsections.

## Resource decisions

| Resource | Placement and gap | Primary evidence checked | Access and verification boundary |
| --- | --- | --- | --- |
| [NeuroGym](https://neurogym.github.io/neurogym/latest/) | Memory and spatial navigation; adds non-spatial working-memory tasks alongside the existing spatial models. | Official [working-memory task catalog](https://neurogym.github.io/neurogym/latest/api/tags/working_memory/) and [PyTorch example](https://neurogym.github.io/neurogym/latest/examples/supervised_learning_pytorch/) describe delayed matching and recurrent-network training on a perceptual decision task. | Public Python package and documentation. Examples use their own ML dependencies. Pages and repository inspected; training not run. This is a task collection, not biological validation of a model. |
| [MEArec](https://mearec.readthedocs.io/en/latest/) | Neural data analysis / Benchmarks; adds a source of simulated ground truth for evaluating spike sorting. | Official documentation and [installation guide](https://mearec.readthedocs.io/en/latest/installation.html) describe extracellular-recording generation and template-generation dependencies. | Public Python package and CLI. Generating new templates requires NEURON and LFPy. Documentation and repository inspected; simulations not run. Synthetic ground truth does not replace evaluation on experimental recordings. |

SpikeInterface's [comparison documentation](https://spikeinterface.readthedocs.io/en/latest/modules/comparison.html) is linked from its existing entry. It distinguishes comparison to known spike times from agreement between sorters; agreement alone is not a ground-truth accuracy measurement. This is a companion link, not a third resource.

The MEArec and NeuroGym repositories were accessible and did not display archive or deprecation notices during review. This is a point-in-time documentation check, not a guarantee of future maintenance or compatibility.

Two existing access descriptions were corrected from their publisher pages: [Bayesian Brain](https://mitpress.mit.edu/9780262042383/bayesian-brain/) lists both print editions as out of print and offers a sample chapter; [Embodied Sensorimotor Control](https://www.annualreviews.org/content/journals/10.1146/annurev-bioeng-102723-020454) states a CC BY-NC-ND 4.0 license, so the previous subscription-dependent description was removed. Automated 403 responses from these pages are distinct from their content and access terms.

## Check scope

The previous workflow sent all Markdown, including historical rejected candidates, to the external link checker. The earlier audit explicitly retains 404s and unavailable legacy hosts, so that scope conflated current recommendations with screening evidence.

The workflow now checks local files and heading anchors across all Markdown, then checks external links outside `docs/curation/`. Both steps retain failure status and produce separate reports. Current recommendations must remain in the README or learning paths to stay in the external check. No HTTP error codes have been accepted and no new URL exceptions have been added.

Resource suggestions and pull requests now ask for access requirements and what was actually verified. Use the [maintenance guide](../../MAINTAINING.md#local-checks) to reproduce the checks.

## Dependency review

`npm ci` and Markdown lint succeeded on Node.js 24.11.0. `npm audit` reported nine findings in the development-only lint toolchain (three low, one moderate, five high). A dry run of `npm audit fix` changed no packages; its proposed forced fix would downgrade the pinned `markdownlint-cli2` release. The dependency files were retained, and Dependabot remains enabled. Recheck the advisories when an upstream compatible release becomes available; this pass does not claim a clean dependency audit.

## Validation results

- Markdown lint passed across all 12 Markdown files. Local file and anchor checks passed, and the catalog contains 138 entries with no duplicate primary URLs.
- A temporary fixture confirmed that the local check rejects broken README anchors and broken file links inside historical curation notes. Input inspection confirmed that the external check excludes historical notes while retaining current reader-facing documents.
- The updated workflow and resource-suggestion form parsed as YAML. GitHub Actions itself was not run from this local editing session.
- The full external check with lychee 0.24.2 reported 230 link occurrences: 221 successful, two pre-existing exclusions, and seven errors. These are link occurrences, not resource counts. All new public-guide URLs passed. The errors below remain visible; an accessible page in the web reader is not recorded as a passing automated check.

| Existing resource entrance | Automated result | Follow-up |
| --- | --- | --- |
| [Bayesian Brain](https://mitpress.mit.edu/9780262042383/bayesian-brain/) | HTTP 403 | Publisher content opened in web reader; out-of-print description corrected. |
| [The Computational Neurobiology of Reaching and Pointing](https://mitpress.mit.edu/9780262195089/the-computational-neurobiology-of-reaching-and-pointing/) | HTTP 403 | Publisher content opened in web reader; retain canonical entrance. |
| [Embodied Sensorimotor Control](https://www.annualreviews.org/content/journals/10.1146/annurev-bioeng-102723-020454) | HTTP 403 | Publisher content opened in web reader; license description corrected. |
| [Synaptic Plasticity Forms and Functions](https://www.annualreviews.org/content/journals/10.1146/annurev-neuro-090919-022842) | HTTP 403 | Publisher content opened in web reader; retain canonical entrance. |
| [NESTML pair-STDP model](https://github.com/nest/nestml/blob/main/models/synapses/stdp_synapse.nestml) | HTTP 503 | The model source opened in web reader; automated availability remains unresolved. |
| [Neuronal Dynamics cognitive-model lectures](https://lcnwww.epfl.ch/gerstner/NeuronalDynamics-MOOC2.html) | Connection closed | Official course page opened in web reader; automated availability remains unresolved. |
| [The Algonauts Project](https://algonautsproject.com/) | Connection closed | Official project page opened in web reader; automated availability remains unresolved. |
