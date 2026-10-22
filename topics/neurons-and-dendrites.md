# Neurons and dendrites

[Collection overview](../README.md) · [All topics](README.md) · [Learn](../learn/README.md) · [Methods](../methods/README.md) · [Resource library](../resources/README.md)

This guide is for asking what a neuron model can explain when its input integration, membrane state, and morphology are made explicit. It spans phenomenological point neurons through compartmental biophysics; the useful level depends on the question and the evidence available.

## Questions to bring

- Which measured features matter: firing rate, spike timing, adaptation, voltage trajectory, spatial integration, or response to patterned synaptic input?
- Does a point-neuron approximation preserve the phenomenon of interest, or do active dendrites, branch structure, or location-dependent inputs matter?
- Which parameters are observed, constrained by physiology, or merely fit to one recording condition?
- Can two distinct mechanisms produce similar input-output curves, and what perturbation would separate them?

## Prerequisites

Be comfortable with differential equations, basic circuit analogies for membrane capacitance and conductance, and numerical time stepping. For conductance-based or multicompartment work, learn the meaning of reversal potentials, channel kinetics, cable coupling, and units. Python or MATLAB helps, but begin by reading equations and reproducing a simple trace before expanding the model.

## A short start route

1. Define the observable and timescale: a spike, an F–I curve, a voltage trace, or a dendritic nonlinear response.
2. Start with a leaky integrate-and-fire or adaptive model; identify what its state variables omit.
3. Add one mechanism at a time and test its effect under matched input conditions.
4. Compare predictions against an independent stimulus or held-out trace, then document parameter uncertainty.

## Research threads

### Excitability and spike generation

Threshold, refractoriness, adaptation, and bursting can be represented with different state variables. A compact model may predict spike times well while missing ionic currents; a Hodgkin–Huxley-style model can express channel mechanisms but introduces parameters that are difficult to identify from sparse recordings. Ask whether the scientific target is prediction, mechanism, or a reduced description.

### Dendritic integration

Dendritic branches can filter inputs and support local nonlinear events. Reduced compartment models trade anatomical detail for tractability, while detailed morphologies increase parameter and computational demands. The [Allen Cell Types Database neuronal models](../resources/datasets-and-benchmarks.md#allen-cell-types-database-neuronal-models) provide a route from electrophysiology to fitted point-neuron and perisomatic biophysical models; [Dendrify](../resources/software.md#dendrify) is useful for exploring reduced active dendritic compartments; [Jaxley](../resources/software.md#jaxley) supports differentiable multicompartment models. These are different modeling choices, not an accuracy ranking.

### From cells to network-ready units

Cellular detail can change network behavior through adaptation, conductance state, and synaptic integration. The [Neuroscience for Machine Learners course](../resources/courses-and-lectures.md#neuroscience-for-machine-learners-neuro4ml) links biophysical, multicompartment, synapse, and network models for a practical bridge. [Modeling Neural Circuits Made Simple with Python](../resources/books.md#modeling-neural-circuits-made-simple-with-python) is a broader route from single cells to circuits with code and neural data examples.

## Small project: what does a compartment buy?

Implement or adapt a two-compartment neuron with a somatic spike mechanism and a dendritic input. Deliver (a) equations and parameter table, (b) somatic voltage and spike output for proximal versus distal inputs, and (c) a brief comparison with a point-neuron model receiving the same total input. Evaluate whether the models make different predictions on a held-out input pattern; vary coupling and input location to show sensitivity. Do not treat a better fit to one trace as evidence that the chosen compartments are the unique biological explanation.

## A useful comparison

Compare models using the same input, observation window, and fitting target. Record complexity alongside predictive performance: number of state variables, free parameters, and data needed to constrain them. Ask whether the added dendritic mechanism makes a new testable prediction.

## Limits and deeper evidence

Model complexity does not itself establish mechanism. Morphology, channel distributions, temperature, recording configuration, and cell-type sampling can all affect fitted parameters and generalization. A fit to somatic voltage may leave dendritic conductances weakly identified. Published database models inherit assumptions of their fitting pipeline; inspect the experimental protocol and model metadata before interpreting parameters. Pair simulations with perturbation or multi-site recordings when the claim concerns causal cellular mechanisms.

## Where to go next

Move to [circuits and dynamics](circuits-and-dynamics.md) when the target is population behavior; to [learning and plasticity](learning-and-plasticity.md) when synapses change; or to [coding and representations](coding-and-representations.md) when the key question is what activity represents. Methods: [theory and model building](../methods/theory-and-model-building.md), [simulation](../methods/simulation.md), [fitting and model comparison](../methods/fitting-and-model-comparison.md). Learning: [prerequisites](../learn/prerequisites.md), [learning paths](../learn/learning-paths.md), [projects](../learn/projects.md). Browse [all topics](README.md), the [collection overview](../README.md), and the [resource library](../resources/README.md).

How morphology forms is covered in [development and self-organization](development-and-self-organization.md); reconstructed wiring and sampling are covered in [connectomics](connectomics.md).
