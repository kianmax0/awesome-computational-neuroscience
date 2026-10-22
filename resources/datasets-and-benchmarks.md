# Datasets and benchmarks

[Repository overview](../README.md) · [Resource index](README.md) · [Topics](../topics/README.md) · [Methods](../methods/README.md)

Neuroscience datasets, model collections, and evaluation benchmarks.

## Open datasets

### DANDI Archive

- [DANDI Archive](https://dandiarchive.org/) - A BRAIN Initiative archive for publishing and sharing neurophysiology, optical physiology, behavioral time-series, and related data. Public dataset downloads do not require an account.

### OpenNeuro

- [OpenNeuro](https://openneuro.org/) - An open archive of BIDS-formatted MRI, PET, MEG, EEG, iEEG, and NIRS datasets. Public dataset downloads do not require an account.

### Allen Brain Observatory and AllenSDK

- [Allen Brain Observatory and AllenSDK](https://allensdk.readthedocs.io/en/latest/brain_observatory.html) - Access and analyze mouse visual-cortex datasets spanning two-photon imaging, Neuropixels recordings, stimuli, and behavior. Public datasets; large downloads may require substantial storage.

### CRCNS Data Sharing

- [CRCNS Data Sharing](https://crcns.org/data-sets) - A catalog of research datasets for computational neuroscience, covering many brain areas, species, recording methods, and simulations. Most downloads require a free account and acceptance of data-use terms.

### NeuroMorpho.Org

- [NeuroMorpho.Org](https://neuromorpho.org/) - A curated, searchable archive of digitally reconstructed neurons and glia with associated metadata. Public morphology downloads.

### IBL Brain-Wide Map

- [IBL Brain-Wide Map](https://docs.internationalbrainlab.org/notebooks_external/2025_data_release_brainwidemap.html) - Public brain-wide Neuropixels recordings with synchronized task and behavioral variables, release notes, and download tutorials for comparing neural activity across regions and sessions.

### Natural Scenes Dataset

- [Natural Scenes Dataset](https://www.naturalscenesdataset.org/) - Repeated 7T fMRI measurements during natural-image viewing support visual encoding, decoding, and model-to-brain comparisons; access requires completing the dataset's agreement.

### THINGS-data

- [THINGS-data](https://things-initiative.org/) - Matched object-image resources, fMRI and MEG recordings, behavioral similarity judgments, and analysis code support comparing object representations across brains, behavior, and models.

### Spiking Heidelberg Digits and Spiking Speech Commands

- [Spiking Heidelberg Digits and Spiking Speech Commands](https://zenkelab.org/resources/spiking-heidelberg-datasets-shd/) - Public cochlea-derived spike datasets with labels, loading examples, and evaluation splits provide auditory classification benchmarks for spiking neural networks.

### FlyWire Codex Connectome Explorer

- [FlyWire Codex Connectome Explorer](https://codex.flywire.ai/) - An interactive portal for searching and analyzing versioned Drosophila connectome snapshots, with public FlyWire data products available for download; interactive features require Google sign-in and downloads use a Codex account token.

### MICrONS Functional Connectomics Dataset

- [MICrONS Functional Connectomics Dataset](https://www.microns-explorer.org/) - A mouse visual-cortex resource that links dense calcium imaging with co-registered electron-microscopy reconstructions and annotations; programmatic CAVE access requires a token and analyses should record the selected materialization version.

### WU-Minn Human Connectome Project 1200 Subjects Release

- [WU-Minn Human Connectome Project 1200 Subjects Release](https://www.humanconnectome.org/study/hcp-young-adult/document/1200-subjects-data-release) - A multimodal human MRI and behavioral release with diffusion and functional imaging for regional connectome analyses; data access is through ConnectomeDB and requires registration and acceptance of applicable use terms.

### BrainSpan Atlas of the Developing Human Brain

- [BrainSpan Atlas of the Developing Human Brain](https://www.brainspan.org/) - An atlas with human developmental transcriptome profiles across brain regions and stages, plus prenatal expression and anatomy resources for constraining developmental models; public listings provide data and metadata archives.

### IBM DVS Gesture dataset

- [IBM DVS Gesture dataset](https://research.ibm.com/interactive/dvsgesture/) - IBM's event-camera gesture benchmark covers 11 categories, 29 subjects, and three lighting conditions; the original download was unverified after a timeout, while a [preprocessed NPY derivative](https://zenodo.org/records/8060604) provides a separate representation that should not be assumed to preserve raw event timing or polarity.

### Transdiagnostic Connectome Project

- [Transdiagnostic Connectome Project](https://openneuro.org/datasets/ds005237/versions/1.0.5) - A public OpenNeuro BIDS snapshot shares behavioral, questionnaire, and MRI data from 241 adults, including participants with a range of psychiatric diagnoses and a comparison group, for research on brain-behavior relationships; sample size and site structure constrain high-dimensional prediction.

## Benchmarks

### Neural Latents Benchmark

- [Neural Latents Benchmark](https://neurallatents.github.io/) - Neural spiking datasets, baseline code, and metrics for comparing latent-variable models; local evaluation remains available after EvalAI submissions closed in January 2026, with public test data requiring care to avoid test-set tuning.

## Model comparison benchmarks

### Brain-Score

- [Brain-Score](https://www.brain-score.org/) - An open benchmarking platform for comparing computational models with neural and behavioral measurements across vision and language.

### The Algonauts Project

- [The Algonauts Project](https://algonautsproject.com/) - Archived challenges, data instructions, and tutorials benchmark prediction of human brain responses to visual and multimodal stimuli; the 2025 competition is closed.

## Neuronal model collections

### Allen Cell Types Database: Neuronal Models

- [Allen Cell Types Database: Neuronal Models](https://brain-map.org/support/documentation/cell-types-database-api) - Browse electrophysiology-linked GLIF point-neuron and perisomatic biophysical models with dendritic morphology, then download and run models through the Allen SDK; biophysical models require NEURON.

## Additional model and evaluation collections

### Computation-through-Dynamics Benchmark and Toolkit

- [Computation-through-Dynamics Benchmark and Toolkit](https://github.com/snel-repo/ComputationThroughDynamicsToolkit) - Compare inferred neural dynamics against task-trained reference models using synthetic spiking datasets and interpretable metrics; installation uses Conda/Python 3.10 and Git LFS, the walkthrough assets require several gigabytes of disk, and GPU access may be needed for default data-model training.

## Decision-making datasets

### IBL decision-making behavior data

- [IBL decision-making behavior data](https://docs.internationalbrainlab.org/notebooks_external/2021_data_release_behavior.html) - Open mouse-training data with visual stimuli, choices, and response times for studying how sensory-guided decisions change from novice to expert; download through the ONE API and cite the associated data release.

## Spatial navigation datasets

### Odor-Place Spatial Association Task (DANDI:001539)

- [Odor-Place Spatial Association Task (DANDI:001539)](https://dandiarchive.org/dandiset/001539) - Shares rat hippocampal, prefrontal, and olfactory-bulb recordings with position and trial outcomes during an odor-place memory task; open access through DANDI.

## Motor-control datasets

### FALCON: Few-shot Algorithms for Consistent Neural decoding

- [FALCON: Few-shot Algorithms for Consistent Neural decoding](https://github.com/snel-repo/falcon-challenge) - Provides DANDI-hosted movement and communication datasets, example decoders, and local evaluation tools for comparing few-shot and adaptive neural decoding across sessions.

### LINK: Long-Term Intracortical Neural Activity and Kinematics

- [LINK: Long-Term Intracortical Neural Activity and Kinematics](https://chesteklab.github.io/LINK_dataset/) - Provides NWB neural and finger-kinematic data from 312 sessions spanning about 3.5 years, enabling study of long-term changes in motor signals and brain-machine-interface decoding.

### Reach-related Single Unit Activity in the Parkinsonian Macaque (DANDI:000947)

- [Reach-related Single Unit Activity in the Parkinsonian Macaque (DANDI:000947)](https://dandiarchive.org/dandiset/000947) - Includes multi-region NWB recordings during macaque reaching, with sessions before and after MPTP-induced parkinsonism; DANDI's linked tutorial demonstrates streaming the files.
