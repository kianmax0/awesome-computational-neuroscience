# Neuromorphic computing

[Collection overview](../README.md) · [All topics](README.md) · [Learn](../learn/README.md) · [Methods](../methods/README.md) · [Resource library](../resources/README.md)

Neuromorphic computing studies hardware and software organized around neural or event-based computation. The term covers distinct designs: digital many-core processors, mixed-signal systems, event-driven accelerators, and conventional-machine simulators. A model that uses spikes does not by itself run on neuromorphic hardware, and hardware deployment does not establish biological fidelity.

## Questions to bring

- What computation is represented, and which features of the target hardware does the algorithm use?
- Does a reported time refer to simulated biological time, wall-clock processing time, or end-to-end sensor-to-output latency?
- Is the result from a simulator, a software emulation, or a physical device?
- Which measurements support an efficiency claim: task accuracy, latency, energy, throughput, or some combination?
- What conversion, quantization, memory, connectivity, and access constraints shape the implementation?

## Scope and prerequisites

This guide focuses on programming and evaluating neuromorphic systems for computational neuroscience and event-based machine learning. It introduces software and hardware interfaces, mapping, data, and evaluation; it is not a survey of device physics or a claim that one architecture is best. Know basic Python, neural networks, and spiking-neuron dynamics. Familiarity with PyTorch or PyNN helps with the routes below. Hardware access varies: some frameworks run on local CPUs, while physical platforms may require a lab account, hosted allocation, or a development kit.

## A short start route

1. Begin with the [Lava walk-through](../resources/software.md#lava-software-framework), which builds a spiking network and runs it on a CPU. Treat this as software execution, not a hardware measurement.
2. Choose a platform model and inspect its constraints before mapping: [Sinabs](../resources/software.md#sinabs) describes conversion and quantization for DYNAP-CNN devices; [BrainScaleS-2 documentation](../resources/tutorials-and-examples.md#brainscales-2-user-documentation) and [SpiNNaker software](../resources/software.md#spinnaker-software-and-spynnaker-documentation) expose distinct system and programming interfaces.
3. Use a labeled event dataset such as [IBM DVS Gesture](../resources/datasets-and-benchmarks.md#ibm-dvs-gesture-dataset) to define a reproducible task and preprocessing path.
4. Record software versions, model and input conversions, device availability, and whether every result came from simulation or hardware.

## Research threads

### Algorithms and hardware mapping

Compare a model before and after platform conversion. Record supported neuron and synapse operations, numeric precision, topology, placement, event routing, and any unsupported layers or fallbacks. A framework’s CPU backend is useful for development, but it does not predict physical-device speed or power. Mapping can change the implemented computation through quantization, discretization, or resource limits.

### Event data and task evaluation

[IBM DVS Gesture](../resources/datasets-and-benchmarks.md#ibm-dvs-gesture-dataset) is a labeled event-camera gesture dataset. The original IBM page links the dataset, but that download link timed out during this review; a [preprocessed Zenodo derivative](https://zenodo.org/records/8060604) is available as large NPY train/test archives. Check the derivative's exact tensor representation before analysis: arbitrary preprocessed tensors may not retain event timestamps or polarities, so do not infer raw sensor timing or end-to-end latency from them. State all transformations, compare against a declared baseline on a fixed split, and report device latency or power only when measured with stated boundaries and conditions.

### Simulation, biological time, and physical time

Spiking simulators can advance a model through a chosen duration of biological time while using a different amount of wall-clock time. Accelerated analog hardware can also make the relationship between those clocks architecture-dependent. For real-time claims, report wall-clock timing and input/output boundaries; for model claims, report the simulated duration and model timestep. Do not treat either as a substitute for the other.

### Learning and device access

Distinguish offline training on a conventional computer from on-device or hardware-in-the-loop learning. A model trained in PyTorch and then converted is a deployment pipeline, not evidence that learning occurred on the chip. Public documentation and code can be explored without hardware; actual platform use may require a development kit, institutional allocation, or account approval. Check access conditions before planning a hardware experiment.

## Small project: map and measure one event classifier

Choose a small classifier and one official platform path. Define input preprocessing and a fixed train/test split, then run a software baseline. If supported hardware is available, convert or map the same model and compare outputs on identical examples. Deliver the conversion settings, unsupported-operation notes, output agreement and task accuracy, plus measured wall-clock latency and power only if the device instrumentation supports them. Keep simulation results separate from physical measurements, state the timing boundary, and include the event-data control or rate-based baseline. This proposed exercise has not been run by the repository; without the device, stop at CPU simulation and leave hardware claims untested.

## Where to go next

For spiking models and event-data tooling, see [coding and representations](coding-and-representations.md), [learning and plasticity](learning-and-plasticity.md), and [NeuroAI](neuroai.md). For model assumptions, runtime, and reproducibility, see [theory and model building](../methods/theory-and-model-building.md), [simulation](../methods/simulation.md), and [reproducible research](../methods/reproducible-research.md). Browse [all topics](README.md) or the [resource library](../resources/README.md) for additional frameworks and datasets.
