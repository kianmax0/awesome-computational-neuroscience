# Simulation-based inference

[Collection](../README.md) · [Methods](README.md) · [Topics](../topics/README.md) · [Resource library](../resources/README.md)

Use simulation-based inference when a model can generate observations for chosen parameters but evaluating the likelihood is impractical. The goal is an approximate account of which parameters remain compatible with observations, conditional on the simulator and prior. Start with ordinary likelihood-based inference when that route is available and adequate.

## Prerequisites

Understand the model parameters, probability distributions, observation process, and the distinction between a parameter estimate and uncertainty about it. Computational work requires a working simulator, basic Python and arrays, and enough resources to generate and check simulations. The [sbi entry](../resources/software.md#sbi) links current documentation and a neuronal example.

## Inputs and outputs

| Input | What to specify |
| --- | --- |
| Simulator | Parameter meaning, units, noise, initial state, and the measurement or task protocol. |
| Prior | Parameter support and why its ranges are plausible for this question. |
| Observation | Its provenance and preprocessing, represented in the same way as simulated data. |
| Data representation | Raw observations, summary statistics, or a learned representation, with their possible information loss. |
| Budget | Simulation cost, training budget, and separate simulations reserved for diagnostics. |

Expected outputs are an approximate posterior or related inference object, diagnostic results, predictive simulations, and a record of what remains weakly constrained.

## A practical sequence

1. **Validate the forward model.** Check that the simulator implements the intended equations and measurement process. Follow [simulation](simulation.md) before trying to invert it.
2. **Inspect prior predictions.** Generate small examples across the prior and compare their ranges with the observation. Investigate invalid outputs and obvious mismatch before training.
3. **Define the representation.** State what each statistic or feature retains. Use the same transformation for simulated and observed data.
4. **Choose an inference approach.** Posterior, likelihood, and likelihood-ratio estimation have different sampling and training requirements. Follow the current package guide rather than transferring an old API example.
5. **Keep diagnostic data separate.** Allocate simulations for recovery and calibration as well as fitting. Fit learned preprocessing using only the appropriate training material.
6. **Recover known examples.** Simulate observations from known parameters and inspect uncertainty and trade-offs, including cases near the prior boundary.
7. **Check predictions and calibration.** Examine whether posterior simulations describe the observations, and use suitable calibration or coverage diagnostics. A plausible predictive trace alone does not validate the posterior.
8. **Challenge the setup.** Change plausible priors, summaries, simulation budgets, and observation assumptions. Record which conclusions depend on them.

## A small project

Use a simple neuron or rate model with two unknown parameters. Generate synthetic observations with known parameters and state their noise. Compare inference using one response summary with inference using two summaries. Deliver the prior, parameter-recovery plots, posterior-predictive plots, a diagnostic evaluation on new simulations, and a table of simulation cost. If a likelihood is tractable in a simplified case, use it as a reference.

This is a suggested exercise, not an executed repository result. Its purpose is to reveal information loss and parameter trade-offs, rather than to establish a biological mechanism.

## Interpretation and limits

An accurate posterior for a simulator can still describe an inadequate model of biology. Calibration averaged over prior-generated examples does not ensure accuracy for a particular observation. A broad posterior may reflect limited information rather than a failed optimizer; a narrow one may conceal misspecification or an overly restrictive prior. Distinguish uncertainty conditional on one model from uncertainty across alternative models.

## Resource routes

- [sbi](../resources/software.md#sbi) provides the inference framework, diagnostics, and neuronal example as one ecosystem.
- [PyRates](../resources/software.md#pyrates) offers a route to neural-population simulators; validate a chosen model independently of its fitting procedure.
- [Probabilistic Machine Learning: Advanced Topics](../resources/books.md#probabilistic-machine-learning-advanced-topics) provides broader inference background.

Continue with [fitting and model comparison](fitting-and-model-comparison.md), [neurons and dendrites](../topics/neurons-and-dendrites.md), [circuits and dynamics](../topics/circuits-and-dynamics.md), or [computational psychiatry](../topics/computational-psychiatry.md), depending on the model and observations.
