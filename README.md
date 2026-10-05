# Awesome Computational Neuroscience [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Mathematical models, neural computation, and reproducible analysis of brain activity.

计算神经科学资源合集 · A curated guide to computational neuroscience, from single neurons and circuits to learning, cognition, and neural data. English descriptions link to official documentation, author pages, and original publications wherever possible.

## Contents

- [Start here](#start-here)
- [Books](#books)
- [Courses and tutorials](#courses-and-tutorials)
- [Mathematical foundations](#mathematical-foundations)
- [Foundational papers](#foundational-papers)
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

- [Neuronal Dynamics: From Single Neurons to Networks and Models of Cognition](https://neuronaldynamics.epfl.ch/online/) - A comprehensive, exercise-rich introduction to spiking neurons, neural coding, populations, networks, learning, and cognition, with Python exercises. Free online book.
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
- [Neuronal Dynamics: Python Exercises](https://neuronaldynamics-exercises.readthedocs.io/en/latest/) - Executable Python exercises accompanying Neuronal Dynamics, covering neuron models, cable equations, Hodgkin–Huxley dynamics, bifurcations, associative memory, learning, and decision-making. Free exercise documentation and code.

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

## Neuron and network simulators

Open-source tools for cellular, circuit, and whole-brain models. Choose a simulator based on the scale and mechanisms your question requires.

- [NEURON](https://www.neuronsimulator.org/en/latest/) - Simulate morphologically detailed single neurons and networks with Python, HOC, or NEURON's GUI.
- [Brian 2](https://brian2.readthedocs.io/en/stable/) - A flexible Python simulator for spiking neural networks, designed for concise model specification and extensibility.
- [NEST Simulator](https://nest-simulator.readthedocs.io/en/stable/) - Simulate large networks of spiking neurons with a broad library of neuron, synapse, and plasticity models.
- [Arbor](https://docs.arbor-sim.org/en/latest/) - A high-performance library for multicompartment neuron and network simulations on modern CPU and GPU systems.
- [NetPyNE](https://github.com/suny-downstate-medical-center/netpyne) - A Python package for defining, simulating, and analyzing biological neuronal networks, built around NEURON.
- [GeNN](https://genn-team.github.io/) - A code-generation framework that accelerates spiking neural network simulations on GPUs. GPU execution requires a compatible GPU backend.
- [PyNN](https://pynn.readthedocs.io/en/latest/) - A simulator-independent Python API for writing neuronal network models across supported simulators and neuromorphic systems. Requires a supported simulator backend.
- [The Virtual Brain](https://docs.thevirtualbrain.org/) - Simulate large-scale brain-network dynamics from structural connectivity using neural-mass models and generate EEG, MEG, or BOLD-like signals.
- [Nengo](https://www.nengo.ai/nengo/) - Build and simulate spiking or non-spiking neural models using the Neural Engineering Framework and extensible backends.
- [ModelDB](https://modeldb.science/) - A curated repository of computational neuroscience models linked to published research, with searchable metadata and downloadable code. Model-specific simulators and dependencies vary.

## Neural data analysis

### Spikes and population activity

- [SpikeInterface](https://spikeinterface.readthedocs.io/en/latest/) - A unified Python framework for extracellular recording I/O, preprocessing, spike sorting, comparison, validation, and curation.
- [Kilosort](https://kilosort.readthedocs.io/en/latest/) - GPU-accelerated spike sorting software for high-density extracellular recordings, with drift correction. A suitable GPU is typically needed for full recordings.
- [phy](https://phy.readthedocs.io/en/latest/) - An interactive GUI for visualizing and manually curating spike-sorted high-density electrophysiology datasets.
- [Elephant](https://elephant.readthedocs.io/en/latest/) - A Python toolkit for generic spike-train and electrophysiology time-series analyses, including LFP and intracellular signals.

- [Pynapple](https://pynapple.org/) - A lightweight Python library for neural and behavioral time series, intervals, tuning curves, cross-correlograms, and related population analyses.

### Calcium imaging

- [Suite2p](https://suite2p.readthedocs.io/) - A Python pipeline for calcium-imaging registration, ROI detection, signal extraction, classification, and spike deconvolution.
- [CaImAn](https://caiman.readthedocs.io/en/latest/) - A computational toolbox for calcium-imaging motion correction, source extraction, deconvolution, and online analysis.

### EEG and MEG

- [MNE-Python](https://mne.tools/stable/) - An open-source Python package for exploring, visualizing, and analyzing EEG, MEG, iEEG, and related human neurophysiology data.
- [FieldTrip](https://www.fieldtriptoolbox.org/) - An open-source MATLAB toolbox with tutorials and methods for MEG, EEG, invasive electrophysiology, and source analysis. Requires MATLAB or a compatible environment.

### Behavior

- [DeepLabCut](https://deeplabcut.github.io/DeepLabCut/) - A deep-learning toolbox for markerless pose estimation and behavioral tracking of animals and humans.

## Open datasets

Check each dataset's license, subject information, and access conditions before reuse.

- [DANDI Archive](https://dandiarchive.org/) - A BRAIN Initiative archive for publishing and sharing neurophysiology, optical physiology, behavioral time-series, and related data. Public dataset downloads do not require an account.
- [OpenNeuro](https://openneuro.org/) - An open archive of BIDS-formatted MRI, PET, MEG, EEG, iEEG, and NIRS datasets. Public dataset downloads do not require an account.
- [Allen Brain Observatory and AllenSDK](https://allensdk.readthedocs.io/en/latest/brain_observatory.html) - Access and analyze mouse visual-cortex datasets spanning two-photon imaging, Neuropixels recordings, stimuli, and behavior. Public datasets; large downloads may require substantial storage.
- [CRCNS Data Sharing](https://crcns.org/data-sets) - A catalog of research datasets for computational neuroscience, covering many brain areas, species, recording methods, and simulations. Most downloads require a free account and acceptance of data-use terms.
- [NeuroMorpho.Org](https://neuromorpho.org/) - A curated, searchable archive of digitally reconstructed neurons and glia with associated metadata. Public morphology downloads.

## Data standards and reproducibility

- [Neurodata Without Borders (NWB)](https://nwb.org/) - A community data standard and software ecosystem for sharing and analyzing neurophysiology and behavioral time-series data.
- [Brain Imaging Data Structure (BIDS)](https://bids.neuroimaging.io/) - A community standard for organizing and validating neuroimaging data, including MRI, EEG, MEG, iEEG, PET, and behavioral data.
- [NeuroML](https://docs.neuroml.org/) - A standardized language and tool ecosystem for describing, validating, sharing, and simulating multiscale neural models.
- [Neo](https://neo.readthedocs.io/en/stable/) - A Python object model and file-I/O library that helps electrophysiology analysis tools exchange recordings and spike trains.

## NeuroAI and spiking neural networks

- [Brain-Score](https://www.brain-score.org/) - An open benchmarking platform for comparing computational models with neural and behavioral measurements across vision and language.
- [Neuromatch Academy: NeuroAI](https://neuroai.neuromatch.io/) - Open course materials connecting neuroscience and AI through generalization, neural representations, circuits, and learning rules.

- [snnTorch](https://snntorch.readthedocs.io/en/stable/) - A PyTorch package for gradient-based learning with spiking neural networks, with tutorials covering neuron models, spike encoding, and surrogate gradients.
- [Norse](https://norse.github.io/norse/) - A PyTorch library of spiking-neuron primitives and modules for building and training spiking neural networks.
- [SpikingJelly](https://github.com/fangwei123456/spikingjelly) - A PyTorch-native framework for large-scale spiking neural network training and inference, with event-based data and acceleration backends.
- [Rockpool](https://rockpool.ai/) - A Python library for designing, simulating, and training spiking or rate-based dynamical networks, including deployment to neuromorphic hardware.

## Community and conferences

- [COSYNE](https://www.cosyne.org/) - A meeting connecting experimental and theoretical approaches to systems neuroscience, with conference and workshop archives.
- [Organization for Computational Neurosciences](https://www.cnsorg.org/) - The community organization behind the annual CNS meeting, with education, events, and community resources.
- [Bernstein Network](https://bernstein-network.de/en/) - A computational neuroscience network with research news, conferences, training opportunities, and job listings.
- [INCF](https://www.incf.org/) - Community resources and standards supporting open, interoperable neuroscience research.
- [Neurostars](https://neurostars.org/) - A public question-and-answer forum for neuroscience software, data, and analysis workflows.

## Contributing

Suggest a resource or report a broken link through [Issues](https://github.com/kianmax0/awesome-computational-neuroscience/issues), or send a pull request following the [contribution guidelines](CONTRIBUTING.md). Explain what the resource helps someone learn or do, and why it belongs in the list.

## Footnotes

- Selection favors resources with a clear computational neuroscience use, accessible documentation, and an identifiable author or project. Classic papers and textbooks are retained for their educational value; software is assessed separately for usability and maintenance.
- Link checks run on pushes, pull requests, a weekly schedule, and manual dispatch. Results and downloadable reports are available in [Actions](https://github.com/kianmax0/awesome-computational-neuroscience/actions); two publisher pages that block automation are documented in [lychee.toml](lychee.toml) for separate review. A successful HTTP response does not establish scientific quality.
- See the [maintenance guide](MAINTAINING.md) for review steps and local checks. Linked books, papers, code, and datasets retain their own licenses and access terms.
