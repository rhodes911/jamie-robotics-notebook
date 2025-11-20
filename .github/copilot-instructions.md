# Repository Custom Instructions for GitHub Copilot

These instructions help GitHub Copilot understand the structure, purpose and conventions of this repository so it can generate meaningful suggestions. They apply whenever the Copilot agent interacts with files in this repo.

## Project overview
This repository is a personal robotics engineering notebook. It documents the journey from beginner to competent robotics engineer, covering theory (Modern Robotics, IBM AI Engineering), software development with ROS 2, simulation with CoppeliaSim, real hardware bring‑up with a Raspberry Pi 5‑driven 6‑DOF arm, CAD and 3D printing, AI perception and reinforcement learning, and career preparation.

## Tech stack
- **Programming language:** Python 3
- **Robotics middleware:** ROS 2 (Humble or later)
- **Simulation:** CoppeliaSim
- **CAD:** Fusion 360 or Onshape
- **AI/ML:** PyTorch, ONNX
- **Hardware:** Raspberry Pi 5, Yahboom 6‑DOF robot arm, Pi camera
- **Documentation:** Markdown

## Coding and documentation guidelines
- Use Markdown for all notes and documentation.
- Keep paragraphs short and use bullet lists or tables for lists of tasks or resources.
- When creating new files, choose filenames that reflect the phase and topic (e.g. `ros2-basics-notes.md`).
- Include checklists (`[ ]`) to track progress where appropriate.
- Include code snippets fenced in triple backticks.
- Avoid using vendor libraries supplied with the arm; instead build drivers and ROS 2 nodes from scratch.
- When referring to the physical workspace, remember the desk dimensions are 43 cm × 104 cm.

## Project structure
- `00-roadmap/` – outlines the phases of study and high‑level tasks.
- `01-foundations/` – notes from Modern Robotics, IBM AI Engineering and basic tooling (ROS 2, simulation, CAD).
- `02-skill-building/` – intermediate ROS 2, first simulation project, initial perception model, CAD practice.
- `03-robot-arrival/` – bring up the real Yahboom arm using custom drivers, build a digital twin.
- `04-ai-perception/` – camera nodes, AI inference nodes, grasping logic, first 3D‑printed upgrades.
- `05-advanced/` – MoveIt 2 integration, advanced perception or reinforcement learning, major mechanical upgrades.
- `06-portfolio/` – documentation of demos, links to separate code repos, CV drafts and job search notes.

## Resources
- ROS 2 documentation: https://docs.ros.org
- CoppeliaSim user manual: https://www.coppeliarobotics.com
- Modern Robotics book: http://modernrobotics.org
- IBM AI Engineering course on Coursera
- GitHub Copilot custom instructions documentation: refer to GitHub Docs for details.

Provide these details in your responses when appropriate, and favour solutions that align with this structure and tech stack.
