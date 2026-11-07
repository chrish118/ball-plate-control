# Day 3 — Arm redesign, shoulders and parts list

I continued working on the mechanical design in Fusion 360. After looking at the arms from Day 2, I realised they were too short for the linkage arrangement I had in mind, so I made a longer version rather than trying to work around the original dimensions.

I also designed the shoulder pieces that will connect the mechanism to the servo arms. The updated parts have mounting holes for the joints, and the CAD model helped me check the shapes before moving on to a physical build.

![Updated arms and shoulder CAD in Fusion 360](Day3_Arm_Shoulder_CAD.png)

*Figure 1 — Revised arm and shoulder designs in Fusion 360. The taller tapered parts are the shoulder components; the shorter cylindrical parts show the updated arm design.*

## Bill of materials (BOM)

I made a parts list alongside the CAD work so I could keep track of what needed ordering and what I already had. The components and sources are below.

| Part | Specification / quantity | Source or status | Use |
|---|---|---|---|
| Servo motors | 4 × Miuzei MF90 9g metal-gear, 180° | Purchased (4-pack) | Drive the four plate linkages |
| IMU | DollaTek GY-BMI160, 6-axis | Selected for the build | Measure plate motion and orientation |
| Servo driver | DollaTek PCA9685, 16-channel, 12-bit I²C PWM | Purchased | Generate servo PWM signals |
| Threaded steel balls | 12 × M4 internal-thread, 12 mm diameter, carbon steel | Selected for the build (12-pack listing) | Ball ends for magnetic linkage joints |
| Cup magnets | 24 × 3 mm diameter × 10 mm, with countersunk holes and M3 screws | Purchased (24-pack) | Magnetic ball-joint holders |
| Grub screws | 20 × M4 × 35 mm DIN 916 stainless-steel socket set screws | Selected for the build (20-pack listing) | Threaded linkage hardware |
| USB-C PD trigger boards | JZK adjustable 5/9/12/15/20 V, 3-board pack | Selected for power arrangement | Obtain a selected voltage from a compatible USB-C PD supply |
| ESP32 | Existing development board | **Already owned** | Main controller |
| CAD parts | Top plate, arms and shoulders; later base | **Designed in CAD; 3D printed through university** | Custom mechanical structure |

The quantities above describe the **packs or parts shown in the product listings**, not necessarily the number used in the finished assembly. I already had the ESP32, so it wasn't part of the new purchases. The custom parts were produced through the university rather than bought as off-the-shelf components.

I haven't recorded an exact total cost because the screenshots show listing prices, which may differ from what I actually paid. I also haven't assumed every listing was ordered: the screenshots explicitly confirm purchases for the servos, PCA9685 and cup magnets, while the other listings identify the selected components.

This was mainly a design and procurement session; I hadn't assembled or tested the full linkage yet.

**Next:** Wire up the BMI160 and PCA9685 and test them separately.
