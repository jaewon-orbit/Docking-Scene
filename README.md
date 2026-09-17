# Docking Scene — Fixed-Wing UAV Recovery Visualization

A Unity demonstration video for a university research project on recovering a fixed-wing UAV with a moving ground vehicle.

## Project Context

The research involved several institutions. I created the visualization to give participating teams, government stakeholders, and other viewers a clear picture of the proposed recovery sequence. It helped communicate the overall concept as the long-term project got underway.

## Scene Structure

The scene combines aircraft and ground-vehicle motion, a recovery target, event triggers, and a Cinemachine camera sequence.

- Target points guide the illustrated approach.
- Trigger colliders start transitions such as release, approach, and attachment.
- Quaternion interpolation smooths orientation changes.
- Camera movement and speed changes help viewers follow each stage.

## My Contribution and Design Choices

I built the Unity visualization and scripted the approach and docking sequence. I used explicit target points and timed or trigger-driven transitions to present the intended operation clearly. The scripts combine Rigidbody movement with interpolated position and rotation during attachment.

## Demo

[![Docking Scene demo](https://img.youtube.com/vi/tNUVmWVUYQc/0.jpg)](https://www.youtube.com/watch?v=tNUVmWVUYQc)

## Scope

The output is a concept visualization for research communication. Motion depends on configured targets and scripted events; it does not establish real aircraft dynamics, recovery accuracy, or autonomous-control performance.

This repository contains scene-control scripts and a Timeline asset. The full Unity scene and its models are not included.
<br>
<br>
<br>

<details>
<summary><strong>Technical Implementation Details</strong> (click to expand)</summary>

### Implementation Overview

The scene was built to clearly illustrate the intended recovery sequence rather than to simulate real flight dynamics.

- **Target-point guided approach**  
  A sequence of waypoints defines the approach path toward the recovery basket on the moving ground vehicle.

- **Trigger-based event sequence**  
  Transparent trigger colliders along the trajectory fire sequential events (e.g., detachment, speed change, attachment) to control the demonstration flow.

- **Smooth orientation changes**  
  Quaternion interpolation (handled via coroutines) is used to produce continuous rotation during the approach and docking phases.

- **Camera presentation**  
  Cinemachine and a Timeline track are used to create a cinematic camera path that follows each stage of the sequence.

- **Physics update timing**  
  Critical motion updates are placed in `FixedUpdate()` for consistent simulation stepping within Unity.

These elements were chosen to make the overall recovery concept easy to follow for research partners and stakeholders.

</details>
