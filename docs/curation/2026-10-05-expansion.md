# Systematic expansion audit — 2026-10-05

The complete original repository was read before curation: README, contribution and maintenance rules, issue/PR templates, CI/configuration files, license, and package metadata/lockfile. The working tree was initially clean at commit `8471f98`. Resource counts refer to catalog entries in README, excluding navigation links, badges, administrative links, and these audit reports.

## Counting and allocation rules

- Before: **69 catalog rows, 68 independent resources**. The Neuronal Dynamics book and Python exercises were two entrances to one educational resource. They are now one row, with both links retained; the related cognitive-model lectures are another entrance, not another count.
- After: **136 independent resources**, including **68 new resources**. No existing independent resource was removed. The raw row increase is 67 because the original duplicate row was merged.
- Each resource receives one primary research theme and one primary resource type for the matrices below. A book may teach several themes and a course may contain code and videos; it is counted once, according to its principal purpose in this list. This conservative allocation avoids making broad textbooks appear to fill every specialist cell.
- `Other` retains the eight existing foundational papers, standards, the general ModelDB portal, and community resources outside the nine requested types. No ordinary research-paper bulk was added. Reviews and published model implementations have separate practical value.
- A particular model implementation is distinct from the simulator or model repository that hosts it. Multiple ports of the same Potjans–Diesmann model, basic pair-STDP examples, software documentation entrances, lecture episodes, and dataset splits were grouped or omitted.
- Main-page/content verification is distinct from executing code, downloading an entire dataset, or playing every recording. The Large-Scale Modeling entry explicitly marks interactive Learn Gala access unverified; its INCF catalog identity and outline were verified.

## Topic additions and candidate exploration

Candidate screens include existing resources, alternatives, and rejected leads. Counts below are screening records per theme, not a quota of additions or a globally unique candidate total. Parent/child overlaps were screened rather than used to inflate the final resource count.

| Theme | Before | Added | After | Screened records | Research report |
| --- | ---: | ---: | ---: | ---: | --- |
| General / foundations / community | 22 | 0 | 22 | — | Existing material retained |
| Neuron and dendrite models | 7 | 4 | 11 | 17 | [Candidate evidence](neurons-networks.md) |
| Network dynamics | 7 | 7 | 14 | 19 | [Candidate evidence](neurons-networks.md) |
| Neural coding | 3 | 5 | 8 | 16 | [Candidate evidence](coding-plasticity.md) |
| Plasticity and learning rules | 3 | 6 | 9 | 16 | [Candidate evidence](coding-plasticity.md) |
| Probabilistic inference and predictive coding | 2 | 7 | 9 | 15 | [Candidate evidence](inference-decision.md) |
| Perception and decision-making | 0 | 6 | 6 | 15 | [Candidate evidence](inference-decision.md) |
| Memory and spatial navigation | 1 | 7 | 8 | 15 | [Candidate evidence](memory-motor.md) |
| Motor control | 1 | 8 | 9 | 16 | [Candidate evidence](memory-motor.md) |
| Neural data analysis | 16 | 9 | 25 | 16 | [Candidate evidence](data-neuroai.md) |
| NeuroAI | 6 | 9 | 15 | 16 | [Candidate evidence](data-neuroai.md) |
| **Total independent resources** | **68** | **68** | **136** | Not summed | |

## Research theme × resource type before

Zeros mean no primary-purpose catalog entry in that cell, not that an omnibus course never mentions the subject. In particular, the general course/textbook path already includes coding, plasticity, inference, and decisions.

| Theme | Textbook | Course | Tutorial | Review | Software | Implementation | Dataset | Benchmark | Lectures | Other | Total |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| General / foundations / community | 8 | 7 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 6 | 22 |
| Neuron and dendrite models | 1 | 0 | 0 | 0 | 2 | 0 | 1 | 0 | 0 | 3 | 7 |
| Network dynamics | 0 | 0 | 0 | 0 | 7 | 0 | 0 | 0 | 0 | 0 | 7 |
| Neural coding | 1 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 1 | 3 |
| Plasticity and learning rules | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 2 | 3 |
| Probabilistic inference and predictive coding | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 2 |
| Perception and decision-making | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| Memory and spatial navigation | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 |
| Motor control | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 |
| Neural data analysis | 1 | 0 | 0 | 0 | 11 | 0 | 2 | 0 | 0 | 2 | 16 |
| NeuroAI | 0 | 1 | 0 | 0 | 4 | 0 | 0 | 1 | 0 | 0 | 6 |
| **Total** | 13 | 8 | 0 | 0 | 24 | 0 | 5 | 1 | 0 | 17 | 68 |

## Research theme × resource type after

| Theme | Textbook | Course | Tutorial | Review | Software | Implementation | Dataset | Benchmark | Lectures | Other | Total |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| General / foundations / community | 8 | 7 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 6 | 22 |
| Neuron and dendrite models | 1 | 1 | 0 | 0 | 4 | 1 | 1 | 0 | 0 | 3 | 11 |
| Network dynamics | 2 | 1 | 1 | 0 | 7 | 1 | 0 | 1 | 1 | 0 | 14 |
| Neural coding | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 0 | 1 | 1 | 8 |
| Plasticity and learning rules | 1 | 1 | 1 | 2 | 0 | 2 | 0 | 0 | 0 | 2 | 9 |
| Probabilistic inference and predictive coding | 2 | 1 | 0 | 2 | 2 | 1 | 0 | 0 | 0 | 1 | 9 |
| Perception and decision-making | 1 | 1 | 0 | 1 | 2 | 0 | 1 | 0 | 0 | 0 | 6 |
| Memory and spatial navigation | 1 | 0 | 0 | 1 | 2 | 2 | 1 | 0 | 0 | 1 | 8 |
| Motor control | 1 | 1 | 0 | 2 | 1 | 0 | 2 | 1 | 0 | 1 | 9 |
| Neural data analysis | 2 | 0 | 0 | 1 | 14 | 1 | 3 | 1 | 1 | 2 | 25 |
| NeuroAI | 0 | 2 | 0 | 1 | 6 | 1 | 3 | 2 | 0 | 0 | 15 |
| **Total** | 20 | 16 | 3 | 11 | 39 | 9 | 13 | 5 | 3 | 17 | 136 |

## Counts by README section

| Section | Before independent | Added | After |
| --- | ---: | ---: | ---: |
| Books | 8 | 0 | 8 |
| Courses and tutorials | 5 | 0 | 5 |
| Mathematical foundations | 7 | 0 | 7 |
| Foundational papers | 8 | 0 | 8 |
| Research topics | 0 | 50 | 50 |
| Neuron and network simulators | 10 | 0 | 10 |
| Neural data analysis | 10 | 8 | 18 |
| Open datasets | 5 | 4 | 9 |
| Data standards and reproducibility | 4 | 0 | 4 |
| NeuroAI and spiking neural networks | 6 | 6 | 12 |
| Community and conferences | 5 | 0 | 5 |

## Main gaps filled

- Neuron/dendrite modeling gains fitted Allen cell models, reduced dendritic compartments, differentiable multicompartment fitting, and a practical course rather than another general simulator list.
- Network dynamics gains neural-field theory, balanced-network lectures, a connectome/mean-field tutorial, a specific cortical microcircuit implementation, and a task-grounded dynamics benchmark.
- Coding/plasticity gains focused coding teaching, statistical-model tutorials, information-theoretic reviews, spike-train similarity tools, eligibility-trace learning, voltage-dependent plasticity, and critical reviews of learning-rule limitations.
- Inference/decisions gains specialist Bayesian teaching, predictive-coding reviews and notebook implementations, HGF/active-inference tools, cognition teaching, sequential-sampling fitting tools, and longitudinal decision behavior.
- Memory/navigation gains hippocampal references, place/grid navigation implementations, spatial-model comparison environments, and an odor-place associative-memory dataset. Motor control gains control teaching, classic and recent reviews, muscle-actuated tasks, cross-session decoder evaluation, and movement datasets.
- Neural data analysis gains fMRI foundations/preprocessing/statistics, latent-model implementations, brain-wide data, methodological review, lectures, and a local benchmark. NeuroAI gains review/course context, model-to-brain comparisons, pretrained visual models, human representation data, auditory spike benchmarks, and archived prediction challenges.

## Still weak

- Dedicated dendritic benchmarks and experimental validation targets; neuron modeling still has no new specialist review or benchmark entry.
- Coding-specific datasets and benchmark tasks, beyond existing archives and Brain-Score; plasticity ground-truth datasets and shared evaluation metrics remain empty.
- Neural Bayesian/predictive-coding datasets and comparative biological benchmarks; cross-framework code exists, but empirical model discrimination needs further curation.
- Non-spatial episodic/working memory, spatial-memory teaching sequences, and mature navigation benchmarks; the memory set is weighted toward hippocampal spatial models.
- Cerebellar, spinal, and central-pattern-generator implementations with clear runnable instructions; motor control is weighted toward reaching, manipulation, and neural decoding.
- Spike-sorting/calcium-imaging ground-truth benchmarks, auditory cortical model comparisons, language, and embodied NeuroAI generalization.

## Unfinished retrieval or verification

- Learn Gala interactive lesson contents and access conditions could not be inspected: the original site returns a JavaScript-only shell, and no computer-use browser was available. The README marks this explicitly.
- SpikeForest current service/content remains unverified; its discovered v2 code is labeled OLD. CNeuroMod needs a dedicated access-condition review.
- University of Missouri hands-on materials and Glasgow decision-course pages remain unresolved. The INCF Module 3 parent relationship remains unclear.
- Legacy OSB Purkinje and cerebellar conversions report incomplete status; they were not added. The complete OSB v2 model space was not exhaustively searched.
- FALCON local code/data were verified, but current EvalAI submission availability remains unknown. NLB submissions are closed and its test data are public; the final entry carries a test-set-tuning caveat.
- No selected research software was installed or run; no full datasets were downloaded or access agreements submitted; external Colab exercises and every lecture video were not exhaustively executed or played.
- This was one bounded discovery pass (15–19 screening records per theme), not an exhaustive literature search. Deferred leads and evidence are retained in the five linked reports.

## Validation

Fresh final checks passed: `npm run lint:md` (10 Markdown files), `git diff --check`, resource identity/count validation (136 rows, 68 additions, zero duplicate primary names or normalized URLs), and relative-link/README-heading checks. An independent read-only review confirmed the same counts and grouping decisions. A final offline lychee pass checked local files and fragments (35 successful local targets, zero errors), and the replacement author-review PDF passed a targeted online lychee check (1/1). Offline exclusion of network URLs is reported separately and does not change the failed full-network result.

The full network check used lychee 0.24.2 with the existing configuration and fragments enabled: `lychee --config lychee.toml --hidden --no-progress --include-fragments --format json './**/*.md'`. It completed in 502 seconds with exit code **2**, so **the network check did not pass**: 470 link occurrences / 253 unique targets, 434 successful occurrences, 24 error occurrences, 10 timeout occurrences, and the two pre-existing exact publisher exclusions. Repeated appearances in reports account for duplicated failure occurrences; there were 19 distinct flagged URLs in that run. The new audit ledger reuses checked resource targets rather than introducing new remote resources.

Four current README primary entrances return 403 to automated clients: the two new MIT Press book records and two Annual Reviews records listed below. Their titles, content, and access conditions were verified by opening the primary pages with the web reader; automated 403 is not represented as a successful network check. No new exclusions or accepted error codes were added. The failing ScienceDirect entrance was replaced in README by the opened author-hosted full-text PDF; the original publisher citation remains part of the screening record. A mistyped legacy OSB host was corrected, while that legacy service still needs availability follow-up.

| Flagged primary or candidate URL | Automated result | Disposition |
| --- | --- | --- |
| <https://doi.org/10.1145/3797870> | HTTP 403 | Alternative/discovery citation; not a new unresolved README entrance |
| <https://mitpress.mit.edu/9780262042383/bayesian-brain/> | HTTP 403 | Current README resource; primary content verified, automated access blocked |
| <https://mitpress.mit.edu/9780262195089/the-computational-neurobiology-of-reaching-and-pointing/> | HTTP 403 | Current README resource; primary content verified, automated access blocked |
| <https://mitpress.mit.edu/9780262548083/modeling-neural-circuits-made-simple-with-python/> | HTTP 403 | Alternative/discovery citation; not a new unresolved README entrance |
| <https://mitpress.mit.edu/9780262681087/spikes/> | HTTP 403 | Alternative/discovery citation; not a new unresolved README entrance |
| <https://nairs.mufaculty.umsystem.edu/training-and-outreach/hands-on-computational-neuroscience-for-undergraduates> | HTTP 404 | Deferred lead; unavailable URL recorded, not added to README |
| <https://neurolib.readthedocs.io/en/latest/> | HTTP 404 | Deferred lead; unavailable URL recorded, not added to README |
| <https://v1.opensourcebrain.org/projects/cerebellargainandtiming> | Timeout | Legacy/deferred implementation; not added to README, current availability unresolved |
| <https://v1.opensourcebrain.org/projects/cerebellarmodelling/wiki/Wiki> | Timeout | Legacy/deferred implementation; not added to README, current availability unresolved |
| <https://v1.opensourcebrain.org/projects/grancellsolinasetal10> | Timeout | Legacy/deferred implementation; not added to README, current availability unresolved |
| <https://v1.opensourcebrain.org/projects/granularlayersolinasnieusdangelo2010> | Timeout | Legacy/deferred implementation; not added to README, current availability unresolved |
| <https://v1.opensourcebrain.org/projects/opencortex> | Timeout | Legacy/deferred implementation; not added to README, current availability unresolved |
| <https://v1.opensourcebrain.org/projects/purkinjecell> | Timeout | Legacy/deferred implementation; not added to README, current availability unresolved |
| <https://webvhpool.gla.ac.uk/coursecatalogue/course/?code=PSYCH5069> | Network/response failure | Alternative/discovery citation; not a new unresolved README entrance |
| <https://www.annualreviews.org/content/journals/10.1146/annurev-bioeng-102723-020454> | HTTP 403 | Current README resource; primary content verified, automated access blocked |
| <https://www.annualreviews.org/content/journals/10.1146/annurev-neuro-090919-022842> | HTTP 403 | Current README resource; primary content verified, automated access blocked |
| <https://www.fgses-um6p.ma/cognitive-foundations-of-decision-making> | HTTP 403 | Alternative/discovery citation; not a new unresolved README entrance |
| <https://www.sciencedirect.com/science/article/pii/S0896627311008919> | HTTP 400 | README now uses verified author PDF; original publisher citation retained in candidate record |
| <https://www.v1.opensourcebrain.org/> | Timeout | Mistyped host corrected to v1.opensourcebrain.org; legacy service follow-up remains |

## Resource allocation ledger

This ledger makes the primary-purpose matrices reproducible. The 68 baseline assignments come from the original README; all added names link to the final primary entrance. Secondary topics/types are described in README and candidate reports.

| Resource | Change | Primary theme | Primary type |
| --- | --- | --- | --- |
| Neuronal Dynamics: From Single Neurons to Networks and Models of Cognition | Existing | General / foundations / community | Textbook |
| Theoretical Neuroscience: Computational and Mathematical Modeling of Neural Systems | Existing | General / foundations / community | Textbook |
| Dynamical Systems in Neuroscience: The Geometry of Excitability and Bursting | Existing | Neuron and dendrite models | Textbook |
| Spikes: Exploring the Neural Code (introductory chapter) | Existing | Neural coding | Textbook |
| Fundamentals of Computational Neuroscience | Existing | General / foundations / community | Textbook |
| An Introductory Course in Computational Neuroscience | Existing | General / foundations / community | Textbook |
| Neural Data Science in Python | Existing | Neural data analysis | Textbook |
| Brain Facts: A Primer on the Brain and Nervous System | Existing | General / foundations / community | Textbook |
| Neuromatch Academy: Computational Neuroscience | Existing | General / foundations / community | Course |
| Computational Neuroscience (University of Washington / Coursera) | Existing | General / foundations / community | Course |
| Introduction to Computational Neuroscience (MIT OCW 9.29J) | Existing | General / foundations / community | Course |
| Computational Neuroscience (University of Edinburgh Open Course Materials) | Existing | General / foundations / community | Course |
| Introduction to Computational Neuroscience (NPTEL, IIT Madras) | Existing | General / foundations / community | Course |
| Mathematics for Machine Learning | Existing | General / foundations / community | Textbook |
| Statistical Thinking for the 21st Century | Existing | General / foundations / community | Textbook |
| Linear Algebra (MIT OpenCourseWare 18.06) | Existing | General / foundations / community | Course |
| Introduction to Probability and Statistics (MIT OpenCourseWare 18.05) | Existing | General / foundations / community | Course |
| Notes on Diffy Qs: Differential Equations for Engineers | Existing | General / foundations / community | Textbook |
| Probabilistic Machine Learning: Advanced Topics | Existing | Probabilistic inference and predictive coding | Textbook |
| Reinforcement Learning: An Introduction (Second Edition) | Existing | Plasticity and learning rules | Textbook |
| A quantitative description of membrane current and its application to conduction and excitation in nerve | Existing | Neuron and dendrite models | Other |
| Neural networks and physical systems with emergent collective computational abilities | Existing | Memory and spatial navigation | Other |
| Emergence of simple-cell receptive field properties by learning a sparse code for natural images | Existing | Neural coding | Other |
| A neural substrate of prediction and reward | Existing | Plasticity and learning rules | Other |
| Synaptic modifications in cultured hippocampal neurons: dependence on spike timing, synaptic strength, and postsynaptic cell type | Existing | Plasticity and learning rules | Other |
| Predictive coding in the visual cortex: a functional interpretation of some extra-classical receptive-field effects | Existing | Probabilistic inference and predictive coding | Other |
| Simple model of spiking neurons | Existing | Neuron and dendrite models | Other |
| Neural population dynamics during reaching | Existing | Motor control | Other |
| [Allen Cell Types Database: Neuronal Models](https://brain-map.org/support/documentation/cell-types-database-api) | Added | Neuron and dendrite models | Implementation |
| [Dendrify](https://dendrify.readthedocs.io/en/latest/) | Added | Neuron and dendrite models | Software |
| [Jaxley](https://jaxley.readthedocs.io/en/stable/) | Added | Neuron and dendrite models | Software |
| [Neuroscience for Machine Learners (Neuro4ML)](https://training.incf.org/course/neuroscience-machine-learners-neuro4ml) | Added | Neuron and dendrite models | Course |
| [Modeling Neural Circuits Made Simple with Python](https://github.com/RobertRosenbaum/ModelingNeuralCircuits) | Added | Network dynamics | Textbook |
| [Neural Fields: Theory and Applications](https://link.springer.com/book/10.1007/978-3-642-54593-1) | Added | Network dynamics | Textbook |
| [Dynamical Neural Systems](https://training.incf.org/course/dynamical-neural-systems) | Added | Network dynamics | Course |
| [Large-Scale Modeling of Brain Dynamics](https://training.incf.org/course/large-scale-modeling-brain-dynamics) | Added | Network dynamics | Tutorial |
| [Cajal Course in Computational Neuroscience](https://training.incf.org/course/cajal-course-computational-neuroscience) | Added | Network dynamics | Lectures |
| [Computation-through-Dynamics Benchmark and Toolkit](https://github.com/snel-repo/ComputationThroughDynamicsToolkit) | Added | Network dynamics | Benchmark |
| [Potjans–Diesmann Cortical Microcircuit Model in NetPyNE](https://modeldb.science/266872) | Added | Network dynamics | Implementation |
| [Coding and Vision 101](https://training.incf.org/course/coding-and-vision-101) | Added | Neural coding | Lectures |
| [The Neural Code (UCL Cortexlab)](https://www.ucl.ac.uk/brain-sciences/cortexlab/courses/neuroinformatics-class-page) | Added | Neural coding | Course |
| [Statistical Models for Neural Data (COSYNE / INCF TrainingSpace)](https://training.incf.org/course/statistical-models) | Added | Neural coding | Tutorial |
| [Information Theory and Neural Coding](https://www.nature.com/articles/nn1199_947) | Added | Neural coding | Review |
| [SPIKY](https://www.thomaskreuz.org/source-codes/spiky) | Added | Neural coding | Software |
| [Computational Modeling of Neuronal Plasticity](https://training.incf.org/course/computational-modeling-neuronal-plasticity) | Added | Plasticity and learning rules | Course |
| [NESTML Dopamine-Modulated STDP Tutorial](https://nestml.readthedocs.io/en/latest/tutorials/stdp_dopa_synapse/stdp_dopa_synapse.html) | Added | Plasticity and learning rules | Tutorial |
| [Brian 2 Clopath Voltage-Based STDP Example](https://brian2.readthedocs.io/en/latest/examples/frompapers.Clopath_et_al_2010_no_homeostasis.html) | Added | Plasticity and learning rules | Implementation |
| [A Simple Model of Neuromodulatory State-Dependent Synaptic Plasticity](https://modeldb.science/222932) | Added | Plasticity and learning rules | Implementation |
| [Synaptic Plasticity Forms and Functions](https://www.annualreviews.org/content/journals/10.1146/annurev-neuro-090919-022842) | Added | Plasticity and learning rules | Review |
| [Spike Timing-Dependent Plasticity: A Consequence of More Fundamental Learning Rules](https://www.frontiersin.org/journals/computational-neuroscience/articles/10.3389/fncom.2010.00019/full) | Added | Plasticity and learning rules | Review |
| [Bayesian Models of Learning and Integration of Neuroimaging Data](https://training.incf.org/course/bayesian-models-learning-and-integration-neuroimaging-data) | Added | Probabilistic inference and predictive coding | Course |
| [Bayesian Brain: Probabilistic Approaches to Neural Coding](https://mitpress.mit.edu/9780262042383/bayesian-brain/) | Added | Probabilistic inference and predictive coding | Textbook |
| [Predictive Coding: a Theoretical and Experimental Review](https://arxiv.org/abs/2107.12979) | Added | Probabilistic inference and predictive coding | Review |
| [Predictive Coding Networks and Inference Learning: Tutorial and Survey](https://arxiv.org/abs/2407.04117) | Added | Probabilistic inference and predictive coding | Review |
| [Predictive Coding](https://github.com/Bogacz-Group/PredictiveCoding) | Added | Probabilistic inference and predictive coding | Implementation |
| [HGF Toolbox](https://github.com/ComputationalPsychiatry/hgf-toolbox) | Added | Probabilistic inference and predictive coding | Software |
| [pymdp](https://github.com/infer-actively/pymdp) | Added | Probabilistic inference and predictive coding | Software |
| [Computational Cognitive Neuroscience (Edinburgh)](https://opencourse.inf.ed.ac.uk/ccn) | Added | Perception and decision-making | Course |
| [Computational Cognitive Neuroscience](https://book.compcogneuro.org/) | Added | Perception and decision-making | Textbook |
| [Computational Models of Decision Making](https://www.cambridge.org/core/books/abs/cambridge-handbook-of-computational-cognitive-sciences/computational-models-of-decision-making/0465E07014E1543151E52851E8E65EC2) | Added | Perception and decision-making | Review |
| [PyDDM](https://pyddm.readthedocs.io/en/stable/) | Added | Perception and decision-making | Software |
| [HSSM](https://lnccbrown.github.io/HSSM/) | Added | Perception and decision-making | Software |
| [IBL decision-making behavior data](https://docs.internationalbrainlab.org/notebooks_external/2021_data_release_behavior.html) | Added | Perception and decision-making | Dataset |
| [Hippocampal Microcircuits: A Computational Modeler's Resource Book](https://link.springer.com/book/10.1007/978-3-319-99103-0) | Added | Memory and spatial navigation | Textbook |
| [RatInABox](https://github.com/RatInABox-Lab/RatInABox) | Added | Memory and spatial navigation | Software |
| [NeuralPlayground](https://github.com/SainsburyWellcomeCentre/NeuralPlayground) | Added | Memory and spatial navigation | Software |
| [Models of Vector Navigation with Grid Cells (ModelDB)](https://modeldb.science/182685) | Added | Memory and spatial navigation | Implementation |
| [Place and Grid Cells in a Loop (ModelDB)](https://modeldb.science/241932) | Added | Memory and spatial navigation | Implementation |
| [Odor-Place Spatial Association Task (DANDI:001539)](https://dandiarchive.org/dandiset/001539) | Added | Memory and spatial navigation | Dataset |
| [Grid Cells and Spatial Maps in Entorhinal Cortex and Hippocampus](https://link.springer.com/chapter/10.1007/978-3-319-28802-4_5) | Added | Memory and spatial navigation | Review |
| [The Computational Neurobiology of Reaching and Pointing](https://mitpress.mit.edu/9780262195089/the-computational-neurobiology-of-reaching-and-pointing/) | Added | Motor control | Textbook |
| [Computational Motor Control (Reza Shadmehr)](https://courses.shadmehrlab.org/compmc.html) | Added | Motor control | Course |
| [Embodied Sensorimotor Control: Computational Modeling of the Neural Control of Movement](https://www.annualreviews.org/content/journals/10.1146/annurev-bioeng-102723-020454) | Added | Motor control | Review |
| [MyoSuite](https://myosuite.readthedocs.io/en/stable/) | Added | Motor control | Software |
| [FALCON: Few-shot Algorithms for Consistent Neural decoding](https://github.com/snel-repo/falcon-challenge) | Added | Motor control | Benchmark |
| [LINK: Long-Term Intracortical Neural Activity and Kinematics](https://chesteklab.github.io/LINK_dataset/) | Added | Motor control | Dataset |
| [Reach-related Single Unit Activity in the Parkinsonian Macaque (DANDI:000947)](https://dandiarchive.org/dandiset/000947) | Added | Motor control | Dataset |
| [Computational Mechanisms of Sensorimotor Control](https://wolpertlab.neuroscience.columbia.edu/sites/wolpertlab.neuroscience.columbia.edu/files/content/papers/FraWol11.pdf) | Added | Motor control | Review |
| NEURON | Existing | Neuron and dendrite models | Software |
| Brian 2 | Existing | Network dynamics | Software |
| NEST Simulator | Existing | Network dynamics | Software |
| Arbor | Existing | Neuron and dendrite models | Software |
| NetPyNE | Existing | Network dynamics | Software |
| GeNN | Existing | Network dynamics | Software |
| PyNN | Existing | Network dynamics | Software |
| The Virtual Brain | Existing | Network dynamics | Software |
| Nengo | Existing | Network dynamics | Software |
| ModelDB | Existing | General / foundations / community | Other |
| [NiPraxis: Practice and theory of brain imaging](https://textbook.nipraxis.org/intro.html) | Added | Neural data analysis | Textbook |
| [NeuroHackademy lecture archive](https://neurohackademy.org/archive/) | Added | Neural data analysis | Lectures |
| [Neural data science: accelerating the experiment-analysis-theory cycle in large-scale neuroscience](https://sites.stat.columbia.edu/liam/teaching/neurostat-fall17/CONB.pdf) | Added | Neural data analysis | Review |
| SpikeInterface | Existing | Neural data analysis | Software |
| Kilosort | Existing | Neural data analysis | Software |
| phy | Existing | Neural data analysis | Software |
| Elephant | Existing | Neural data analysis | Software |
| Pynapple | Existing | Neural data analysis | Software |
| [CEBRA](https://cebra.ai/docs/) | Added | Neural data analysis | Software |
| [lfads-torch](https://github.com/arsedler9/lfads-torch) | Added | Neural data analysis | Implementation |
| Suite2p | Existing | Neural data analysis | Software |
| CaImAn | Existing | Neural data analysis | Software |
| MNE-Python | Existing | Neural data analysis | Software |
| FieldTrip | Existing | Neural data analysis | Software |
| [Nilearn](https://nilearn.github.io/stable/index.html) | Added | Neural data analysis | Software |
| [fMRIPrep](https://fmriprep.org/en/stable/) | Added | Neural data analysis | Software |
| [Neural Latents Benchmark](https://neurallatents.github.io/) | Added | Neural data analysis | Benchmark |
| DeepLabCut | Existing | Neural data analysis | Software |
| DANDI Archive | Existing | Neural data analysis | Dataset |
| OpenNeuro | Existing | Neural data analysis | Dataset |
| Allen Brain Observatory and AllenSDK | Existing | Neural coding | Dataset |
| CRCNS Data Sharing | Existing | General / foundations / community | Dataset |
| NeuroMorpho.Org | Existing | Neuron and dendrite models | Dataset |
| [IBL Brain-Wide Map](https://docs.internationalbrainlab.org/notebooks_external/2025_data_release_brainwidemap.html) | Added | Neural data analysis | Dataset |
| [Natural Scenes Dataset](https://www.naturalscenesdataset.org/) | Added | NeuroAI | Dataset |
| [THINGS-data](https://things-initiative.org/) | Added | NeuroAI | Dataset |
| [Spiking Heidelberg Digits and Spiking Speech Commands](https://zenkelab.org/resources/spiking-heidelberg-datasets-shd/) | Added | NeuroAI | Dataset |
| Neurodata Without Borders (NWB) | Existing | Neural data analysis | Other |
| Brain Imaging Data Structure (BIDS) | Existing | Neural data analysis | Other |
| NeuroML | Existing | Neuron and dendrite models | Other |
| Neo | Existing | Neural data analysis | Software |
| Neuromatch Academy: NeuroAI | Existing | NeuroAI | Course |
| [Brains, Minds and Machines Summer Course (MIT OCW)](https://ocw.mit.edu/courses/res-9-003-brains-minds-and-machines-summer-course-summer-2015/) | Added | NeuroAI | Course |
| [Neuroscience-Inspired Artificial Intelligence](https://pubmed.ncbi.nlm.nih.gov/28728020/) | Added | NeuroAI | Review |
| Brain-Score | Existing | NeuroAI | Benchmark |
| [Net2Brain](https://net2brain.readthedocs.io/en/latest/) | Added | NeuroAI | Software |
| [CORnet](https://github.com/dicarlolab/CORnet) | Added | NeuroAI | Implementation |
| [The Algonauts Project](https://algonautsproject.com/) | Added | NeuroAI | Benchmark |
| snnTorch | Existing | NeuroAI | Software |
| Norse | Existing | NeuroAI | Software |
| SpikingJelly | Existing | NeuroAI | Software |
| Rockpool | Existing | NeuroAI | Software |
| [Tonic](https://tonic.readthedocs.io/en/latest/) | Added | NeuroAI | Software |
| COSYNE | Existing | General / foundations / community | Other |
| Organization for Computational Neurosciences | Existing | General / foundations / community | Other |
| Bernstein Network | Existing | General / foundations / community | Other |
| INCF | Existing | General / foundations / community | Other |
| Neurostars | Existing | General / foundations / community | Other |
