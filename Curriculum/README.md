# Intro to Robotics — Course Overview

> An Edge AI Robotics course built on the Arduino UNO Q dual-brain platform with Arduino Modulino sensors.

---

## About This Course

**Intro to Robotics** is a 36-week, project-based introduction to robotics, computer vision, edge machine learning, and autonomous systems. Students build mobile robots that perceive, decide, and act — running real AI models on-device, not in the cloud.

The course leverages the Arduino UNO Q's unique dual-brain architecture: a real-time microcontroller (MCU) for motor and sensor control, and a Linux-capable Qualcomm QRB2210 MPU for computer vision, ML inference, and networking. Standardized Arduino Modulino sensors plug in via I2C — no soldering, fast setup, more time spent on systems integration.

**Hardware:** Arduino UNO Q + Modulino sensors + robot chassis &nbsp;·&nbsp; **Languages:** C++ (MCU), Python (MPU) &nbsp;·&nbsp; **Workflow:** Git + GitHub Actions + Sensai AI

For the complete framework, see the [Edge AI Robotics Curriculum Proposal](./Edge_AI_Robotics_Curriculum.md).

---

## Learning Outcomes

Upon completing this course, students will be able to:

- Build and control a differential-drive mobile robot with closed-loop feedback
- Apply computer vision (OpenCV) for object detection and visual servoing
- Train, deploy, and evaluate edge ML models running on-device
- Design autonomous behaviors using sensor fusion and state machines
- Profile and optimize for real-time latency and power constraints
- Analyze ethical, safety, and societal implications of autonomous AI systems
- Deliver a portfolio-grade capstone project demonstrating end-to-end engineering

---

## Module Map

| Module | Weeks | Topic | Skills | Deliverable |
|--------|-------|-------|--------|-------------|
| [01 — Foundations](./modules/module-01-foundations/README.md) | 1–2 | Safety, GPIO, Modulino I/O | Setup, digitalWrite, digitalRead | I/O demo |
| [02 — Motion](./modules/module-02-motion/README.md) | 3–4 | Motors, PWM, encoders, IMU | Closed-loop drive | Stable driving |
| [03 — Sensing](./modules/module-03-sensing/README.md) | 5–6 | Range / ToF sensing, obstacle avoidance | I2C, sensor reads | Avoidance demo |
| [04 — Odometry & MPU](./modules/module-04-odometry/README.md) | 7–8 | Pose estimation, Linux MPU intro | IMU + encoders, SSH, Python | Path tracking |
| [05 — Computer Vision](./modules/module-05-vision/README.md) | 9–12 | Camera, OpenCV, perception-action | Image processing, vision-driven motion | Integrated demo |
| [06 — Edge ML](./modules/module-06-edge-ml/README.md) | 13–17 | Datasets, training, on-device inference | TFLite, model deployment | Inference demo |
| [07 — Midterm](./modules/module-07-midterm/README.md) | 18 | Reactive AI Robot | System integration | Midterm project |
| [08 — Autonomy](./modules/module-08-autonomy/README.md) | 19–24 | State machines, sensor fusion, object detection, recovery | Autonomous design | Robust autonomy |
| [09 — Optimization](./modules/module-09-optimization/README.md) | 25–28 | Telemetry, latency, power, responsible AI | Profiling, ethics | Performance report |
| [10 — Capstone](./modules/module-10-capstone/README.md) | 29–36 | Autonomous Edge-AI Robot | End-to-end engineering | Capstone demo |

---

## Required Hardware Kit (Standard, 3–4 Students)

- Arduino UNO Q
- Differential-drive robot chassis
- Motor driver and encoder motors
- Arduino Modulino Movement (IMU)
- Arduino Modulino Distance Range / ToF
- Arduino Modulino Buttons
- Arduino Modulino LEDs
- USB camera
- USB microphone
- Battery, power regulation, cabling

A 1:1 device ratio kit uses the same components provisioned per student.

---

## Learning Paths

Choose your path when you open your Learning Contract:

| Path | Name | Who It's For | What You Build |
|------|------|-------------|----------------|
| **A** | Guided | New learners | Follow each module's reference robot and tests |
| **B** | Explorer | Self-directed | Design an original autonomous behavior using the same hardware |
| **C** | Expert | Advanced | Submit PRs improving the curriculum, prompts, or test suites |

---

## Student Checklist (Per Module)

- [ ] Open a Learning Contract issue in the class repo
- [ ] Pull the latest starter code from the module's `starter-code/` directory
- [ ] Wire the required Modulino sensors per the module README
- [ ] Implement the TODOs in the starter code
- [ ] Pass the AutoGrader by `git push`
- [ ] Review 2 peers' Pull Requests
- [ ] Add a resource to `community-resources/`
- [ ] Open your PR and wait for peer + teacher review

---

## Grading

Each module is worth **100 points**:

| Component | Points | What It Checks |
|-----------|--------|----------------|
| Learning Contract | 25 | `learning-contract.md` exists and is complete |
| Implementation Mastery | 50 | Code passes all AutoGrader tests |
| Community Contribution | 25 | A `.md` file added to `community-resources/` |

Passing all three components makes you **credential-eligible** for a Sensai workforce micro-credential mapped to CSTA AI Learning Priorities and AI4K12 Five Big Ideas.

---

## Standards Alignment

This course aligns with:

- **CSTA AI Learning Priorities** — Perception, Representation, Learning, Natural Interaction, Societal Impact
- **AI4K12 Five Big Ideas** — Perception, Representation & Reasoning, Learning, Natural Interaction, Societal Impact
- **Industry 4.0 / Workforce Frameworks** — robotics, embedded AI, automation technician pathways

---

## Course Structure

```text
Courses/Intro to Robotics/
├── README.md                              # This file
├── Edge_AI_Robotics_Curriculum.md         # Full curriculum proposal (reference)
└── modules/
    ├── module-01-foundations/             # Safety, GPIO, Modulino I/O
    │   ├── README.md
    │   ├── starter-code/
    │   │   └── modulino_io.ino
    │   └── tests/
    │       └── test_sketch.py
    ├── module-02-motion/                  # Motors, PWM, encoders, IMU
    ├── module-03-sensing/                 # Distance/ToF sensing
    ├── module-04-odometry/                # Pose estimation, MPU intro
    ├── module-05-vision/                  # Camera, OpenCV
    ├── module-06-edge-ml/                 # Datasets, inference
    ├── module-07-midterm/                 # Reactive AI Robot
    ├── module-08-autonomy/                # State machines, fusion, recovery
    ├── module-09-optimization/            # Telemetry, latency, ethics
    └── module-10-capstone/                # Final autonomous robot
```

---

## Contributing to This Course (Path C)

All improvements go through the standard PR + peer review process.

| Contribution Type | Where | Example |
|-------------------|-------|---------|
| Fix a bug or typo | `Courses/Intro to Robotics/modules/` | Correct a wiring diagram or pin map |
| Add a test case | `modules/*/tests/` | Validate encoder reading edge cases |
| Improve resources | `community-resources/` | Curated Modulino tutorial or ML guide |
| **Improve AI prompts** | `.github/prompts/` | Better explanations for vision pipeline failures |
| **Add a starter sketch** | `modules/*/starter-code/` | Reference implementation for a behavior |

---

> Back to [Curriculum Master](../../README.md)
