# Custom Webcam with Embedded Web Streaming

## 📖 Overview
This project involved designing a **custom webcam** capable of streaming images to a **custom-built webpage**.  
The system integrates a **camera module**, **microcontroller**, and **Wi-Fi chip** into a compact, custom PCB with a 3D-printed enclosure.

**Key Components:**
- **Camera Module:** OV2640
- **Microcontroller:** Atmel SAM4S8B
- **Wi-Fi Module:** ESP32-WROOM

**Key Responsibilities:**
- Soldering and assembling circuit with breakout boards
- Writing microcontroller firmware for image streaming (C)
- Designing and soldering a compact PCB
- Designing a custom enclosure in Onshape (CAD)

---

## 🔄 System Data Flow

Camera → Microcontroller → Wi-Fi Module → Webpage

---

## 🛠 Implementation Details

### 1. Circuit Assembly with Breakout Boards
- Soldered microcontroller, Wi-Fi, and camera breakout boards
- Consulted datasheets to ensure correct pin connections and functionality mapping
- Used unused pins where possible for expansion/debugging

### 2. Firmware Development
- Written in **C** for Atmel SAM4S8B
- **Peripheral setup:**
  - UART for ESP32 configuration
  - I²C for camera communication and image transfer to MCU registers
  - SPI for high-speed image transfer from MCU → ESP32 → webpage
- Camera initialization and configuration via I²C
- Main loop handles continuous image acquisition and transmission

### 3. Enclosure Design
- Designed in **Onshape**, intended for 3D printing
- Considered user interaction:
  - Camera cutout
  - Power LED visibility
  - Access to control buttons and power jack

---

## 📷 Media
![PCB Bottom Layer](docs/img/webcam_bottom_pcb.png) 
![PCB Top Layer](docs/img/webcam_top_pcb.png) 
---

## 🧰 Skills & Tools
- **Embedded Systems:** C programming, UART/I²C/SPI communication
- **Hardware Design:** PCB layout & routing (EAGLE/KiCad)
- **CAD:** Onshape for enclosure design
- **Prototyping:** Soldering, breakout board assembly
- **Networking:** ESP32 web streaming integration
- **Debugging:** Iterative hardware/software testing

