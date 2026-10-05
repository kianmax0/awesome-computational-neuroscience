# Awesome Computational Neuroscience [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Mathematical models, neural computation, and reproducible analysis of brain activity.

计算神经科学资源合集 · A curated guide to computational neuroscience, from single neurons and circuits to learning, cognition, and neural data. English descriptions link to official documentation, author pages, and original publications wherever possible.

## Contents

- [Start here](#start-here)
- [Books](#books)
- [Courses and tutorials](#courses-and-tutorials)
- [Mathematical foundations](#mathematical-foundations)
- [Foundational papers](#foundational-papers)
- [Research topics](#research-topics)
  - [Neuron and dendrite models](#neuron-and-dendrite-models)
  - [Network dynamics](#network-dynamics)
  - [Neural coding](#neural-coding)
  - [Plasticity and learning rules](#plasticity-and-learning-rules)
  - [Probabilistic inference and predictive coding](#probabilistic-inference-and-predictive-coding)
  - [Perception and decision-making](#perception-and-decision-making)
  - [Memory and spatial navigation](#memory-and-spatial-navigation)
  - [Motor control](#motor-control)
- [Neuron and network simulators](#neuron-and-network-simulators)
- [Neural data analysis](#neural-data-analysis)
- [Open datasets](#open-datasets)
- [Data standards and reproducibility](#data-standards-and-reproducibility)
- [NeuroAI and spiking neural networks](#neuroai-and-spiking-neural-networks)
- [Community and conferences](#community-and-conferences)

## Start here

Choose a route based on the question you want to answer:

1. **New to the field:** Start with Neuromatch Academy's Computational Neuroscience course and the free *Neuronal Dynamics* textbook. Implement a leaky integrate-and-fire neuron, then compare its behavior with a biophysical model.
2. **Modeling neurons and circuits:** Use Brian 2 for equation-based spiking networks, NEURON for detailed cellular models, or NEST for large spiking networks. Begin with an official tutorial and reproduce a documented example.
3. **Working with recordings:** Use SpikeInterface and Elephant for extracellular spikes, Suite2p or CaImAn for calcium imaging, and MNE-Python for EEG/MEG. Inspect recording quality and preprocessing before fitting a model.
4. **Connecting brains and AI:** Study coding, plasticity, and population dynamics before exploring NeuroAI courses and spiking-network libraries. Compare models with neural or behavioral observations, as well as task performance.

The routes above are suggested starting points. Access notes distinguish free texts from book information pages; a public dataset may still require an account or agreement.

## Books

- [Neuronal Dynamics: From Single Neurons to Networks and Models of Cognition](https://neuronaldynamics.epfl.ch/online/) - A comprehensive, exercise-rich introduction to spiking neurons, neural coding, populations, networks, learning, and cognition, with [Python exercises](https://neuronaldynamics-exercises.readthedocs.io/en/latest/). Free online book and companion exercises, with an associated [cognitive-model lecture collection](https://lcnwww.epfl.ch/gerstner/NeuronalDynamics-MOOC2.html).
- [Theoretical Neuroscience: Computational and Mathematical Modeling of Neural Systems](https://www.gatsby.ucl.ac.uk/~dayan/book/) - A foundational treatment of neural coding, biophysical neuron and circuit models, plasticity, and learning, with mathematical appendices and exercises. Author page with exercises and a sample chapter; full book via purchase or library.
- [Dynamical Systems in Neuroscience: The Geometry of Excitability and Bursting](https://www.izhikevich.org/publications/dsn/index.htm) - Builds geometric intuition for applying nonlinear dynamics to neuronal excitability, spiking patterns, and bursting. Free full-text PDF on the author's site.
- [Spikes: Exploring the Neural Code (introductory chapter)](https://swh.princeton.edu/~wbialek/our_papers/spikes_intro.pdf) - Develops quantitative ways to ask how sensory information is represented in spike trains, grounded in experiments on sensory neurons. Free introductory chapter from coauthor William Bialek; full print editions are out of print.
- [Fundamentals of Computational Neuroscience](https://academic.oup.com/book/45368) - An introductory text covering neuroscience concepts, programming, mathematical foundations, neuron and population models, networks, and brain-level examples. Publisher listing for the third edition; purchase or institutional access.
- [An Introductory Course in Computational Neuroscience](https://github.com/primon23/Intro-Comp-Neuro) - A course-oriented path from mathematical and coding preliminaries to single neurons, circuits, and systems-level computational models. Author-announced MATLAB companion code; full book via purchase or library.
- [Neural Data Science in Python](https://neuraldatascience.io/) - An online textbook teaching Python data analysis through neuroscience examples including single-unit recordings, EEG, and fMRI. Free online text.

### Biological background

- [Brain Facts: A Primer on the Brain and Nervous System](https://www.brainfacts.org/brain-basics) - A concise, illustrated primer on brain structures, neurons, signaling, circuits, and major neuroscience topics for readers who need biological context. Free primer from the Society for Neuroscience.

## Courses and tutorials

- [Neuromatch Academy: Computational Neuroscience](https://compneuro.neuromatch.io/tutorials/intro.html) - A broad, hands-on curriculum spanning modeling, model fitting, GLMs, dimensionality reduction, deep learning, signal processing, neuron models, dynamics, Bayesian decisions, and reinforcement learning. Free online coursebook.
- [Computational Neuroscience (University of Washington / Coursera)](https://www.coursera.org/learn/computational-neuroscience) - A beginner-level course introducing computational methods for understanding what nervous systems do and how they function. Enrollment and certificate fees depend on Coursera access options.
- [Introduction to Computational Neuroscience (MIT OCW 9.29J)](https://ocw.mit.edu/courses/9-29j-introduction-to-computational-neuroscience-spring-2004/) - Archived MIT course materials by Sebastian Seung, including lecture notes and problem sets for a computational neuroscience introduction. Free materials from the 2004 course.
- [Computational Neuroscience (University of Edinburgh Open Course Materials)](https://opencourse.inf.ed.ac.uk/cns/schedule) - A structured course with lecture slides, computational labs, readings, and topics from differential equations and neuron models to spike statistics and neural coding. Open slides and labs; some readings need library access.
- [Introduction to Computational Neuroscience (NPTEL, IIT Madras)](https://nptel.ac.in/courses/102106023) - A lecture-based introduction to neurobiology, mathematical preliminaries, Hodgkin–Huxley and simplified neuron models, neural networks, and learning. Online lecture materials; certification is separate.

## Mathematical foundations

- [Mathematics for Machine Learning](https://mml-book.github.io/) - A visual, application-focused review of linear algebra, analytic geometry, matrix decompositions, vector calculus, probability, optimization, and machine learning. Free author-provided PDF.
- [Statistical Thinking for the 21st Century](https://statsthinking21.org/) - An applied statistics text emphasizing data, uncertainty, modeling, resampling, hypothesis tests, Bayesian reasoning, and reproducible analysis. Free online text with Python and R companions.
- [Linear Algebra (MIT OpenCourseWare 18.06)](https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/) - Gilbert Strang's course covers systems of equations, vector spaces, determinants, eigenvalues, similarity, and positive-definite matrices. Free course materials.
- [Introduction to Probability and Statistics (MIT OpenCourseWare 18.05)](https://ocw.mit.edu/courses/18-05-introduction-to-probability-and-statistics-spring-2022/) - A course in probability distributions, Bayesian inference, estimation, hypothesis testing, confidence intervals, and regression, with readings and problem sets. Free course materials.
- [Notes on Diffy Qs: Differential Equations for Engineers](https://www.jirka.org/diffyqs/) - An exercise-rich introduction to ordinary differential equations, systems, nonlinear dynamics, Fourier series, and linear algebra, directly useful for neuronal dynamics. Free online book and PDF.
- [Probabilistic Machine Learning: Advanced Topics](https://probml.github.io/pml-book/book2.html) - Kevin Murphy's reference for probabilistic modeling, approximate inference, latent-variable models, and decision-making methods. Free author-provided draft PDF and companion code.
- [Reinforcement Learning: An Introduction (Second Edition)](https://mitpress.mit.edu/9780262039246/reinforcement-learning/) - A foundational account of reinforcement-learning concepts and algorithms, from tabular methods through function approximation, policy gradients, and applications including connections to psychology and neuroscience. Publisher listing; purchase or library access. The publisher also links an author-hosted open edition.

## Foundational papers

A small reading path through modeling, coding, learning, and population dynamics. Links lead to bibliographic records or author pages with available full text; inclusion describes the contribution of a paper, not a claim that its model explains all neural systems.

- [A quantitative description of membrane current and its application to conduction and excitation in nerve](https://pubmed.ncbi.nlm.nih.gov/12991237/) - Hodgkin and Huxley (1952): Conductance-based equations connecting ionic currents to action potentials.
- [Neural networks and physical systems with emergent collective computational abilities](https://pubmed.ncbi.nlm.nih.gov/6953413/) - Hopfield (1982): Recurrent networks and content-addressable memory through collective dynamics.
- [Emergence of simple-cell receptive field properties by learning a sparse code for natural images](https://pubmed.ncbi.nlm.nih.gov/8637596/) - Olshausen and Field (1996): Sparse coding as a model of receptive-field structure in visual cortex.
- [A neural substrate of prediction and reward](https://pubmed.ncbi.nlm.nih.gov/9054347/) - Schultz, Dayan, and Montague (1997): Connections between dopamine responses and reward prediction errors.
- [Synaptic modifications in cultured hippocampal neurons: dependence on spike timing, synaptic strength, and postsynaptic cell type](https://pubmed.ncbi.nlm.nih.gov/9852584/) - Bi and Poo (1998): Experimental constraints on spike-timing-dependent synaptic plasticity.
- [Predictive coding in the visual cortex: a functional interpretation of some extra-classical receptive-field effects](https://pubmed.ncbi.nlm.nih.gov/10195184/) - Rao and Ballard (1999): A hierarchical model using feedback predictions and feedforward residual errors.
- [Simple model of spiking neurons](https://www.izhikevich.org/publications/spikes.htm) - Izhikevich (2003): A compact model reproducing several spiking and bursting patterns.
- [Neural population dynamics during reaching](https://pubmed.ncbi.nlm.nih.gov/22722855/) - Churchland et al. (2012): A population-level dynamical perspective on motor cortical activity.

## Research topics

Focused resources connect the broad reading path to specific research questions. Each resource is listed once; its documentation, companion code, lecture episodes, and dataset splits stay with the parent entry.

### Neuron and dendrite models

- [Allen Cell Types Database: Neuronal Models](https://brain-map.org/support/documentation/cell-types-database-api) - Browse electrophysiology-linked GLIF point-neuron and perisomatic biophysical models with dendritic morphology, then download and run models through the Allen SDK; biophysical models require NEURON.
- [Dendrify](https://dendrify.readthedocs.io/en/latest/) - Build reduced-compartment neuron models with active dendritic and synaptic properties for Brian 2 networks; install with Python and Brian 2, and use the official tutorials for custom models and simulation.
- [Jaxley](https://jaxley.readthedocs.io/en/stable/) - Define and fit differentiable multicompartment biophysical neuron models with JAX on CPU, GPU, or TPU; CPU support is available through the standard install, while accelerators require a compatible JAX backend.
- [Neuroscience for Machine Learners (Neuro4ML)](https://training.incf.org/course/neuroscience-machine-learners-neuro4ml) - A free INCF course for machine-learning audiences covering biophysical and multicompartment neuron models, synapses, Dendrify, networks, and accompanying practical exercises.

### Network dynamics

- [Modeling Neural Circuits Made Simple with Python](https://github.com/RobertRosenbaum/ModelingNeuralCircuits) - An accessible computational neuroscience text that builds from neuron biophysics to neural coding, learning, and whole-network models, with a free author-provided PDF and Python notebooks for exploring circuit behavior and analyzing example recordings.
- [Neural Fields: Theory and Applications](https://link.springer.com/book/10.1007/978-3-642-54593-1) - An edited reference on neural-field models, spatially extended population dynamics, and their mathematical foundations; full-book access may require a purchase or library subscription.
- [Dynamical Neural Systems](https://training.incf.org/course/dynamical-neural-systems) - A free INCF course covering neural stability, oscillations, bursting, coupled oscillators, firing-rate networks, and spatiotemporal patterns through a structured lecture sequence.
- [Large-Scale Modeling of Brain Dynamics](https://training.incf.org/course/large-scale-modeling-brain-dynamics) - A hands-on INCF tutorial implementing coupled Wilson–Cowan neural masses with empirical structural connectivity to explore BOLD signals and lesion effects; the catalog was verified, but interactive lesson access on JavaScript-based Learn Gala remains unverified.
- [Cajal Course in Computational Neuroscience](https://training.incf.org/course/cajal-course-computational-neuroscience) - A structured graduate-level course with focused units on balanced excitatory–inhibitory network stability, gain modulation, and rate-based and spiking balanced-network dynamics; free online materials.
- [Computation-through-Dynamics Benchmark and Toolkit](https://github.com/snel-repo/ComputationThroughDynamicsToolkit) - Compare inferred neural dynamics against task-trained reference models using synthetic spiking datasets and interpretable metrics; installation uses Conda/Python 3.10 and Git LFS, the walkthrough assets require several gigabytes of disk, and GPU access may be needed for default data-model training.
- [Potjans–Diesmann Cortical Microcircuit Model in NetPyNE](https://modeldb.science/266872) - A documented layered cortical network implementation with scripts for rescaling and extending the model to multicompartment neurons, available through ModelDB and its linked code repository; requires Python, NetPyNE, and NEURON, and full-size runs can be compute-intensive.

### Neural coding

- [Coding and Vision 101](https://training.incf.org/course/coding-and-vision-101) - A free 12-lecture Allen Institute course on visual-system organization and neural coding, including information-theoretic analysis of neuronal responses; it helps examine what visual neurons represent and how response properties can be quantified.
- [The Neural Code (UCL Cortexlab)](https://www.ucl.ac.uk/brain-sciences/cortexlab/courses/neuroinformatics-class-page) - Public lecture slides and Colab worksheets cover rate, temporal, and population codes, decoding, information theory, and point processes; the practicals show how competing coding hypotheses can be tested on neural data.
- [Statistical Models for Neural Data (COSYNE / INCF TrainingSpace)](https://training.incf.org/course/statistical-models) - Two free, in-depth tutorial lectures progress from GLMs to latent-variable models and discuss coding, multiple spike trains, and regularization; they help readers compare models for structure in neural responses.
- [Information Theory and Neural Coding](https://www.nature.com/articles/nn1199_947) - Borst and Theunissen’s review explains information-theoretic tests of stimulus-response models and spike-time precision; it clarifies information estimates and their assumptions, and full text requires institutional access or purchase.
- [SPIKY](https://www.thomaskreuz.org/source-codes/spiky) - This MATLAB GUI calculates and visualizes ISI-distance, SPIKE-distance, and spike-train synchrony across multiple trains, for comparing similarity and synchrony across population spike trains; the maintainer page offers a download, and MATLAB is required.

### Plasticity and learning rules

- [Computational Modeling of Neuronal Plasticity](https://training.incf.org/course/computational-modeling-neuronal-plasticity) - A free intermediate course provides notes, code, exercises, and solutions for building a LIF model and adding STDP, synaptic normalization, intrinsic plasticity, facilitation, and depression; it shows how distinct plasticity mechanisms change neuronal and synaptic behavior.
- [NESTML Dopamine-Modulated STDP Tutorial](https://nestml.readthedocs.io/en/latest/tutorials/stdp_dopa_synapse/stdp_dopa_synapse.html) - This executable NESTML tutorial implements an eligibility trace gated by dopamine and demonstrates reward- and punishment-modulated learning; it illustrates how delayed reinforcement can assign credit to earlier spike patterns; running it requires NEST/NESTML and compilation dependencies.
- [Brian 2 Clopath Voltage-Based STDP Example](https://brian2.readthedocs.io/en/latest/examples/frompapers.Clopath_et_al_2010_no_homeostasis.html) - This code implements an adapted voltage-based triplet STDP rule in Brian 2 and illustrates frequency-dependent changes; the example omits homeostatic metaplasticity and says its parameters are qualitative rather than fitted.
- [A Simple Model of Neuromodulatory State-Dependent Synaptic Plasticity](https://modeldb.science/222932) - ModelDB provides the Python implementation and associated files for a model of how neuromodulatory state changes synaptic plasticity; it supports exploration of how state-dependent modulation affects cortical learning and learning rate; model-specific Python dependencies apply.
- [Synaptic Plasticity Forms and Functions](https://www.annualreviews.org/content/journals/10.1146/annurev-neuro-090919-022842) - This review compares Hebbian, three-factor/eligibility-trace, supervised, and behavioral-timescale plasticity by their functions and limitations; it helps relate rule classes to learning capabilities; full text may require institutional access.
- [Spike Timing-Dependent Plasticity: A Consequence of More Fundamental Learning Rules](https://www.frontiersin.org/journals/computational-neuroscience/articles/10.3389/fncom.2010.00019/full) - This open review explains why spike-pair timing alone cannot capture many observed plasticity effects and discusses cellular-mechanism models; it outlines when a simple STDP rule is inadequate.

### Probabilistic inference and predictive coding

- [Bayesian Models of Learning and Integration of Neuroimaging Data](https://training.incf.org/course/bayesian-models-learning-and-integration-neuroimaging-data) - A course combining Bayesian models of learning and perception, Hierarchical Gaussian Filter tutorials, and Bayesian dynamic causal modeling for fMRI and EEG; free INCF-hosted lessons, slides, code, and datasets.
- [Bayesian Brain: Probabilistic Approaches to Neural Coding](https://mitpress.mit.edu/9780262042383/bayesian-brain/) - An edited collection on Bayesian approaches to neural coding, perception, decision-making, and belief propagation, useful for connecting probabilistic models with spike-train and neuroimaging data; purchase or library access.
- [Predictive Coding: a Theoretical and Experimental Review](https://arxiv.org/abs/2107.12979) - A review of predictive coding's mathematical structure, proposed neural implementations, empirical predictions, and connections to backpropagation and machine learning; free author manuscript.
- [Predictive Coding Networks and Inference Learning: Tutorial and Survey](https://arxiv.org/abs/2407.04117) - An open tutorial and survey specifying predictive-coding network inference and learning procedures, with complexity analysis and supplemental derivations, useful for comparing concrete algorithms.
- [Predictive Coding](https://github.com/Bogacz-Group/PredictiveCoding) - A Python repository with executable notebooks for supervised, unsupervised, recurrent, temporal, and bidirectional predictive-coding models; install the listed Python requirements to run the examples.
- [HGF Toolbox](https://github.com/ComputationalPsychiatry/hgf-toolbox) - A maintained MATLAB toolbox for fitting and simulating Hierarchical Gaussian Filter belief trajectories and choice models, with demos and architecture documentation; requires MATLAB.
- [pymdp](https://github.com/infer-actively/pymdp) - A documented Python package for building discrete-state Active Inference agents in partially observable Markov decision processes, with quick-start and task notebooks; Python/JAX setup required.

### Perception and decision-making

- [Computational Cognitive Neuroscience (Edinburgh)](https://opencourse.inf.ed.ac.uk/ccn) - An open course on how neural computations produce perception, learning, and decisions, with probabilistic models, reinforcement learning, fitting, and model comparison; assumes coding and basic quantitative preparation.
- [Computational Cognitive Neuroscience](https://book.compcogneuro.org/) - A free online textbook connecting neural-network principles to perception, learning, memory, and other cognitive functions, with companion simulations and downloadable PDF/ePub versions.
- [Computational Models of Decision Making](https://www.cambridge.org/core/books/abs/cambridge-handbook-of-computational-cognitive-sciences/computational-models-of-decision-making/0465E07014E1543151E52851E8E65EC2) - A handbook chapter comparing computational choice models and explaining sequential evidence accumulation, process tracing, and model discrimination; purchase or library access may be required.
- [PyDDM](https://pyddm.readthedocs.io/en/stable/) - A Python framework for simulating and fitting generalized drift-diffusion models with time- or state-dependent components, with tutorials that validate models against open choice/response-time data; docs note beta status.
- [HSSM](https://lnccbrown.github.io/HSSM/) - A maintained Python package and tutorial set for hierarchical Bayesian fitting of choice and response-time data with sequential-sampling models, including regression, reinforcement-learning models, diagnostics, and model comparison; Python 3.12 or newer required.
- [IBL decision-making behavior data](https://docs.internationalbrainlab.org/notebooks_external/2021_data_release_behavior.html) - Open mouse-training data with visual stimuli, choices, and response times for studying how sensory-guided decisions change from novice to expert; download through the ONE API and cite the associated data release.

### Memory and spatial navigation

- [Hippocampal Microcircuits: A Computational Modeler's Resource Book](https://link.springer.com/book/10.1007/978-3-319-99103-0) - Connects hippocampal cellular and circuit models to memory, rhythms, and spatial navigation; publisher information page, with full text via purchase or library.
- [RatInABox](https://github.com/RatInABox-Lab/RatInABox) - Simulates continuous-space movement and generates synthetic place-, grid-, boundary-vector-, and head-direction-cell activity, with worked notebooks for spatial coding and decoding.
- [NeuralPlayground](https://github.com/SainsburyWellcomeCentre/NeuralPlayground) - Provides arenas, published hippocampal and entorhinal models, and experimental datasets in a common Python interface for comparing spatial representations; installation and tutorial instructions are available in the repository.
- [Models of Vector Navigation with Grid Cells (ModelDB)](https://modeldb.science/182685) - Collects four MATLAB models that use grid-cell codes to estimate the direction or displacement from a start location to a goal.
- [Place and Grid Cells in a Loop (ModelDB)](https://modeldb.science/241932) - Provides a Python attractor-network model of interacting place and grid cells for studying spatial coding and remapping.
- [Odor-Place Spatial Association Task (DANDI:001539)](https://dandiarchive.org/dandiset/001539) - Shares rat hippocampal, prefrontal, and olfactory-bulb recordings with position and trial outcomes during an odor-place memory task; open access through DANDI.
- [Grid Cells and Spatial Maps in Entorhinal Cortex and Hippocampus](https://link.springer.com/chapter/10.1007/978-3-319-28802-4_5) - Reviews how grid and place-cell representations support spatial maps, remapping, and memory; full chapter text is available through Springer and the linked free NCBI Bookshelf edition.

### Motor control

- [The Computational Neurobiology of Reaching and Pointing](https://mitpress.mit.edu/9780262195089/the-computational-neurobiology-of-reaching-and-pointing/) - Develops computational accounts of limb mechanics, state estimation, reaching, and motor learning, with supplemental simulation code and derivations; full book via purchase or library.
- [Computational Motor Control (Reza Shadmehr)](https://courses.shadmehrlab.org/compmc.html) - Teaches motor control through robotics, control theory, biomechanical models, sensory feedback, and neural evidence, with lecture materials and homework; simulations require Mathematica or MATLAB.
- [Embodied Sensorimotor Control: Computational Modeling of the Neural Control of Movement](https://www.annualreviews.org/content/journals/10.1146/annurev-bioeng-102723-020454) - Reviews how neural population dynamics, feedback control, and body mechanics combine in models of movement; 2026 Annual Reviews article, with access depending on subscription.
- [MyoSuite](https://myosuite.readthedocs.io/en/stable/) - Offers MuJoCo-based, muscle-actuated reaching, hand-manipulation, and locomotion environments for studying and benchmarking musculoskeletal control; see its installation guide and task documentation.
- [FALCON: Few-shot Algorithms for Consistent Neural decoding](https://github.com/snel-repo/falcon-challenge) - Provides DANDI-hosted movement and communication datasets, example decoders, and local evaluation tools for comparing few-shot and adaptive neural decoding across sessions.
- [LINK: Long-Term Intracortical Neural Activity and Kinematics](https://chesteklab.github.io/LINK_dataset/) - Provides NWB neural and finger-kinematic data from 312 sessions spanning about 3.5 years, enabling study of long-term changes in motor signals and brain-machine-interface decoding.
- [Reach-related Single Unit Activity in the Parkinsonian Macaque (DANDI:000947)](https://dandiarchive.org/dandiset/000947) - Includes multi-region NWB recordings during macaque reaching, with sessions before and after MPTP-induced parkinsonism; DANDI's linked tutorial demonstrates streaming the files.
- [Computational Mechanisms of Sensorimotor Control](https://wolpertlab.neuroscience.columbia.edu/sites/wolpertlab.neuroscience.columbia.edu/files/content/papers/FraWol11.pdf) - Synthesizes optimal feedback, impedance control, prediction, Bayesian decision theory, and sensorimotor learning as solutions to uncertainty, noise, delay, and redundancy in movement; free author-posted full text.

## Neuron and network simulators

Open-source tools for cellular, circuit, and whole-brain models. Choose a simulator based on the scale and mechanisms your question requires.

- [NEURON](https://www.neuronsimulator.org/en/latest/) - Simulate morphologically detailed single neurons and networks with Python, HOC, or NEURON's GUI.
- [Brian 2](https://brian2.readthedocs.io/en/stable/) - A flexible Python simulator for spiking neural networks, designed for concise model specification and extensibility, with a [pair-based STDP example](https://brian2.readthedocs.io/en/latest/examples/synapses.STDP.html).
- [NEST Simulator](https://nest-simulator.readthedocs.io/en/stable/) - Simulate large networks of spiking neurons with a broad library of neuron, synapse, and plasticity models; the related NESTML project supplies a [weight-dependent pair-STDP model](https://github.com/nest/nestml/blob/main/models/synapses/stdp_synapse.nestml).
- [Arbor](https://docs.arbor-sim.org/en/latest/) - A high-performance library for multicompartment neuron and network simulations on modern CPU and GPU systems.
- [NetPyNE](https://github.com/suny-downstate-medical-center/netpyne) - A Python package for defining, simulating, and analyzing biological neuronal networks, built around NEURON.
- [GeNN](https://genn-team.github.io/) - A code-generation framework that accelerates spiking neural network simulations on GPUs. GPU execution requires a compatible GPU backend.
- [PyNN](https://pynn.readthedocs.io/en/latest/) - A simulator-independent Python API for writing neuronal network models across supported simulators and neuromorphic systems. Requires a supported simulator backend.
- [The Virtual Brain](https://docs.thevirtualbrain.org/) - Simulate large-scale brain-network dynamics from structural connectivity using neural-mass models and generate EEG, MEG, or BOLD-like signals.
- [Nengo](https://www.nengo.ai/nengo/) - Build and simulate spiking or non-spiking neural models using the Neural Engineering Framework and extensible backends.
- [ModelDB](https://modeldb.science/) - A curated repository of computational neuroscience models linked to published research, with searchable metadata and downloadable code. Model-specific simulators and dependencies vary.

## Neural data analysis

### Tutorials and methodological reviews

- [NiPraxis: Practice and theory of brain imaging](https://textbook.nipraxis.org/intro.html) - A free online textbook with Python exercises on NIfTI images, voxel time series, regression, GLMs, and reproducibility for understanding and building fMRI analyses.
- [NeuroHackademy lecture archive](https://neurohackademy.org/archive/) - Recorded summer-school lectures and tutorials on neuroimaging, neural decoding, statistical learning, and reproducible computing for developing a complete data-analysis workflow.
- [Neural data science: accelerating the experiment-analysis-theory cycle in large-scale neuroscience](https://sites.stat.columbia.edu/liam/teaching/neurostat-fall17/CONB.pdf) - Paninski and Cunningham's review connects signal extraction, dimensionality reduction, decoding, and network inference to the questions large-scale recordings can answer; free author-hosted manuscript.

### Spikes and population activity

- [SpikeInterface](https://spikeinterface.readthedocs.io/en/latest/) - A unified Python framework for extracellular recording I/O, preprocessing, spike sorting, comparison, validation, and curation.
- [Kilosort](https://kilosort.readthedocs.io/en/latest/) - GPU-accelerated spike sorting software for high-density extracellular recordings, with drift correction. A suitable GPU is typically needed for full recordings.
- [phy](https://phy.readthedocs.io/en/latest/) - An interactive GUI for visualizing and manually curating spike-sorted high-density electrophysiology datasets.
- [Elephant](https://elephant.readthedocs.io/en/latest/) - A Python toolkit for generic spike-train and electrophysiology time-series analyses, including LFP and intracellular signals.
- [Pynapple](https://pynapple.org/) - A lightweight Python library for neural and behavioral time series, intervals, tuning curves, cross-correlograms, and related population analyses.
- [CEBRA](https://cebra.ai/docs/) - A documented contrastive-learning implementation with neural and behavioral notebooks for estimating latent embeddings and studying how population activity relates to measured behavior.
- [lfads-torch](https://github.com/arsedler9/lfads-torch) - A PyTorch implementation of LFADS and AutoLFADS with data preparation and training walkthroughs for inferring latent dynamics and firing rates from population spike recordings.

### Calcium imaging

- [Suite2p](https://suite2p.readthedocs.io/) - A Python pipeline for calcium-imaging registration, ROI detection, signal extraction, classification, and spike deconvolution.
- [CaImAn](https://caiman.readthedocs.io/en/latest/) - A computational toolbox for calcium-imaging motion correction, source extraction, deconvolution, and online analysis.

### EEG and MEG

- [MNE-Python](https://mne.tools/stable/) - An open-source Python package for exploring, visualizing, and analyzing EEG, MEG, iEEG, and related human neurophysiology data.
- [FieldTrip](https://www.fieldtriptoolbox.org/) - An open-source MATLAB toolbox with tutorials and methods for MEG, EEG, invasive electrophysiology, and source analysis. Requires MATLAB or a compatible environment.

### fMRI

- [Nilearn](https://nilearn.github.io/stable/index.html) - Python tools and worked examples for fMRI GLMs, decoding, functional connectivity, and visualization, useful for testing statistical models of brain images.
- [fMRIPrep](https://fmriprep.org/en/stable/) - A documented pipeline that preprocesses BIDS fMRI data and produces visual quality-control reports and analysis-ready derivatives; relevant FreeSurfer components require a license file.

### Benchmarks

- [Neural Latents Benchmark](https://neurallatents.github.io/) - Neural spiking datasets, baseline code, and metrics for comparing latent-variable models; local evaluation remains available after EvalAI submissions closed in January 2026, with public test data requiring care to avoid test-set tuning.

### Behavior

- [DeepLabCut](https://deeplabcut.github.io/DeepLabCut/) - A deep-learning toolbox for markerless pose estimation and behavioral tracking of animals and humans.

## Open datasets

Check each dataset's license, subject information, and access conditions before reuse.

- [DANDI Archive](https://dandiarchive.org/) - A BRAIN Initiative archive for publishing and sharing neurophysiology, optical physiology, behavioral time-series, and related data. Public dataset downloads do not require an account.
- [OpenNeuro](https://openneuro.org/) - An open archive of BIDS-formatted MRI, PET, MEG, EEG, iEEG, and NIRS datasets. Public dataset downloads do not require an account.
- [Allen Brain Observatory and AllenSDK](https://allensdk.readthedocs.io/en/latest/brain_observatory.html) - Access and analyze mouse visual-cortex datasets spanning two-photon imaging, Neuropixels recordings, stimuli, and behavior. Public datasets; large downloads may require substantial storage.
- [CRCNS Data Sharing](https://crcns.org/data-sets) - A catalog of research datasets for computational neuroscience, covering many brain areas, species, recording methods, and simulations. Most downloads require a free account and acceptance of data-use terms.
- [NeuroMorpho.Org](https://neuromorpho.org/) - A curated, searchable archive of digitally reconstructed neurons and glia with associated metadata. Public morphology downloads.
- [IBL Brain-Wide Map](https://docs.internationalbrainlab.org/notebooks_external/2025_data_release_brainwidemap.html) - Public brain-wide Neuropixels recordings with synchronized task and behavioral variables, release notes, and download tutorials for comparing neural activity across regions and sessions.
- [Natural Scenes Dataset](https://www.naturalscenesdataset.org/) - Repeated 7T fMRI measurements during natural-image viewing support visual encoding, decoding, and model-to-brain comparisons; access requires completing the dataset's agreement.
- [THINGS-data](https://things-initiative.org/) - Matched object-image resources, fMRI and MEG recordings, behavioral similarity judgments, and analysis code support comparing object representations across brains, behavior, and models.
- [Spiking Heidelberg Digits and Spiking Speech Commands](https://zenkelab.org/resources/spiking-heidelberg-datasets-shd/) - Public cochlea-derived spike datasets with labels, loading examples, and evaluation splits provide auditory classification benchmarks for spiking neural networks.

## Data standards and reproducibility

- [Neurodata Without Borders (NWB)](https://nwb.org/) - A community data standard and software ecosystem for sharing and analyzing neurophysiology and behavioral time-series data.
- [Brain Imaging Data Structure (BIDS)](https://bids.neuroimaging.io/) - A community standard for organizing and validating neuroimaging data, including MRI, EEG, MEG, iEEG, PET, and behavioral data.
- [NeuroML](https://docs.neuroml.org/) - A standardized language and tool ecosystem for describing, validating, sharing, and simulating multiscale neural models.
- [Neo](https://neo.readthedocs.io/en/stable/) - A Python object model and file-I/O library that helps electrophysiology analysis tools exchange recordings and spike trains.

## NeuroAI and spiking neural networks

### Courses and reviews

- [Neuromatch Academy: NeuroAI](https://neuroai.neuromatch.io/) - Open course materials connecting neuroscience and AI through generalization, neural representations, circuits, and learning rules.
- [Brains, Minds and Machines Summer Course (MIT OCW)](https://ocw.mit.edu/courses/res-9-003-brains-minds-and-machines-summer-course-summer-2015/) - Free lecture videos, tutorials, and projects connect neural circuits, vision, cognition, and robotics for studying intelligence across biological and artificial systems.
- [Neuroscience-Inspired Artificial Intelligence](https://pubmed.ncbi.nlm.nih.gov/28728020/) - Hassabis and colleagues' review surveys how neural computation has informed AI and identifies shared research questions, providing context for choosing brain-inspired mechanisms to investigate.

### Model comparison and implementations

- [Brain-Score](https://www.brain-score.org/) - An open benchmarking platform for comparing computational models with neural and behavioral measurements across vision and language.
- [Net2Brain](https://net2brain.readthedocs.io/en/latest/) - A toolbox with pretrained model feature extraction, representational dissimilarity matrices, and evaluation methods for comparing artificial-network representations with human brain responses.
- [CORnet](https://github.com/dicarlolab/CORnet) - Documented PyTorch visual-system model variants and pretrained weights support testing feedforward and recurrent accounts of object recognition against neural and behavioral measurements.
- [The Algonauts Project](https://algonautsproject.com/) - Archived challenges, data instructions, and tutorials benchmark prediction of human brain responses to visual and multimodal stimuli; the 2025 competition is closed.

### Spiking networks and event-based data

- [snnTorch](https://snntorch.readthedocs.io/en/stable/) - A PyTorch package for gradient-based learning with spiking neural networks, with tutorials covering neuron models, spike encoding, and surrogate gradients.
- [Norse](https://norse.github.io/norse/) - A PyTorch library of spiking-neuron primitives and modules for building and training spiking neural networks.
- [SpikingJelly](https://github.com/fangwei123456/spikingjelly) - A PyTorch-native framework for large-scale spiking neural network training and inference, with event-based data and acceleration backends.
- [Rockpool](https://rockpool.ai/) - A Python library for designing, simulating, and training spiking or rate-based dynamical networks, including deployment to neuromorphic hardware.
- [Tonic](https://tonic.readthedocs.io/en/latest/) - Dataset loaders, event transformations, and batching tutorials prepare event-based vision and audio data for reproducible spiking-network experiments.

## Community and conferences

- [COSYNE](https://www.cosyne.org/) - A meeting connecting experimental and theoretical approaches to systems neuroscience, with conference and workshop archives.
- [Organization for Computational Neurosciences](https://www.cnsorg.org/) - The community organization behind the annual CNS meeting, with education, events, and community resources.
- [Bernstein Network](https://bernstein-network.de/en/) - A computational neuroscience network with research news, conferences, training opportunities, and job listings.
- [INCF](https://www.incf.org/) - Community resources and standards supporting open, interoperable neuroscience research.
- [Neurostars](https://neurostars.org/) - A public question-and-answer forum for neuroscience software, data, and analysis workflows.

## Contributing

Suggest a resource or report a broken link through [Issues](https://github.com/kianmax0/awesome-computational-neuroscience/issues), or send a pull request following the [contribution guidelines](CONTRIBUTING.md). Explain what the resource helps someone learn or do, and why it belongs in the list.

## Footnotes

- The [2026-10-05 expansion audit](docs/curation/2026-10-05-expansion.md) records resource counts, research-theme coverage, screened candidates, primary-source checks, and unresolved access questions.
- Selection favors resources with a clear computational neuroscience use, accessible documentation, and an identifiable author or project. Classic papers and textbooks are retained for their educational value; software is assessed separately for usability and maintenance.
- Link checks run on pushes, pull requests, a weekly schedule, and manual dispatch. Results and downloadable reports are available in [Actions](https://github.com/kianmax0/awesome-computational-neuroscience/actions); two publisher pages that block automation are documented in [lychee.toml](lychee.toml) for separate review. A successful HTTP response does not establish scientific quality.
- See the [maintenance guide](MAINTAINING.md) for review steps and local checks. Linked books, papers, code, and datasets retain their own licenses and access terms.
