## Human-in-the-loop learning

1. [Robot Learning via Human Adversarial Games](http://www.stefanosnikolaidis.net/papers/duan_IROS_2019.pdf)
	- 2 player game with incomplete information. Turn-taking.
	- Reward = reward for robot action in absence of adversary - penalty induced by human action = Rr - αRh
	- Method: Robot policy is CNN. Initialize parameters by optimizing for Rr. 2D input image (top down). CNN predicts probability of success for every grasping angle for a grasp location (corresponding to each image patch). Policy then chooses best patch and angle. Rr = 1 if robot succeeds, 0 if fails. Rh = 1 if human succeeds, 0 if fails. Loss function for CNN is binary cross entropy loss between network's prediction and received reward. Network trained using RMSProp. 
	- Study: Baxter in Mujoco. Each user trained with the robot on only one object presented to robot at the same orientation. 
	- Concerns/advantages: What if the human does not know the best grasp? What if the grasp that is best for the human (according to his domain knowledge) is not the best for the robot. I can see that despite of this, the robot can end up learning robusts grasps efficiently as the human is not trying to impose its own way of grasping, rather removing the cup based on the way the robot would grasp it. I think this is an advantage over methods that use human as a collaborator or expert demonstrator.
	- Questions: 1) Why a neural network is represented the way it is in figure 3? How to make these diagrams?