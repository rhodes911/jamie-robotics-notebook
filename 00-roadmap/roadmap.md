# Jamie's Complete Robotics Roadmap

This roadmap lays out a structured path from absolute beginner to a job ‑ready robotics engineer. Each phase lists its goal and the key tasks or topics to focus on. The timeline is approximate and assumes consistent study alongside your normal schedule. Adjust the pacing as needed.

---

## Phase 1 — Foundations (Months 0–2)

**Goals:** Build core understanding of robot kinematics, basic AI concepts and the tooling you'll be using throughout this journey.

* **Modern Robotics (Coursera):** Learn coordinate frames, forward/inverse kinematics, Jacobians and trajectory generation.
* **IBM AI Engineering (Coursera):** Master CNNs, object detection and model deployment (e.g. exporting to ONNX for embedded inference).
* **ROS 2 basics:** Get familiar with nodes, topics, publishers/subscribers and the TF2 coordinate transformation library.
* **CoppeliaSim basics:** Experiment with simple mechanisms, cameras and objects; practise creating and moving joints.
* **CAD basics:** Use Fusion 360 or Onshape to sketch, extrude and export STL files. This will enable you to design custom parts later.

---

## Phase 2 — Skill Building (Months 2–5)

**Goals:** Connect the theory to practical projects and start building your core robotic software skills.

* **ROS 2 intermediate:** Learn services, actions, parameters, URDF robot description files, RViz visualisation and ros2_control.
* **Simulated arm project:** Build a 6‑DOF arm in CoppeliaSim that roughly matches your Yahboom arm. Add a virtual camera and create a simple workspace on your desk dimensions (43 × 104 cm).
* **Perception model project:** Train a basic computer vision model to recognise simple features (colours, shapes or objects) and export it to ONNX.
* **CAD level‑up:** Design simple grippers, trays or mounts. Focus on tolerances and assembly constraints so your parts fit together when printed.

---

## Phase 3 — Robot Arrival (Weeks 1‑4 after delivery)

**Goals:** Set up the Yahboom arm using only your own code and integrate it with ROS 2.

* **Assembly:** Build the mechanical arm following the manual but ignore the vendor software. Ensure wiring and servo mounting are correct.
* **Ubuntu 22.04 setup:** Flash a clean OS onto the Pi 5; enable the UART and confirm serial communication with the servo controller board.
* **Low‑level driver:** Write a Python library (`dofbot.py`) that sends serial commands to individual servos. Expose simple functions such as `set_joint_angle()` and `get_joint_angle()`.
* **ROS 2 driver stack:** Create a package with a driver node that wraps your library. Publish joint states, subscribe to joint commands, and serve a URDF description for RViz.
* **Digital twin:** Build a matching CoppeliaSim model using the same link lengths and joint limits. Visualise the real and simulated robots side by side.

---

## Phase 4 — AI + Perception (Months 5–7)

**Goals:** Give the robot eyes and simple decision‑making.

* **Camera pipeline:** Publish images from the Pi camera as ROS 2 topics. Calibrate the camera's position relative to the arm.
* **AI inference node:** Load your perception model on the Pi 5 (ONNX runtime or PyTorch). Subscribe to the camera topic and publish detections or target poses.
* **Grasping logic:** Implement a node that reads detection output, computes an approximate pick point, plans a simple trajectory and controls the arm to pick and place objects.
* **3D‑printed upgrades:** Design and print new gripper fingers, a wrist‑mounted camera holder and a heavier base. Test these upgrades on your arm.

---

## Phase 5 — Advanced Robotics (Months 7–10)

**Goals:** Move towards industry‑level robotics expertise.

* **MoveIt 2 integration:** Use MoveIt 2 for inverse kinematics, motion planning and collision avoidance. Implement a pick‑and‑place pipeline.
* **Major upgrades:** Design a full upgrade kit. Experiment with different gripper types, wrist cameras and desk fixtures to improve stability and performance.
* **Advanced perception or RL:** Tackle a reinforcement learning project (e.g. training an RL agent to grasp objects) or an advanced perception task (e.g. pose estimation). Start in simulation and transfer to the real arm.

---

## Phase 6 — Portfolio & Jobs (Months 10–12)

**Goals:** Consolidate your work into a professional portfolio and start applying for robotics roles.

* **Record demos:** Capture videos of the robot performing tasks (sorting, following objects, drawing, stacking) and include them in your portfolio.
* **Publish separate code repositories:** Break out your ROS 2 driver, description, control stack, AI models, CAD designs and simulation scenes into their own public repositories.
* **Robotics CV:** Write a CV highlighting your AI skills, robotics math, ROS 2 experience, simulation work, CAD/3D printing and real hardware projects.
* **Job applications:** Track positions, deadlines and outcomes. Apply for roles such as robotics software engineer, manipulation developer, perception engineer and AI robotics engineer.

---

## Notes & Ideas

Use this section to jot down ideas, potential experiments, or anything else that doesn't fit neatly into a specific phase.

* Additional sensors to explore: force sensors, IMUs, tactile sensors.
* Multi‑robot coordination (two arms or mobile base + arm).
* Integration with large language models for natural language control.
* Offloading heavy computation to a desktop or cloud machine.
