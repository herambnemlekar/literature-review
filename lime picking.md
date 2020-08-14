## Lime detection
1. [Computer vision for fruit harvesting robots – state of the art and challenges ahead](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.298.2555&rep=rep1&type=pdf)
    - Motivation: Agricultural tasks are handled manually despite the expensive and diminishing agricultural labour, physically demanding and time-consuming operations.
    - Challenge: Unstructured environment - different colours, shapes, sizes, textures, reflectance properties, uncertainty in environment, changing illumination and shadows, and occlusions.
    - Sensors & Cues: Single camera fixed on the robot or/and on the robot arm. Multiple cameras for stero vision to get depth. RGBD sesnors for depth. *Spectral imaging for recognition based on reflection, especially when fruit and foliage have same colour. However it is sensitive to illumination, and there is also the possibility that the fruit and foliage have similar spectral signature.* Hyperspectral imaging (RGB + spectral imaging) provides complete spectral signature of each pixel, however requires extensive acquisition and processing time. Other cues - Thermal imaging is highly susceptible to illumination. Texture, usually combined with colour sensing. Shape is immune to illumination and very useful for spherical fruits, but is computationally intensive to extract, may be affected by perspective and highly sensitive to occlusions.
    - Algorithms: 1) Adaptive global threholding not suitable for image segmentation in unstructured environments and ignores shape information. Watershed segmentation considers grey scale image as topographical surface. 2) Clustering is sensitive to illumination and ignores shape information. 3) Template matching only useful when variability of target object is small. 4-5) Global shape inference is computationally intensive. Local shape inference with circular Hough transform is used for spherical fruits like tomatoes. 6) Neural networks with RGB values as features. Waschs et al. (2010) use three NNs, one each for RGB, HSV and L\*a\*b\*, and then take a majority vote.
    - Future challenges: 1) Use other cues like texture with colour for segmentation. 2) Make hyperspectral imaging computationally manageable for real-time use. 3) Realize the entire shape and pose of occluded fruits by using some prior knowledge of the expected shape. 4) Apply Gestalt principles of good continuation inspired from human vision for occluded fruits. 5) Active vision like Blake (1992) by combining planning with 3D inference. 5) 3D estimation of fruit, peduncle, nearby leaves and branches. 6) Extensive evaluation of the performance of proposed methods along with creating a public dataset for future evaluations.

2. [YOLO-Tomato: A Robust Algorithm for Tomato Detection Based on YOLOv3](https://www.mdpi.com/1424-8220/20/7/2145/pdf)  
    - Problem: Tackles illumination variation, and branch, leaf and tomato occlusions.
    - Contributions: 1) Dense architecture incorporated into YOLOv3 to improve prediction by reuse of features. 2) Circular bounding box (C-Box) for tomato localization.  

3. [An Autonomous Fruit and Vegetable Harvester with a Low-Cost Gripper Using a 3D Sensor](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6982854/#sec6-sensors-20-00093)
    - Section 4 details their generalized approach in detecting & locating cutting points.

4. [DeepFruits: A Fruit Detection System Using Deep Neural Networks](https://www.mdpi.com/1424-8220/16/8/1222)
    - Approach using Faster R-CNN for segmentation and detection that is robust to lighting variation and occlusion.

5. [Determination of the number of green apples in RGB images recorded in orchards](https://www.sciencedirect.com/science/article/pii/S0168169911002638)
    - Used color and texture information to classify green apples
    - Illumination variation and color saturation had a large impact on the results

## Motion planning for lime picking
1. [Simulation of Apple Picking Path Planning Based On Artificial Potential Field Method](https://iopscience.iop.org/article/10.1088/1755-1315/252/5/052148/meta)

1. [Analysis of a motion planning problem for sweet-pepper harvesting in a dense obstacle environment](https://www.sciencedirect.com/science/article/pii/S1537511015001191)

1. [RRT-based path planning for an intelligent litchi-picking manipulator](https://www.sciencedirect.com/science/article/pii/S0168169918303971)
    - Branches are simplified to a series of cylinders. Therefore for collision detection, collision should be checked between: 6 cylinders of the robot x (no. of branches x no. of cylinders per branch).
    - Limitation: Branches easy to model as cylinders in the litchi plant simulation as the branches are not heavily covered with leaves.

1. [Path Planning for a Fruit Picking Manipulator](http://www.geyseco.es/geystiona/adjs/comunicaciones/304/C03090001.pdf)

### Summary
1. [Motion Planning and Obstacle Avoidance](https://link.springer.com/chapter/10.1007/978-3-319-32552-1_47)
    - This is a chapter of a rather recent(2016) book that includes state-of-the-art algorithms on robot motion planning and obstacle avoidance.

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
1. [Bidirectional Potential Guided RRT* for Motion Planning](https://ieeexplore.ieee.org/document/8763966)
    - Combine RRT*-connect with APF to solve local minima problem of APF
    - Improve performance of RRT* by reducing its randomness with APF guiding the exploration
    - Particularly suited to narrow channels, which could be well suited for our case
2. [Rapidly-Exploring Random Vines (RRV) for Motion Planning in Configuration Spaces with Narrow Passages](https://ieeexplore-ieee-org.libproxy1.usc.edu/document/8460186)
    - Improved RRT to work better in narrow corridors.
    - Expands far less nodes than RRT or RRT connect and is significantly faster. From the experiments it seems that the cost is that is produces sub-optimal paths that are far worse than those produced by RRT.
    - Need to read more in depth.
3. [Potential guided directional-RRT* for accelerated motion planning in cluttered environments](https://ieeexplore.ieee.org/abstract/document/6617971)
4. [Adaptive Potential guided directional-RRT](https://ieeexplore.ieee.org/abstract/document/6739744)
5. [Potential functions based sampling heuristic for optimal path planning](https://link.springer.com/article/10.1007/s10514-015-9518-0)

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