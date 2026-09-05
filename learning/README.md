# Learning Physical AI

A curated learning map for people who want to build robots, autonomous systems, and embodied AI systems that perceive, reason, and act in the physical world.

This is not intended to be an exhaustive syllabus. The goal is to point to durable, high-signal resources and show how the pieces fit together into practical career paths.

## How to use this guide

You do not need to master every topic before building something. Pick a target role, learn the foundations that role repeatedly depends on, and turn each stage into a working project.

A useful loop is:

`learn a concept -> implement it -> test it in simulation or hardware -> document the result -> compare your skills with real job descriptions`

## Choose a path

### Robotics Software Engineer

A practical sequence:

`Python/C++ -> Linux -> ROS 2 -> kinematics -> motion planning -> manipulation/navigation -> portfolio project`

Focus on software architecture, debugging distributed robot systems, sensor and actuator interfaces, real-time constraints, and reproducible deployments.

### Perception and Autonomy Engineer

A practical sequence:

`linear algebra -> Python/C++ -> computer vision -> PyTorch -> 3D geometry -> state estimation -> mapping/localization -> autonomy project`

Focus on turning camera, LiDAR, radar, and other sensor data into reliable world models and decisions.

### Controls and Motion Engineer

A practical sequence:

`linear algebra/calculus -> dynamics -> feedback control -> state estimation -> trajectory optimization -> MPC -> simulated or hardware controller`

Focus on making physical systems move accurately, safely, and robustly under uncertainty.

### Robot Learning / Embodied AI Engineer

A practical sequence:

`Python -> PyTorch -> robotics fundamentals -> imitation learning -> reinforcement learning -> robot datasets -> simulation -> real or simulated policy deployment`

Focus on learning behaviors from demonstrations, interaction, and large multimodal datasets while retaining enough classical robotics knowledge to understand the physical system.

### Simulation and Validation Engineer

A practical sequence:

`robotics fundamentals -> physics simulation -> ROS 2 -> sensors -> scenario generation -> automated evaluation -> sim-to-real considerations`

Focus on building repeatable environments where robot and autonomy software can be developed, tested, benchmarked, and validated safely.

## Foundations

- [Python Tutorial](https://docs.python.org/3/tutorial/) - Official Python introduction and language reference path.
- [cppreference](https://en.cppreference.com/) - Comprehensive C++ language and standard-library reference.
- [MIT 18.06 Linear Algebra](https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/) - Gilbert Strang's foundational linear algebra course through MIT OpenCourseWare.
- [Modern Robotics](https://hades.mech.northwestern.edu/index.php/Modern_Robotics) - Free textbook materials and courses covering kinematics, dynamics, motion planning, control, manipulation, and mobile robotics.

## Core Robotics

- [Modern Robotics](https://hades.mech.northwestern.edu/index.php/Modern_Robotics) - Strong structured foundation for robot motion, kinematics, dynamics, planning, and control.
- [ROS 2 Tutorials](https://docs.ros.org/en/lyrical/Tutorials.html) - Official step-by-step learning path for nodes, topics, services, actions, parameters, launch files, and ROS 2 development.
- [MoveIt 2 Tutorials](https://moveit.picknik.ai/main/doc/tutorials/tutorials.html) - Official tutorials for robot motion planning, collision-aware planning, and manipulation with MoveIt 2.
- [Underactuated Robotics](https://underactuated.csail.mit.edu/) - MIT course notes on nonlinear dynamics, control, locomotion, manipulation, and optimization for complex robotic systems.

## Perception and Autonomy

- [Stanford CS231n](https://cs231n.stanford.edu/) - Deep learning for computer vision with strong foundations in modern visual recognition systems.
- [OpenCV Tutorials](https://docs.opencv.org/4.x/d9/df8/tutorial_root.html) - Official practical tutorials for image processing, feature extraction, calibration, geometry, and vision pipelines.
- [PyTorch Tutorials](https://docs.pytorch.org/tutorials/) - Official hands-on guides for building, training, debugging, and deploying neural networks.

After these foundations, move into 3D geometry, camera calibration, point clouds, state estimation, sensor fusion, SLAM, mapping, and localization through projects that combine multiple sensors rather than treating perception as image classification alone.

## Controls and Motion

- [Modern Robotics - Motion Planning and Control](https://hades.mech.northwestern.edu/index.php/Modern_Robotics) - Covers planning, feedback control, force control, and mobile manipulation within a unified robotics curriculum.
- [Underactuated Robotics](https://underactuated.csail.mit.edu/) - Goes deeper into nonlinear control, trajectory optimization, model-predictive control, and dynamic systems.
- [Drake](https://drake.mit.edu/) - Open-source toolbox from the MIT robotics community for model-based design, optimization, planning, and control.

A good controls project should expose the dynamics you are controlling, the objective, the constraints, and quantitative results such as tracking error, stability, or robustness under disturbances.

## Robot Learning and Embodied AI

- [Hugging Face Robotics Course](https://huggingface.co/learn/robotics-course/en/unit0/1) - Free course connecting classical robotics with modern learning-based robotics and LeRobot.
- [LeRobot](https://github.com/huggingface/lerobot) - Open-source toolkit for robot datasets, policies, training, and deployment on supported real robotic platforms.
- [UC Berkeley CS 285](https://www2.eecs.berkeley.edu/Courses/CS285/) - Deep reinforcement learning, decision making, imitation learning, model-based RL, and control.
- [PyTorch Tutorials](https://docs.pytorch.org/tutorials/) - Practical foundation for implementing and training learning-based policies and perception models.
- [Isaac Lab](https://isaac-sim.github.io/IsaacLab/) - Open-source framework for robot learning and reinforcement learning on NVIDIA Isaac Sim.
- [MuJoCo](https://mujoco.org/) - Physics engine widely used for control, reinforcement learning, manipulation, and embodied AI research.

Do not skip classical robotics entirely when studying embodied AI. Understanding kinematics, dynamics, control, sensing, and failure modes makes it much easier to diagnose whether a learned policy is solving the intended physical problem.

## Simulation and Validation

- [Gazebo](https://gazebosim.org/) - Open-source simulator for robots, sensors, environments, and ROS-based systems.
- [Isaac Lab](https://isaac-sim.github.io/IsaacLab/) - Robot-learning and simulation framework built on NVIDIA Isaac Sim.
- [MuJoCo](https://mujoco.org/) - Fast physics simulation for control and robot-learning experiments.
- [Webots](https://cyberbotics.com/) - General-purpose open-source robot simulator with many robot and sensor models.

When learning simulation, avoid stopping at a visually impressive scene. Build automated scenarios, measurable success criteria, deterministic seeds where appropriate, and failure cases that reveal weaknesses in the autonomy stack.

## Projects that build job-ready evidence

A strong portfolio project demonstrates system thinking rather than just following a tutorial. Good examples include:

- Build a ROS 2 mobile robot in simulation with mapping, localization, path planning, and obstacle avoidance.
- Implement a manipulator pick-and-place task using MoveIt 2, including collision objects and recovery from failed plans.
- Build a camera perception pipeline that calibrates a camera, detects or segments objects, estimates geometry, and publishes usable robot-frame outputs.
- Implement and compare two controllers for the same dynamic system, then report tracking error and behavior under disturbances.
- Train an imitation-learning policy on a small robot dataset and evaluate it across held-out initial conditions.
- Create a simulation benchmark with automated success metrics for an autonomy or manipulation task.
- Connect a real sensor or low-cost robot to ROS 2 and document latency, calibration, failure modes, and deployment steps.

## Portfolio checklist

For each serious project, include:

- A concise README explaining the physical problem and why it matters.
- An architecture diagram showing sensors, software components, models, and actuators.
- Reproducible setup and run instructions.
- A short video or visual demonstration.
- Quantitative evaluation, not only screenshots.
- Failure cases and what you learned from them.
- A clear explanation of which parts you implemented yourself.

A small number of complete, measurable projects is usually more convincing than many tutorial clones.

## Learn from real job descriptions

Use current Physical AI job descriptions as a living curriculum. Look for skills that repeatedly appear across roles you want, then prioritize the gaps that show up most often.

[Browse current Physical AI roles](https://www.physicalai.jobs/jobs) and compare their requirements with the learning paths above.

## Contributing learning resources

High-quality additions are welcome. Prefer official course materials, university resources, project documentation, substantial open-source curricula, and resources that teach transferable concepts.

Avoid thin SEO articles, referral links, generic AI courses with little connection to physical systems, and large collections that add quantity without a clear learning purpose. See the repository's [Contribution Guidelines](../CONTRIBUTING.md).
