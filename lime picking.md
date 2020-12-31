# Motion planning techniques used in fruit harvesting
1. [Simulation of Apple Picking Path Planning Based On Artificial Potential Field Method](https://iopscience.iop.org/article/10.1088/1755-1315/252/5/052148/meta)
    - Claims: Combine characteristics of obstacles in environment, use APF in 3D joint-space, and a more smooth obstacle avoidance motion curve. 
    - Summary: Uses APF to plan motion. Done completely in simulation. Does not mention obstacle characteristics or smooth motion curve.

1. [Analysis of a motion planning problem for sweet-pepper harvesting in a dense obstacle environment](https://www.sciencedirect.com/science/article/pii/S1537511015001191)
    - Manually measured position of all peppers and their stems in a greenhouse and created simulation environment.
    - IK used to get joint angles for possible end effector poses for picking.
    - Bi-directional RRT used for path planning, smoothing done by divide and conquer. Maximum possible planning time was 30 mins. 
    - Shape primitives used for collision checking eg. cylinder for the sweet pepper.
    - Analyse motion planning success with respect to angle of approach, end effector size, robot position, fruit location, stem spacing. 

1. [Evaluation of a direct optimization method for trajectory planning of a 9-DOF redundant fruit-picking manipulator](https://ieeexplore-ieee-org.libproxy1.usc.edu/document/7139558/references#references)
    - Initial path found in workspace. B-spline curve such that gripper enters plant radially.
    - Path optimized with hard constraints for joint limits, start and end velocities. Collision avoidance done by minimising the objective function.
    - For collision avoidance, robot and environment geometries modelled using swept-sphere volumes.
    - Limitation: Tested in green house where the there is just one vertical stem, which can be easily modelled as a vertical cylinder.

1. [RRT-based path planning for an intelligent litchi-picking manipulator](https://www.sciencedirect.com/science/article/pii/S0168169918303971)
    - Avoid branches and untargeted fruit. Branches are simplified to a series of cylinders. Therefore for collision detection, collision should be checked between: 6 cylinders of the robot x (no. of branches x no. of cylinders per branch).
    - RRT with target gravity used to find paths. Paths improved using Genetic algorithm where shorter paths with greater distance from obstacles considered more fit. After which path smoothing is done.
    - They claim to use binocular vision to detect branches. However don't provide details of how they get such accurate measurements.
    - Limitation: Branches easy to model as cylinders in the litchi plant simulation as the branches are not heavily covered with leaves.

1. [Path Planning for a Fruit Picking Manipulator](http://www.geyseco.es/geystiona/adjs/comunicaciones/304/C03090001.pdf)
    - Considers only stems and fruits as obstacles. Ignores leaves and branches. 
    - Claim to represent obstacles as primitive objects - cylinders and spheres. However their experiments only use stem center coordinates and the fruit center coordinates.
    - Plans in workspace using APF and converts trajectory to join space using inverse kinematics.
    - Does not mention how the center coordinates would be obtained in real-world tasks.

1. [An autonomous robot for harvesting cucumbers in greenhouses](file:///tmp/mozilla_heramb0/VanHenten2002_Article_AnAutonomousRobotForHarvesting.pdf)
    - Detect green cucumbers against green background.
    - Cucumbers and obstacles modelled for collision checking.
    - Inverse kinematics used to map end effector pose for grasping cucumber to configuration space.
    - A* used for planning by dicretising the configuration space.
    - Does not provide details of how obstacles are detected and mapped to the configuration space.
    - Same paper: [Collision-free Motion Planning for a Cucumber Picking Robot](https://www.sciencedirect.com/science/article/pii/S1537511003001338)

1. [**Task and Motion Planning for Apple Harvesting Robot**](https://www.sciencedirect.com/science/article/pii/S1474667015349922)
    - Uses point cloud data to formm collision map
    - Uses RRTConnect in OMPL for planning collision free path given robot urdf and collision map.

1. Obstacle avoidance path planning of hybrid harvesting manipulator based on joint configuration space
    - Paper is in chinese
    - Uses RRT.

1. [On-line near minimum-time path planning and control of an industrial robot for picking fruits](https://www.sciencedirect.com/science/article/pii/S0168169904000912)


1. [Development of an autonomous kiwifruit picking robot](https://www.researchgate.net/profile/Claire_Flemmer/publication/220774427_Development_of_an_autonomous_kiwifruit_picking_robot/links/0046353065c888a409000000/Development-of-an-autonomous-kiwifruit-picking-robot.pdf)
    - Nothing about motion planning

1. [Near-minimum-time task planning for fruit-picking robots](https://ieeexplore-ieee-org.libproxy1.usc.edu/stamp/stamp.jsp?tp=&arnumber=68069)
    - Travelling Salesman Problem (TSP) for finding the near optimal path for picking *n* fruits
    - Motion between fruits equvivalent to moving along straight line in a Euclidean configuration space.

1. [Robotic melon harvesting](https://ieeexplore-ieee-org.libproxy1.usc.edu/document/897793)
    - TSP for moving the tractor carrying the picking manipulator to a cluster of melons
    - Motion planning for picking not clearly explained. Need to read paper again.


# Motion Planning: RRT

### Real-world application
1. An integrated approach to inverse kinematics and path planning for redundant manipulators

### Summary
1. [Motion Planning and Obstacle Avoidance](https://link.springer.com/chapter/10.1007/978-3-319-32552-1_47)
    - This is a chapter of a rather recent(2016) book that includes state-of-the-art algorithms on robot motion planning and obstacle avoidance.

## Cost-based RRT
1. [Cost  Based  Planning  with  RRT  in  Outdoor  Environments](https://ieeexplore.ieee.org/abstract/document/4651052?casa_token=Ny5AFrGl6BgAAAAA:_nAUBZRKTWI8RJ2OAo2VLKRWRBRu10L5R4JTfcET2MvZu-Lb_uLk7oCzWbjU_RsFloacUvcYeg)
    - Selecting nearest node based on cost + distance.

1. [Transition-based RRT for Path Planning in Continuous Cost Spaces](https://ieeexplore-ieee-org.libproxy2.usc.edu/stamp/stamp.jsp?tp=&arnumber=4650993)
    - [Sampling-Based Path Planning on Configuration-Space Costmaps](https://ieeexplore-ieee-org.libproxy1.usc.edu/stamp/stamp.jsp?tp=&arnumber=5477164)
    - Each configuration is associated with a cost.
    - If the cost of a new node is more than the nearest node, the new node is added to the tree with a probability inversely proportional to the cost difference.
    - Temperature which is the hyperparameter for calculating the probability is adapted according to how many nodes have been rejected or accepted.

1. [Addressing  Cost-Space  Chasms  in  Manipulation  Planning](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=5979797&casa_token=uAlYkW0o8egAAAAA:f_dFy31tGXm2xY_ZlISaais2SiTLPhD30g96deiKvsUCRTZ5KdfxeNCJhy0mJzhLuD0hSpywRg)
    - Based on transition-based RRT
    - If a configuration is rejected because its cost is above the threshold, gradient descent is used to shift the configuration to a lower cost. If the new configuration has lower cost than the parent node or passes the temperature check, the node is is accepted, however this acceptance is used to adapt the temperature.

1. Rapidly-exploring Random Trees for Testing Automated Vehicles
    - Uses transition-based RRT to accept or reject a configuration based on cost of collision.

1. [Enhancing the Transition-based RRT to Deal with Complex Cost Spaces](https://ieeexplore-ieee-org.libproxy1.usc.edu/stamp/stamp.jsp?tp=&arnumber=6631158)
    - Bi-directional transition-based RRT

1. [Motion Planning by T‐RRT with Potential Function for Vertical Articulated Robots](https://onlinelibrary.wiley.com/doi/full/10.1002/eej.23103)
    - Uses APF as cost function for transition-based RRT. 
    - Length of path comparable to RRT\*, computation time much less than RRT\*. However they (probably) used a different cost function for their RRT\* implementation.

### RRT-star approaches

1. [Sampling-based algorithms for optimal motion planning](https://journals-sagepub-com.libproxy1.usc.edu/doi/pdf/10.1177/0278364911406761)
    - RRT*

1. [Fast Sampling-Based Cost-Aware Path Planning With Nonmyopic Extensions Using Cross Entropy](https://ieeexplore-ieee-org.libproxy1.usc.edu/stamp/stamp.jsp?tp=&arnumber=8017656)
    - RRT* with a cross entropy based extend/steer algorithm


1. [Traversability-Based RRT* for Planetary Rover Path Planning in Rough Terrain with LIDAR Point Cloud Data](https://search-proquest-com.libproxy2.usc.edu/docview/2465810115?accountid=14749&pq-origsite=summon)
    - RRT* with a custom cost function and *traversability assessment* to check if extend possible.

1. [**Optimal Path Planning in Complex Cost Spaces With Sampling-Based Algorithms**](https://ieeexplore-ieee-org.libproxy2.usc.edu/stamp/stamp.jsp?tp=&arnumber=7305826)
    - T-RRT + RRT*
    - 
1. [Optimal Path Planning Based on a Multi-Tree T-RRT* Approach for Robotic Task Planningin Continuous Cost Spaces](https://strathprints.strath.ac.uk/64678/1/Wang_etal_Mecatronics2018_Optimal_path_planning_based_on_a_multi_tree_T_RRT.pdf)

1. [**Potential Guided Directional-RRT* for Accelerated Motion Planning in Cluttered Environments**](https://ieeexplore-ieee-org.libproxy2.usc.edu/stamp/stamp.jsp?tp=&arnumber=6617971)
    - Applies gradient descent on random sample

1. [Adaptive Potential guided directional-RRT](https://ieeexplore.ieee.org/abstract/document/6739744)

1. [Potential functions based sampling heuristic for optimal path planning](https://link.springer.com/article/10.1007/s10514-015-9518-0)

1. [Potential and Sampling Based RRT Star for Real-Time Dynamic Motion Planning Accounting for Momentum in Cost Function]

1. [Bidirectional Potential Guided RRT* for Motion Planning](https://ieeexplore-ieee-org.libproxy2.usc.edu/stamp/stamp.jsp?tp=&arnumber=8763966)
    - Claim: Suitable for narrow channels
    - Similar to P-RRT\*, randomized gradient descent (RGD) used to shift random sample along gradient. 
    - The target for attractive field for each of the two trees is not mentioned.

1. [Potentially guided bidirectionalized RRT* for fast optimal path planning in cluttered environments](https://www.sciencedirect.com/science/article/pii/S0921889017309387)
    -

1. [Optimal path planning in cluttered environment using RRT\*-AB](https://link.springer.com/article/10.1007/s11370-017-0236-7)
    - Claim: Improves upon Informed-RRT\*
    - Does not test against Informed-RRT\*, only RRT\* and RRT\*-Smart. RRT\*-AB more efficient than RRT\* and RRT\*-Smart.
    - It searches a path using RRT\* by random sampling within a constrained *connectivity region* defined by the start and goal configuration. After a *complete scan* if a path is not found, the connectivity region is increased. 
    - Does not say how connectivity region and complete scan are implemented. However it seems it is along a straight line connecting start and goal configurations.
    - If the complete scan determines that path is not found after too many samples. then the efficiency of this method would be as poor as RRT\*.

1. [RRT\*N: an efficient approach to path planning in 3D for Static and Dynamic Environments](https://www.tandfonline.com/doi/pdf/10.1080/01691864.2020.1850349?needAccess=true)
    - Claim: Improves upon Informed-RRT\* and Bidirectional RRT\*.
    - Extends RRT\*N to 3D environments.
    - Samples from a normal distribution along a straight line connecting the start and goal configurations.
    - For dynamic obstacles, a path is initially found, then the parts of the path that would collide with the dynamic obstacle are removed and a new path is found between the cut off points. 

1. [**Biased Sampling Potentially Guided Intelligent Bidirectional RRT\* Algorithm for UAV Path Planning in 3D Environment**](https://www.hindawi.com/journals/mpe/2019/5157403/)
    - Claim: Improves upon Potentially Guided Bidirectional RRT\*
    - Note: RGD in previous work is not exactly gradient of APF. It is gradient of attractive force towards goal/start which stops whenever node reaches close to obstacle.
    - First a sampling bias (Bi-bias) is applied on the random sample. Bi-bias moves the random sample towards the previous new node of either tree A or tree B (alternatively).
    - Next it applies APF (which includes repulsive force from obstacles) with attractive force towards previous new node of one of the trees alternatively.

1. [An Improved RRT* Path Planning Algorithm for Service Robot, May 2020](https://ieeexplore-ieee-org.libproxy1.usc.edu/document/9085226)
    - Simialr to RRT\*-AB
    - Samples wihtin a *connectivity region* and modifies connectivity region after a *complete scan*.
    - *Connectivity region* seems to be around a straight line connecting start and goal configurations.
    - May not be effective for a maze.
    - Once a path is found, it uses Informed-RRT\* to optimize the path.

1. [Deep Learning rooted Potential piloted RRT\* for expeditious Path Planning, July 2019](https://dl-acm-org.libproxy1.usc.edu/doi/pdf/10.1145/3351917.3351990)
    - Predict parameters for potential guided RRT\*. Parameters are the APF gains for attraction towards goal and repulsion from obstacles in different parts of the configuration space.
    - Trains a neural network to predict the parameters of an APF. Start, goal and obstacle centers and area used as input features. Dijkstra's used to calculate ground truth.

1. [Accelerated RRT* and its evaluation on Autonomous Parking, Feb 2020](https://arxiv.org/pdf/2002.04521v1.pdf)
    - Unpublished?

1. [3-D Trajectory Planning of Aerial Vehicles Using RRT\*, May 2017](https://ieeexplore-ieee-org.libproxy1.usc.edu/stamp/stamp.jsp?tp=&arnumber=7505628)
    - Applies APF on random sample.

1. [A Survey of Asymptotically Optimal Sampling-based Motion Planning Methods, Sep 2020](https://arxiv.org/pdf/2009.10484.pdf)
    - [Adaptively Informed Trees (AIT\*): Fast Asymptotically Optimal Path Planning through Adaptive Heuristics](https://arxiv.org/pdf/2002.06599.pdf)

### Artificial Potential Field
1. [An Improved Artificial Potential Field Method Based on DWA and Path Optimization](https://ieeexplore.ieee.org/document/8996014)
    - Use Dynamic Window Approach to solve local minima problem of APF
2. [Trajectory Optimization of Pickup Manipulator in Obstacle Environment Based on Improved Artificial Potential Field Method](https://www.mdpi.com/2076-3417/10/3/935)
    - Complete APF by increasing number of sub-target points and improving the obstacle repulsion field function.
    - Applied on a 5-DoF robot
3. [Robotic Arm Path Planning Based on Three-Dimensional Artificial Potential Field](https://ieeexplore.ieee.org/document/8571458)
    - Using rotational repulsive field around obstacles instead of pushing robot directly away
    - Another attempt to solve local minima problem
4. [Obstacle Avoidance for Mobile Robots Using Artificial Potential Field Approach with Simulated Annealing](https://ieeexplore.ieee.org/document/931933)
    - Ancient paper (2001)
    - Uses Simulated Annealing to escape from local minima
5. [6-DOF Robotic Obstacle Avoidance Path Planning Based on Artificial Potential Field Method](https://ieeexplore.ieee.org/abstract/document/8768792)
    - Similar to the apple picking paper, but is better written : )


### RRT related
1. [Rapidly-Exploring Random Vines (RRV) for Motion Planning in Configuration Spaces with Narrow Passages](https://ieeexplore-ieee-org.libproxy1.usc.edu/document/8460186)
    - Improved RRT to work better in narrow corridors.
    - Expands far less nodes than RRT or RRT connect and is significantly faster. From the experiments it seems that the cost is that is produces sub-optimal paths that are far worse than those produced by RRT.
    - Need to read more in depth.


### Others
1. [Robotic Path Planning Based on Improved Ant Colony Algorithm](https://link.springer.com/chapter/10.1007/978-3-030-22796-8_37)
    - Interesting method but only applied to 2D discrete space
    - Doesn't seem to be applicable since we have a continuous space
2. [Task and Motion Planning for Apple Harvesting Robot](https://www.sciencedirect.com/science/article/pii/S1474667015349922)
    - High level symbolic planning
    - Low level use sampling based planning, including RRT, RRTConnect, KPIECE etc.
3. [Path planning and obstacle avoidance approaches for robot arm](https://ieeexplore.ieee.org/document/8105619)
    - Use of Non Uniform Rational B-splines to make the path more smooth. 

### Benchmarks for Motion Planners
1. [Comparing different sampling-based motion planners in multiple configuration spaces](https://www.diva-portal.org/smash/get/diva2:1214377/FULLTEXT01.pdf)

1. [SR-RRT: Selective retraction-based RRT planner](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6224928)

1. [A generic infrastructure for benchmarking motion planners](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6386228)

1. [An efficient retraction-based RRT planner](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4543785)

1. [Planners Benchmarking Documentation](https://readthedocs.org/projects/planners-benchmarking/downloads/pdf/latest/)

1. [Benchmarking Motion Planning Algorithms](http://kavrakilab.org/publications/moll-sucan2015benchmarking-motion-planning.pdf)


# Lime detection
1. [Computer vision for fruit harvesting robots – state of the art and challenges ahead](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.298.2555&rep=rep1&type=pdf)
    - Motivation: Agricultural tasks are handled manually despite the expensive and diminishing agricultural labour, physically demanding and time-consuming operations.
    - Challenge: Unstructured environment - different colours, shapes, sizes, textures, reflectance properties, uncertainty in environment, changing illumination and shadows, and occlusions.
    - Sensors & Cues: Single camera fixed on the robot or/and on the robot arm. Multiple cameras for stero vision to get depth. RGBD sesnors for depth. *Spectral imaging for recognition based on reflection, especially when fruit and foliage have same colour. However it is sensitive to illumination, and there is also the possibility that the fruit and foliage have similar spectral signature.* Hyperspectral imaging (RGB + spectral imaging) provides complete spectral signature of each pixel, however requires extensive acquisition and processing time. Other cues - Thermal imaging is highly susceptible to illumination. Texture, usually combined with colour sensing. Shape is immune to illumination and very useful for spherical fruits, but is computationally intensive to extract, may be affected by perspective and highly sensitive to occlusions.
    - Algorithms: 1) Adaptive global threholding not suitable for image segmentation in unstructured environments and ignores shape information. Watershed segmentation considers grey scale image as topographical surface. 2) Clustering is sensitive to illumination and ignores shape information. 3) Template matching only useful when variability of target object is small. 4-5) Global shape inference is computationally intensive. Local shape inference with circular Hough transform is used for spherical fruits like tomatoes. 6) Neural networks with RGB values as features. Waschs et al. (2010) use three NNs, one each for RGB, HSV and L\*a\*b\*, and then take a majority vote.
    - Future challenges: 1) Use other cues like texture with colour for segmentation. 2) Make hyperspectral imaging computationally manageable for real-time use. 3) Realize the entire shape and pose of occluded fruits by using some prior knowledge of the expected shape. 4) Apply Gestalt principles of good continuation inspired from human vision for occluded fruits. 5) Active vision like Blake (1992) by combining planning with 3D inference. 5) 3D estimation of fruit, peduncle, nearby leaves and branches. 6) Extensive evaluation of the performance of proposed methods along with creating a public dataset for future evaluations.

2. [YOLO-Tomato: A Robust Algorithm for Tomato Detection Based on YOLOv3](https://www.mdpi.com/1424-8220/20/7/2145/pdf)  
    - Problem: Tackles illumination variation, and branch, leaf and tomato occlusions.
    - Contributions: 1) Dense architecture incorporated into YOLOv3 to improve prediction by reuse of features. 2) Circular bounding box (C-Bbox) for tomato localization.  
    - Data: Pictures of tomatoes in different conditions - ripe, unripe, individual, clusters, occluded, dark and bright. Data augmented by scaling and flipping.
    - Technical details: 1) Dense net specifics. 2) Loss function details. 3) Non-Maximum Suppression (NMS) used to find final bounding boxes. At each iteration, NMS selects the bbox with most confidence and moves it to the final list of bboxes, then checks if other bboxes in the original bbox list overlap (IoU) with the max confidence bbox for a given threshold, overlapping bboxes are removed, then the process is repeated.
    - Experiments & Results: 1) Intyersection over union for C-Bbox was more than R-Bbox. 2) F1 score for YOLO-Tomato (dense + C-bbox) > YOLO-dense > YOLOv3. 3) YOLO-Tomato peforms well in different lighting and occlusion conditions, mostly due to the dataset. 4) Overall prediction accuracy YOLO-Tomato > YOLO-dense > YOLOv3.

3. [An Autonomous Fruit and Vegetable Harvester with a Low-Cost Gripper Using a 3D Sensor](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6982854/#sec6-sensors-20-00093)
    - Section 4 details their generalized approach in detecting & locating cutting points.

4. [DeepFruits: A Fruit Detection System Using Deep Neural Networks](https://www.mdpi.com/1424-8220/16/8/1222)
    - Approach using Faster R-CNN for segmentation and detection that is robust to lighting variation and occlusion.

5. [Determination of the number of green apples in RGB images recorded in orchards](https://www.sciencedirect.com/science/article/pii/S0168169911002638)
    - Used color and texture information to classify green apples
    - Illumination variation and color saturation had a large impact on the results


