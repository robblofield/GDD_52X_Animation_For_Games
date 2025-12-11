# **1. Module Overview**

## **1.1 What This Module Is About**

This module introduces students to **practical animation techniques for game development**, focusing on **low-complexity, high-impact workflows** that avoid the overhead of full custom character pipelines.
Instead of sculpting, retopology, UVs, and advanced rigging, students will work with **provided characters**, **Mixamo rigs**, **Unity’s animation system**, and **procedural + inorganic animation techniques** suitable for production-focused prototyping.

The goal is not to turn students into professional character animators.
The goal is to give them **practical, implementable skills** to bring life, motion, and responsiveness into their game projects.

---

## **1.2 Aims for Learners**

By the end of the module, students should be able to:

* Understand how animation integrates into a real-time game engine and what constraints this introduces.
* Import, configure, and retarget humanoid animations from external sources (e.g., Mixamo).
* Construct animation state machines and blend animations effectively for responsive gameplay.
* Design and implement inorganic animations (e.g., doors, platforms, mechanisms) using Unity’s animation tools and animation curves.
* Gain introductory experience with procedural animation workflows using ScriptableObjects and runtime curve manipulation.
* Combine multiple animation techniques into a small playable scene or micro-prototype.

---

## **1.3 Skills We Will Cover**

### **Humanoid Animation Skills**

* Using Mixamo to auto-rig meshes
* Applying and blending Mixamo animations in Unity
* Retargeting animations between different humanoid rigs
* Using Avatar Masks and animation layers for partial-body animation (upper/lower body splits)

### **Inorganic Animation Skills**

* Animating environment objects (doors, moving platforms, puzzle mechanisms)
* Using Unity’s Animation window and curve editor
* Creating looped, event-driven, and timeline-based motion
* Understanding root-motion vs in-place animation

### **Procedural Animation Foundations**

* Animating non-humanoid creatures with curve-driven motion
* Using ScriptableObjects to store animation curve profiles
* Swapping animation data at runtime (e.g., “damaged leg” behaviour)
* Blending procedural systems with keyframed animation

### **General Engine Animation Workflow**

* Building Animator Controllers and Blend Trees
* Triggering animations from code
* Understanding transitions, exit times, and parameters
* Debugging and testing animation behaviour in real time

---

## **1.4 What We Are *Not* Covering**

This module intentionally excludes a number of highly specialised skills:

### **Character Art Pipeline**

* Concept art / character design
* Sculpting (ZBrush, Blender high-poly)
* Retopology
* UV unwrapping
* Texturing / PBR workflow
* Baking maps (normals, AO etc.)

### **Advanced Rigging**

* Creating custom humanoid rigs from scratch
* Complex skin weighting / painting
* IK/FK switching workflows
* Facial rigging and blendshape systems

### **Advanced Animation Production**

* Acting-based keyframe character animation
* Motion capture cleanup
* Cinematics pipelines
* Advanced procedural animation (full IK systems, ragdolls, dynamic locomotion)

Where relevant, some of these areas may be touched on **conceptually**, but **students will not be assessed** on them and will not need the skills to complete coursework.

---

## **1.5 Practical Projects in the Semester**

Students will complete **two core practical projects** plus several **in-class micro-exercises**:

### **1) Animation Systems Mini-Scene (Weeks 5–9)**

A functional scene containing:

* A humanoid character using retargeted and blended animations
* At least one inorganic animated object (door/mechanism/platform)
* Some interaction demonstrating animation triggering

This focuses on demonstrating core competencies in **Mixamo → Unity workflow**, **Animator Controller design**, and **inorganic animation**.

---

### **2) Procedural Creature Animation Prototype (Weeks 10–12)**

* **Creature Path:** Implement the procedural alien leg system using curves and ScriptableObjects

This project emphasises **creativity**, **iteration**, and  procedural thinking with complex curve-based setup.

---

```mermaid
graph TD;

  %% Core asset acquisition
  A[Animation Sources] --> A1[Mixamo Humanoid Animations];
  A --> A2[Unity Keyframed Inorganic Animations];
  A --> A3[Procedural Curves / ScriptableObjects];

  %% Humanoid import path
  A1 --> B[Unity Import Settings];
  B --> B1[Avatar Definition];
  B --> B2[Humanoid Rig Mapping];
  B --> B3[Root Motion Settings];

  %% Controller setup
  B --> C[Animator Controller];
  A2 --> C;
  C --> C1[States & Transitions];
  C --> C2[Blend Trees];
  C --> C3[Avatar Masks / Layers];

  %% Runtime control
  C1 --> D[Parameter Driven Animations];
  C2 --> D;
  C3 --> D;
  D --> D1[Gameplay Scripts Trigger Animations];

  %% Inorganic / curve animation path
  A2 --> E[Animation Window / Curves];
  E --> E1[Doors / Platforms / Mechanisms];
  E1 --> D1;

  %% Procedural animation path
  A3 --> F[Curve Assets Stored in ScriptableObjects];
  F --> F1[Runtime Curve Swapping (Normal / Damaged / Custom)];
  F1 --> F2[Procedural Creature Leg Motion];
  F2 --> D1;

  %% Output
  D1 --> Z[Playable Scene / Prototype];
```
