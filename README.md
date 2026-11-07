# Ball-and-Plate Control

A work-in-progress, four-servo ball-balancing platform built around an ESP32, PCA9685 PWM driver, BMI160 IMU, and a 160 × 160 × 3.5 mm acrylic plate. The long-term goal is to balance a table-tennis ball and track target positions using camera feedback.

**Status — 7 November 2026:** Mechanical CAD and component selection have progressed; preliminary ESP32 firmware has been uploaded. **No verified closed-loop balancing, PID control, or camera tracking has been implemented.**

## Hardware and mechanical design

| Subsystem | Current design | Status |
|---|---|---|
| Plate | 160 × 160 × 3.5 mm acrylic | Selected; full assembly unverified |
| Actuation | Four Miuzei 9 g metal-gear 180° positional servos | Acquired; coordinated motion unverified |
| Linkages | Custom Fusion 360 arms/shoulders, 12 mm M4-threaded steel balls and magnetic ring holders | CAD developed; mechanical performance unverified |
| Servo driver | PCA9685 16-channel PWM board | Wiring in progress |
| Controller | ESP32 | Initial PlatformIO firmware upload successful |
| IMU | GY-BMI160 6-axis accelerometer/gyroscope | Selected; readings not yet verified |
| Power | Separate regulated 5 V servo supply and logic power with common ground | Planned/wiring explored; combined load not validated |
| Camera | Under-plate tracking, initially potentially a phone | Planned; not integrated |

The first prototype uses a **parallel servo layout**. Alternative diagonal geometry was considered. Custom servo mounts, magnetic joints, printed base parts and mounting hardware have been designed or investigated. Fit, stiffness, maximum tilt, backlash and servo loads remain to be tested.

**Power caution:** A 5 V/2 A source was considered, but has not been verified sufficient for four servos under load. Check peak current, wiring and common ground before energising the assembled mechanism.

## Firmware and electronics progress

Development uses **VS Code + PlatformIO (C++ for ESP32)**. Initial firmware uploaded successfully, and the serial monitor displayed repeated I²C scanning output. This does **not** establish that the BMI160 and PCA9685 have both been detected or that the servos operate correctly. Firmware source has not yet been published in this repository.

## Development milestones

- [x] Define ball-and-plate concept and provisional plate dimensions.
- [x] Select ESP32, PCA9685, BMI160 and four Miuzei positional servos.
- [x] Develop Fusion 360 CAD for base, arms, shoulders and magnetic ball-joint linkages.
- [x] Select parallel servo orientation for initial prototype.
- [x] Set up PlatformIO and upload preliminary ESP32 firmware.
- [x] Observe serial I²C scanning output.
- [ ] Fabricate, assemble and mechanically validate the full platform.
- [ ] Verify power distribution, I²C devices and IMU measurements.
- [ ] Calibrate servo neutral points and coordinated plate tilt.
- [ ] Model ball dynamics in MATLAB/Simulink.
- [ ] Develop and tune PID or other feedback control.
- [ ] Implement Python/OpenCV ball tracking.
- [ ] Demonstrate and measure stable ball balancing and target tracking.

## Development update: October–7 November 2026

**Mechanical:** Custom Fusion 360 base and linkage CAD developed; M4 internal-thread steel balls and magnetic rings selected; M2/M3 fastening, servo horns, interference clearances and 3D printing explored. The complete assembly is not yet validated.

**Electronics:** Four 180° servos, ESP32, PCA9685 and BMI160 selected. Separate servo power and logic power with common ground planned. Safe combined current draw and end-to-end servo actuation remain unverified.

**Software:** PlatformIO environment configured and an ESP32 firmware upload succeeded; serial I²C scan messages observed. No calibrated tilt-feedback loop, camera tracking or balancing controller is yet demonstrated.

**Next:** Finish printed assembly and mounts, verify the supply and sensor communications, calibrate the four servos, then begin controlled tilt tests before implementing ball tracking and feedback control.

## Engineering questions

- How will the mechanism prevent unwanted translation/yaw while permitting pitch and roll?
- How can four servos be coordinated without over-constraining the plate?
- What are the usable tilt range, stiffness, backlash and torque requirements?
- What current rating is required for simultaneous servo motion?
- How will camera perspective and acrylic reflections affect position measurements?

## Development logbook

The project currently has **five recorded development sessions** (not five consecutive calendar days):

| Day | Work | Log |
|---|---|---|
| 1 | Initial concept, research and system architecture | [Day 1](01_ProjectLog) |
| 2 | CAD for the initial arms and top plate | [Day 2](02_Day2_CAD.md) |
| 3 | Shoulder CAD, longer revised arms, BOM and component orders | [Day 3](03_Day3_Arm_Revision_BOM.md) |
| 4 | Wiring and individual BMI160/PCA9685 module tests | [Day 4](04_Day4_Wiring_Component_Tests.md) |
| 5 | Main base CAD design | [Day 5](05_Day5_Base_Design.md) |

The original Day 1 record is preserved unchanged. Session dates for Days 2–5 were not established and have not been invented.
