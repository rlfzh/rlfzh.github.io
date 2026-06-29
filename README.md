# Ghilmo Choi

I am an undergraduate student in Mechanical Engineering at Korea Aerospace University, expected to graduate in February 2027.

My interests are autonomous driving, mobile robotics, robotic perception, and vision-language models. I am especially interested in connecting perception, localization, planning, and decision making into systems that work on real vehicles and mobile robots.

- Portfolio: <https://rlfzh.github.io/>
- CV: <https://rlfzh.github.io/assets/cv_ghilmo_choi.pdf>
- Email: <ggghilmo@naver.com>

## Selected Projects

### On-device VLM-based Robotic Mission Execution

Developed a natural-language mission execution framework for a ROS2-based UGV platform that converts human commands into executable robot behaviors.

In this framework, an on-device VLM generates high-level plans as pseudo-function sequences such as move, pick, place, search, and return-to-base. The robot grounds these plans using RTAB-Map-based visual SLAM, object detection, and structured world-state representations.

The system combines:

- On-device VLM planner
- Actor-Guard-Critic validation for hallucination-aware planning
- RTAB-Map-based visual SLAM
- Object detection and structured world states
- ROS2/Nav2 control for real-robot language-to-motion execution
- AirSim-based object detection, 3D reconstruction, and path generation

To reduce infeasible or hallucinated actions, I designed an Actor-Guard-Critic validation loop. The Guard filters rule-violating plans, and the Critic checks contextual consistency before execution or replanning. The validated plan is then connected to ROS2/Nav2-based motion execution on a UGV platform. This work was accepted to ICCAIS 2025.

Currently extending the framework with AirSim-based perception and planning by applying YOLOE, NanoOWL, and Grounding DINO for object detection on AirSim data, using NVBlox for 3D reconstruction, and generating paths with the OMPL library.

Reference code from the joint project:

- <https://github.com/LeeSeungGyu1026/VlmRobotPlanner>

Demo/results:

- VlmRobotPlanner demo video: <https://rlfzh.github.io/assets/media/on_device_vlm_mission_execution.mp4>

### ERP42 Autonomous Driving and Parking

Worked on a real ERP42 autonomous vehicle platform as a member and later team leader of KAUVOY.

Main components:

- Dual EKF localization using IMU, wheel encoder, and RTK-GPS measurements
- Autonomous parking pipeline with cone perception and parking-space decision
- Hybrid A* path planning under nonholonomic vehicle constraints
- Pure Pursuit-based path tracking
- FSM-based decision-making logic for urban driving scenarios

For localization, I implemented a Dual EKF architecture using ROS robot_localization. A local EKF estimates short-term relative motion from IMU and wheel encoder measurements, while a global EKF incorporates RTK-GPS to correct long-term drift and provide a stable global pose for autonomous driving.

The localization system was evaluated on outdoor vehicle tests and reported in a KSAE 2025 paper, achieving ATE (RMS) of 0.073 m on a one-lap run and 0.146 m after three laps.

Demo/results:

- EKF localization result: <https://rlfzh.github.io/assets/media/ekf_localization.png>
- LIO-SAM campus demo: <https://rlfzh.github.io/assets/media/liosam_campus_demo.mp4>
- Autonomous parking demo: <https://rlfzh.github.io/assets/media/autonomous_parking_demo.mp4>

Project code will be added after repository cleanup.

### Machine Learning Classification and Regression Pipeline

Built classification and regression pipelines for Introduction to Machine Learning course projects.

Methods used:

- Preprocessing and class-imbalance handling
- PCA, LDA, KPCA, and SBS dimensionality reduction
- Baseline classifiers and ensemble methods
- Fully connected neural networks
- Cross validation and model diagnostics

Result:

- 0.915 macro F1 on a 4-class imbalanced classification task

## Publications

- Co-author, "On-Device Vision Language Model Based Natural Language Mission Execution Framework," ICCAIS 2025.
- Co-author, "ROS robot_localization Dual EKF: Verification of Localization Accuracy and Application to Autonomous Driving Path Tracking," KSAE 2025.

## Awards

- 5th Place, Airbus 101 (2026)
- Excellence Award, Drone X AI Marketing Challenge (2026)
- Finalist, College Mobility Innovation Competition (2025)

## Demo Links

- EKF localization result: <https://rlfzh.github.io/assets/media/ekf_localization.png>
- LIO-SAM campus demo: <https://rlfzh.github.io/assets/media/liosam_campus_demo.mp4>
- VlmRobotPlanner demo video: <https://rlfzh.github.io/assets/media/on_device_vlm_mission_execution.mp4>
- Autonomous parking demo: <https://rlfzh.github.io/assets/media/autonomous_parking_demo.mp4>
