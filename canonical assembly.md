# Learning preferences from canonical assembly tasks
## What is a canonical task?
1. [Canonical tasks, environments and models for social simulation](https://link.springer.com/article/10.1023/A:1009629602618)
	- [Social simulation](https://whatis.techtarget.com/definition/social-simulation): the application of computer-based methods and technologies to replicate human social behavior in various environments and scenarios. 
	- In mathematics, canonical matrices are effectively matrices of a standard form and transformations can be performed on other matrices to show that they can be converted into canonical matrices. All matrices which, by means of allowable operations, can be transformed into a canonical matrix have the properties of the canonical matrix.
	- Canonical environment: an abstract form with known properties that can be used to represent environments.
	- Canonical tasks: abstract forms that capture aspects of the tasks undertaken by agents in applications models. 
	- Canonical model: A model incorporating a canonical environment in which agents undertake canonical tasks. Representations and effects of socially situated cognitive behaviour implemented in models with particular domains of application can be mapped unambiguously into common abstract models. Consequently, when there are demonstrated relationships among canonical models, those relationships apply to the applications models that map into the canonical models.
	- Initial representation of the canonical environment: the digit string. Ordering the 1s and 0s by operating site and event type (intruder, fire, mains collapse, chlorine leak,etc.) yields a digit-string representation of the environment.
	- function of the organization is correctly to recognize somecharacteristic of the digit string
	- Effect of actions on state captured through an action-state-change matrix. Transitioning from one state to next without taking actions is captured through a state-state-change matrix.
	- When each action in the collaborative task is independent, the collaborative task reduces to the independent task. When no actions are taken in the independent task, it reduces to the recognition task.


1. [Towards canonical task types for user interface design](https://ieeexplore.ieee.org/abstract/document/5341619/)


## Assembly skill tranfer
1. [Application of the Assembly Skill Transfer System in an Actual Cellular Manufacturing System, Jan 2012](https://ieeexplore-ieee-org.libproxy2.usc.edu/stamp/stamp.jsp?tp=&arnumber=5985491)
	- Cellular manufacturing system: A human-centered production system that satisfies manufacturing flexibility and assembly efficiency requirements. It consists of a team of operators with various skills.
	- Human skill model involves Cognition, then Decision and then Execution. In this paper, the decision skill aspect is ignored as assembly decisions are taken by desginers and not operators. Cognition skill is a function that maps the actual state to the state perceived by the operator. Motor (execution) skill is a function that maps the intended action to the actual action executed by the operator.
	- Skill Transfer System: Extract assembly skills from skilled operators and then transfer them to novice ones, in both cognition and execution aspects.
	- The proposed assembly system includes physical support (assisting operators with automation), informational support (providing assembly information), and the assembly skill transfer system (improving operator performance).
	- Physical support: Two 6-DOF manipulators deliver assembly parts from a tray shelf to an assembly table and grasp the assembly parts to prevent any wobbling during the assembly process.
	- Information support: LCD display for instructions from an Assembly Information Database, laser pointer to indicate accurate assembly position and audio speakers.
	- Cable harness task example: An *assembly task* is composed of *assembly operations* i.e. insert cable and fasten cable. Each *assembly operation* consists a series of *steps* i.e. hold cable, move cable to connector, insert cable in connector, release cable. Each step has a *situation* i.e. state of assembly and an *action* i.e. operator's movements that change the situation. 
	- Hypothesis: Extracting the assembly skills that the skilled operators and the novice operators lay different emphasis on, and transferring them to the novice operators could improve the novices’ assembly performance effectively.
	- Method: 1) Represent skills in natural language i.e. if <situation> then <verb, object, modifier> or if <action> then <verb, object, modifier>. Verbs for cognition skills - Focus, Memorize, Compare. verbs for motor skills - Hold, Keep (Pose), Move. Not all assembly skills can be represented in natural language as cognition and motor skills. 2) S skill candidates are provided by skilled operators. 3) Performance of P operators (skilled and novice) measured. For each skill in S, the degree of emphasis (DOE) by each of the P operators is calculated. By checking correlation between DOE and performance, the skills to be tranferred are extracted. The novice operators are then trained on these extracted skills.
	

### Cellular Manufacturing
1. [Multi-modal assembly-support system for cell production]
	- Operators only required to execute the complicated and flexible assembly tasks that need human assembly skills; while robots are employed to execute the monotonous and repeated tasks such as the parts feeding repetitions during the assembly process.
1. [A new cell production assembly system with twin manipulators on mobile base]
	- Operators only required to execute the complicated and flexible assembly tasks that need human assembly skills; while robots are employed to execute the monotonous and repeated tasks such as the parts feeding repetitions during the assembly process.

### Test bed design
1. [Designing open-loop plans for planar micro-manipulation, May 2006](https://ieeexplore-ieee-org.libproxy2.usc.edu/stamp/stamp.jsp?tp=&arnumber=1641782)
	- Directly considers the canonical assembly problem of a peg-in-the-hole task of moving a peg from configuration A to configuration B by means of a series of pushing operations.
	- Their goal is to use simulation and motion planning tools to design open loop manipulation plans that rely only on an estimate of initial position and orientation.
	- Use RRT based algorithm to find manipulation plans.
1. [Automated Assembly for Mesoscale Parts, July 2011](https://ieeexplore-ieee-org.libproxy2.usc.edu/stamp/stamp.jsp?tp=&arnumber=5753963)
	- Describes a test-bed for planar micro and mesoscale manipulation. Show how planar peg-in-the-hole assembly tasks can be designed with randomized motion planning.
	- Considers uncertainty due to unknown geometric and physical parameters characterizing the environment.
	- The goal is to come up with a manipulation plan, consisting of pushing motions, that guarantees successful assembly in the presence of uncertainty.
	- Directly describes the canonical problem of the peg-in-the-hole task as assembling a planar rectangular part into a planar rectangular slot. The paper provides logical reasons as to why this task is a good representation of the micro and meso-assembly environment.
	- Used RRT based algorithm to find manipulation plans.


## Object-action association
1. [On the Relations Between Seen Objects and Components of Potential Actions, 1998](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.211.6311&rep=rep1&type=pdf)
	- Prior work shows that humans possess strong associations between objects and the actions commonly carried out with them.
	- Hypothesis: Visual objects potentiate actions even in the absence of explicit intentions to act.
	- Experiment: Participants had to decide as fast as possible whether each object was upright or inverted. There were total 22 household objects images and their left-right and top-down inverted images.
	- Results: **(a)** Seen objects automatically potentiate components of the actions they afford, (b) Compatibility effects of an irrelevant stimulus dimension can be obtained across a wide variety of naturally occurring stimuli, and **(c)** Intentions to act operate on already existing motor representations of the possible actions in a visual scene.

1. [The paired-object affordance effect, Aug 2010](https://search-proquest-com.libproxy1.usc.edu/docview/745195699/fulltextPDF/83819CE207D94688PQ/1?accountid=14749)
	- Prior work showed that actions were generated directly from the visual properties of the stimuli and not necessarily from semantic knowledge.
	- Results: (a) participants are sensitive to whether objects are positioned correctly for their own actions, (b) the position information is coded within an egocentric reference frame, (c) the critical representation involved is visual and not semantic, and (d) the effects are enhanced by a sense of agency.

1. Does selecting one visual object from several require inhibition of the actions associated with nonselected objects?

1. Actions or Hand-Object Interactions? Human Inferior Frontal Cortex and Action Observation

1. [What do 15,000 object categories tell us about classifying and localizing actions?, 2015](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Jain_What_do_15000_2015_CVPR_paper.pdf)
	- Contributions: (i) In-depth study of encoding objects for actions. (ii) Show that objects matter for actions. Combining object information with motion improves action classification. Especially objects that are close to the action. (iii) Establish that actions have object preferences. **(iv)** Reveal that object-action relations are generic, allows to transfer these relationships from the one domain to the other. (v) Objects when combined with motion, improve the state-of-the-art for both action classification and localization.
	- Object detection: CNN to compute the likelihood of the presence of each of 15k object categories in each frame of the considered videos.
	- Action classification: Linear SVM with one-against-rest approach.
	- Future work: Use object locations instead of just detecting object presence.

1. [Spatial-Aware Object Embeddings for Zero-Shot Localization and Classification of Actions](https://openaccess.thecvf.com/content_ICCV_2017/papers/Mettes_Spatial-Aware_Object_Embeddings_ICCV_2017_paper.pdf)

1. [On the relations between action planning, object identification, and motor representations of observed actions and objects, Mar 2008]

1. [Object Action Complexes as an Interface for Planning and Robot Control]

1. [Classifying Actions and Measuring Action Similarity by Modeling the Mutual Context of Objects and Human Poses]

## Relations between objects
1. Family Resemblances: Studies in the Internal Structure of Categories

1. [EGAD! An Evolved Grasping Analysis Dataset for Diversity and Reproducibility in Robotic Manipulation](https://ieeexplore-ieee-org.libproxy1.usc.edu/stamp/stamp.jsp?tp=&arnumber=9085936)
	- Compositional Pattern Producing Networks (CPPNs) used to generate 3D shapes. CPPNs are randomly initialized and then *evolved* by randomly adding and removing network nodes and connections, and changing weights, biases and activation functions.
	- At each iteration, a population is randomly sampled from the search space to undergo evolution and produce a new population of objects, which are subsequently evaluated and assigned to cells in the search space.
	- Diversity between the objects is measured using the Topology Matching metric based on Multiresolutional Reeb Graphs (MRGs) which provides a shape similarity score between two object meshes.

1. [Topology Matching for Fully Automatic Similarity Estimation of 3D Shapes](https://dl-acm-org.libproxy2.usc.edu/doi/pdf/10.1145/383259.383282)

## Relevant Prof. SK Gupta papers

1. [Toward Safe Human Robot Collaboration byusing Multiple Kinects based Real-time HumanTracking](http://terpconnect.umd.edu/~skgupta/Publication/JCISE2013_Morato_draft.pdf)
	- 4 kinects run on 4 local machines. For each kinect, a seperate Kalman filter is used for each of the 20 joint. Therefore the information from the 4x20 kalman filters is sent to a common server where particle filters are used to fuse the information of the 4 kinects for each joint.

1. [Design of Hybrid Cells to Facilitate Safe and Efficient Human–Robot Collaboration During Assembly Operations](https://asmedigitalcollection-asme-org.libproxy1.usc.edu/computingengineering/article/18/3/031004/367978/Design-of-Hybrid-Cells-to-Facilitate-Safe-and)