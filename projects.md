---
layout: page
title: Projects
permalink: /projects/
---

Below are a few projects I’ve worked on.

## Capstone: Magnetically Actuated Soft-Continuum Robot (ENT) {#capstone}
### Why build this?
Ear, nose, and throat (ENT) surgery often means working inside exceptionally narrow, twisty passages where rigid tools can struggle to maneuver without damaging surrounding tissue. Using current ENT surgical tools often requires multiple personnel involvement and repeated tool swapping. And in some cases, surgeons must enlarge pathways by removing bone to reach a target or gain vision in an area. After speaking with sinus surgeons and researching current techniques, it was clear there was room for a gentler, more dexterous approach that could navigate tight anatomy without adding trauma.

We set out to build a magnetically steered soft-continuum robot. The objective was to keep the instrument compliant inside the anatomy, shift actuation from outside the body via controlled magnetic fields, and coordinate it with a linear stage to orient the tip precisely and advance along that heading.

> **Need Statement**  
> Design a magnetically actuated continuum robot for use in ENT surgery, enhancing dexterity in navigating complex and confined anatomical spaces while remaining less invasive than current tools.
<br>

### How it works
This platform brings together four subsystems that operate as one:
- **Soft robot body.** The body was cast in medical-grade silicone and reinforced with a **nitinol** wire backbone for resilience and shape support. The tip was **magnetized** by embedding **NdFeB** particles and aligning their magnetization along the robot’s axis so external fields can produce a steering torque.
- **Tri-axial electromagnetic coils.** Three orthogonally arranged coils generate a controllable **magnetic field**. By adjusting coil currents, we can shape a resultant field that applies torque on the tip, creating smooth, directional bending without bulky on-board actuators.
- **Linear actuator (follow-the-leader).** A stepper-driven stage advances or retracts the robot along its axis. Coupled with the magnetic steering, this lets us point the tip first and then “follow” that direction with axial motion—reducing wall contact.
- **Real-time control GUI.** A **Python** interface handles live steering + extension together. Commands stream over low-latency serial to a microcontroller that drives the stepper and **PWM coil drivers** (with H-bridge switching). The GUI provides mode selection, telemetry, and safety interlocks (limits, timeouts, E-stop) to prevent unintended motion.

We validated the integrated system on the bench, in **3D-printed sinus phantoms**, and anatomical models, checking range of motion, geometric compatibility, and repeatable tip control. While this is a research prototype, the results were encouraging and informed our continuous rounds of tuning and safety controls.

### Risk & safety: my FTA work (ISO 14971)
I led a **Fault Tree Analysis (FTA)** to identify health and safety risks across implementation, prototyping, validation, manufacturing, and deployment. Using a top-down approach aligned with **ISO 14971:2019**, I defined intended use and reasonably foreseeable misuse, identified hazards (thermal exposure, unintended motion, electrical faults, magnetic interference), traced root causes (driver failures, timing issues, mechanical jams), and proposed controls (current limits, interlocks, watchdogs, clear UI states, labeling, and verification tests). We aimed to identify critical hazards as early as possible and either eliminate them or implement safeguards before they could affect users.

### Impact (why this matters)
A softer, magnetically steered tool can reach where rigid tools struggle, **reducing invasiveness**, instrument swaps, and potentially procedure time—benefits that can cascade into **faster recovery** and fewer complications for patients, and efficiency gains for providers.

### Future directions
- **Specialized end effectors:** graspers for biopsies, a **laser** for polyp removal, a **balloon** for sinus dilation, an onboard **camera** for visualization, and targeted **medication injection**.  
- **OR integration:** smoother workflows with existing imaging/navigation, plus exploration of semi-autonomous or closed-loop steering.

###Gallery
<p align="center">
  <img src="/assets/img/capstoneposter.jpg" alt="Image of SCai Capstone Poster" width="300"/>
  <img src="/assets/img/capstonepamphlet.jpg" alt="Image of SCai Capstone Pamphlet" width="300"/>
</p>

--- <br>

## Interview Buddy {#interview-buddy}
- **What it is:** A browser app that records responses and provides feedback with computer vision and NLP.
- **My role:** Implemented **Media Capture** on the frontend, a **Django** backend with REST endpoints, and Python pipelines for **speech/text similarity**.
- **Tech:** HTML/CSS/JS, Django/REST, Python (TF‑IDF, basic CV), Docker (optional).
- **Links:** [Repo](#) · [Demo](#)

--- <br>

## Mastermordle (Wordle x Mastermind) 
- A word puzzle where each guess receives vowel/consonant feedback counts.
- Renders Wordle‑style tiles plus a feedback table
- **Tech Stack:** Node.js, TypeScript, React, HTML/CSS



