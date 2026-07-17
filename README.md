# Boardoza VL53L7CX-3 Time-of-Flight Breakout Board

The **Boardoza VL53L7CX-3 Time-of-Flight Breakout Board** is a compact distance sensing solution built around the **STMicroelectronics VL53L7CX** multizone Time-of-Flight (ToF) sensor. The sensor combines a **940 nm invisible VCSEL emitter** and a **SPAD receiving array** to deliver accurate distance measurements across a configurable **4×4 or 8×8 ranging zone matrix**, providing up to **64 independent zones**.

Designed specifically for **3.3V to 5V powered systems**, this breakout board integrates a low-dropout voltage regulator and level-shifting circuitry for I²C communication and interrupt signaling.This enables direct connection to both 3.3V and 5V microcontroller systems while providing the required operating voltage for the sensor. The board also provides extra control functions such as interrupt output (INT), communication enable control (LPn), and I²C interface reset (RST). Its dual-connector layout also allows multiple boards to be connected in a **cascade connection**, making it easier to use more than one VL53L7CX board on the same I²C bus. Typical applications include **robotics, occupancy detection, gesture recognition, obstacle avoidance, smart appliances, industrial automation, and embedded sensing applications** where compact size and reliable ranging performance are required.

## [Click here to purchase!](https://www.ozdisan.com/p/moduller-870/boardoza-vl53l7cx-3-1577677?s=VL53L7CX-3)

| Front Side | Back Side |
| :---: | :---: |
| ![Front](./assets/VL53L7CX-3%20Front.png) | ![Back](./assets/VL53L7CX-3%20Back.png) |

---

## Key Features

- **Multizone Distance Sensing:** Supports both 4×4 and 8×8 ranging configurations, providing up to 64 independent measurement zones.
- **Ultra-Wide Field of View:** Provides a 60° × 60° square detection FoV with a 90° diagonal field of view.
- **3.3V–5V System Compatible:** Supports a 3.3V to 5V supply input with onboard voltage regulation.
- **Level-Shifted Communication and Interrupt Lines:** SDA, SCL, and INT lines include level shifting for compatibility with 3.3V and 5V microcontroller systems.
- **3.3V Control Signals:** RST and LPn pins operate at 3.3V logic level and should not be driven with 5V signals.
- **Eye-Safe Operation:** Integrated Class 1 invisible 940nm VCSEL (Vertical-Cavity Surface-Emitting Laser) emitter is safe for the eyes and enables safe operation in consumer and industrial products.
- **Multitarget Detection:** Capable of detecting and measuring multiple targets within each ranging zone.
- **Autonomous Low-Power Mode:** Supports autonomous operation with programmable interrupt thresholds for host wake-up applications.
- **Power Status Indicator:** Integrated LED provides visual confirmation of power availability.

---

## Technical Specifications

**Model:** VL53L7CX-3  
**Manufacturer:** Boardoza  
**Manufacturer IC:** STMicroelectronics     
**Function:** Multizone Time-of-Flight (ToF) Distance Sensor  
**Board Supply Voltage:** 3.3V to 5V  
**Onboard Regulation:** 3.3V LDO Regulator  
**Communication Interface:** I²C  
**I²C Address:** 0x52 (8-bit address)  
**Maximum I²C Speed:** 1 Mbit/s  
**Ranging Zones:** 4 × 4 or 8 × 8, up to 64 zones  
**Maximum Sampling Rate:** Up to 60Hz  
**Measurement Range:** 2cm to 350cm per zone  
**Field of View:** 60° × 60° detection FoV, 90° diagonal  
**Emitter Type:** 940nm invisible VCSEL (Vertical-Cavity Surface-Emitting Laser)  
**Detector Type:** SPAD (Single Photon Avalanche Diode) receiving array  
**Safety Classification:** Class 1 Eye-Safe  
**Logic Levels:** 5V compatible on SDA, SCL, and INT; 3.3V on RST and LPn  
**Operating Temperature:** -30°C to +85°C  
**Board Dimensions:** 20mm × 20mm  

---

## Model Comparison

All four boards use the same **STMicroelectronics VL53L7CX multizone Time-of-Flight sensor** and provide the same core ranging capabilities. The main differences between the models are their **supply voltage requirements** and the signals on which **logic-level shifting** is provided.

|      Model     | Board Supply Input | Onboard 3.3V Regulator | 5V-Compatible Signals | Native 3.3V Signals     | Practical Difference                                                                                                                                                                                             | Recommended Use                                                                                             |
| :------------: | :----------------: | :--------------------: | :-------------------- | :---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **VL53L7CX-1** |        3.3V        |           No           | None                  | SDA, SCL, INT, RST, LPn | The entire board operates directly from 3.3V. No voltage regulation or logic-level shifting is included. All connected signals must remain at 3.3V.                                                              | Best for systems in which both the power supply and the microcontroller logic operate at 3.3V.              |
| **VL53L7CX-2** |     3.3V to 5V     |           Yes          | SDA, SCL              | INT, RST, LPn           | The board can be powered from either 3.3V or 5V. The I²C communication lines are level-shifted, allowing SDA and SCL to communicate with both 3.3V and 5V hosts. The control signals remain at 3.3V logic level. | Best when the host uses 5V I²C communication but the INT, RST, and LPn control pins can be handled at 3.3V. |
| **VL53L7CX-3** |     3.3V to 5V     |           Yes          | SDA, SCL, INT         | RST, LPn                | In addition to the I²C lines, the interrupt output is also level-shifted. This allows the host to receive the INT signal at its own logic voltage. RST and LPn still operate at 3.3V.                            | Best when both I²C communication and the interrupt signal need to be compatible with a 5V microcontroller.  |
| **VL53L7CX-4** |         3.3V to 5V         |           Yes          | None                  | SDA, SCL, INT, RST, LPn | The board is powered from 5V, but all communication and control signals remain at native 3.3V logic levels. The connected host must therefore use 3.3V-compatible I/O signals.                                   | Best for systems that provide a 5V power rail but use a 3.3V microcontroller or 3.3V host interface.        |

### How to Select the Right Model

* Choose **VL53L7CX-1** when the complete system operates at **3.3V**.
* Choose **VL53L7CX-2** when you need **3.3V–5V compatible I²C communication**, but the control pins can remain at 3.3V.
* Choose **VL53L7CX-3** when both the **I²C lines and the INT output** must be compatible with a 5V host.
* Choose **VL53L7CX-4** when the board will be powered from **3.3V-5V**, but the connected microcontroller uses **3.3V logic**.

> **Important Note:** A board being powered from 5V does not automatically mean that all of its communication and control pins can accept 5V logic signals. Always check the logic-level compatibility of SDA, SCL, INT, RST, and LPn before connecting the board to a host system.

### Common Features of All Four Models

The following features are identical across all four models:

* STMicroelectronics VL53L7CX multizone Time-of-Flight sensor
* 4×4 or 8×8 ranging configurations
* Up to 64 independent measurement zones
* 60° × 60° square detection field of view
* 90° diagonal field of view
* Up to 60Hz ranging frequency
* Multitarget detection within each zone
* I²C communication
* INT, RST, and LPn control functions
* Class 1 eye-safe 940nm VCSEL emitter
* Dual-connector layout for easier multi-board connection

---

## Board Pinout

### ( J1 ) Power & I²C Connector

| Pin Number | Pin Name | Description |
| :---: | :---: | --- |
| 1 | GND | Ground |
| 2 | SCL | I²C Serial Clock |
| 3 | SDA | I²C Serial Data |
| 4 | 5V | Positive Power Supply |

### ( J2 ) Control & I²C Connector

| Pin Number | Pin Name | Description |
| :---: | :---: | --- |
| 1 | 5V | Positive Power Supply |
| 2 | GND | Ground |
| 3 | SDA | I²C Serial Data |
| 4 | SCL | I²C Serial Clock |
| 5 | RST | I²C interface reset input, active high. Toggle from Low to High and back to Low to reset the I²C target interface only. Operates at 3.3V logic level. |
| 6 | INT | Level-shifted interrupt output. Used to notify the host when ranging data or threshold events are available. |
| 7 | LPn | Communication enable input. Pulled up to 3.3V for normal operation; drive Low to disable I²C communication. |

---

## Board Dimensions

<img src="./assets/VL53L7CX-3 Dimensions.png" alt="Board Dimensions" width="450"/>

---

## Step Files

[Boardoza VL53L7CX-3.step](./assets/VL53L7CX-3%20Step.step)

---

## Datasheet

[VL53L7CX Datasheet.pdf](./assets/VL53L7CX-3%20Datasheet.pdf)

---

## Version History

- V1.0.0 - Initial Release

---

## Support

- If you have any questions or need support, please contact <support@boardoza.com>

---

## **License**

This repository contains both hardware and software components:

### **Hardware Design**

[![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

All hardware design files are licensed under [Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg

### **Software/Firmware**

[![BSD-3-Clause][bsd-shield]][bsd]

All software and firmware are licensed under [BSD 3-Clause License][bsd].

[bsd]: https://opensource.org/licenses/BSD-3-Clause
[bsd-shield]: https://img.shields.io/badge/License-BSD%203--Clause-blue.svg
