## Active learning

1. [Designing Robot Learners that Ask Good Questions](https://www.cc.gatech.edu/social-machines/papers/cakmak12_hri_active.pdf)
	- Active learning + hri + lfd
	- Types of queries: 1) Label query -  execute a motion and ask whether the skill was performed correctly. 2) Demo query - Create a new scenario (learner specifies certain constraints) and requesting a demonstration from the teacher. Ways to constrain i. provide a start config or ii. allow user to control only certain dofs. 3) Feature query
	- Queries made by the robot are pre-scripted, to avoid the large variance that would occur in queries automatically generated based on the teacher’s demonstration.
	- Result: 1) Feature queries are perceived as smartest. Label queries are easiest to answer.

1. [Active Preference-Based Learning of Reward Functions](https://people.eecs.berkeley.edu/~sastry/pubs/Pdfs%20of%202017/SadighActive2017.pdf)
	- Preferences: Comparisons. Person provides the system a relative preference between two trajectories. 
	- System decides on what preference queries to make.
	- We learn the reward function from a continuous hypothesis space by maximizing the volume removed from the hypothesis space by each query.
	- Hypothesis: 1) The continuous and high-dimensional nature of the queries renders relying on a discrete set (of queries) ineffective.  2) Active generation of queries leads to better reward functions faster.
	- Contribution:  Actively synthesize queries that satisfy the dynamics of the system. We learn the reward function from a **continuous hypothesis space** by maximizing the volume removed from the hypothesis space by each query. We use the human’s response to assign weights to the hypothesis space in the form of a log-concave distribution, which provides an approximation of the objective via a Metropolis algorithm that makes it differentiable w.r.t. the query parameters. We provide a bound on the number of iterations required to converge.
	- Fully-observable