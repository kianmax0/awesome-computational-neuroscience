# Causal inference and experimental design

[Collection](../README.md) · [Methods](README.md) · [Topics](../topics/README.md) · [Resource library](../resources/README.md)

Use this guide when the question concerns the effect of changing a stimulus, neural component, intervention, or learning condition. Predicting an observation and estimating the effect of an intervention require different assumptions. The [Causal Inference: What If entry](../resources/books.md#causal-inference-what-if) provides general background to use alongside neuroscience-specific models and measurements.

## Start with the effect you want to estimate

State the intervention or exposure, comparison condition, outcome, time window, population or preparation, and experimental unit. For example, ask how a defined perturbation changes a circuit response over a fixed interval. Name whether the target is an average effect across preparations, a within-preparation effect, or a response under a particular context.

A structural wiring diagram, a correlation graph, and a causal model need different edge semantics. Document the assumed relationship rather than interpreting a displayed arrow as causal evidence.

## Inputs and outputs

**Inputs:** the scientific question; candidate causal assumptions; the measurement process; available interventions or observational data; sampling and assignment rules; and plausible alternatives.

**Outputs:** a clearly defined effect or prediction, a design or identification argument, an analysis plan, uncertainty and sensitivity checks, and a statement of the conditions under which the inference applies.

## Design and analysis decisions

1. **Draw the assumed relationships.** Define variables, their timing, and the meaning of edges. Include plausible common causes and consequences of the intervention. Mark which are observed.
2. **Choose the unit.** Distinguish animals, participants, preparations, sessions, trials, and time bins. Repeated observations within a unit do not automatically provide independent experimental replications.
3. **Examine assignment.** If conditions are randomized, specify the randomization unit and relevant blocking or ordering. If using observational data, state what assumptions allow the comparison and which common causes are measured.
4. **Match the control to the claim.** Control for the stimulus, handling, recording, or nonspecific perturbation effects relevant to the proposed mechanism. A control that answers a different question may leave the key alternative untouched.
5. **Consider time and interaction.** Anticipate carry-over, adaptation, learning across trials, and dependence among interacting units. The effect can depend on the history and circuit state.
6. **Plan measurement and exclusions.** State the outcome window, quality criteria, missing-data handling, and exclusions before inspecting the target effect where possible.
7. **Choose adjustment deliberately.** Base adjustment on the causal question and assumptions; adding every measured variable can introduce bias, particularly for variables affected by the intervention or selection process.
8. **Evaluate uncertainty and alternatives.** Respect the sampling hierarchy, report effect sizes and uncertainty, and test sensitivity to plausible measurement and causal assumptions.
9. **Bound the conclusion.** Explain the population, preparation, intervention, and timescale supported by the design. Consider what would be required to transfer the effect elsewhere.

## A small project without laboratory work

Create a synthetic three-variable example with a shared cause of an exposure and outcome. Specify a data-generating model, then compare an unadjusted association, an appropriately adjusted estimate, and a simulated randomized assignment. Deliver a graph with declared semantics, the target effect, equations or generation code, and a comparison table. A hand-worked finite example is enough for a conceptual version.

Keep the parameter choices fixed while comparing methods. Repeat stochastic simulations to show variation, and include a case where the identification assumptions fail. The exercise is suggested and has not been executed by this repository.

## Limits

A perturbation can affect several components at once, and the measured signal can be an indirect consequence. Randomization does not repair an ill-defined intervention, measurement artifact, or unsupported extrapolation. Observational identification depends on assumptions that data alone may not settle. State what competing mechanism would remain compatible with the result.

## Where this connects

- [Connectomics](../topics/connectomics.md) separates reconstructed structure, statistical association, and evidence about causal influence.
- [Learning and plasticity](../topics/learning-and-plasticity.md) supplies questions about teaching signals, timing, and competing learning rules.
- [Computational psychiatry](../topics/computational-psychiatry.md) connects behavioral parameters and population variation to research-design limits.
- [Neural data analysis](neural-data-analysis.md) addresses measurement and preprocessing, while [fitting and model comparison](fitting-and-model-comparison.md) addresses parameter inference and predictive comparisons.
- [Reproducible research](reproducible-research.md) explains how to preserve the choices needed to inspect an analysis.
