# Neural data analysis and NeuroAI curation

Reviewed on 2026-10-05. This report records discovery and editorial decisions; it is not a software execution or full dataset download test. `Accept` means the primary page was opened and its identity, substantive content, and advertised access path were inspected. Existing entries are retained, not counted as additions. Parent curricula, documentation, companion code, and dataset subsets are not counted as separate resources.

## Discovery paths

- [Awesome Neuroscience](https://github.com/analyticalmonk/awesome-neuroscience) led to NiPraxis, Andy's Brain Book, NeuroHackademy, Nilearn, and fMRIPrep; their primary sites were then opened.
- [Awesome Computational Neuroscience by eselkin](https://github.com/eselkin/awesome-computational-neuroscience) was inspected but primarily catalogs researchers and institutions, so it did not supply bulk resource entries.
- [INCF TrainingSpace](https://training.incf.org/) and its [Statistics and Machine Learning collection](https://training.incf.org/collection/statistics-machine-learning) exposed statistical teaching and tool families; these were compared with the existing Neuromatch curriculum.
- [Neuromatch's neuron dataset guide](https://compneuro.neuromatch.io/projects/neurons/README.html) and [fMRI dataset guide](https://compneuro.neuromatch.io/projects/fMRI/README.html) supplied recording and representation-analysis starting points, followed to official dataset and tool pages. Individual notebooks remain part of their parent course.
- [Neuromatch NeuroAI](https://neuroai.neuromatch.io/) supplied the scope of brain/model comparison, architectures, learning, and generalization. [Net2Brain's model catalog](https://net2brain.readthedocs.io/en/latest/existing_models.html) led to CORnet, and its [dataset documentation](https://net2brain.readthedocs.io/en/latest/datasets.html) led to NSD, THINGS, and Algonauts. The original sites were inspected separately.
- [Neural Latents Benchmark](https://neurallatents.github.io/) led to its [codepack](https://github.com/neurallatents/nlb_tools), LFADS-related implementations, and related decoding/dynamics benchmarks. [CEBRA's demo collection](https://cebra.ai/docs/demos.html) was checked for worked neural/behavioral analyses.
- [Tonic's dataset catalog](https://tonic.readthedocs.io/en/latest/) led to [SHD's loader documentation](https://tonic.readthedocs.io/en/latest/generated/tonic.datasets.SHD.html), then the original Zenke Lab data page. SHD and SSC are grouped as one Heidelberg resource family.
- [MIT's Brains, Minds and Machines summer course](https://ocw.mit.edu/courses/res-9-003-brains-minds-and-machines-summer-course-summer-2015/) and [NeuroHackademy's archive](https://neurohackademy.org/archive/) were opened as complete lecture collections, not split into sessions.

## Neural data analysis candidates

| Candidate and primary source | Type | Decision | Evidence and reason |
| --- | --- | --- | --- |
| [NiPraxis: Practice and theory of brain imaging](https://textbook.nipraxis.org/intro.html) | Textbook/tutorial | Accept | Open contents include NIfTI, array operations, voxel regression, GLMs, hypothesis testing, and reproducible Python; fills a focused fMRI teaching gap. |
| [Andy's Brain Book](https://andysbrainbook.readthedocs.io/en/latest/) | Tutorial | Defer | Opened its tutorial contents; useful but overlaps the selected NiPraxis path. Not unavailable or rejected for age. |
| [NeuroHackademy archive](https://neurohackademy.org/archive/) | Lectures/course | Accept | Opened yearly schedules with linked lecture videos on reproducibility, neural decoding, imaging pipelines, and statistical learning. Playback of every video was not tested. |
| [Nilearn](https://nilearn.github.io/stable/index.html) | Software | Accept | Inspected official API/examples for decoding, decomposition, and GLMs; adds statistical neuroimaging analysis missing from the original tool list. |
| [fMRIPrep](https://fmriprep.org/en/stable/) | Software | Accept | Official workflow, usage, outputs, and release documentation inspected; fills fMRI preprocessing. Requires a FreeSurfer license for relevant components. |
| [CEBRA](https://cebra.ai/docs/) | Software/model implementation | Accept | Opened usage, demos, installation, and official source; latent embeddings join neural time series with auxiliary behavior. Documentation warns of API changes. |
| [lfads-torch](https://github.com/arsedler9/lfads-torch) | Model implementation | Accept | Original repository has installation, data preparation, configuration, and training walkthroughs for LFADS/AutoLFADS; adds a documented latent dynamics implementation. |
| [Neural Latents Benchmark](https://neurallatents.github.io/) | Benchmark/datasets | Accept | Opened site and codepack. Site explicitly says EvalAI submissions closed in January 2026 and test splits support local evaluation. |
| [IBL Brain-Wide Map](https://docs.internationalbrainlab.org/notebooks_external/2025_data_release_brainwidemap.html) | Dataset/tutorial | Accept | Followed IBL's data page to release docs, download instructions, dataset tag, and changelog; adds standardized brain-wide recordings tied to behavior. |
| [Neural data science: accelerating the experiment-analysis-theory cycle in large-scale neuroscience](https://sites.stat.columbia.edu/liam/teaching/neurostat-fall17/CONB.pdf) | Review | Accept | Opened author-hosted PDF and checked title/authors against the publisher record; discusses signal extraction, population structure, decoding, and inference. |
| [SpikeForest](https://spikeforest.flatironinstitute.org/) | Benchmark | Defer: incomplete verification | The site yielded no substantive body to the reader. The discovered [v2 repository](https://github.com/flatironinstitute/spikeforest2) labels itself OLD; current service/content usability was not established. |
| [Neural Data Science in Python](https://neuraldatascience.io/) | Textbook | Existing | Already provides a broad Python neuroscience path; no duplicate added. |
| [SpikeInterface](https://spikeinterface.readthedocs.io/en/latest/) | Software | Existing | Already covers extracellular processing, sorting, comparison, and validation. |
| [Pynapple](https://pynapple.org/) | Software | Existing | Existing time-series and tuning-curve toolkit; no extra documentation entry. |
| [DANDI Archive](https://dandiarchive.org/) | Dataset archive | Existing | Keep the archive and a specific benchmark dataset conceptually distinct; do not count each NLB DANDI split independently. |
| [Allen Brain Observatory and AllenSDK](https://allensdk.readthedocs.io/en/latest/brain_observatory.html) | Dataset/software | Existing | Keep SDK and underlying resource family together, as in the original list. |

## NeuroAI candidates

| Candidate and primary source | Type | Decision | Evidence and reason |
| --- | --- | --- | --- |
| [Neuroscience-Inspired Artificial Intelligence](https://pubmed.ncbi.nlm.nih.gov/28728020/) | Review | Accept | Opened title, authors, abstract, review classification, and full-text links; historical connections and concrete routes from neuroscience to AI. |
| [Brains, Minds and Machines Summer Course](https://ocw.mit.edu/courses/res-9-003-brains-minds-and-machines-summer-course-summer-2015/) | Course/lectures | Accept | Official syllabus has neural circuits, cognition, vision, audition, robotics, lecture videos, tutorials, and projects; all units counted once. |
| [Net2Brain](https://net2brain.readthedocs.io/en/latest/) | Software | Accept | Inspected installation, feature extraction, RDM creation, evaluation, model zoo, dataset docs, and original repository; adds model-to-brain comparison workflow. |
| [CORnet](https://github.com/dicarlolab/CORnet) | Model implementation | Accept | Original lab repository supplies model variants, pretrained weights, and feature-extraction command. Prefer corrected CORnet-RT over legacy CORnet-R. Classic research implementation, not a newly validated biological model. |
| [Natural Scenes Dataset](https://www.naturalscenesdataset.org/) | Dataset | Accept | Opened original description and access agreement notice; 7T fMRI natural-image responses support visual encoding/decoding. Data access agreement required. |
| [THINGS-data](https://things-initiative.org/) | Dataset | Accept | Original initiative links fMRI/MEG releases, behavioral judgments, analysis code, derivatives, and public download routes. Modalities are grouped, not inflated into multiple items. |
| [Tonic](https://tonic.readthedocs.io/en/latest/) | Software/tutorial | Accept | Official installation, event transforms, caching/batching tutorials, and audio/vision dataset catalog inspected; complements existing SNN training libraries. |
| [Spiking Heidelberg Digits and Spiking Speech Commands](https://zenkelab.org/resources/spiking-heidelberg-datasets-shd/) | Dataset/benchmark | Accept | Original page has task labels, cochlea-based spike conversion, HDF5 layout, downloads, and sample loading code; adds auditory evaluation rather than more visual data alone. |
| [The Algonauts Project](https://algonautsproject.com/) | Benchmark | Accept | Original archive and 2025 description inspected; provides model-prediction challenges with multimodal movie responses. The 2025 submission deadline has passed; no open challenge is implied. |
| [CNeuroMod](https://docs.cneuromod.ca/) | Dataset | Defer | Followed Algonauts to original documentation. Rich related resource, but access conditions and all requested data paths need a dedicated pass; avoid redundancy this round. |
| [Brain-Score](https://www.brain-score.org/) | Benchmark | Existing | Official platform and documentation opened; existing primary model-to-neural/behavioral benchmark remains one entry. |
| [Neuromatch Academy: NeuroAI](https://neuroai.neuromatch.io/) | Course/tutorial | Existing | Curriculum overview opened; do not turn each day into an independent addition. |
| [snnTorch](https://snntorch.readthedocs.io/en/stable/) | Software/tutorial | Existing | Existing training library; do not split official tutorials from package. |
| [Norse](https://norse.github.io/norse/) | Software | Existing | Existing SNN library; another entry would duplicate coverage. |
| [SpikingJelly](https://github.com/fangwei123456/spikingjelly) | Software | Existing | Existing SNN framework; retained without a fork or mirror. |
| [Rockpool](https://rockpool.ai/) | Software | Existing | Existing dynamical-network/hardware toolkit; more tools alone would not fix the benchmark/review gaps. |

## Selected entries

### Neural data analysis

- [NiPraxis: Practice and theory of brain imaging](https://textbook.nipraxis.org/intro.html) - A free online textbook with Python exercises on NIfTI images, voxel time series, regression, GLMs, and reproducibility for understanding and building fMRI analyses.
- [NeuroHackademy lecture archive](https://neurohackademy.org/archive/) - Recorded summer-school lectures and tutorials on neuroimaging, neural decoding, statistical learning, and reproducible computing for developing a complete data-analysis workflow.
- [Nilearn](https://nilearn.github.io/stable/index.html) - Python tools and worked examples for fMRI GLMs, decoding, functional connectivity, and visualization, useful for testing statistical models of brain images.
- [fMRIPrep](https://fmriprep.org/en/stable/) - A documented pipeline that preprocesses BIDS fMRI data and produces visual quality-control reports and analysis-ready derivatives; relevant FreeSurfer components require a license file.
- [CEBRA](https://cebra.ai/docs/) - A documented contrastive-learning implementation with neural and behavioral notebooks for estimating latent embeddings and studying how population activity relates to measured behavior.
- [lfads-torch](https://github.com/arsedler9/lfads-torch) - A PyTorch implementation of LFADS and AutoLFADS with data preparation and training walkthroughs for inferring latent dynamics and firing rates from population spike recordings.
- [Neural Latents Benchmark](https://neurallatents.github.io/) - Neural spiking datasets, baseline code, and metrics for comparing latent-variable models; local evaluation remains available after EvalAI submissions closed in January 2026.
- [IBL Brain-Wide Map](https://docs.internationalbrainlab.org/notebooks_external/2025_data_release_brainwidemap.html) - Public brain-wide Neuropixels recordings with synchronized task and behavioral variables, release notes, and download tutorials for comparing neural activity across regions and sessions.
- [Neural data science: accelerating the experiment-analysis-theory cycle in large-scale neuroscience](https://sites.stat.columbia.edu/liam/teaching/neurostat-fall17/CONB.pdf) - Paninski and Cunningham's review connects signal extraction, dimensionality reduction, decoding, and network inference to the questions large-scale recordings can answer; free author-hosted manuscript.

### NeuroAI

- [Neuroscience-Inspired Artificial Intelligence](https://pubmed.ncbi.nlm.nih.gov/28728020/) - Hassabis and colleagues' review surveys how neural computation has informed AI and identifies shared research questions, providing context for choosing brain-inspired mechanisms to investigate.
- [Brains, Minds and Machines Summer Course (MIT OCW)](https://ocw.mit.edu/courses/res-9-003-brains-minds-and-machines-summer-course-summer-2015/) - Free lecture videos, tutorials, and projects connect neural circuits, vision, cognition, and robotics for studying intelligence across biological and artificial systems.
- [Net2Brain](https://net2brain.readthedocs.io/en/latest/) - A toolbox with pretrained model feature extraction, representational dissimilarity matrices, and evaluation methods for comparing artificial-network representations with human brain responses.
- [CORnet](https://github.com/dicarlolab/CORnet) - Documented PyTorch visual-system model variants and pretrained weights support testing feedforward and recurrent accounts of object recognition against neural and behavioral measurements.
- [Natural Scenes Dataset](https://www.naturalscenesdataset.org/) - Repeated 7T fMRI measurements during natural-image viewing support visual encoding, decoding, and model-to-brain comparisons; access requires completing the dataset's agreement.
- [THINGS-data](https://things-initiative.org/) - Matched object-image resources, fMRI and MEG recordings, behavioral similarity judgments, and analysis code support comparing object representations across brains, behavior, and models.
- [Tonic](https://tonic.readthedocs.io/en/latest/) - Dataset loaders, event transformations, and batching tutorials prepare event-based vision and audio data for reproducible spiking-network experiments.
- [Spiking Heidelberg Digits and Spiking Speech Commands](https://zenkelab.org/resources/spiking-heidelberg-datasets-shd/) - Public cochlea-derived spike datasets with labels, loading examples, and evaluation splits provide auditory classification benchmarks for spiking neural networks.
- [The Algonauts Project](https://algonautsproject.com/) - Archived challenges, data instructions, and tutorials benchmark prediction of human brain responses to visual and multimodal stimuli; the 2025 competition is closed.

## Verification limits and remaining gaps

The canonical pages of all 18 selected resources were opened. GitHub metadata checks corroborated non-archived repositories for the selected tools and model implementations; this does not prove compatibility with every current environment. No large dataset was downloaded, no access agreement submitted, and no training pipeline executed. Videos were checked as linked archive materials rather than exhaustively played.

SpikeForest's current site content and service need browser-level verification. CNeuroMod merits a separate access review. Data-analysis coverage still lacks a selected spike-sorting ground-truth benchmark and a dedicated calcium-imaging ground-truth evaluation resource. NeuroAI is stronger in visual representations and event-based classification than in auditory cortical model comparison, language, embodied generalization, or a unified cross-domain benchmark. These are next-pass targets, not claims of completed retrieval.
