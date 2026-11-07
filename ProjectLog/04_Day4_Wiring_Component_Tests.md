# Day 4 — Components arrived, wiring and module testing

All the components I ordered for the prototype had arrived by this session, so I could start working with the actual electronics instead of just planning the connections. I already had the ESP32, which I'm using as the main controller.

## Wiring

I started wiring the **BMI160 IMU** and **PCA9685 servo driver** to the ESP32. Both modules use I²C, so the idea is to share the SDA and SCL lines while keeping the modules individually addressable.

| Connection | Wiring / purpose |
|---|---|
| ESP32 → BMI160 | Power, ground, SDA and SCL for I²C communication |
| ESP32 → PCA9685 | Logic power, ground, SDA and SCL for I²C control |
| PCA9685 → servos | Three-pin servo headers for signal, positive supply and ground |
| USB-C PD trigger board → servo supply | Separate power path planned for the servos rather than drawing motor current from the ESP32 |
| Grounds | The controller and servo supply need a common ground so the PWM signals have the correct reference |

On the BMI160 breakout, I also looked at the **VIN/3V3, CS and SA0** pins to understand the supply and interface options. On the PCA9685, I checked the difference between its logic supply (**VCC**) and servo supply (**V+**), as well as the **OE** (output enable) pin. These details matter because the board can communicate with the ESP32 without necessarily having motor power connected.

The USB-C PD trigger board is intended to provide a selected voltage from a compatible USB-C PD charger. The servo supply must be set to a voltage within the servo's rated range before the motors are connected; a PD trigger board doesn't regulate the voltage by itself.

## Individual testing

I tested the **BMI160** and **PCA9685** separately before trying to combine everything. I used **VS Code with PlatformIO** for the ESP32 firmware, uploaded an initial test program and checked the serial output, including I²C scanning.

The initial firmware upload and serial output worked, but I haven't recorded the detected addresses or detailed sensor readings here. I'm not treating this as proof that the complete four-servo mechanism works yet.

## Where I left it

The electronics had arrived, the initial wiring was done and I'd started checking the two I²C modules individually. The next session focused on designing the **base** in Fusion 360. Coordinated servo movement, IMU-based feedback control, PID and camera tracking were still to come.
