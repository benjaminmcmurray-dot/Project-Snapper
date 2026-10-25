# 🦈 Project Snapper (Snapper-ROV)

A modular, high-performance **8-Thruster Vectored Underwater ROV (6-DOF)** built for coastal exploration down to a 40m nominal (80m max) depth rating[cite: 3]. 

---

## 🎯 Project Overview & Specs
* **Vehicle Type:** 50cm Mid-size 8-Thruster Vectored ROV (Full 6 Degrees of Freedom)[cite: 3]
* **Depth Rating:** 40m nominal / 80m max (10 bar rating)[cite: 3]
* **Estimated Budget:** ~$2,145 NZD[cite: 2]
* **Control Interface:** Xbox Controller via QGroundControl / MAVLink over local BlueOS network[cite: 3]
* **Video Feed:** Low-latency RTSP video stream viewed via laptop HUD[cite: 3]

---

## ⚙️ Core Architecture

### 1. Propulsion & Thruster Layout (8-Thruster Config)
* **Configuration:** 4 horizontal vectored thrusters (Surge, Sway, Yaw) + 4 vertical vectored thrusters (Heave, Pitch, Roll)[cite: 3].
* **Motors:** DIY waterproofed outrunner BLDC motors featuring epoxy-potted stator windings, full ceramic/316 stainless steel bearings, and custom 3D-printed ducted nozzles[cite: 3].
* **ESCs:** 8x 30A bi-directional reversible ESCs[cite: 3].

### 2. Pressure Hull & Exoskeleton Frame
* **Hull Enclosure:** 4" (100mm ID) x 8mm wall cast acrylic tube with 6061-T6 aluminum end-caps and dual Viton O-ring seals[cite: 3].
* **Frame:** Modular 3D-printed PETG/ASA exoskeleton rail system with an internal sliding quick-release electronics tray[cite: 3].

### 3. Avionics & Topside Station
* **Brains:** Raspberry Pi 4 (running BlueOS) paired with a Pixhawk flight controller running ArduSub[cite: 3].
* **Topside Case:** Rugged IP67 field case housing a local Wi-Fi router, HomePlug Ethernet-over-power adapter, and field battery[cite: 3].
* **Tether:** 100m thin neutral-buoyancy tether handling power and high-bandwidth signal data[cite: 3].

---

## 📂 Repository Structure
```text
Project-Snapper/
├── cad/             # 3D printable PETG/ASA exoskeleton STL/STEP files & end-caps
├── electronics/     # Wiring diagrams, pinouts, and schematics
├── docs/            # Build logs, safety guidelines, and BOM.csv spreadsheet
├── src/             # Custom scripts, BlueOS extensions, and configuration files
└── README.md
