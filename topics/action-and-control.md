# Action and control

[Collection overview](../README.md) · [All topics](README.md) · [Learn](../learn/README.md) · [Methods](../methods/README.md) · [Resource library](../resources/README.md)

Computational motor neuroscience studies how nervous systems generate, monitor, and correct movement in bodies with noise, delays, and changing dynamics. Control theory offers useful language for prediction and feedback, but a mathematically successful controller is not automatically a model of the neural implementation.

## Questions to bring

- What is controlled: endpoint, trajectory, force, posture, or task success?
- What are the relevant body dynamics, sensory feedback, delays, and uncertainties?
- Which errors are corrected online, and which changes reflect learning across trials?
- How do neural signals relate to movement variables and to a controller’s internal state?

## Prerequisites

Review vectors, linear systems, feedback, and basic probability. Understand kinematics and the distinction between a desired trajectory, measured movement, and control input. For neural data, align spikes, kinematics, and task events while checking for session drift and repeated-trial structure.

## A short start route

1. Specify the plant, control objective, sensory observations, and constraints.
2. Build a simple feedforward or feedback controller and simulate a perturbation.
3. Measure behavior and neural activity on aligned time axes.
4. Compare a model’s predicted correction or adaptation with held-out perturbations.

## Research threads

### Reaching and optimal feedback

Reaching provides tractable tasks for studying redundancy, uncertainty, and feedback corrections. [The Computational Neurobiology of Reaching and Pointing](../resources/books.md#the-computational-neurobiology-of-reaching-and-pointing) develops theoretical models and accompanying code; [Computational Motor Control](../resources/courses-and-lectures.md#computational-motor-control-reza-shadmehr) provides a teaching route. [Computational Mechanisms of Sensorimotor Control](../resources/papers-and-reviews.md#computational-mechanisms-of-sensorimotor-control) reviews prediction, feedback, impedance, and learning. These normative accounts clarify trade-offs but require empirical constraints on costs, noise, and state estimates.

### Embodied dynamics and learning

Musculoskeletal systems add nonlinear mechanics and constraints. [MyoSuite](../resources/software.md#myosuite) offers environments for studying control of musculoskeletal models. [Embodied Sensorimotor Control](../resources/papers-and-reviews.md#embodied-sensorimotor-control-computational-modeling-of-the-neural-control-of-movement) connects body, environment, and neural control in computational modeling. Performance in a simulator depends on its physics and reward definition; report these alongside controller results.

### Neural recordings and decoding over time

Movement-related activity can drift across days and conditions. [LINK: Long-Term Intracortical Neural Activity and Kinematics](../resources/datasets-and-benchmarks.md#link-long-term-intracortical-neural-activity-and-kinematics) provides long-term recordings for examining stability. [Reach-related Single Unit Activity in the Parkinsonian Macaque](../resources/datasets-and-benchmarks.md#reach-related-single-unit-activity-in-the-parkinsonian-macaque-dandi000947) provides a multi-region, disease-related dataset. The [FALCON decoding benchmark](../resources/datasets-and-benchmarks.md#falcon-few-shot-algorithms-for-consistent-neural-decoding) frames neural decoding under data efficiency and cross-condition challenges. A decoder can predict kinematics without identifying a causal control signal.

## Small project: compare open-loop and feedback control

Simulate a point mass reaching to a target with motor noise and a mid-flight perturbation. Compare an open-loop controller with a feedback controller that receives delayed position observations. Deliver equations, trajectories, endpoint error, and correction latency across noise and delay settings. Evaluate both target accuracy and control effort on held-out perturbation directions. State which simplifications—body mechanics, sensory noise, or neural dynamics—limit interpretation. This proposed exercise has not been run or validated by the repository.

## A useful comparison

Evaluate both task outcome and control cost, since a controller can improve accuracy by using unrealistic effort. Sweep feedback delay and sensory noise independently. Compare the timing and direction of corrections after perturbation, not only final endpoint error.

## Limits and deeper evidence

Inverse dynamics and optimal-control models can explain behavior without specifying neural implementation. Movement data are affected by biomechanics, task instructions, fatigue, and adaptation. Neural decoding should use time-aware splits and test across sessions where possible. Stronger mechanism claims need interventions that alter the proposed feedback or learning process, not just correlations between activity and movement.

## Where to go next

Explore [perception and decision](perception-and-decision.md) for selecting actions under uncertainty, [learning and plasticity](learning-and-plasticity.md) for adaptation, and [memory and navigation](memory-and-navigation.md) for spatial behavior. Methods: [theory and model building](../methods/theory-and-model-building.md), [simulation](../methods/simulation.md), [neural data analysis](../methods/neural-data-analysis.md), [fitting and model comparison](../methods/fitting-and-model-comparison.md), [reproducible research](../methods/reproducible-research.md). Learning: [prerequisites](../learn/prerequisites.md), [learning paths](../learn/learning-paths.md), [projects](../learn/projects.md), [teaching](../learn/teaching.md). Browse [all topics](README.md), the [collection overview](../README.md), and [resources](../resources/README.md).
