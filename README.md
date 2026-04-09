<div align="center">

# Cosmin Leonardo Cozaciuc

**Electrical Engineering Student** · Year III · Universitatea Politehnica București  
Specialisation: Electric Drives & Power Electronics



</div>

---

## About Me

I'm an Electrical Engineering student at UPB (Universitatea Politehnica București) specialising in **Electric Drives and Power Electronics**. I build embedded systems and hardware from the ground up — from schematic design and PCB layout to firmware, testing and documentation.

My projects span automotive electronics, industrial automation and robotics. I work at the intersection of hardware and software, with a growing focus on integrating **local AI inference** into embedded systems for predictive control and intelligent automation.

I've presented projects at **European Researchers' Night** (Noaptea Cercetătorilor) and been published in a student technical journal. I'm currently developing a commercial-grade greenhouse automation controller as a standalone product.

---

## 🔧 Technical Stack

### Embedded & Hardware
```
Microcontrollers    Arduino (Uno, Nano, Mega, Nano Every) · ESP32 WROOM · Raspberry Pi 5
Languages           Embedded C · C++ · Python
Protocols           UART · I2C · SPI · RS-485 · Modbus RTU · ESP-NOW · Bluetooth (HC-05) · PWM
Motor Control       H-Bridge (L293D, TB6612FNG) · ESC · Servo · DC gear motors · PID control
Power Electronics   Buck converters · Linear regulators · LiPo/NiMH/Li-Ion · INA219 monitoring
Sensors             TCRT5000 · MPU-6050 · BMP280 · DHT22 · SHT31 · RS-485 industrial sensors
```

### Design & Simulation
```
PCB Design          KiCad (schematic + layout) · EasyEDA
Circuit Simulation  Proteus · LTSpice
CAD                 Autodesk Fusion 360 · AutoCAD
MATLAB              Simulink · Simscape · Signal Processing · PI/PID algorithms
```

### AI & Software
```
AI Integration      Gemma 4 (local inference on Raspberry Pi 5) · LLM prompt engineering
Version Control     Git · GitHub
OS                  Linux (Raspberry Pi OS) · Windows
Design              Figma · Canva · Framer
```

### Lab Skills
```
Equipment           Oscilloscope · Multimeter · Power supply · Logic analyzer
Hands-on            Soldering (THT + SMD basics) · PCB bring-up · Hardware debugging
Documentation       Technical reports · BOM preparation · Schematic reading
```

---

## 🚀 Projects

### 🌿 [Greenhouse Automation System](https://github.com/leogamerxxl/greenhouse-automation)
> **Research & PCB Design Phase**

Industrial-grade precision agriculture controller for a **0.7ha greenhouse** — designed as a standalone commercial product. Single enclosure, plug-and-play deployment.

- **Control core:** Portenta H7 / Arduino Giga R1 + Raspberry Pi 5 (8GB)
- **AI layer:** Gemma 4 running locally — predictive control, anomaly detection, crop recommendations
- **Sensor bus:** RS-485 / Modbus RTU — temperature, humidity, light, anemometer per zone
- **Actuation:** 4× AC motor (reversible via relay) for side panels, irrigation, ventilation per zone
- **Telemetry:** LoRa 868MHz field → ESP32 WiFi gateway → mobile app
- **HMI:** Waveshare 10" AMOLED touch — industrial SCADA-style UI, fully autonomous offline
- **PCB:** Custom board — aluminium anodised enclosure, IP65, integrated LoRa antenna, M12 connectors

`Raspberry Pi 5` `Arduino Giga R1` `RS-485` `Modbus RTU` `LoRa 868MHz` `KiCad` `Gemma 4` `SCADA`

---

### 🚗 [Steering Wheel Adapter — Renault Clio 5 → Dacia Logan I](https://github.com/leogamerxxl/steering-wheel-adapter)
> **Ongoing**

Wireless gateway between OEM Clio 5 steering wheel controls and an aftermarket infotainment unit on a Logan I. Solved a real automotive integration problem with zero infrastructure dependency.

- **Architecture:** Two ESP32 WROOM boards communicating via **ESP-NOW** (peer-to-peer, no router)
- **Latency:** ~1ms button response — imperceptible to the driver
- **Wiring:** Direct GPIO connections to physical steering wheel buttons — no LIN bus required
- **Power:** 12V automotive → 3.3V regulated per board

`ESP32 WROOM` `ESP-NOW` `Embedded C` `Automotive` `GPIO` `Peer-to-peer wireless`

---

### 🤖 [Wall Crawler — Vertical Surface Robot](https://github.com/leogamerxxl/wall-crawler)
> **v1 Prototype · v2 In Design**

Robot with active adhesion for vertical surfaces. v1 presented at **European Researchers' Night** and published in student journal **Sirius**.

**v2 improvements (in design):**
- Brushless motor + CFD-optimised duct — calculated ΔP ≥ 1.8 kPa (68% above minimum)
- Closed-loop pressure control via BMP280 + PID
- IMU tilt detection (MPU-6050) — adaptive suction setpoint per surface angle
- TB6612FNG motor driver — 95% efficiency vs 70% (L298N)
- INA219 current monitoring per rail — overcurrent protection
- Non-blocking firmware — millis()-based task scheduler, zero delay()

`Arduino` `TB6612FNG` `MPU-6050` `BMP280` `INA219` `PID` `Brushless` `ESC`

---

### 🚙 [Bluetooth Mini Tank — v1] ([https://github.com/leogamerxxl/Mini-Tank-Bluetooth-Controlled-with-Turret])
> **v1 Completed · v2 In Design**

Tracked vehicle with 4 DC motors, 2-axis servo turret (360° pan + 90° tilt), controlled via Android app using ASCII commands over Bluetooth.

- **Steering:** Differential PWM — smooth arcs, not jerky pivots
- **Turret:** Pan servo (continuous 360°) + tilt servo (90°) — mapped to app buttons
- **Driver:** L293D dual H-bridge — 4 channels, motors wired in parallel pairs
- **Control app:** Bluetooth RC Car (Android) — full ASCII command map documented

`Arduino Uno` `L293D` `HC-05` `PWM` `Servo` `Android` `3D Print`

---

### ➡️ [Line Follower PID — v1](https://github.com/leogamerxxl/line-follower-pid)
> **v1 Completed · v2 In Design**

High-speed line follower with PID control on Arduino Nano. 5-sensor TCRT5000 array with weighted position error and automatic calibration at startup.

- **Algorithm:** Weighted average across 5 sensors → PID error → differential motor speed
- **Calibration:** 3-second auto-calibration on boot — normalises per ambient light conditions
- **Anti-windup:** Integral clamped ±50 — prevents overshoot on straight sections
- **Line-lost recovery:** Last known error × 1.5 — robot recovers instead of stopping

`Arduino Nano` `TCRT5000×5` `L293D` `PID` `Embedded C` `Acrylic chassis`

---


## 📚 Education

### Universitatea Politehnica București *(2023 – present)*
**B.Eng. Electrical Engineering**  
Specialisation: **Electric Drives and Power Electronics**

| Course | Relevance |
|--------|-----------|
| Electric Drives | Motor control theory, drive systems |
| Power Electronics | Converters, inverters, rectifiers |
| Electrical Machines | AC/DC machines, transformers |
| Static Converters | Buck, boost, H-bridge topologies |
| Measurement Systems | Sensors, signal conditioning, ADC |
| Systems Theory | Control systems, transfer functions, stability |
| Electronics | Analogue & digital circuit design |

### Colegiul Național Eudoxiu Hurmuzachi, Rădăuți *(2019 – 2023)*
**Baccalaureate — Mathematics & Computer Science**  
Cambridge C1 English Certificate

---

## 🤝 Volunteering

**IT & Media — ASIE** *(Association of Electrical Engineering Students, UPB)*  
2023 – present · Bucharest  
Banner and social media design using Figma. Active member — coordinator role declined to prioritise academic performance.

**Logistics — Voluntari UNS UPB**  
2023 – present · Bucharest  
Event logistics at major UPB events: Polifest, Autofest, and institutional events.

---

## 📊 Recognition

| Event | Details |
|-------|---------|
| 🏛️ European Researchers' Night | Presented Wall Crawler robot — public EU science event |
| 📰 Published — Sirius Journal | Technical article on Wall Crawler — CN Eudoxiu Hurmuzachi |
| 🎓 Cambridge C1 English | Certified advanced English proficiency |

---

## 🌐 Languages

| Language | Level | Certificate |
|----------|-------|-------------|
| Romanian | Native | — |
| English | C1 Advanced | Cambridge Certificate |
| German | B1/B2 | 2 years intensive (6h/week) |

---

<div align="center">

*Open to internships and collaborations in embedded systems, automotive electronics and industrial automation.*  
 · 🌐 [cozaciuc.dev](https://cozaciuc.dev)

</div>
