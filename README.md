# MOSFET Audio Amplifier Design

Electronics Workshop II Project

**Author:** Aditya Ranjan Padhi
**Roll Number:** 2022122001
Indian Institute of Information Technology Hyderabad

---

## Overview

This repository contains the complete design, simulation, analysis, and hardware implementation of a multi-stage audio amplifier designed as part of the Electronics Workshop II course.

The objective of the project is to amplify a low-amplitude microphone signal and drive an 8 Ω loudspeaker using a four-stage amplifier architecture.

The amplifier consists of:

* Current Mirror
* Differential Pre-Amplifier
* Active Load Stage
* Common Source Gain Stage
* Low-Pass Filter
* Class-AB Power Amplifier

---

## Project Specifications

| Parameter        | Value             |
| ---------------- | ----------------- |
| Supply Voltage   | 12 V              |
| Microphone Input | 20 mVpp           |
| Required Gain    | 500               |
| Output Voltage   | 10 Vpp            |
| Speaker Load     | 8 Ω               |
| Output Power     | Approximately 1 W |

---

## Amplifier Architecture

```text
Microphone
     │
     ▼
Differential Amplifier
     │
     ▼
Active Load Stage
     │
     ▼
Common Source Amplifier
     │
     ▼
Low-Pass Filter
     │
     ▼
Class-AB Power Amplifier
     │
     ▼
8 Ω Speaker
```

---

## Circuit Stages

### 1. Current Mirror

A MOSFET current mirror using 2N7000 devices is used to generate a stable current source.

Features:

* Approximately 1 mA bias current
* Improves differential amplifier operation
* Enhances gain and linearity

---

### 2. Differential Amplifier

The differential amplifier provides the initial voltage gain while rejecting common-mode signals.

Features:

* Differential gain ≈ 200
* Common-mode rejection
* 1 mA tail current
* 2N7000 MOSFET pair

---

### 3. Active Load

PMOS active loads replace drain resistors to:

* Increase gain
* Maintain saturation
* Provide single-ended output

Devices used:

* IRF9540N PMOS

---

### 4. Common Source Amplifier

The second gain stage increases the output swing to approximately 10 Vpp.

Features:

* Gain ≈ 35
* Source degeneration
* Bypass capacitor for increased AC gain

---

### 5. Low-Pass Filter

A passive RC filter removes high-frequency noise.

Specifications:

* Cutoff frequency: 8 kHz
* Capacitor: 1 nF
* Resistor: 20 kΩ

---

### 6. Class-AB Power Amplifier

The output stage drives an 8 Ω speaker.

Features:

* Push-pull configuration
* High efficiency
* Reduced crossover distortion

Devices:

* TIP31C
* TIP32C
* 1N4151 diodes

---

## Simulation Results

The amplifier achieves:

* Differential gain ≈ 200
* Overall gain ≈ 500
* Output swing ≈ 10 Vpp
* Low-frequency audio amplification
* Successful speaker drive

Oscilloscope and simulation results are included throughout the report.

---

## Hardware Implementation

The amplifier was physically implemented and tested.

Practical observations:

* Device parameters differed from theoretical values.
* Bias voltages required adjustment.
* Component values were tuned experimentally.
* Hardware measurements closely matched simulations.

---

## Software Used

* Proteus
* Desmos
* Oscilloscope measurements
* Manual analytical calculations

---

## Components Used

### MOSFETs

* 2N7000
* IRF9540N

### BJTs

* TIP31C
* TIP32C

### Diodes

* 1N4151

### Passive Components

* Resistors
* Ceramic capacitors
* Electrolytic capacitors

---

## Future Improvements

* THD measurement
* CMRR characterization
* Stability analysis
* Active filter implementation
* PCB design
* SPICE optimization

---

## Report

The complete project report is available in:

```text
Report.pdf
```

---

## Acknowledgements

The author would like to thank:

* Arti Yardi Ma'am
* Anshu Sarje Ma'am
* Course Teaching Assistants

for their guidance and support throughout the project.

---

## Author

**Aditya Ranjan Padhi**
Electronics and Communication Engineering
Indian Institute of Information Technology Hyderabad

---

## License

This project is provided for academic and educational purposes.

Copyright © Aditya Ranjan Padhi.
All rights reserved.
