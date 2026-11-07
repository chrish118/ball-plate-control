# Day 3 — Arm redesign, shoulders and parts list

I continued working on the mechanical design in Fusion 360. After looking at the arms from Day 2, I realised they were too short for the linkage arrangement I had in mind, so I made a longer version rather than trying to work around the original dimensions.

I also designed the shoulder pieces that will connect the mechanism to the servo arms. The updated parts have mounting holes for the joints, and the CAD model helped me check the shapes before moving on to a physical build.

![Updated arms and shoulder CAD in Fusion 360](Day3_Arm_Shoulder_CAD.png)

*Figure 1 — Revised arm and shoulder designs in Fusion 360. The taller tapered parts are the shoulder components; the shorter cylindrical parts show the updated arm design.*

## Bill of materials (BOM)

I also put together a BOM to keep track of what the build would need and ordered parts for the prototype. The main items on the project parts list include:

| Part | Purpose |
|---|---|
| 4 × Miuzei 9g metal-gear 180° servos | Move the plate through the four linkages |
| ESP32 | Main controller |
| PCA9685 16-channel PWM driver | Generate the servo control signals |
| BMI160 IMU | Measure plate movement and tilt |
| Magnetic ball-joint hardware (12 mm steel balls with M4 internal threads and matching magnetic holders) | Allow movement at the linkage connections |
| Custom CAD parts (plate, arms and shoulders) | Mechanical structure and linkages |
| Wiring, connectors and suitable power supply | Connect and power the electronics and servos |

This is a summary of the planned hardware, **not an item-by-item record of what arrived or was ordered on Day 3**. I haven't added quantities or prices where they aren't confirmed.

This was mainly a design and procurement session; I hadn't assembled or tested the full linkage yet.

**Next:** Wire up the BMI160 and PCA9685 and test them separately.
