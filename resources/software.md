# Software

[Repository overview](../README.md) · [Resource index](README.md) · [Topics](../topics/README.md) · [Methods](../methods/README.md)

Software libraries, simulation tools, analysis packages, and model repositories.

## Section navigation

[Data tools and object models](#data-tools-and-object-models) · [Neural data analysis](#neural-data-analysis) · [Synthetic recording software](#synthetic-recording-software) · [Model comparison and visual models](#model-comparison-and-visual-models) · [Spiking neural networks](#spiking-neural-networks) · [Neuron and dendrite modeling](#neuron-and-dendrite-modeling) · [Inference and decision tools](#inference-and-decision-tools) · [Behavioral and navigation environments](#behavioral-and-navigation-environments) · [Network simulators](#network-simulators) · [Simulation interfaces](#simulation-interfaces) · [Whole-brain simulation](#whole-brain-simulation) · [Functional neural models](#functional-neural-models) · [Model repositories](#model-repositories) · [Statistical and simulation-based inference](#statistical-and-simulation-based-inference) · [Population dynamics and model construction](#population-dynamics-and-model-construction) · [Data provenance and reproducible environments](#data-provenance-and-reproducible-environments) · [Recording acquisition and inspection](#recording-acquisition-and-inspection) · [Connectomics and network analysis](#connectomics-and-network-analysis)

## Data tools and object models

### Neo

- [Neo](https://neo.readthedocs.io/en/stable/) - A Python object model and file-I/O library that helps electrophysiology analysis tools exchange recordings and spike trains.

## Neural data analysis

### SpikeInterface

- [SpikeInterface](https://spikeinterface.readthedocs.io/en/latest/) - A unified Python framework for extracellular recording I/O, preprocessing, spike sorting, comparison, validation, and curation, with [ground-truth comparison documentation](https://spikeinterface.readthedocs.io/en/latest/modules/comparison.html) for evaluating sorting accuracy.

### Kilosort

- [Kilosort](https://kilosort.readthedocs.io/en/latest/) - GPU-accelerated spike sorting software for high-density extracellular recordings, with drift correction. A suitable GPU is typically needed for full recordings.

### phy

- [phy](https://phy.readthedocs.io/en/latest/) - An interactive GUI for visualizing and manually curating spike-sorted high-density electrophysiology datasets.

### Elephant

- [Elephant](https://elephant.readthedocs.io/en/latest/) - A Python toolkit for generic spike-train and electrophysiology time-series analyses, including LFP and intracellular signals.

### Pynapple

- [Pynapple](https://pynapple.org/) - A lightweight Python library for neural and behavioral time series, intervals, tuning curves, cross-correlograms, and related population analyses.

### CEBRA

- [CEBRA](https://cebra.ai/docs/) - A documented contrastive-learning implementation with neural and behavioral notebooks for estimating latent embeddings and studying how population activity relates to measured behavior.

### lfads-torch

- [lfads-torch](https://github.com/arsedler9/lfads-torch) - A PyTorch implementation of LFADS and AutoLFADS with data preparation and training walkthroughs for inferring latent dynamics and firing rates from population spike recordings.

### Suite2p

- [Suite2p](https://suite2p.readthedocs.io/) - A Python pipeline for calcium-imaging registration, ROI detection, signal extraction, classification, and spike deconvolution.

### CaImAn

- [CaImAn](https://caiman.readthedocs.io/en/latest/) - A computational toolbox for calcium-imaging motion correction, source extraction, deconvolution, and online analysis.

### MNE-Python

- [MNE-Python](https://mne.tools/stable/) - An open-source Python package for exploring, visualizing, and analyzing EEG, MEG, iEEG, and related human neurophysiology data.

### FieldTrip

- [FieldTrip](https://www.fieldtriptoolbox.org/) - An open-source MATLAB toolbox with tutorials and methods for MEG, EEG, invasive electrophysiology, and source analysis. Requires MATLAB or a compatible environment.

### Nilearn

- [Nilearn](https://nilearn.github.io/stable/index.html) - Python tools and worked examples for fMRI GLMs, decoding, functional connectivity, and visualization, useful for testing statistical models of brain images.

### fMRIPrep

- [fMRIPrep](https://fmriprep.org/en/stable/) - A documented pipeline that preprocesses BIDS fMRI data and produces visual quality-control reports and analysis-ready derivatives; relevant FreeSurfer components require a license file.

### DeepLabCut

- [DeepLabCut](https://deeplabcut.github.io/DeepLabCut/) - A deep-learning toolbox for markerless pose estimation and behavioral tracking of animals and humans.

### SPIKY

- [SPIKY](https://www.thomaskreuz.org/source-codes/spiky) - This MATLAB GUI calculates and visualizes ISI-distance, SPIKE-distance, and spike-train synchrony across multiple trains, for comparing similarity and synchrony across population spike trains; the maintainer page offers a download, and MATLAB is required.

### PCNtoolkit

- [PCNtoolkit](https://pcntoolkit.readthedocs.io/en/stable/) - An open-source Python package for normative-model research and methods teaching with neuroimaging data, including model evaluation, transfer, and comparison; its documentation gives current installation details, and the [normative-modeling protocol](https://pmc.ncbi.nlm.nih.gov/articles/PMC7613648/) covers data selection and interpretation while current docs govern executable steps.

## Synthetic recording software

### MEArec

- [MEArec](https://mearec.readthedocs.io/en/latest/) - Generate synthetic extracellular recordings with known spike times to evaluate spike sorting under controlled conditions; Python package with tutorials and a CLI. Generating new biophysical templates additionally requires NEURON and LFPy.

## Model comparison and visual models

### Net2Brain

- [Net2Brain](https://net2brain.readthedocs.io/en/latest/) - A toolbox with pretrained model feature extraction, representational dissimilarity matrices, and evaluation methods for comparing artificial-network representations with human brain responses.

### CORnet

- [CORnet](https://github.com/dicarlolab/CORnet) - Documented PyTorch visual-system model variants and pretrained weights support testing feedforward and recurrent accounts of object recognition against neural and behavioral measurements.

## Spiking neural networks

### snnTorch

- [snnTorch](https://snntorch.readthedocs.io/en/stable/) - A PyTorch package for gradient-based learning with spiking neural networks, with tutorials covering neuron models, spike encoding, and surrogate gradients.

### Norse

- [Norse](https://norse.github.io/norse/) - A PyTorch library of spiking-neuron primitives and modules for building and training spiking neural networks.

### SpikingJelly

- [SpikingJelly](https://github.com/fangwei123456/spikingjelly) - A PyTorch-native framework for large-scale spiking neural network training and inference, with event-based data and acceleration backends.

### Rockpool

- [Rockpool](https://rockpool.ai/) - A Python library for designing, simulating, and training spiking or rate-based dynamical networks, including deployment to neuromorphic hardware.

### Tonic

- [Tonic](https://tonic.readthedocs.io/en/latest/) - Dataset loaders, event transformations, and batching tutorials prepare event-based vision and audio data for reproducible spiking-network experiments.

### Lava Software Framework

- [Lava Software Framework](https://lava-nc.org/) - An open Python framework for composing event-driven processes and exploring spiking applications on CPU before checking platform-specific hardware support; documentation and walk-through are public.

### Sinabs

- [Sinabs](https://sinabs.readthedocs.io/) - A PyTorch-based spiking-network library with documented conversion and quantization paths for DYNAP-CNN/SPECK development kits; hardware deployment requires a compatible kit, while documentation is public.

## Neuron and dendrite modeling

### Dendrify

- [Dendrify](https://dendrify.readthedocs.io/en/latest/) - Build reduced-compartment neuron models with active dendritic and synaptic properties for Brian 2 networks; install with Python and Brian 2, and use the official tutorials for custom models and simulation.

### Jaxley

- [Jaxley](https://jaxley.readthedocs.io/en/stable/) - Define and fit differentiable multicompartment biophysical neuron models with JAX on CPU, GPU, or TPU; CPU support is available through the standard install, while accelerators require a compatible JAX backend.

### NEURON

- [NEURON](https://www.neuronsimulator.org/en/latest/) - Simulate morphologically detailed single neurons and networks with Python, HOC, or NEURON's GUI.

### Arbor

- [Arbor](https://docs.arbor-sim.org/en/latest/) - A high-performance library for multicompartment neuron and network simulations on modern CPU and GPU systems.

### NeuroDevSim

- [NeuroDevSim](https://github.com/CNS-OIST/NeuroDevSim) - A Python framework for phenomenological simulations of neurite growth, soma migration, environmental interactions, and emerging microcircuits, with tutorials for Python users on Linux or macOS.

### TREES Toolbox

- [TREES Toolbox](https://treestoolbox.org/) - A MATLAB toolbox for graph-based neuronal tree generation, editing, visualization, reconstruction, and analysis; its manual notes incomplete 2010 documentation, and the download page distinguishes interim and stable versions.

## Inference and decision tools

### Predictive Coding

- [Predictive Coding](https://github.com/Bogacz-Group/PredictiveCoding) - A Python repository with executable notebooks for supervised, unsupervised, recurrent, temporal, and bidirectional predictive-coding models; install the listed Python requirements to run the examples.

### HGF Toolbox

- [HGF Toolbox](https://github.com/ComputationalPsychiatry/hgf-toolbox) - A maintained MATLAB toolbox for fitting and simulating Hierarchical Gaussian Filter belief trajectories and choice models, with demos and architecture documentation; requires MATLAB.

### pymdp

- [pymdp](https://github.com/infer-actively/pymdp) - A documented Python package for building discrete-state Active Inference agents in partially observable Markov decision processes, with quick-start and task notebooks; Python/JAX setup required.

### PyDDM

- [PyDDM](https://pyddm.readthedocs.io/en/stable/) - A Python framework for simulating and fitting generalized drift-diffusion models with time- or state-dependent components, with tutorials that validate models against open choice/response-time data; docs note beta status.

### HSSM

- [HSSM](https://lnccbrown.github.io/HSSM/) - A maintained Python package and tutorial set for hierarchical Bayesian fitting of choice and response-time data with sequential-sampling models, including regression, reinforcement-learning models, diagnostics, and model comparison; Python 3.12 or newer required.

### hBayesDM

- [hBayesDM](https://github.com/CCS-Lab/hBayesDM) - An R and Python package for research on reinforcement-learning and decision-making behavior through hierarchical Bayesian models implemented with Stan; its documentation gives language-specific setup, and the [open package paper](https://pmc.ncbi.nlm.nih.gov/articles/PMC5869013/) describes model comparisons and trial-wise neural regressors.

## Behavioral and navigation environments

### NeuroGym

- [NeuroGym](https://neurogym.github.io/neurogym/latest/) - A Python collection of behavioral tasks with a common Gymnasium-based interface, including delayed matching, working memory, and perceptual decisions; includes recurrent-network training examples with PyTorch and Keras.

### RatInABox

- [RatInABox](https://github.com/RatInABox-Lab/RatInABox) - Simulates continuous-space movement and generates synthetic place-, grid-, boundary-vector-, and head-direction-cell activity, with worked notebooks for spatial coding and decoding.

### NeuralPlayground

- [NeuralPlayground](https://github.com/SainsburyWellcomeCentre/NeuralPlayground) - Provides arenas, published hippocampal and entorhinal models, and experimental datasets in a common Python interface for comparing spatial representations; installation and tutorial instructions are available in the repository.

### MyoSuite

- [MyoSuite](https://myosuite.readthedocs.io/en/stable/) - Offers MuJoCo-based, muscle-actuated reaching, hand-manipulation, and locomotion environments for studying and benchmarking musculoskeletal control; see its installation guide and task documentation.

## Network simulators

### Brian 2

- [Brian 2](https://brian2.readthedocs.io/en/stable/) - A flexible Python simulator for spiking neural networks, designed for concise model specification and extensibility, with a [pair-based STDP example](https://brian2.readthedocs.io/en/latest/examples/synapses.STDP.html).

### NEST Simulator

- [NEST Simulator](https://nest-simulator.readthedocs.io/en/stable/) - Simulate large networks of spiking neurons with a broad library of neuron, synapse, and plasticity models; the related NESTML project supplies a [weight-dependent pair-STDP model](https://github.com/nest/nestml/blob/main/models/synapses/stdp_synapse.nestml).

### NetPyNE

- [NetPyNE](https://github.com/suny-downstate-medical-center/netpyne) - A Python package for defining, simulating, and analyzing biological neuronal networks, built around NEURON.

### GeNN

- [GeNN](https://genn-team.github.io/) - A code-generation framework that accelerates spiking neural network simulations on GPUs. GPU execution requires a compatible GPU backend.

## Simulation interfaces

### PyNN

- [PyNN](https://pynn.readthedocs.io/en/latest/) - A simulator-independent Python API for writing neuronal network models across supported simulators and neuromorphic systems. Requires a supported simulator backend.

### SpiNNaker software and sPyNNaker documentation

- [SpiNNaker software and sPyNNaker documentation](https://spinnakermanchester.github.io/) - University of Manchester documentation for the SpiNNaker platform includes its PyNN interface, current release paths, and installation guidance; running on physical SpiNNaker requires local hardware or access to a hosted machine.

## Whole-brain simulation

### The Virtual Brain

- [The Virtual Brain](https://docs.thevirtualbrain.org/) - Simulate large-scale brain-network dynamics from structural connectivity using neural-mass models and generate EEG, MEG, or BOLD-like signals.

## Functional neural models

### Nengo

- [Nengo](https://www.nengo.ai/nengo/) - Build and simulate spiking or non-spiking neural models using the Neural Engineering Framework and extensible backends.

## Model repositories

### ModelDB

- [ModelDB](https://modeldb.science/) - A curated repository of computational neuroscience models linked to published research, with searchable metadata and downloadable code. Model-specific simulators and dependencies vary.

## Statistical and simulation-based inference

### sbi

- [sbi](https://sbi.readthedocs.io/en/latest/) - A Python toolkit for estimating parameter uncertainty from simulators, with Bayesian-workflow diagnostics and a [Hodgkin–Huxley inference example](https://sbi.readthedocs.io/en/latest/tutorials/Example_00_HodgkinHuxleyModel.html); requires Python, PyTorch, and a simulator with a suitable simulation budget.

## Population dynamics and model construction

### PyRates

- [PyRates](https://pyrates.readthedocs.io/en/latest/) - A Python framework for constructing dynamical systems from equations and connected model components, with neural-population models, documented examples, parameter sweeps, and multiple execution backends; setup depends on the selected backend.

## Data provenance and reproducible environments

### DataLad

- [DataLad](https://www.datalad.org/) - Version-control and provenance tools for data and code, with a [handbook](https://handbook.datalad.org/en/latest/) covering reproducible neuroimaging and on-demand data access; installation uses Python, Git, and git-annex.

### Neurodesk

- [Neurodesk](https://neurodesk.org/) - Container-based neuroimaging environments and tutorials for using versioned analysis tools through desktops, notebooks, command lines, or computing clusters; consult the setup guide for container and host requirements.

## Recording acquisition and inspection

### Open Ephys GUI

- [Open Ephys GUI](https://open-ephys.github.io/gui-docs/) - A plugin-based application and documentation for acquiring extracellular electrophysiology recordings, with installation and workflow tutorials; recording new signals requires compatible acquisition hardware, and some plugins are operating-system specific.

## Connectomics and network analysis

### Brain Connectivity Toolbox

- [Brain Connectivity Toolbox](https://sites.google.com/site/bctnet/getting-started) - A MATLAB toolbox for graph analysis of structural and functional brain-connectivity matrices, with function-specific requirements for directed, weighted, and signed networks; it assumes prepared square adjacency matrices and its official release page lists 2019 as the latest dated update.

### navis

- [navis](https://navis-org.github.io/navis/stable/) - A Python library for loading, transforming, measuring, processing, and visualizing neuron skeletons, meshes, dotprops, and images; Python familiarity is useful, and its documentation includes a quickstart and API reference.

### neuprint-python Client

- [neuprint-python Client](https://connectome-neuprint.github.io/neuprint-python/docs/quickstart.html) - A Python client for querying neuron and synapse graphs hosted by neuPrint, with convenience and Cypher queries; use requires a server address, named dataset, and personal authorization token.
