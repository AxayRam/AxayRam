<div align="center">

# Axay Ram
### Embedded Systems, Firmware & PCB Design Engineer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-axay--ram-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/ram-axay)
[![Email](https://img.shields.io/badge/Email-axay19392%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:axay19392@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-AxayRam-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/AxayRam)
[![Profile Views](https://komarev.com/ghpvc/?username=AxayRam&color=0e75b6&style=flat-square&label=Profile+Views)](https://github.com/AxayRam)

</div>

---

## About

Embedded systems engineer focused on firmware development, hardware interfacing, and real-time behavior in resource-constrained systems.  
I build end-to-end solutions across embedded C, Linux-based development, PCB design, and validation workflows.

Currently working on **industrial Modbus TCP weight measurement firmware** on STM32F4 with FreeRTOS, LwIP, and precision ADC interfacing for real-time load cell data acquisition and network telemetry.

Previously delivered a **smart home automation system** during an internship at **Emertxe Information Technologies**, covering sensor integration, cloud telemetry, and reliability-focused control logic.

### Core Competencies

| Area | Skills |
|---|---|
| Firmware | Bare-metal C, HAL/LL drivers, RTOS task design, DMA transfers, interrupt-driven I/O |
| RTOS | FreeRTOS (CMSIS V2): tasks, semaphores, mutexes, queues, priority scheduling |
| Hardware | Load cell interfacing, sensor integration, GPIO multiplexing, 7-segment display driving |
| Protocols | UART, I2C, SPI, Ethernet (RMII), Modbus TCP, EtherCAT, Wi-Fi, HTTP, GSM, GPS |
| Networking | LwIP TCP/IP stack, static IP configuration, Modbus TCP server, socket management |
| Platforms | STM32F4 (Cortex-M4), ARM Cortex-M, ARM7, ESP32, AVR, Raspberry Pi |
| PCB & EDA | Schematic design, EasyEDA, Gerber generation, BOM preparation, 3D PCB visualization |
| Storage | Flash EEPROM emulation (log-structured), EEPROM drivers, non-volatile config management |
| Linux | Shell scripting, GPIO, system programming, build tools |
| Tools | STM32CubeIDE, STM32CubeMX, GDB, logic analyzer, PICSimLab, Git, VS Code |

---

## Education

**B.E. Electronics & Communication Engineering**

Relevant Coursework: Embedded Systems · Microprocessors & Microcontrollers · Digital Signal Processing · Computer Networks · Operating Systems · Digital Electronics

---

## Technical Stack

### Languages
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Assembly](https://img.shields.io/badge/Assembly-0071C5?style=for-the-badge&logo=arm&logoColor=white)
![Shell](https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white)

### Hardware Platforms
![STM32](https://img.shields.io/badge/STM32-03234B?style=for-the-badge&logo=stmicroelectronics&logoColor=white)
![ESP32](https://img.shields.io/badge/ESP32-000000?style=for-the-badge&logo=espressif&logoColor=white)
![ARM](https://img.shields.io/badge/ARM_Cortex--M-0071C5?style=for-the-badge&logo=arm&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=Arduino&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22333?style=for-the-badge&logo=Raspberry%20Pi&logoColor=white)

### RTOS & Middleware
![FreeRTOS](https://img.shields.io/badge/FreeRTOS-6DB33F?style=for-the-badge&logo=freertos&logoColor=white)
![LwIP](https://img.shields.io/badge/LwIP_TCP/IP-005571?style=for-the-badge&logo=internetcomputer&logoColor=white)

### PCB & EDA Tools
![EasyEDA](https://img.shields.io/badge/EasyEDA-2D8CFF?style=for-the-badge&logo=easyeda&logoColor=white)
![STM32CubeIDE](https://img.shields.io/badge/STM32CubeIDE-03234B?style=for-the-badge&logo=stmicroelectronics&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=Visual%20Studio%20Code&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

### Communication Protocols
`UART` | `I2C` | `SPI` | `Ethernet (RMII)` | `Modbus TCP` | `EtherCAT` | `Wi-Fi` | `HTTP` | `GSM` | `GPS`

---

## Engineering Projects

### 1) Industrial TCP Weight Measurement System
**STM32F407 · FreeRTOS · LwIP · Modbus TCP · CS5551 ADC**

Production-grade industrial weighing system firmware for real-time load cell data acquisition, signal processing, and network-based telemetry:

- **STM32F407VGT6** (ARM Cortex-M4 @ 168 MHz) bare-metal firmware with STM32 HAL
- **FreeRTOS** multi-task architecture (5 tasks): ADC sampling, LCD refresh, Modbus server, button debounce, and network management with mutex/semaphore/queue synchronization
- **CS5551 precision ADC** driver (SPI, x128 PGA gain) with alpha-trimmed mean filter for ±0.01% measurement stability
- **Modbus TCP server** (port 502) on **LwIP** stack over Ethernet RMII (LAN8742 PHY) — holding register read/write for SCADA/HMI integration
- **Log-structured flash EEPROM emulation** (128 KB sector, ~1638 write cycles before erase) for non-volatile storage of calibration, network config, and operational parameters
- **6-digit multiplexed 7-segment display** with 20+ level hierarchical menu system for runtime configuration (IP/subnet/gateway, calibration, filter settings)
- DMA-accelerated SPI transfers with ISR→task signaling via binary semaphores

`STM32F4` `FreeRTOS` `LwIP` `Modbus TCP` `SPI` `DMA` `CS5551 ADC` `Ethernet` `EEPROM Emulation` `Embedded C`

**[View Repository →](https://github.com/AxayRam/stm32-tcp-weight-system)**


---

### 2) Smart Home Automation System (IoT Internship)
**Emertxe Information Technologies** · *Sep 2024 – Nov 2024*

End-to-end IoT solution with remote management and safety automation:
- Cloud control through the Blynk IoT platform
- LM35 thermal sensor-based automatic relay cut-off
- LDR-based adaptive lighting control
- Automated water-tank level sensing and pump control
- 16×2 LCD human-machine interface for runtime status

`Embedded C` `ESP32` `Blynk Cloud` `UART` `I2C` `Sensors`

**[View Repository →](https://github.com/AxayRam/SMART-HOME-AUTOMATION-)**

---

### 3) LAN9252 EtherCAT SPI Evaluation Board
**Industrial EtherCAT Slave PCB Design**

Professional PCB design for an EtherCAT slave evaluation board based on the Microchip LAN9252 controller with SPI host interface. The repository includes production-ready hardware deliverables for review and fabrication.

Highlights:
- EtherCAT slave controller based on LAN9252
- SPI interface for external MCU integration
- PCB design files prepared in EasyEDA
- Gerber package for manufacturing
- Bill of Materials (BOM) for component planning
- 3D PCB renders and layout documentation

`EtherCAT Design` `LAN9252` `SPI` `EasyEDA` `PCB Design` `Gerber` `BOM`

**[View Repository →](https://github.com/AxayRam/LAN9252-EtherCAT-SPI-EVB)**

---

### 4) Strawman's Eye — Motion-Triggered Security Camera
ESP32-CAM · PIR sensor · Telegram Bot API

Low-power, event-driven security system:
- PIR-triggered image capture on motion events
- Telegram bot-based image delivery to mobile in real time

`ESP32-CAM` `PIR Sensor` `Telegram API` `Embedded C`

**[View Repository →](https://github.com/AxayRam/Strawman-s-Eye)**

---

### 5) Raspberry Pi 5 — Adaptive LED and Ultrasonic Sensor
Raspberry Pi 5 · C · WiringPi · HC-SR04

Embedded C project running on Raspberry Pi 5:
- GPIO LED control with timing behavior
- HC-SR04 distance measurement in centimeters
- Distance-based adaptive LED blink logic

`Raspberry Pi 5` `C` `WiringPi` `HC-SR04` `GPIO`

**[View Repository →](https://github.com/AxayRam/Raspberry-Pi-LED-Ultrasonic-Project)**

---

### 6) ESP32-CAM Wireless Surveillance System
ESP32-CAM · C/Arduino Core · Telegram API

Network-based surveillance prototype:
- Wi-Fi live stream over local network
- Telegram bot integration for remote commands and alerts

`ESP32-CAM` `C` `Arduino Core` `Wi-Fi`

**[View Repository →](https://github.com/AxayRam/Camera_Surveillance_System)**

---

### 7) Women's Safety and GPS Tracking Device
ARM7 · NEO-6M GPS · SIM800L GSM · EEPROM

Embedded safety device for real-time location tracking and emergency response:
- GPS-based latitude/longitude tracking
- SIM800L emergency SMS and call triggering
- EEPROM-based emergency contact persistence

`ARM7` `GPS` `GSM` `EEPROM` `Embedded C`

**[View Repository →](https://github.com/AxayRam/WOMAN_SEFTY_DEVICE)**

---

### 8) PCM Audio Generator (DSP Project)
C · Audacity · DSP

Pulse Code Modulation implementation in C:
- Custom waveform generation exported as raw audio
- Spectrum/timing validation in Audacity
- Circular buffer-based memory-efficient data flow

`C` `DSP` `PCM` `Audacity`

**[View Repository →](https://github.com/AxayRam/PCM-PULSE-CODE-MODULATIO-N)**

---

## Work Experience

### Embedded Firmware Engineer — Vraj Enterprises
*2026 – Present · Gujarat, India*

Developing production-grade industrial weighing system firmware on STM32F4:
- Designed multi-task FreeRTOS architecture (5 concurrent tasks) with mutex, semaphore, and queue-based synchronization for deterministic ADC sampling and LCD refresh
- Implemented custom CS5551 precision ADC driver over SPI with DMA acceleration and alpha-trimmed mean filter achieving ±0.01% measurement repeatability
- Built Modbus TCP server from scratch on LwIP stack (Ethernet RMII + LAN8742 PHY) for real-time weight data exposure to SCADA/HMI systems
- Engineered log-structured flash EEPROM emulation (128 KB sector, ~320 µs write latency) eliminating 1–4 second display freezes from sector erase operations
- Developed 20+ level hierarchical menu system on multiplexed 7-segment display with button debounce, runtime IP/calibration configuration, and password-protected settings

---

### IoT Intern — Emertxe Information Technologies
*Sep 2024 – Nov 2024 · Hyderabad, India*

- Designed end-to-end embedded IoT solutions (sensors → firmware → cloud)
- Developed reusable C drivers for peripherals and communication modules
- Performed unit testing and hardware-in-loop validation using PICSimLab
- Documented design decisions, tests, and results using SDLC-style workflows

---

## Certifications

| Certification | Institute | Key Topics |
|:---|:---|:---|
| IoT Internship | Emertxe InfoTech | Industrial IoT, sensor interfacing, cloud |
| Advanced C Programming | Bharat Acharya Education | Pointers, memory management |
| 8086 Microprocessor | Bharat Acharya Education | CPU architecture, assembly, interrupts |
| ARM7 Microcontroller | Bharat Acharya Education | 32-bit architecture, peripherals, drivers |
| ARM Cortex-M 101 | PyjamaBrah | Cortex-M, exceptions, peripherals |
| GNU Make and Build Systems | PyjamaBrah | Makefiles, cross-compilation |
| C Programming on Raspberry Pi | Udemy | Linux GPIO, file I/O, hardware access |

---

## Current Learning Focus

- Embedded Linux: Character drivers, device tree, kernel modules
- RTOS: FreeRTOS multitasking on ARM Cortex-M
- HAL design: Reusable hardware abstraction layers for MCUs
- Embedded security: Secure boot, cryptography, OTA updates

---

## GitHub Stats

<div align="center">

![Axay's GitHub Stats](https://github-readme-stats.vercel.app/api?username=AxayRam&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=AxayRam&layout=compact&theme=tokyonight&hide_border=true&langs_count=6)

[![GitHub Streak](https://streak-stats.demolab.com?user=AxayRam&theme=tokyonight&hide_border=true)](https://git.io/streak-stats)

</div>

---

<div align="center">

## Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/ram-axay)
[![Email](https://img.shields.io/badge/Gmail-Mail%20Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:axay19392@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AxayRam)

**Open to embedded systems, firmware engineering, and PCB design opportunities.**

*Last updated: April 2026*

</div>
