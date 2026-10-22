# Simulation

[Collection](../README.md) · [Learn](../learn/README.md) · [Topics](../topics/README.md) · [Methods](README.md) · [Resources](../resources/README.md) · [Community](../community/README.md)

Use simulation when equations define a model but its behavior is difficult to derive, when you want to explore consequences across conditions, or when you need a controlled computational experiment. Simulation can clarify a theory, check an implementation, and generate predictions; it cannot establish that the modeled mechanism occurs in the brain.

## When to use this workflow

- The model contains coupled nonlinear dynamics, stochastic events, or many interacting units.
- You need to map parameter changes to stability, activity patterns, learning, or task performance.
- You want to reproduce a published computational result or compare implementation choices.
- A controlled model experiment can reveal a boundary condition or prediction for later empirical work.

For analytic questions, derive what can be derived before running a large simulation. For estimating parameters from observations, see [fitting and model comparison](fitting-and-model-comparison.md).

For a first model, prefer a small case whose expected behavior you can explain by inspection.

## Prerequisites

Know the model equations, units, parameters, initial conditions, and intended observables. Numerical work requires enough programming and numerical analysis to understand time steps, solvers, random number generation, and numerical error. Choose software that fits the scale and representation; the [software catalog](../resources/software.md) includes simulators and analysis tools.

## Inputs and outputs

**Inputs:** equations or update rules; parameter ranges and biologically meaningful constraints; initial state; input or task protocol; numerical method and resolution; and random-seed policy if the model is stochastic.

**Outputs:** trajectories or event records; summaries tied to the question; numerical and parameter-sensitivity checks; and a run record with code version, configuration, software versions, and seeds.

## Decision sequence

1. **Write the computational question.** Choose a measurable output such as firing rate, oscillation frequency, decoding accuracy, or recovery after perturbation. State the conditions to compare.
2. **Translate the model faithfully.** Map each state variable and equation to code. Declare whether updates are synchronous, sequential, event-based, or continuous-time, and how graph edges or coupling terms operate.
3. **Check dimensions and signs.** Verify units, parameter ranges, reset or boundary rules, conservation constraints, and limiting cases against the written model.
4. **Choose the simulator and solver.** Match the numerical method to the equations and scales. For spiking models, use a tool with documented event and synapse semantics; for detailed cellular models, consider a cellular simulator. See [software](../resources/software.md) and [tutorials and examples](../resources/tutorials-and-examples.md).
5. **Build a small reference case.** Start with a case whose behavior is analytically known, has a published reference, or is simple enough to inspect manually. Compare its output before scaling up.
6. **Set resolution and duration.** Make the time step or solver tolerance small enough to resolve the fastest relevant process. Run long enough to capture the target behavior, while separating transients from the analyzed interval.
7. **Plan comparisons before execution.** Define parameter sweeps, control conditions, initial states, and seeds. Change one interpretable factor at a time unless a factorial design answers the question better.
8. **Run and inspect raw behavior.** Plot states, events, and summary measures. Check for numerical blow-up, impossible values, transients, silent units, or artifacts at boundaries.
9. **Test robustness.** Repeat stochastic runs across seeds, vary resolution, and perturb key parameters. Compare summaries and conclusions, not just visually similar traces.
10. **Record and interpret.** Save configurations and outputs. Explain what the model predicts under stated assumptions and what additional empirical evidence would be needed.

## Evaluation

Evaluate whether the implementation reproduces the specified equations and whether conclusions survive reasonable numerical and parameter changes. Use convergence checks by reducing step size or tightening tolerances; compare with analytic solutions or reference implementations when available. For stochastic models, report variability across runs rather than a single favorable trace.

Useful outputs depend on the question: trajectories for dynamics, distributions for stochastic outcomes, rates for population activity, or task metrics for behavior. Summaries should retain relevant time, condition, and unit structure. Avoid aggregating away a difference that defines the hypothesis. Keep exploratory parameter sweeps distinct from tests of predictions specified before the run.

## Limitations

Simulation results are conditional on the equations, code, solver, parameterization, and chosen conditions. A plausible trajectory does not validate a model. Agreement with one published figure may conceal implementation errors if only a summary statistic is matched. Numerical stability is not biological realism; detailed models can still be underconstrained.

## Selected resources

- [Neuronal Dynamics](../resources/books.md#neuronal-dynamics-from-single-neurons-to-networks-and-models-of-cognition) — connects model equations with spiking behavior, coding, and exercises.
- [Brian 2](../resources/software.md#brian-2) — equation-based spiking network simulation with documented examples.
- [NEST Simulator](../resources/software.md#nest-simulator) — infrastructure for large-scale spiking network simulations.
- [Potjans–Diesmann cortical microcircuit model in NetPyNE](../resources/tutorials-and-examples.md#potjansdiesmann-cortical-microcircuit-model-in-netpyne) — a concrete network model for studying implementation and emergent activity choices.
- [Computation through Dynamics Benchmark and Toolkit](../resources/datasets-and-benchmarks.md#computation-through-dynamics-benchmark-and-toolkit) — examples and benchmarks for evaluating dynamical computation.

## Continue

Choose a domain in [topics](../topics/README.md), then use [reproducible research](reproducible-research.md) to preserve the run setup. If parameters come from observations, see [fitting and model comparison](fitting-and-model-comparison.md); if outputs need empirical interpretation, see [neural data analysis](neural-data-analysis.md).

For equation-based population modeling and parameter sweeps, consider [PyRates](../resources/software.md#pyrates). For growth or device-mapping questions, continue to [development](../topics/development-and-self-organization.md) or [neuromorphic computing](../topics/neuromorphic-computing.md).
