# ESP32-C3-Motor-Control-Board-Round-
A compact, circular PCB designed for DC motor control using the ESP32-C3 microcontroller and the DRV8838 motor driver. Includes a 3.3V regulator, USB-C connectivity, an I2C breakout for expansion, and a dedicated battery power input. Perfect for robotics, smart devices, and motorized IoT projects.
# 🔵 Round Motor Control PCB (ESP32-C3 + DRV8838)

![PCB Top View](images/PCB_Top.png)

This repository contains the complete hardware design files for a **circular DC Motor Control Board** based on the **ESP32-C3** microcontroller. The board is specifically designed to drive a brushed DC motor using the **DRV8838** motor driver IC, making it an excellent choice for compact robotics, motorized IoT devices, and DIY electronics projects.

---

## ✨ Key Features

*   **Main Controller:** ESP32-C3-WROOM-02-N4 (4MB Flash, Wi-Fi + BLE).
*   **Motor Driver:** DRV8838DSGR – Capable of driving a single brushed DC motor.
*   **Power Management:** 
    *   AP2112K 3.3V LDO Regulator.
    *   DMP1045U P-Channel MOSFET for power switching/control.
    *   SS34 Schottky Diode for protection.
*   **Connectivity:**
    *   USB‑C Interface for power and programming (with ESD Protection).
    *   I2C Connector (U4) for external sensors or expansion (compatible with STWLC38).
    *   Debugging & Test Points (INT, SCL, SDA, VSYS, VBATT).
    *   Motor connector (CN4) and Battery connector (CN3).
*   **Logic:** 74HC14D Schmitt Trigger for signal conditioning.
*   **Controls:** Reset and Boot buttons for easy programming.

---

## 🖼️ Gallery
<img width="1350" height="851" alt="Schematic_Motor_PCB_2026-05-03" src="https://github.com/user-attachments/assets/4fb82976-88f0-4211-8846-f865d2e0a7f2" />

| PCB Layout | Schematic Preview |
<img width="576" height="587" alt="Motor_PCB_3D_Top_View" src="https://github.com/user-attachments/assets/56a63290-621b-41c6-a60c-7532f21cea34" />

| :---: | :---: |
<img width="582" height="573" alt="Motor_PCB_3D_Bottom_View" src="https://github.com/user-attachments/assets/9e002f8d-5410-4b54-b63a-a9563b5b22c6" />

| [![PCB Layout](images/PCB_Top_Back.png)](images/PCB_Top_Back.png) | [![Schematic](images/Schematic.png)](images/Schematic.png) |
<img width="681" height="678" alt="Motor_PCB_2D_View" src="https://github.com/user-attachments/assets/9ea14584-9f5a-411f-93b0-30c8098e800e" />

*(Add your 3D render or the PDF images to this section in the `images/` folder)*

---

## 🔌 Hardware Specifications

| Component | Description |
| :--- | :--- |
| **MCU** | ESP32-C3-WROOM-02-N4 |
| **Motor Driver** | DRV8838DSGR (H-Bridge for DC Motor) |
| **Power (Logic)** | 3.3V via AP2112K LDO (from VSYS) |
| **Power Inputs** | VBATT (Battery) / VSYS (System) |
| **Motor Output** | CN4 (2-pin JST XH connector) |
| **Programming** | USB‑C (Type‑C) using onboard CHxxx equivalent/ESP32 native |
| **Expansion** | I2C Breakout (U4) |

---

## 🛠️ Getting Started / Assembly

1.  **Order the PCB:** Use the provided `PCB_PCB_Motor_PCB-copy_2026-05-03.pdf` to order your PCB from your manufacturer of choice (JLCPCB, PCBWay, etc.).
2.  **Source Components:** Use the `BOM_Motor_PCB_2026-05-03.csv` file to purchase the exact listed components. 
3.  **Assembly:** Populate the PCB using the `PickAndPlace_PCB_Motor_PCB-copy_2026-05-03.csv` file. Pay attention to the orientation of the ICs and the polarity of the capacitors.
4.  **Power:** Connect a **3.7V - 5V** battery to the `CN3` connector or power the board via the USB‑C port.
5.  **Programming:** 
    *   Connect the board via USB‑C.
    *   Use the Arduino IDE or ESP-IDF.
    *   Select `ESP32C3 Dev Module` as your board.
    *   Press and hold the **BOOT** button, then click **Upload**.
6.  **Test:**
    *   Connect a DC brushed motor to `CN4`.
    *   Use the `GPIO18` and `GPIO19` pins to control the motor driver (`IN1` and `IN2` on the DRV8838).

---

## 📦 Bill of Materials (BOM)

The complete BOM is available in the file [`BOM_Motor_PCB_2026-05-03.csv`](BOM_Motor_PCB_2026-05-03.csv).

---

## 🗂️ Repository Structure
