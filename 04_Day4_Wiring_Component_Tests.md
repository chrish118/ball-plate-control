# Day 4 — Wiring and Individual Module Testing

> Session date: not recorded. This is the fourth actual development session.

## Objective
Wire and test the inertial measurement unit and servo PWM driver as separate modules before system integration.

## Work completed
- Carried out wiring for the **GY-BMI160 IMU**.
- Carried out wiring for the **PCA9685 16-channel PWM servo driver**.
- Tested the **BMI160 IMU individually**.
- Tested the **PCA9685 driver individually**.

## Hardware context
- **ESP32** microcontroller.
- **BMI160** accelerometer and gyroscope breakout for intended plate tilt and angular-rate feedback.
- **PCA9685** I²C-controlled PWM module for intended servo control.
- Separate servo power and logic power were considered in the wiring design, with a shared ground required for reliable operation.

## Outcome
Individual wiring and module testing undertaken, as reported in the project development record.

## Next session
Design the main base for the mechanical assembly.

## Verification and remaining work
The precise test sketches, measured outputs, detected I²C addresses and acceptance criteria have not been supplied for this log. Accordingly, the entry records that individual testing took place, **not** that all measurements were calibrated or the integrated four-servo system was verified. Servo load testing, coordinated actuation, PID and ball tracking remain outstanding.
