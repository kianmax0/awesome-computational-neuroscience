# Advanced modeling and research interpretation — 2026-10-11

This review targets the transition from implementing models to fitting, interpreting, and comparing them. It checks the current entries in all seven `resources/*.md` pages and follows candidates to primary documentation, papers, and repositories. `Accept` records an editorial recommendation with inspected content and access evidence; it does not mean a software installation, tutorial, or experiment was run.

The review keeps Neuromatch curricula and their episodes together, does not duplicate the existing advanced books, and leaves simulation-based inference, NeMoS, and Wilson and Collins's behavioral-modeling tutorial to the parallel methods review. Suggested exercises below are learning outcomes proposed by this review, not claims that the source supplies or that we executed those exact exercises.

## Accepted resources

### BluePyOpt

- **Canonical URL:** [BluePyOpt stable documentation](https://bluepyopt.readthedocs.io/en/stable/).
- **Stage:** Advanced implementation to research modeling.
- **Prerequisites:** Python, conductance-based neuron models, electrophysiological features, and an existing understanding of simulation. The documentation specifies Python 3.9+ and NEURON with Python support for the default electrophysiology route; Arbor is an optional backend.
- **Access:** Free documentation and code. Model optimization can require more computation than a single simulation.
- **Evidence:** The [quick-start documentation](https://bluepyopt.readthedocs.io/en/stable/#quick-start) contains a two-conductance single-compartment example, detailed layer-5 pyramidal and thalamocortical cells, and synaptic-plasticity fitting. The [original methods paper](https://www.frontiersin.org/journals/neuroinformatics/articles/10.3389/fninf.2016.00017/full) explains feature-based objectives and multiobjective optimization.
- **Maintenance:** The [current repository](https://github.com/openbraininstitute/BluePyOpt) is under Open Brain Institute. Its live GitHub API returned `archived: false` and `disabled: false`; [release 1.14.25](https://github.com/openbraininstitute/BluePyOpt/releases/tag/1.14.25) was published on 2026-08-24. No installation was attempted.
- **Placement:** `resources/simulators.md`, proposed `Model fitting` section. The existing NEURON, Arbor, and Jaxley entries do not substitute for a dedicated feature-based parameter-optimization workflow.
- **Suggested outcome:** Fit the introductory conductances, then compare fitted responses on an additional current stimulus withheld from the fitting objectives.

Ready entry:

- [BluePyOpt](https://bluepyopt.readthedocs.io/en/stable/) - A Python framework for fitting neuron and synapse model parameters to electrophysiological features, with introductory single-compartment, detailed pyramidal-cell, and synaptic-plasticity examples. Useful after learning to simulate a model, when the next question is how data constrain its parameters. Free documentation and code; electrophysiology examples require a supported simulator.

### Opening the Black Box: Low-Dimensional Dynamics in High-Dimensional Recurrent Neural Networks

- **Canonical URL:** [Stanford-hosted full paper](https://web.stanford.edu/class/cs379c/archive/2016/calendar_invited_talks/articles/SussilloandBarakNC-13.pdf).
- **Stage:** Advanced theory to research interpretation.
- **Prerequisites:** Recurrent networks, ordinary differential equations, Jacobians, eigenvalues, and local stability.
- **Access:** Free university-hosted PDF. A direct retrieval returned a 24-page PDF, and the first page was extracted to verify the title, authors, and publication identity.
- **Evidence:** Sussillo and Barak (2013), [bibliographic record](https://pubmed.ncbi.nlm.nih.gov/23272922/), analyze trained recurrent networks through fixed points, slow points, and local linearization. Worked examples include memory switching, oscillation generation, and temporal averaging.
- **Placement:** `resources/research-topics.md`, `Network dynamics`. This is a focused explanatory method reading; the existing Computation-through-Dynamics toolkit instead emphasizes benchmarking inferred dynamics against reference models.
- **Suggested outcome:** Explain which local stable or unstable modes support a computation, and distinguish a slow region from a true fixed point before interpreting a trajectory projection.

Ready entry:

- [Opening the Black Box: Low-Dimensional Dynamics in High-Dimensional Recurrent Neural Networks](https://web.stanford.edu/class/cs379c/archive/2016/calendar_invited_talks/articles/SussilloandBarakNC-13.pdf) - Sussillo and Barak's methods paper explains how fixed points, slow points, and local linearization reveal computations in trained recurrent networks. Memory, oscillation, and temporal-averaging examples connect dynamical-systems mathematics with interpretable network mechanisms. Free university-hosted full text; assumes recurrent networks, Jacobians, and local stability analysis.

### Interpreting encoding and decoding models

- **Canonical URL:** [Author-hosted full paper](https://kriegeskortelab.zuckermaninstitute.columbia.edu/sites/default/files/content/KriegeskorteDouglas_2019_CurrOpinNeurobiol.pdf).
- **Stage:** Advanced analysis to research interpretation.
- **Prerequisites:** Linear regression or classification, regularization, train/test separation, and basic neural-response analysis.
- **Access:** Free 13-page author-posted PDF; its full text and publication identity were inspected. [Author preprint record](https://arxiv.org/abs/1812.00278) provides a second open access route.
- **Evidence:** Kriegeskorte and Douglas (2019) discuss how correlated predictors, noise, and regularization complicate weight interpretation. They distinguish generalization to new measurements, new stimuli, and new stimulus populations, and explain why comparing alternative models provides stronger theoretical constraints than significant performance for one model.
- **Placement:** `resources/neural-data-analysis.md`, `Tutorials and methodological reviews`; cross-link from the brains-and-AI learning path. This supplies interpretation principles that the current tool and benchmark entries do not themselves organize as a reading resource.
- **Suggested outcome:** For an encoding or decoding result, state what was held out, what population the claim generalizes to, and one competing mechanism consistent with the same performance.

Ready entry:

- [Interpreting encoding and decoding models](https://kriegeskortelab.zuckermaninstitute.columbia.edu/sites/default/files/content/KriegeskorteDouglas_2019_CurrOpinNeurobiol.pdf) - Kriegeskorte and Douglas explain what encoding and decoding results can establish about neural representations, including pitfalls in interpreting weights, correlated noise, and regularized fits. The review distinguishes levels of generalization and motivates inferential comparison of competing models. Free author-posted full text; useful before interpreting model-to-brain prediction scores.

## Deferred or rejected candidates

| Candidate | Decision | Evidence and reason |
| --- | --- | --- |
| [FixedPointFinder](https://github.com/mattgolub/fixed-point-finder) | Defer as a standalone software recommendation | GitHub API reports non-archived status, but the latest default-branch commit is dated 2023-09-12 and [latest release v1.5.0](https://github.com/mattgolub/fixed-point-finder/releases/tag/v1.5.0) is dated 2022-12-15. Its README restricts the documented TensorFlow path to versions through 2.8. The suggested PyTorch install command names `requirements-torch.txt`, while the repository file is `requirements-torch`. This does not prove the code is unusable, but the reviewed installation path needs a compatibility check. Prefer the original dynamics paper for this pass; do not describe the package as actively maintained. |
| [Reverse Engineering Neural Networks](https://github.com/google-research/reverse-engineering-neural-networks) | Reject as a new maintained-tool entry | The live GitHub API reports `archived: true`. It overlaps the selected dynamics reading and existing toolkit coverage; archived research code can still be useful for reproducing a paper, but does not fill the current maintained-tool gap. |

## Verification boundaries

GitHub metadata was fetched through the public repository API on the review date, including archive flags, default-branch commits, and releases. Documentation and article content were inspected, but no packages were installed and no numerical result was reproduced.

The Barak-lab version of the Sussillo and Barak PDF timed out in the web reader, and a direct request returned a small HTML block page despite HTTP 200. The selected Stanford URL instead returned `application/pdf` and an extractable 24-page paper. The original lab's code-download link was not verified, so the ready entry makes no code-availability claim. This distinction prevents a successful HTTP status from being mistaken for usable content.
