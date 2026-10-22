# Start here: what is computational neuroscience?

[Collection overview](README.md) · [Learn](learn/README.md) · [Topics](topics/README.md) · [Resource library](resources/README.md)

Computational neuroscience uses explicit models and quantitative analysis to investigate how nervous systems work. A model might describe electrical activity in one neuron, the changing activity of a circuit, how an animal chooses an action, or how learning changes a network. Data analysis connects these accounts to measurements and tests what they explain.

You can use this page without prior neuroscience, calculus, or programming. Follow the links when a particular question interests you; the [prerequisite guide](learn/prerequisites.md) helps you add background as needed.

## Begin with a question

| Question | An example of a computational approach | Explore |
| --- | --- | --- |
| Why does a neuron fire in response to some inputs? | Represent membrane voltage and input current, then predict spike times as the input changes. | [Neurons and dendrites](topics/neurons-and-dendrites.md) |
| How does a circuit sustain or change its activity? | Connect interacting units and study stable activity, oscillations, or transitions. | [Circuits and dynamics](topics/circuits-and-dynamics.md) |
| What does neural activity tell us about the world? | Compare responses across stimuli and test an encoding or decoding model. | [Coding and representations](topics/coding-and-representations.md) |
| How does experience change future behavior? | Specify a learning rule and examine what a network can learn under it. | [Learning and plasticity](topics/learning-and-plasticity.md) |
| How do uncertain observations guide a choice? | Model how observations update beliefs or accumulate evidence, then compare predicted choices with behavior. | [Inference](topics/inference-and-prediction.md) and [decision-making](topics/perception-and-decision.md) |
| How can a system remember a location or control movement? | Link internal state, sensory observations, body dynamics, and actions to measurable behavior. | [Memory and navigation](topics/memory-and-navigation.md) and [action and control](topics/action-and-control.md) |
| What can biological and artificial systems teach us about each other? | Compare learning procedures, task behavior, or representations under an explicit test. | [NeuroAI](topics/neuroai.md) |
| How is neural wiring organized? | Analyze reconstructed connections or regional measurements while keeping structural and statistical relationships distinct. | [Connectomics](topics/connectomics.md) |
| How does neural structure form? | Specify local growth rules and compare their predicted branching or spatial patterns with developmental observations. | [Development and self-organization](topics/development-and-self-organization.md) |
| How do computations relate to individual differences? | Compare behavioral models or statistical reference distributions with brain and symptom measurements. | [Computational psychiatry](topics/computational-psychiatry.md) |
| How can neural computation be implemented in hardware? | Map a model to an event-driven platform and measure its accuracy, latency, and resource use. | [Neuromorphic computing](topics/neuromorphic-computing.md) |

These are overlapping ways into the subject. A memory model can involve single-cell properties, network dynamics, learning, and behavior at once.

## A small example: predicting a neuron's response

Imagine a simplified neuron receiving a steady input. Its membrane voltage rises with input, relaxes toward a resting value, and produces a spike when it reaches a chosen threshold. After a spike, the model resets the voltage.

| Part of this example | What it represents |
| --- | --- |
| Input | A current supplied to the model. |
| State | Membrane voltage, which changes over time. |
| Rule | How the current and voltage leak change that state; when a spike and reset occur. |
| Prediction | The voltage trace and number of spikes during a stated interval. |
| Comparison | Whether those predictions agree with a reference simulation or measured response under the same input. |
| Omission | Detailed dendritic geometry, individual ion-channel mechanisms, and many adaptation effects. |

Before writing any code, sketch what you expect a stronger input to do. Then ask which details this simplified account needs to answer that question. A compact model is useful when its assumptions fit the question; richer biological detail serves other questions.

To try it, follow the [learning paths](learn/learning-paths.md) and [projects](learn/projects.md). To examine the assumptions more closely, use [theory and model building](methods/theory-and-model-building.md).

## Models, measurements, and explanations

A model can summarize a pattern, predict an observation, propose a mechanism, or study the consequences of an objective and constraints. Say which purpose is being tested. A good prediction alone does not establish the proposed biological mechanism, and an optimal solution to a mathematical problem needs evidence before it is attributed to a nervous system.

Measurements also require interpretation. Spikes, calcium fluorescence, EEG, and fMRI reflect different processes at different scales. An analysis should connect the recorded quantity to its question and account for preprocessing, uncertainty, and alternative explanations. The [data-analysis workflow](methods/neural-data-analysis.md) starts with those choices.

## Choose your next step

| Your immediate goal | A useful next step |
| --- | --- |
| Keep exploring without coding | Read one [topic guide](topics/README.md), then choose its introductory reading or lecture. |
| Get a connected introduction | Choose one [learning path](learn/learning-paths.md) and use a single main course or book. |
| Bring a biology or experimental background | Add the quantitative skills you need through [prerequisites](learn/prerequisites.md), then choose a modeling or analysis task. |
| Bring mathematics, physics, or machine learning | Use the biological and measurement bridges in [prerequisites](learn/prerequisites.md), then inspect a model's assumptions and evidence. |
| Start work on a specific question | Go directly to a [topic](topics/README.md) or [method](methods/README.md). |
| Find material for a class or reading group | Use [teaching suggestions](learn/teaching.md). |
| Look for a book, package, or dataset | Browse the [resource library](resources/README.md). |
| Find people and places to ask questions | Visit [Community](community/README.md). |

There is no required order through the whole collection. Choose one question and one resource, then use the next gap you encounter to decide what to learn.
