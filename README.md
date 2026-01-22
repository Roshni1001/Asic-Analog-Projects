# ASIC / Analog IC Design Projects

Collection of transistor-level IC design mini-projects implemented in **Cadence** Virtuoso, focused on fundamentals useful for an ASIC / Analog Design Engineer role.

## Overview

This repository documents:
- Basic CMOS logic gates (inverter, NAND, NOR) at schematic level
- Resistive-load amplifier design and biasing
- Differential amplifier design with basic performance characterization

All projects include schematics and simulation plots (DC/AC/transient) captured from Virtuoso.

## Tools and Technology

- **EDA tool**: Cadence Virtuoso (schematic + simulation)
- **Simulator**: Spectre / ADE
- **Technology**: [ gpdk180 / 180 nm CMOS]
- **Supply**: [e.g. 1.8 V / 3.3 V]
- **Temperature**: Typical simulations at [e.g. 27 °C]

> Note: No PDK or proprietary design files are shared; this repo only contains screenshots and documentation.

---

## 1. Basic CMOS Gates

### 1.1 Inverter

- Implemented a standard CMOS inverter.
- Verified correct logic transfer characteristics and noise margins using DC sweep and transient simulations.

Example schematic and waveform (replace with your images):

![<img width="330" height="325" alt="CMOSInvckt_schematic" src="https://github.com/user-attachments/assets/497ef29c-1de1-40c7-b6bc-4d02796ca344" />
]

**Key points:**
- Checked \( V_{IL} \), \( V_{IH} \), noise margins from DC transfer curve.
- Observed rise/fall time differences based on PMOS/NMOS sizing.

### 1.2 NAND and NOR Gates

- Designed 2-input CMOS NAND and NOR using series/parallel transistor configurations.
- Verified truth tables and propagation delay using transient simulations.

Example images:

![<img width="417" height="595" alt="CMOS_NAND_schematic" src="https://github.com/user-attachments/assets/b73ad43d-1a95-4050-aa21-e66548a442a0" />
]
**What was studied:**
- Effect of series stacking on delay for NAND vs NOR.
- Basic sizing to balance pull-up and pull-down networks.

---

## 2. Resistive-Load Amplifier

Designed a single-stage resistive-load amplifier to understand gain, biasing and trade-off between gain, swing and power.

![<img width="422" height="489" alt="RLckt_schematic" src="https://github.com/user-attachments/assets/4ee7c0bb-68a4-476b-b3ac-01c41d39fd07" />
]
![<img width="557" height="585" alt="RLckt_DC Tran_analysis" src="https://github.com/user-attachments/assets/b35de41e-4230-49d4-96b1-80338f3584f0" />
]

**Design targets (example, edit with your actual numbers):**
- Midband gain ≈ 10–20 V/V
- Bandwidth in the [x] kHz / MHz range
- Operated from [VDD value] with [bias current]

**Simulations:**
- **DC operating point** to verify biasing and overdrive regions.
- **AC analysis** to extract gain and 3 dB bandwidth.
- **Transient** to check large-signal swing and distortion.

---

## 3. Differential Amplifier

Implemented a basic differential pair to study differential gain, common-mode gain and CMRR.

![<img width="383" height="361" alt="CMOS_DiffAmp_schematic" src="https://github.com/user-attachments/assets/2b9b8b58-9525-4826-9ad1-619dc8288e75" />]

![<img width="375" height="367" alt="DiffAmp_TestBenchSymbol" src="https://github.com/user-attachments/assets/a347a79d-1060-4938-98f8-88183d4f3f41" />
]
![<img width="537" height="565" alt="DiffAmp_DC Tran_analysis" src="https://github.com/user-attachments/assets/d2e0f833-e902-4c5c-b4dd-f10b57092983" />
]

**Focus areas:**
- Biasing using current source tail.
- Measuring differential gain \( A_d \) and common-mode gain \( A_{cm} \).
- Calculating CMRR \( = 20 \log_{10}(A_d / A_{cm}) \).

**Simulations:**
- Differential and common-mode AC sweeps.
- Transient response for step differential input.
- Output swing limitations based on headroom.

---

## 4. Future Work / To-Do

Planned additions to this repo:
- Add layout screenshots (DRC/LVS clean) for selected blocks.
- Characterization across PVT corners.
- More advanced blocks (current mirrors, simple op-amp, comparators).

---

## Contact

If you are interested in my VLSI / ASIC work or want more details about these designs:

- **GitHub**: [Roshni1001](https://github.com/your-username)
- **Email**: [23f3000143@es.study.iitm.ac.in]

