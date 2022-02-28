1. TAMPC: A Controller for Escaping Traps in Novel Environments
	- Trap-Aware Model Predictive Control

1.  Learning When to Trust a Dynamics Model for Planning in Reduced State Spaces (2020)

1. [Simultaneous learning of hierarchy and primitives for complex robot tasks (2018)](https://link.springer.com/content/pdf/10.1007/s10514-018-9749-y.pdf)


## Relevant
1. Keep it Simple: Data-efficient Learning for Controlling Complex Systems with Simple Models (2021)
	- 


## Prediction of human motion

1. Unsupervised Early Prediction of Human Reaching for Human-robot Collaboration in Shared Workspaces (2018)
	- Maintain a two-layer library: Layer 1 - GMMs for palm (position) motion and Layer 2 - GMMs for human arm (joint center position) motion.
	- For new user, either update an existing GMM or create a new GMM depending on some threshold, in layer 1. Then depending on the GMM in layer 1, we update the corresponding (or create a new) GMMs in layer 2.
	- What is a membership-proportional prior?

1. Goal Set Inverse Optimal Control and Iterative Re-planning for Predicting Human Reaching Motions in Shared Workspaces (2016)
	- Collect demonstrations from a pair of users performing a table-top manipulation task.
	- Use Path Integral Inverse Reinforcement Learning (PI IRL) to learn the user's cost function i.e. weights for feature functions. Assuption: user's objective while reaching is to minimize this cost function.
	- Cost function used to iteratively compute paths to a goal region (not just a single goal configuration as it may be unknown) from the user's current state.


## Motion planning

1. Task Space Regions: A framework for pose-constrained manipulation planning (2011)