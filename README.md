# Ball-and-Plate Control

A project to balance a table tennis ball on a tilting acrylic platform using computer vision, an IMU and an ESP32.

The initial goal is to bring the ball to the centre and hold it there. Later goals include moving between target positions and following paths.

## Current Status

Concept development. Component selection and mechanical validation are pending. Simulation and hardware testing have not yet started.

## Proposed Design

| Component | Plan |
|---|---|
| Plate | Clear acrylic, 160 × 160 × 3.5 mm; approximately 106 g |
| Ball | Table tennis ball |
| Actuation | Four positional servos linked to the plate’s corners |
| Camera | Mounted underneath to track ball position |
| IMU | Mounted on the moving plate to estimate tilt and measure angular velocity |
| Microcontroller | ESP32 |
| Computer | Laptop for image processing and control development |

The camera will track the ball’s position, with successive frames used to estimate its velocity. The controller will calculate a desired plate tilt, and the ESP32 will coordinate the servos. IMU measurements will provide feedback on the plate’s motion.

Load-cell sensing is deferred from the initial build.

## Planned Tools

- MATLAB/Simulink — system modelling and controller development.
- Python/OpenCV — camera processing and ball tracking.
- C/C++ — ESP32 firmware.
- CAD software — mechanical design and printed components.

## Development Plan

- [x] Define the initial concept and provisional dimensions.
- [x] Review available components.
- [x] Contact the university about borrowing hardware.
- [ ] Model one-axis ball motion in Simulink.
- [ ] Develop and evaluate a controller in simulation.
- [ ] Validate the linkage design and mechanical constraints.
- [ ] Select and test the camera, IMU and servos.
- [ ] Build and test the platform.
- [ ] Integrate ball tracking and feedback control.
- [ ] Measure balancing and target-tracking performance.

## Engineering Questions

- How will the mechanism constrain sideways movement and unwanted rotation?
- How should the four servos be coordinated without fighting each other?
- What torque, speed and power supply are required?
- How will plate tilt and acrylic reflections affect camera measurements?
- Is the proposed acrylic thickness sufficiently stiff at the corner mounts?

## Project Logs

Daily progress, decisions, experiments and results are recorded in [project logs](project%20logs/).
