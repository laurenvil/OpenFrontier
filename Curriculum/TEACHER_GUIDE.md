# Intro to Robotics — Teacher's Guide

> Companion to the [course README](./README.md). The README explains the course to **students**; this guide explains it to **teachers**.

---

## 1. Purpose & Audience

- **For:** classroom teachers, lab assistants, PD facilitators, and CTE coordinators preparing to deliver Intro to Robotics.
- **Assumes:** reader has skimmed the [course README](./README.md) and the [Edge AI Robotics Curriculum Proposal](./Edge_AI_Robotics_Curriculum.md).
- **Does not replace:** robot-safety vendor training, district safety policy, or the per-component vendor documentation in each module's `resources.md`.

---

## 2. Course at a Glance

| Item | Value |
|------|-------|
| Grade band | 9–12 (recommended after Intro to IoT or equivalent) |
| Total modules | 10 (spanning 36 weeks) |
| Recommended pacing | Year-long; see Pacing Plans |
| Team size | 3–4 students per UNO Q (default), 1:1 in well-funded settings |
| Primary hardware | Arduino UNO Q + Modulino IMU/Range/Buttons/LEDs + chassis + camera |
| Primary languages | C++ (MCU side), Python (MPU/Linux side) |
| Capstone deliverable | Module 10 — Autonomous Edge-AI Robot |

---

## 3. The Sensai Open Classroom Model in Practice

Same three principles as every Sensai course:

1. **Hands-on learning.** This course is *especially* lab-heavy. Lecture <20%. The robots have to roll.
2. **Real-world workflow.** Git/GitHub PRs with AutoGrader feedback. Students submit *systems*, not just sketches.
3. **Community-driven growth.** Robotics courses generate the most failure stories. Have students write them up — that *is* the community contribution.

### Path A / B / C — Routing Students

| Path | Signal | Default Move |
|------|--------|--------------|
| A — Guided | New to robotics, OK with following recipes | Reference robot first; deviations only after working baseline |
| B — Explorer | Wants to swap parts or design a behavior | Approve Learning Contract variation; require a written safety review of the change |
| C — Expert | Robotics club, FRC/FTC veteran, or repeating | PR on tests/prompts; mentor a Path A team |

Team dynamics matter here — assign roles (driver, perception, autonomy, integration) and rotate them across modules.

---

## 4. Standards Alignment (Course-Level)

- **CSTA AI Learning Priorities** — Perception, Representation, Learning, Natural Interaction, Societal Impact (course-wide)
- **AI4K12 Five Big Ideas** — All five Big Ideas, with emphasis on Perception (BI 1) in Modules 03–05, Learning (BI 3) in Module 06, and Societal Impact (BI 5) in Module 09
- **CSTA K-12 CS Standards** — 3B-CS-01 through 3B-CS-02 (systems), 3B-AP-08 through 3B-AP-22 (algorithms, abstraction, modularity), 3B-NI-04 (networks)
- **NGSS** — HS-ETS1-1 through HS-ETS1-4 (engineering design), HS-PS3 (energy)
- **ISTE Standards for Students** — 1.4 Innovative Designer, 1.5 Computational Thinker, 1.6 Creative Communicator
- **Industry / Workforce** — robotics technician, mechatronics, embedded AI engineer pathways

Each module's `LESSON_PLAN.md` lists specific codes.

---

## 5. Prerequisites

### Student Prerequisites

- **Intro to IoT or equivalent** — students must already know `setup()` / `loop()`, GPIO, and basic Serial debugging
- Basic Python literacy is helpful by Module 04 (MPU side)
- Algebra-level math for Module 04 odometry and Module 06 model accuracy stats

### Teacher Prerequisites

- Comfort with both Arduino C++ *and* Linux command-line Python
- Familiarity with SSH and remote-edit workflows
- Robot safety certification (mechanical pinch hazards, battery handling)
- Ability to debug an OpenCV pipeline at the conceptual level

### Recommended Teacher PD Before Week 1 (24–32 hours, more than Intro to IoT)

1. Walk every module end-to-end. *Especially* Modules 05 (CV) and 06 (Edge ML) — these break in ways the others don't.
2. Pre-stage a known-good robot per kit before students arrive.
3. Run the capstone yourself on a personal kit before week 25.
4. LiPo / battery safety training per district policy.

---

## 6. Equipment & Classroom Setup

### Standard Classroom Kit (3–4 students)

- Arduino UNO Q
- Differential-drive chassis with encoder motors and motor driver
- Modulino Movement (IMU), Distance/ToF, Buttons, LEDs
- USB camera + USB microphone
- LiPo or NiMH battery, regulator, switch
- Cabling, mounting hardware

### Per Classroom

- Charging cabinet for batteries (LiPo-safe bag inside, ideally)
- Open floor space ≥ 3 m × 3 m for driving tests
- Painter's tape and printed AR-tag markers for navigation tasks
- "Crash mat" or low foam border to prevent robots driving off tables
- Fast Wi-Fi; outbound HTTPS to GitHub, model registries

### Software

- Arduino CLI 1.4.1+ for MCU side
- Python 3.11+, OpenCV 4.x, NumPy on UNO Q MPU and on teacher laptop
- Edge ML toolchain per Module 06 (TFLite Micro or equivalent)
- GitHub Desktop or `git` CLI

---

## 7. Pacing Plans

### Plan A — Full Year (36 weeks)

| Weeks | Module |
|-------|--------|
| 1–2 | 01 — Foundations |
| 3–4 | 02 — Motion |
| 5–6 | 03 — Sensing |
| 7–8 | 04 — Odometry & MPU |
| 9–12 | 05 — Computer Vision |
| 13–17 | 06 — Edge ML |
| 18 | 07 — Midterm |
| 19–24 | 08 — Autonomy |
| 25–28 | 09 — Optimization |
| 29–36 | 10 — Capstone |

This matches the Edge_AI_Robotics_Curriculum.md scope and sequence.

### Plan B — Semester (18 weeks, double block ~85 min)

Compress Modules 01–04 into 4 weeks, 05–06 into 5 weeks, 07–09 into 4 weeks, 10 into 5 weeks. Drop the optimization deep-dive — touch ethics only.

### Plan C — Two-Year Pathway

Year 1: Modules 01–06 + Midterm. Year 2: Modules 08–10 + advanced electives.

---

## 8. Assessment Philosophy

The AutoGrader handles 50/100 on each module. Your job: Learning Contracts (25), community contributions (25), and the soft skills outside the 100.

### Holistic 4-Point Rubric (Soft Factors)

| Level | What it looks like |
|-------|--------------------|
| 4 — Exemplary | Diagnoses team failures; pushes a Path C PR; presents under pressure |
| 3 — Proficient | Completes module on time; participates in peer review |
| 2 — Developing | Needs teacher prompts; peer review is shallow |
| 1 — Beginning | Significant scaffolding required |

### Capstone Rubric (Module 10)

Use the seven categories from `Edge_AI_Robotics_Curriculum.md` Appendix D:

1. Technical functionality
2. Modulino integration
3. On-device AI/vision
4. Autonomy
5. Robustness
6. Ethics & safety
7. Technical documentation

Each scored 1–4. Total /28 (mapped back to /100 for the gradebook).

---

## 9. Safety

### Mechanical

- **Hair tied back, no loose sleeves** during driving tests
- Robots **always** powered down before reaching into the chassis
- "Driver / Spotter" rule: two people present whenever a robot is driving
- Set an arena boundary — painter's tape on the floor

### Electrical / Battery

- **LiPo safe bag** for storage. Never leave charging unattended.
- Inspect cells before every charge. Swollen cell = dispose per district policy.
- Use a balance charger, not a wall-wart.

### Vision / Privacy

- The cameras are *on*. Students should know they're being recorded if they're in frame.
- Don't commit training images that contain identifiable students' faces.
- Anonymize datasets before pushing to GitHub.

---

## 10. Differentiation & Inclusion

### IEPs/504s

- Team-based work distributes load naturally. Assign students roles matched to strengths.
- Path A's reference robot is fully buildable without independent design decisions.

### English Learners

- The Linux/MPU side (Module 04+) is heavy on English error messages. Encourage Sensai-translated explanations.

### Advanced students

- Move to Path B by Module 03. By Module 05, they should be remixing the perception pipeline.
- Path C: contributions to Modulino driver libraries or computer-vision tutorials in `community-resources/`.

---

## 11. Module-by-Module Teacher Notes

Detailed notes live in each module's [`LESSON_PLAN.md`](./modules). Read each lesson plan before the period.

- **01 Foundations** — Establish the safety contract today. Don't let a robot move until the contract is signed.
- **02 Motion** — Encoder polarity is the most common bug. Test reverse first.
- **03 Sensing** — ToF range sensors lie at < 50 mm. Calibrate.
- **04 Odometry & MPU** — First Linux/Python module. Plan extra time for SSH setup.
- **05 Computer Vision** — Lighting kills CV. Use the same lab lighting for training and testing.
- **06 Edge ML** — Dataset bias = robot bias. Make this explicit.
- **07 Midterm** — Real-world deadline practice. Treat it like a sprint review.
- **08 Autonomy** — State machines on a whiteboard *before* code. Insist on this.
- **09 Optimization** — Ethics module is real, not filler. Use real news stories from this month.
- **10 Capstone** — See the **Capstone Playbook** below.

---

## 12. Common Pitfalls (Course-Wide)

| Pitfall | First Move |
|---------|------------|
| Robot drives in circles | Encoder polarity or motor wiring — flip one motor's leads |
| ToF sensor reads 0 | Within minimum range — back off ≥ 50 mm |
| OpenCV pipeline freezes | Dropped USB frame — wrap reads in try/except + log |
| ML model accuracy collapses in classroom | Training images had different lighting — re-shoot in the test environment |
| LiPo won't charge | Cell over-discharged below 3.0 V — dispose, do not revive |
| Team can't agree on a behavior | Force a written architecture decision in the Learning Contract before coding |

---

## 13. Working with the Sensai AI

Same posture as every Sensai course: model good prompts.

### Robotics-specific Sensai prompts to model

- *"Explain why my encoder count goes negative when I drive forward."*
- *"Help me design a state machine for 'find ball, push ball, return home.'"*
- *"What's likely wrong if my model is 95% accurate at training but 50% in the classroom?"*

### Redirect

- *"Write the autonomy code for me."* — Ask for the state diagram first.
- *"What hyperparameters should I use?"* — Push the student to reason about the trade-off Sensai cites.

---

## 14. Capstone Playbook (Module 10)

The Autonomous Edge-AI Robot is the showcase. Recommendations:

1. **Demo arena** set up a full week before showcase day so teams practice on it.
2. **Three-judge panel** — at least one outside guest (industry, parent, district administrator).
3. **Rubric posted** so teams self-assess on the seven categories before they present.
4. **Failure recovery** counts. Award teams that diagnose live failures.
5. **Documentation deliverable** matters as much as the demo — judges read the README.

---

## 15. Family Communication

Before week 1:

- Robotics involves real physical objects. Students will operate moving hardware under supervision.
- Cameras and microphones are part of the build. Privacy norms apply.
- Battery handling is a real safety topic — students will be trained.
- Year-long course; expected commitment outside class is ~1 hour/week for the first half, ~2 hours/week during the capstone.

---

## 16. Troubleshooting & Escalation

| Symptom | First Move | Escalate If… |
|---------|-----------|--------------|
| UNO Q MPU unreachable via SSH | Power-cycle and check IP — confirm Wi-Fi association | Reachable but `arduino` user can't log in — escalate to IT |
| All robots' models perform poorly | Lighting changed, or dataset shifted | Same issue across teams day-over-day — refresh classroom calibration |
| LiPo bag smells | Evacuate area, kill power, follow district policy | Smoke or flame — district fire procedure |
| Sensai confidently wrong on a safety topic | Stop, correct in class, log a curriculum issue | Repeats after correction — escalate to curriculum maintainers |

---

## 17. Resources for Teachers

- [Sensai Classes — Curriculum Master](../../README.md)
- [Edge AI Robotics Curriculum Proposal](./Edge_AI_Robotics_Curriculum.md)
- [Community Resources](../../community-resources/)
- [Arduino Modulino Documentation](https://www.arduino.cc/) — Look for current Modulino product pages
- [CSTA AI Learning Priorities](https://csteachers.org/page/ai-resources)
- [AI4K12 — Five Big Ideas](https://ai4k12.org/)
- [LiPo Safety (PRBA / industry briefings)](https://www.prba.org/) — for your battery safety policy

---

## 18. Revision History

| Date | Author | Change |
|------|--------|--------|
| 2026-05-17 | Sensai Curriculum | Initial guide |

---

> Back to [Intro to Robotics Overview](./README.md)
