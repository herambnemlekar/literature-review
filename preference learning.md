## Factors affecting human preferences
1. [Identification and validation of cognitive design principles for automated generation of assembly instructions](https://dl.acm.org/doi/abs/10.1145/989863.989917)
	- Creates computer-generated instructions for assembly lines, compares it to hand-designed instructions. The user chooses between the two.
	- This paper would be interesting because one could compare the computer generated and hand-designed instructions to see what specific differences there are, and therefore learn about user preference.

2. [Cognitive aspects affecting Human Performance in Manual Assembly](https://www.google.com/books/edition/Advances_in_Manufacturing_Technology_XXX/AhjpDAAAQBAJ?hl=en&gbpv=1&dq=factors+affecting+human+performance+assembly+manufacturing&pg=PA231&printsec=frontcover)
	- This paper talks about how human performance deteriorates as they become fatigued throughout the building process, and assesses the cognitive effects of this.
	- Based on how fatigued a human becomes, a robot would need to be more/less involved in holding a certain part or fetching a part from a storage room.

3. [Quality improvement in manufacturing through human performance enhancement](https://www.emerald.com/insight/content/doi/10.1108/EUM0000000005713/full/html)
	- This article talks about the importance of ergonomics in a work environment. Similar to the previous paper, this one explores the different ways that a robot could most efficiently help a human in a workplace environment.

4. [Modeling and Control of Trust in Human-Robot Collaborative Manufacturing](https://link.springer.com/chapter/10.1007/978-1-4899-7668-0_7)
	- This is also related to the previous two papers, where they predict the amount of work the robot needs to do based on how much of a 9 hour work day has passed.

5. [An integrated framework for human-robot collaborative assembly in hybrid manufacturing cells](https://ieeexplore.ieee.org/abstract/document/7743441)
	- This paper talks about the trust factors involved in robots working with humans in the workplace. If the worker does not trust the robot as much, it will make it do less work, or have it assist from far away.
	- This factor can affect how much the robot is involved in each assembly task.

6. [Collaborative manufacturing with physical human–robot interaction](https://www.sciencedirect.com/science/article/abs/pii/S0736584515301769)
	- Cobot: a robot that assists people with various tasks
	- This paper describes a successful way of implementing robots into a workforce environment. It describes how the working strain of the worker decreases as the robot helps more.

7. [Modelling human performance within an automotive engine assembly line](https://link.springer.com/article/10.1007%2Fs00170-012-4714-y)
	- Walking worker: worker that does many tasks (like the ones we are targeting)
	- Study analyzes the effects of a robot assisting a worker who performs multiple tasks.

8. [Optimised scheduling in human–robot collaboration – a use case in the assembly of printed circuit boards](https://www.tandfonline.com/doi/full/10.1080/00207543.2018.1470695)
	- This study aims to create a linear distribution of the number of tasks a user does versus the number of tasks the robot does.

9. [Working with Walt: How a Cobot Was Developed and Inserted on an Auto Assembly Line](https://ieeexplore.ieee.org/abstract/document/8360084)
	- This article references a study where robots were used in assistance at an Audi car manufacturer. It would be interesting to read about what factors they took into account when they deployed these robots.

10. [The Comfort Zone Concept in a Human-Robot Cooperative Task](https://www.google.com/books/edition/Precision_Assembly_in_the_Digital_Age/W_CBDwAAQBAJ?hl=en&gbpv=1&dq=human+preference+and+robot+needs+assembly+manufacturing&pg=PA82&printsec=frontcover)
	- This paper contains a useful table with links to different papers relating to this research. It has links to psychology, cognitive aspects, cognitive robotics and automation, and human-robot interaction papers which could be useful for this research.

1. Act identities bear systematic relations to one another in an organized cognitive represention of the action-the action's identity structure. An identity structure is essentially a hierarchical arrangement of an action's various identities. Lower level identities in this hierarchy convey the details or specifics of the action and so indicate how the action is done. Higher level identities convey a more general understanding of the action, indicating why the action is done or what its effects and implications are. Relative to low-level identities, higher level identities tend to be less movement defined and more abstract and more abstract and to provide a more comprehensive understanding of the action.

## Preferences in human-robot collaboration

1. [Preference Learning in Assistive Robotics: Observational Repeated Inverse Reinforcement Learning](http://proceedings.mlr.press/v85/woodworth18a/woodworth18a.pdf)
	- Current preference learning techniques lack the ability to inferlong-term, task-independent preferences in realistic, interactive, incomplete-information settings.
	- Observational Repeated Inverse Reinforcement Learning (ORIRL), the robot observes the user completing multiple tasks in which the user selects a set of actions.
	- 

1. [Warmth and Competence to Predict Human Preference of Robot Behavior in Physical Human-Robot Interaction](https://ieeexplore-ieee-org.libproxy2.usc.edu/stamp/stamp.jsp?tp=&arnumber=9223478)
	- Social cognition. Which robot a person would choose to interact with again, if given a choice?
	- Limitations in prior work: 1) In Godspeed dimensions, Animacy and Anthromorphism load onto each other. 2) Perception of robot images may be different than its embodiment.
	- Motivating work: People perceived as warm and competent elicit positive experiences. 
	- Investigate if the dimensions Warmth and Competence are useful for physical, embodied interaction studies.
	- Found that Warmth and Competence, among all RoSAS (Robotics Social Attribute Scale) dimensions and Godspeed dimensions (Animacy, Anthromorphism, Likeability, Perceived Intelligence and Perceived Safety), are most important predictors for human preferences between different robot behaviours.

1. [Preference-Based Assistance Prediction for Human–Robot Collaboration Tasks](https://alessandro.ronc.one/papers/2018_Grigore_IROS_assistance_pre
diction.pdf)
	- Supportive actions are separate from task actions
	- Users annotate their preferred supportive behaviours
	- Preference variables dependent on hidden state of task
	
1. [Towards Learning to Handle Deviations using User Preferences in a Human Robot Collaboration Scenario](https://pervasive.uni-klu.ac.at/BR/pubs/2016/Akkaladevi_IHCI2016.pdf)
	- Interactive RL. User provides feedback about the robot's action, especially if they deviate from the user's preference.

1. [Preference Learning on the Execution of Collaborative Human-RobotTasks](https://ipvs.informatik.uni-stuttgart.de/mlr/papers/17-munzer-ICRA.pdf)
	- Use Relational Activity Processes (RAP) which represents task as SMDP.
	- overall Q* = task Q* + preference Q

## Learning and predicting human preference and actions

1. [PlanIt: A crowdsourcing approach for learning to plan paths from large scale preference feedback])(https://ieeexplore.ieee.org/abstract/document/7139281)



1. [Anticipation in Human-Robot Cooperation: A Recurrent Neural Network Approach for Multiple Action Sequences  Prediction](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8460924&tag=1)

1. Anticipating many futures: Online human motion prediction and synthesis for human-robot collaboration
	- Predicts a window if future human motion given a window of past frames by training a conditional variational autoencoder on skeletal data.

1. Probabilistically Safe Robot Planning with Confidence-Based Human Predictions
	- When human behaviour departs from learned model, update the human model confidence in real time

1. *A Bayesian Approach for Task Recognition and Future Human Activity Prediction*
	- Task represented as a sequence of manipulated objects and performed actions.
	- Objects and actions are separately classified starting from RGB-D raw data. 
	- The task is modelled with a Dynamic Bayesian Network (DBN), which takes as input manipulated objects and performed actions. The DBN is responsible for estimating the current task, predicting the most probable future pairs of action-object and correcting possible misclassification.
	- 

1. *A Hierarchical Representation for Future Action Prediction*

1. Anticipating Human Activities using Object Affordances for Reactive Robotic Response
1. Anticipatory Planning for Human-Robot Teams

1. Anticipatory Robot Control for Efficient Human-Robot Collaboration
	- Predict task intent based on observed gaze patterns

1. *Human-Aware Task Planning for Mobile Robots*
	- Human plan recognition module: Use rule based system to detect actions and activities (sequence of actions). Predict future sequence of activities from a set of predefined plans using a HMM.

1. **Probabilistic human action prediction and wait-sensitive planning for responsive human-robot collaboration**
1. *Anticipating human actions for collaboration in the presence of task and sensor uncertainty*

1. Intention-Aware Motion Planning Using Learning Based Human Motion Prediction
	 - 3D joint positions are tracked using OpenNI.
	 - Next action predicted based on probabilities (not the most accurate way to say it, needs to be updated).

1. Multimodal Probabilistic Model-Based Planning for Human-Robot Interaction
	- Learn multimodal probability distributions over human actions and condition on interaction history as well as future robot actions.
	- Conditional variational autoencoders - generative model of human driver behaviour.
	- u(t+1) <= p(x(0:t), u(0:t), u_r(t+1))
	- Full observability of all past states and actions.
	- Real-time robot policy construction by massively parallel sampling of human responses to candidate robot actions.
	- Calculate u_r(t+1:t+N) but execute only u_r(t+1) (like in MPC).

### Search "Robot predict human preference"

1. Robot, Organize my Shelves! Tidying up Objects by Predicting User Preferences
	- Learn the user preferences using collaborative filtering based on crowdsourced data.
	- 2-levels: (1) Predict pairwise object preferences, (2) Sub-divide objects in containers by modelling a spectral clustering problem.
	- "At the same time, it is highly impractical for the robot to constantly query users about their preferences."
	- Difference to proposed method: The user preference is encoded in the object pairing and not action sequence. The features are obtained from surveys and crowdsourced data. Features help to relate objects to one another. Features hard to define for action sequences.

1. Organizing objects by predicting user preferences through collaborative filtering
	- Journal version of: Robot, Organize my Shelves! Tidying up Objects by Predicting User Preferences

1. [Human Intent Prediction Using Markov Decision Processes](https://pdfs.semanticscholar.org/2756/579b05ce72ca2d902225571431e018260866.pdf)
	- 'simulated human' model - non-specific and generalized to statistical norms of human reaction obtained from human subject testing.  
	- 'human matching' model - produces the same output as a particular human subject, requiring online learning for improved accuracy. 
	- When given a time history of previous actions as input, predicts the most likely action a human agent will make next.
	- Human action recognition - the process of sensing and determining a human’s current state from observing their motion using template matching or state-space models (HMMs).
	- Assumptions: (1) Human’s actions and their decision-making process (their goal-objectives) are fully-observable (hence MDP and not POMDP). (2) Unobtrusive: the human can ignore the robot (cooperative not collaborative). Robot actions would not influence the human directly; no feedback where the human reasons about the robot’s actions. (3) Use only implicit communication – passive visual sensing of physical motion and gaze. Although human is allowed to explicitly communicate when they like, but no prompting from the robot. (4) Robot has sufficient memory to store an n-action history. (5) Structured action sequences are known for the application. 
	- Environmental information is included in the form of sensed events that are folded into the human’s goal/objectives prior to inclusion in the MDP state vector.
	- States: The human’s low-priority mission goal states G, actions A_i, the abbreviated past history of n_h actions in A, and the high-priority interruptive goal states F_i, changes in the human’s workspace that are activated by sensed events and override mission goals.
	- Explicit communication information is preprocessed into the sensed input human state. This is the ‘human matching’ model.
	- For the ‘human matching’ model, prior to the start of interaction, a pre-existing initial baseline model of human preferences and uncertainties in performing the most preferred action and an online database of similar MDP policies to search, is available.
	- To predict the next action, an updated human state is sensed from the environment, and human’s known goal-objectives and previous actions are given to the MDP model policy.
	- Model of human preferences (simulated human) periodically improved in real-time.
	- A timer input is used to control when an updated policy is calculated and transmitted to the MDP block.
	- Ordered set is an n-tuple (action) sequence, where n is the number of actions corresponding to completing a goal. Some goals may have many satisficing action-sequences, if the actions do not need to be completed in a strict order with no interruptions in sequence.

1. Older Adults’ Preferences for and Acceptance of Robot Assistance for Everyday Living Tasks
	- Unrelated
	- Preference: Which tasks do older adults prefer to have robot assistance for. 

1. Deep Reinforcement Learning from Human Preferences
	- Unrelated
	- Learn reward function by asking humans to compare possible trajectories of the agent.
	- Preference: Human selects which trajectory segment they prefer.

1. User-Adaptive Interaction in Social Robots: A Survey Focusing on Non-physical Interaction
	- User models encode the attributes of the user that are relevant to the operation of the system.
	- Categories: 1) Adaptive systems with no user model, 2) Systems Based on Static User Models, and 3) Systems Based on Dynamic User Models

### Papers in survey: User-Adaptive Interaction in Social Robots

1. A POMDP framework for modelling human interaction with assistive robots
	- User goal and satisfaction modelled as hidden variables in POMDP.
	- Does not maintain a user model, simply adapts to user goal and satisfaction.

1. Experience based domestic environment and user adaptive cleaning algorithm of a robot cleaner
	- Robot does not keep an explicit model of the user.
	- Identifies the user’s commands and any obstacles it finds on its map, and determines the times of the day where these areas are best accessible, thus adapting to its users’ occupancy of the environment.

1. Effects of voice-adaptation and social dialogue on perceptions of a robotic learning companion
	- Adjusts its pitch as the interactions with the user progresses, progressively matching that of the user.

1. Personalising game difficulty to keep children motivated to play with a social robot: a Bayesian approach
	- Observes the user’s answering pattern and adapts its difficulty depending on the number of correct answers

1. Planning for human-robot interaction in socially situated tasks: the impact of representing time and intention
	- Include user intention and explicit time dependency as hidden variables in a POMDP framework. 

1. A different approach of using Personas in human–robot interaction: integrating personas as computational models to modify robot companions’ behaviour
1. Using personas for supporting user modeling on scheduling systems
	- Personas: manually-built user profiles from questionnaires.
	- Each persona represents a number of users, and new users are matched to a known persona.

1. Adaptive human-robot interaction in sensorimotor task instruction: from human to robot dance tutors
	- Maintains a static model of their personal information and history of interactions, which it uses to adapt its speech and gestures

1. Hobbit, a care robot supporting independent living at home: first prototype and lessons learned
	- Initialization phase where the user provides their preferences, such as speech volume and voice.

1. Making robots proactive through equilibrium maintenance
1. Accompany: acceptable robotics companions for ageing years - multidimensional aspects of human–system interactions
	- Maintains a state of the user and a set of rules for how the state to evolves.
	- By observing the environment and the user’s choices, robot takes action that change users' state.

1. An implemented theory of mind to improve human–robot shared plans execution
	- System maintains a Theory of Mind representation of the user i.e. their task and beliefs. 
	- Representation is updated as the interaction takes place. Robot aims to minimize explicit instructions between it and the user.

1. Adaptive artificial companions learning from users feedback
	- User preferences updated using interaction traces.
	- ...

1. Towards a synchronised grammars framework for adaptive musical human–robot collaboration
	- Uses Context-Free Stochastic Grammars, and is taught a base-line user profile in a dedicated interaction.
	- The user informs the system that they dislike the robot’s musical decisions, which triggers a change in their preferences profile.

1. Robot recommender system using affection-based episode ontology for personalization
	- Builds and maintains a preferences profile of the user, in an ontology.
	- Profile is updated during interaction via n-gram analysis of the events. 
	- ...


## Clustering sequences
1. [Unsupervised Learning of Proceduresfrom Demonstration Videos](https://www.ml.cmu.edu/research/dap-papers/S18/dap-goel-karan.pdf)
	- Using procedures

1. [Unsupervised Clickstream Clustering for
User Behavior Analysis](https://dl.acm.org/doi/pdf/10.1145/2858036.2858107?download=true)
	- Hierarchical clustering by removing the important clustering features after each level.

1. [Clickstream Clustering using Weighted Longest Common Subsequences](https://www.researchgate.net/publication/2365525_Clickstream_Clustering_using_Weighted_Longest_Common_Subsequences)

1. [Algorithms for clustering clickstream data](https://www.sciencedirect.com/science/article/pii/S0020019008003670)

1. [Clickstream User Behavior Models](https://dl.acm.org/doi/abs/10.1145/3068332?casa_token=Li8jJQDJuKEAAAAA:n0nIIuiommbktUb-wUbcO-cuF9mk0YmE9JnOA8mD4urScRsPAlOhww2Esw58mdBZ3cQFF0MmDb7UmQ)

1. [Consumers' decision-making process and their online shopping behavior: a clickstream analysis](https://www.sciencedirect.com/science/article/abs/pii/S0148296304001985)

1. [Clustering of DNA Sequences in Human Promoters](https://genome.cshlp.org/content/14/8/1562.full)

1. [Cluster-Buster: finding dense clusters of motifs in DNA sequences](https://academic.oup.com/nar/article/31/13/3666/2904162)

1. [BLAST (basic local alignment search tool)](https://en.wikipedia.org/wiki/BLAST_(biotechnology))

1. [Detection of cis -element clusters in higher eukaryotic DNA](https://academic.oup.com/bioinformatics/article/17/10/878/251511)

1. [A comparative evaluation of sequenceclassification programs](https://bmcbioinformatics.biomedcentral.com/track/pdf/10.1186/1471-2105-13-92)

1. [Sequence Similarity Methods](http://shodor.org/talks/calvin_cbbe11/d1s4/D1.3.Sequence_Comparison_Methods.pdf)


## Modelling human-robot collaboration
1. [Relational activity processes for modeling concurrent cooperation](https://ieeexplore.ieee.org/document/7487765)

1. [Multimodal Probabilistic Model-Based Planning for Human-Robot Interaction](https://ieeexplore.ieee.org/document/8460766)

1. [Optimization of Temporal Dynamics for Adaptive Human-Robot Interaction in Assembly Manufacturing](http://www.stefanosnikolaidis.net/papers/RSS_2012_Published_Version.pdf)

1. [Human-robot collaboration by intention recognition using probabilistic state machines](https://ieeexplore.ieee.org/abstract/document/5524605)


## IKEA assembly simulation
1. [IKEA Furniture Assembly Environmentfor Long-Horizon Complex Manipulation Tasks](https://arxiv.org/pdf/1911.07246.pdf)


## Robot assistance in assembly tasks
1. [Will A Robot Take My Manufacturing Job? Yes, No, And Maybe](https://www.forbes.com/sites/jimvinoski/2018/09/03/will-a-robot-take-my-manufacturing-job-yes-no-and-maybe/#8611148123f5)


## Pose for human action prediction
1. [Towards safe robot-human collaboration systems using human pose detection](https://ieeexplore.ieee.org/document/7219658)
