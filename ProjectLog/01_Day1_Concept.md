# Day 1 — 5 October 2026

## Goal
Develop a platform that tilts automatically to balance a table tennis ball and bring it towards a target position.

## Work completed
- Sketched the initial design.
- Selected a provisional clear acrylic plate measuring 160 × 160 × 3.5 mm.
- Estimated the plate mass at approximately 106 g using an acrylic density of 1.18 g/cm³.
- Chose a table tennis ball.
- Settled on four positional servos with articulated linkages connected at the plate’s corners.
- Chose an underneath camera for ball tracking and an IMU for plate motion and tilt estimation.
- Deferred load cells from the first version.
- Emailed my module leader to ask about borrowing components.
- Created this GitHub repository.

## Available equipment
- ESP32.
- Jumper wires and USB data cable.
- Joystick, buttons and LEDs for possible controls and indicators.
- Access to university 3D printing and measurement equipment.

## Components still to source
- Four matching positional servos.
- IMU containing an accelerometer and gyroscope.
- USB camera.
- Suitable servo power supply and power distribution components.

## Questions to resolve
- How to prevent sideways movement and unwanted rotation while allowing tilt.
- Linkage geometry and coordinated movement of the four servos.
- Servo torque, speed and power requirements.
- Camera focus, viewing distance and reflections through the acrylic.
- Plate stiffness and corner mounting.

## Next session
Begin a simplified one-axis model in MATLAB/Simulink.

## Current status
Concept stage. No simulation or physical prototype tested yet.
