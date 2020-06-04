## Lime detection
1. [Computer vision for fruit harvesting robots–state of the art and challenges ahead](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.298.2555&rep=rep1&type=pdf)

## Motion planning for lime picking
1. [Simulation of Apple Picking Path Planning Based On Artificial Potential Field Method](https://iopscience.iop.org/article/10.1088/1755-1315/252/5/052148/meta)

1. [Analysis of a motion planning problem for sweet-pepper harvesting in a dense obstacle environment](https://www.sciencedirect.com/science/article/pii/S1537511015001191)

1. [RRT-based path planning for an intelligent litchi-picking manipulator](https://www.sciencedirect.com/science/article/pii/S0168169918303971)

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

### Others
1. [Robotic Path Planning Based on Improved Ant Colony Algorithm](https://link.springer.com/chapter/10.1007/978-3-030-22796-8_37)
    - Interesting method but only applied to 2D discrete space
    - Doesn't seem to be applicable since we have a continuous space
2. [Task and Motion Planning for Apple Harvesting Robot](https://www.sciencedirect.com/science/article/pii/S1474667015349922)
    - High level symbolic planning
    - Low level use sampling based planning, including RRT, RRTConnect, KPIECE etc.
3. [Path planning and obstacle avoidance approaches for robot arm](https://ieeexplore.ieee.org/document/8105619)
    - Use of Non Uniform Rational B-splines to make the path more smooth. 
