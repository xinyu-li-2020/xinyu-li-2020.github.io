---
permalink: /
title: "About Me"
excerpt: "About me"
description: "I am Changhao Wang, a fifth-year Ph.D. student at UC Berkeley. I obtained my bachelor degree at Shanghai Jiao Tong University(SJTU) in 2018."
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a fifth-year Ph.D. student at [UC Berkeley](https://www.berkeley.edu){:target="_blank"} advised by [Prof. Masayoshi Tomizuka](http://www.me.berkeley.edu/people/faculty/masayoshi-tomizuka){:target="_blank"}. My research interest lies in the interdisciplinary combination of robotics, optimization, reinforcement learning and control theories with applications to **robotic manipulation** and **motion planning**, and **robot skill learning**.

Here is my [Curriculum Vitae](/files/CV_Changhao.pdf){:target="_blank"} (Updated in Aug 2022).

## Recent Updates

- May 2022: I begin my intern(resident) at (Google) X, the Moonshot Factory on the Everyday Robots project.
- May 2022: Paper: Safe Online Gain Optimization for Cartesian Space Variable Impedance Control accepted by CASE 2022
- Feb 2022: Paper: Offline-Online Learning of Deformation Model for Cable Manipulation With Graph Neural Networks accepted by IEEE Robotics and Automation Letters (RA-L).
- Feb 2022: Paper: Robotic cable routing with spatial representation accepted by IEEE Robotics and Automation Letters (RA-L).
- Jan 2022: Paper: Learning Insertion Primitives with Discrete-Continuous Hybrid Action Space for Robotic Assembly Tasks accepted by ICRA 2022
- Jan 2022: Paper: BPOMP: A Bilevel Path Optimization Formulation for Motion Planning  accepted by ACC 2022
- June 2021: Paper: Trajectory Splitting: A Distributed Formulation for Collision Avoiding Trajectory Optimization accepted by IROS 2021.
- June 2021: Paper: Online Learning of Unknown Dynamics for Model-Based Controllers in Legged Locomotion accepted by IEEE Robotics and Automation Letters (RA-L).
- Jan 2021: Paper: Contact Pose Identification for Peg-in-hole Assembly under Uncertainties accepted by ACC 2020.
- May 2020: I begin my robotics research intern at (Google) X, the Moonshot Factory.
- June 2019: Paper: Robust Deformation Model Approximation for Robotic Cable Manipulation accepted by IROS 2019.
- June 2019: I begin my robotics reserach intern at FANUC Advanced Reserach Laboratory.
- July 2018: Paper: A Framework for Manipulating Deformable Linear Objects by Coherent Point Drift accepted by IEEE Robotics and Automation Letters (RA-L).

## Education

- **Ph.D. Mechanical Engineering, UC Berkeley (Berkeley, CA), 2018 - 2023 (Expected)**

    - Major: Controls　　　　　　　　Minors: Optimization, Robotics
    - GPA: 4.0/4.0 　　　　　　　　　Advisor: Prof. Masayoshi Tomizuka
    - Research Interest: Robotics Manipulation, Motion Planning. 

- **B.S. Mechanical Engineering, Shanghai Jiao Tong University (Shanghai, China), 2014 - 2018**

    - Thesis: Vision-based Object Classification and Size Detection for Robotic Manipulation
    - Advisor:  [Prof. Ye Ding](http://me.sjtu.edu.cn/teacher_directory1/dinghua.html){:target="_blank"}, [Prof. Xinjun Sheng](http://me.sjtu.edu.cn/teacher_directory1/shengxinjun.html){:target="_blank"}

## Work Experience
- **Resident**, (Google) X, the Moonshot Factory (Mountain View, CA), May 2022 - August 2022
- **Robotics Research Intern**, (Google) X, the Moonshot Factory (Remote), May 2020 - August 2020
- **Robotics Research Intern**, FANUC Advanced Research Laboratory (Union City, CA), June 2019 - August 2019


## Representative Publications

### Offline-Online Learning of Deformation Model for Cable Manipulation with Graph Neural Networks \[[Website](https://msc.berkeley.edu/research/deformable-GNN.html)\]
<p align="center">
<img src="/images/deformable_GNN.jpg" width="700">
</p>
Manipulating deformable objects by robots has a wide range of applications, e.g.,  manufacturing and medical surgery. To complete such tasks, an accurate dynamics model for predicting the deformation is critical for robust control. In this work, we deal with this challenge by proposing a hybrid offline-online method to learn the dynamics of deformable objects in a data-efficient manner. In the offline phase, we adopt Graph Neural Network (GNN) to learn the deformation dynamics purely from the simulation data. Then an online local residual model is learned to resolve the sim-to-real gap in order to achieve better accuracy and generalizability. The learned model is then utilized as the dynamics constraint of a Model Predictive Controller (MPC) to calculate the optimal robot movements. The online learning and MPC run in a closed-loop manner to robustly accomplish the task. Comparative results with existing methods are provided to show the effectiveness and robustness quantitatively.

### Safe Online Gain Optimization for Variable Impedance Control \[[Website](https://msc.berkeley.edu/research/safe-ongo-vic.html)\]
<p align="center">
<iframe src="https://www.youtube.com/embed/T6KEq6VmpLg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>
Smooth behaviors are preferable for many contact-rich manipulation tasks. Impedance control arises as an effective way to regulate robot movements by mimicking a mass-spring-damping system. Consequently, the robot behavior can be determined by the impedance gains. However, tuning the impedance gains for different tasks is tricky, especially for unstructured environments. Moreover, online adapting the optimal gains to meet the time-varying performance index is even more challenging. In this paper, we present Safe Online Gain Optimization for Variable Impedance Control (Safe OnGO-VIC). By reformulating the dynamics of impedance control as a control-affine system, in which the impedance gains are the inputs, we provide a novel perspective to understand variable impedance control. Additionally, we innovatively formulate an optimization problem with online collected force information to obtain the optimal impedance gains in real-time. Safety constraints are also embedded in the proposed framework to avoid unwanted collisions.

### Trajectory Splitting: A Distributed Formulation for Collision Avoiding Trajectory Optimization   
<p align="center">
<img src="/images/trajsplit.jpg" width="700">
</p>
Efficient trajectory optimization is essential for avoiding collisions in unstructured environments, but it remains challenging to have both speed and quality in the solutions. One reason is that second-order optimality requires calculating Hessian matrices that can grow with $O(N^2)$ with the number of waypoints. Decreasing the waypoints can quadratically decrease computation time. Unfortunately, fewer waypoints result in lower quality trajectories that may not avoid the collision. To have both, dense waypoints and reduced computation time, we took inspiration from recent studies on consensus optimization and propose a distributed formulation of collocated trajectory optimization. It breaks a long trajectory into several segments, where each segment becomes a subproblem of a few waypoints. These subproblems are solved classically, but in parallel, and the solutions are fused into a single trajectory with a consensus constraint that enforces continuity of the segments through a consensus update. With this scheme, the quadratic complexity is distributed to each segment and enables solving for higher-quality trajectories with denser waypoints. Furthermore, the proposed formulation is amenable to using any existing trajectory optimizer for solving the subproblems. 

### Online Learning of Unknown Dynamics for Model-Based Controllers in Legged Locomotion
<p align="center">
<img src="/images/leg_robot.jpg" width="700">
</p>
The performance of a model-based controller can severely suffer when its model inaccurately represents the real world dynamics. We propose to learn a time-varying, locally linear residual model along the robot's current trajectory, to compensate for the prediction errors of the controller's model. Supervised learning is performed online, as the robot is running in the unknown environment, using data collected from its immediate past. We theoretically investigate our method in its general formulation, then apply it to a bipedal controller derived from the full-order dynamics of virtual constraints, and a quadrupedal controller derived from a simplified model of contact forces. For a biped in simulation, our method consistently outperforms the baseline and a recent learning-based method. We also experiment with a 12\,kg quadruped in simulation and real world, where the baseline fails to walk with 10\,kg of payload but our method succeeds.

### BPOMP: A Bilevel Path Optimization Formulation for Motion Planning \[[Website](https://changhaowang.github.io/BPOMP/BPOMP.html)\]
<p align="center">
<img src="/images/BPOMP.jpg" width="700">
</p>
Balancing computation efficiency and success rate is challenging for path optimization. To obtain a collision-free path, each waypoint along the path should be collision-free, and the waypoints should be dense. As a consequence, the solutions are computationally expensive to obtain. This paper introduces a bilevel path optimization formulation for motion planning (BPOMP). Different from standard formulations that only consider the collision on each waypoint, BPOMP additionally constraints the closest position to the obstacle along the continuous path. Intuitively, if the closest position is out of collision, the entire path should be collision-free. The problem is formulated as a bilevel optimization and then relaxed to canonical nonlinear programming (NLP), which can be solved classically.

### Robotic Bottle Filpping and Landing with TRPO and Adaptive MPC
<p align="center">
<img src="/images/demo_video_reduce_size.gif" width="700">
</p>
Robotic bottle filpping is a challenging task. Since the dynamics of the bottle is hard to model in the presence of noise and uncertainties, and the bottle flipping skills is hard to learn. We proposed a framework combining the Trust Region Policy Optimization (TRPO) to let the robot learn the bottle flipping skills with an Adaptive MPC controller to stablize the bottle. The trajectory of the bottle is predicted by an three layers LSTM network. Simulation results show that this framework is able to let the robots finish the task robustly.

### Robotic Deformable Object Manipulation

<p align="center">
<img src="/images/cable_manipulation.jpg" width="700">
</p>

Manipulation of deformable objects is a challenging task for robots. These objects have infinite-dimensional configuration space and are computational-expensive to model, making it difficult for real-time tracking, planning and control. To deal with these challenges, we proposed two different model-free methods: 

- Learning from demonstration based on coherent point drift. \[[paper](/files/rope_framework.pdf){:target="_blank"}\] \[[website](https://me.berkeley.edu/~tetang/RAL2018/RopeManipulation.html){:target="_blank"}\]

- SPR-RWLS for online deformation model approximation. \[paper\] \[[website](https://changhaowang.github.io/IROS2019/SPRRWLS){:target="_blank"}\] \[[presentation](/files/CW_SPR_RWLS_Group_Meeting.pdf){:target="_blank"}\]