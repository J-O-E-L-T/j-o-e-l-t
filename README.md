# ⚡ Joel T. (`@J-O-E-L-T`)

### Founder & Principal Systems Architect @ [49Caliber Labs](https://github.com/49Caliber-Labs)
**Systems Builder | RF & LoRa Mesh Architect | Environmental Telemetry & AI-Augmented Application Developer**

[![49Caliber Labs](https://img.shields.io/badge/Founder-49Caliber_Labs-0b2545.svg)](https://github.com/49Caliber-Labs)
[![MeshMule-Core](https://img.shields.io/badge/Open_Source-MeshMule--Core_(915_MHz_DTN)-10b981.svg)](https://github.com/49Caliber-Labs/MeshMule-core)
[![BiteWindow Vector7](https://img.shields.io/badge/Telemetry_Engine-BiteWindow_Vector7-00d2ff.svg)](https://github.com/49Caliber-Labs/bitewindow-vector7)
[![RF Engineering](https://img.shields.io/badge/RF_Design-915_MHz_LoRa_%26_Antennas-ffb800.svg)](#3-computational-rf--antenna-design)
[![GitHub Sponsors](https://img.shields.io/badge/Sponsor-GitHub_Sponsors-ff1e56.svg)](#-github-sponsors--research-grants-why-back-my-work)

---

I specialize in building resilient, field-grade software and hardware systems by pairing deep domain physics with high-velocity AI-augmented engineering. From bit-packed 915 MHz LoRa delay-tolerant mesh protocols and computational RF antenna design to nationwide hydrological telemetry pipelines and autonomous dispatch engines, my focus is on turning ambitious technical concepts into verifiable, production-ready tools.

---

## 🛰️ Active Projects & Engineering Highlights

### 1. [`MeshMule-Core`](https://github.com/49Caliber-Labs/MeshMule-core) — Open-Source 915 MHz Citizen-Science DTN, Barometric Phased-Array & GPS-Denied SAR Engine
An open-source (MIT) off-grid scientific data-mule protocol and backcountry situational-awareness stack built for **USGS, NPS, USFS, NOAA, CDFW, and Search-and-Rescue (SAR)** operations in zero-cellular wilderness corridors:
- **32-Byte Binary Wire Protocol (`0xA1` & `0xB2`):** Sub-65ms 915 MHz LoRa frames packing 6-character station callsigns, 24-bit fixed-point coordinates ($\approx 1.1\text{ m}$ precision), 3 scientific telemetry channels, 5 historical delta steps, battery-RTC relative-age drift correction, and a **32-bit keyed SipHash-2-4 MAC**.
- **2D Distributed Barometric Phased-Array ($\nabla P$):** Normalizes raw peer-node barometers to sea level ($P_0$) via the international hypsometric equation and solves a 2D Ordinary Least Squares (OLS) pressure plane to compute approaching squall-front bearing ($^\circ$) and velocity ($\text{mph}$) completely off-grid.
- **GPS-Denied Canyon SAR Trilateration:** Combines barometric altimeter elevation contour lock ($\pm 14\text{ ft}$) with a 12-iteration damped Gauss-Newton 915 MHz LoRa RSSI/SNR trilateration solver when satellite GNSS fails or is occluded by canyon walls.
- **Passive 915 MHz RF Atmospheric Tomography:** Uses bistatic Friis Free-Space Path Loss ($FSPL$) vs. measured LoRa RSSI/SNR residuals to invert boundary-layer refractivity ($K$-factor, ITU $N$-units) and detect thermal inversion ducting.
- **Agency Collector Gateway:** Persistent `IndexedDB` mobile outbox with multi-mule witness deduplication (`stationCallsign:sequenceNumber`), zero-identity contributor tokens (`MULE-XXXX-XXXX`), and one-click **RFC 7946 GeoJSON** and **CSV** exports.

---

### 2. [`BiteWindow Vector7`](https://github.com/49Caliber-Labs/bitewindow-vector7) — Off-Grid Marine & Backcountry Telemetry Platform
A field-ready environmental prediction and hydrological telemetry engine running a 7-vector analytical algorithm to calculate real-time feeding probabilities and strike windows across the United States:
- **Nationwide Public Data Ingestion:** Indexes **34,651 USGS waterways** across all 50 states, automatically querying and normalizing live discharge (CFS), gauge height, water temperature, barometric trend Z-scores, and astronomical solunar transits.
- **Virtual Waterway Triangulation Engine:** Dynamically discovers proximal live USGS monitoring stations for unmonitored backcountry creeks and alpine lakes to synthesize localized microclimate flow and thermal models.
- **Embedded MeshMule-Core LoRa Bridge:** Pairs directly with ESP32-S3 and nRF52840 Meshtastic transceivers over **Web Bluetooth (BLE)**, **USB-C Serial**, and **Wi-Fi HTTP** for zero-cellular situational awareness.

---

### 3. Computational RF & Antenna Design
Practical RF design workflow bridging physical antenna geometry with electromagnetic simulation:
- Evaluates structural dimensions, dielectric substrate materials, impedance matching, and radiation patterns against established RF physics models prior to physical fabrication.
- Compresses hardware prototyping cycles by filtering early concepts down to high-gain, low-VSWR 915 MHz ISM candidates before cutting physical metal for bench and backcountry range verification.

---

### 4. Legacy Sports Automation Engine (Open-Source Release)
Re-engineered and automated a 40-year-old family and community tradition into a full-featured digital management platform:
- **Core Capabilities:** Real-time live scoreboard tracking, automated pick submission & admin validation engines, and continuous data aggregation via custom API pipelines.
- **Autonomous Dispatch Pipeline:** Pulls live league statistics, injuries, and standings to draft customized, voice-infused recap dispatches directly to Gmail drafts for single-click human approval—reducing administrative overhead to under five minutes per week.

---

## 🛠️ Tech & Engineering Stack

| Domain | Core Technologies & Capabilities |
| :--- | :--- |
| **RF & Off-Grid Hardware** | 915 MHz LoRa (SX1262 / LR1110), ESP32-S3, nRF52840, Meshtastic Protobuf (`0x94 0xC3`), Web Bluetooth GATT, Web Serial UART, RF Antenna Prototyping |
| **Telemetry & Math Engines** | TypeScript, React 19, Bit-Packed Binary Codecs (`DataView`), SipHash-2-4 MAC, Ordinary Least Squares ($\nabla P$), Gauss-Newton RF Trilateration, Friis FSPL Tomography |
| **Data & Cloud Pipelines** | USGS Water Services API, NOAA/NWS Telemetry, RFC 7946 GeoJSON, IndexedDB Offline Outboxes, Workbox PWA Service Workers, Google Apps Script & Webhook Automation |

---

## 💖 GitHub Sponsors & Research Grants: Why Back My Work?

Sponsorship and research grants directly sustain the transition of physical RF and digital telemetry prototypes into thoroughly documented, open-source public infrastructure:

1. **Open-Source Citizen-Science Infrastructure (`MeshMule-Core`):** Supporting ongoing releases of 32-byte binary sensor codecs, agency GeoJSON/CSV collector gateways, and backcountry delay-tolerant networking tools.
2. **RF & Solar Sensor Node Prototyping:** Funding bench-test materials, SMA/N-type RF connectors, 915 MHz LoRa transceiver boards, solar/LiFePO4 enclosures, and field-testing equipment.
3. **Practical Field Documentation:** Backing in-depth technical write-ups covering off-grid data routing, GPS-denied canyon positioning, human-in-the-loop automation, and AI-accelerated RF modeling.

### Sponsorship & Collaboration Tiers

| Tier | Monthly Contribution | Benefits & Impact |
| :--- | :--- | :--- |
| ☕ **Tip Jar & Community Supporter** | **$5 / month** | Keeps the coffee hot and telemetry scripts running. Name listed on open-source project READMEs. |
| 📡 **Hardware & RF Sustainer** | **$20 / month** | Offsets component costs for ESP32-S3 / nRF52840 LoRa boards, test antennas, and field-sensor iterations. |
| 🛰️ **Architecture Collaborator** | **$75 / month** | Direct access to project architecture discussions, early previews of off-grid communication experiments, and priority feature requests for open toolsets. |
| 🏛️ **Institutional & Conservation Grant Partner** | **Custom / Grant** | Turnkey custom sensor-domain allocations (`0xA1`), basin-specific SipHash-2-4 key provisioning, and field deployment support for NPS, USFS, USGS, CDFW, and non-profit watershed coalitions. |
