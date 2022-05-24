# Electrical Design

## Introduction

Electrical engineering; design and development. Resistance, capacitance, inductance in the complex source-sink-impedance dynamics of signal-power transmission. Forward and return paths (ground shift), parasitics (leakage, distortion) and electromagnetics (EMI, EMC), form-tradeoffs (3D size, weight) and thermals (real-time distribution, ambient expansion, operating range, cycling, MTBF effects). Whiskering and corrosion (ECM, CAF), part-protection (SMT/THT shock-resist, IP rating, TVS, moisture-sensitivity, conformal-coat/encapsulation), user-safety (fuses, flammability, total-impact of material-lifecycle). Stack-up definition (layers, surface finish, impedance control), production stress (reflow conduction-paths, flux activation, soldermask-defined-pads), quality-assurance (optical inspection, QVL/PPAP), performance-limits and failure-modes (FIT, cascading-events). User experience (silkscreen, connector-mechanisms) and ease-of-maintenance (top vs bottom assembly, universal footprints/pinouts), modularity (universal interfaces, multiple firmware options).

## Reference

[Canadian Electrical Code, 25th Edition](https://www.csagroup.org/store/product/CSA%20C22.1:21/)

[Wire Gauge Chart (Powerstream)](https://www.powerstream.com/Wire_Size.htm)

## Resources

[Linear Circuit Design Handbook, 2008, by Analog Devices](https://www.analog.com/en/education/education-library/linear-circuit-design-handbook.html)

[Art of Electronics, 3rd Edition, by Paul Horowitz and Winfield Hill](https://archive.org/details/art-of-electronics-3e)

Thermal Intuition, TI, SLPA015 ([PDF](https://www.ti.com/lit/an/slpa015/slpa015.pdf))

Bus Solutions, TI, SLLA067C ([PDF](https://www.ti.com/lit/an/slla067c/slla067c.pdf))

## MFG

[Design Limits, Candor Webpage](https://www.candorind.com/design-limits/)

## Design Quality Standards and Targets

METRIC, qualified vendor list (QVL), qualified parts list (QPL)

Composition: RoHS-compliant (RoHS3, EU Directive 2015/863, without exemptions), halogen-free (IEC 61249-2-21), red-phosphorous-free, antimony-free, REACH-compliant (EU Regulation 1907/2006, without candidate substances)

Reliability: 10yr+ MTBF, IPC-2/3 fab class, ENIG surface finish, AEC-Q (target, grade 1), UL94-V0 flame resistance, glow-wire connectors, tin-finishes are matte-tin (reduced whiskering), operating temperature -40C to 85C MIN (-40C to 125C TARGET), MSL1 TARGET, soft-termination MLCCs (bend-crack resistance), aluminum-polymer bulk capacitors (high lifetime)

Form: 1608 metric size, 4xM3 mounting holes, rounded corners (5mm+ radius), green soldermask (optical ergonomics), white silkscreen

Options: conformal-coating, encapsulation

MFG: electrical testing, impedance control (for high-frequency, precision-analog)

Material: high thermal stability (ex. low-CTE, cycling tolerance, high electromechanical stability, high thermal conductivity (ex. 0.7W/mK is a good non-ceramic benchmark), good impedance-properties (ex. low relative-permittivity, low dissipation-factor).

Assembly: lead-free solder (SAC305 preferred), low-activity no-halogen flux (category L0) (no-clean IPA-washable preferred)

Footprints: pad rounded-corner (0.05mm), BGA pads soldermask-defined, thermal reliefs for THT and high-maintenance SMT

Vias: full-depth preferred

Via Standards (type, drill dia, ring dia):

* vias-in-pad (0.2mm, 0.3mm)
* compact (0.25mm, 0.3mm)
* traditional (0.4mm, 0.8mm)
* thermal (0.5mm, 0.6mm)

Other: board-edge to silkscreen (0.2mm+)

Silkscreen: reference-designator for each part-footprint (ideal), remove designators when space is limited (use fab drawing for assembly), complete perimeter outline per footprint (incomplete outline for space; dotted/dashed outline for flux-scatter, ex. high-rel BGA assembly), functional label for every external pin

Silkscreen Standard:

* Company Name (ex. Guidebolt)
* Part ID (ex. SOMEPART-MK1R3)
* Batch ID (ex. 2021-01-20_XYZFAB)
* MFG Origin (ex. Made in Canada with imported parts)

Special Markings: flammability (ex. UL94V-0), WEEE directive, RoHS, REACH, CE, UL Recognized, UL Listed

## Passive

Resistor Standard: R1608M (SMT), AEC-Q200, 100V, Thin Film, Inorganic Passivation, -55C to 175C

MLC Capacitor Standard: AEC-Q200, 100V, Soft Termination, X7S/X8L

## Diode

10A: Diodes Inc, SBR10M100P5Q-13 (100V, 2uA leak-max 25C, 0.88V drop-max, 18ns switch, 245pF junction, -55 to 175C, 4x6.5/26mm2) (recommended)

## Controller Area Network (CAN)

Standards: CAN, CAN-FD, CAN-SiC (CiA 601-4), CAN-XL, CANOpen

CAN-FD Transceiver: (testing) (target spec: CAN-FD-SiC, AECQ-G1, 8Mbps, -58 to 58V bus fault tolerance, exposed pad, ESD tolerance, UVLO, standby, VIO, hot-swap, thermal shutdown, 3x3mm)

## RS485

RS485 Transceiver: Maxim Integrated, MAX14775EATA+ 
(-40 to 125C, 20Mbps, -65 to 65V fault tolerance, hot-swap, thermal shutdown, 3 to 5.5V input, SCP, reliable output state)
(3x3x0.75mm, TDFN8, exposed pad, side pads)
([Datasheet](https://datasheets.maximintegrated.com/en/ds/MAX14775E-MAX14776E.pdf))

We wanted 100Mbps (ex. Maxim Integrated, MAX22501E) but we highly value 60V+ fault protection (given our 48VDC power standard) and our current node MCU frequencies are too low anyway (future goal, 1GHz+ low-power compact MCUs).

## Data Storage

Commercial SATA 2.5FF SSD: SAMSUNG, 870 EVO, 4TB (0 to 70C, 2400TBW) 
([Datasheet](https://semiconductor.samsung.com/resources/data-sheet/Samsung_SSD_870_EVO_Data_Sheet_Rev1.1.pdf))

Industrial M.2 NVMe SSD: (testing) (target spec: PCIe 3.0, NVMe 1.4, -40C to 85C, 2280FF, SLC, vibration/shock/altitude)

Embedded Flash: Ferroelectric RAM (testing) (target spec: SMT, AECQ-G1, on-die ECC, 2Mbit, 10^14 writes/bit, 10+ year data retention)

## CPU

* 8 Core, 16 Thread, 3+ GHz Base, iGPU
* Cache: L1-I 32KBx8, L1-D 32KBx8, L2 512KBx8, L3 16MBx1
* 64GB DDR5 RAM Support
* <30W TDP

## MCU

* AECQ-G1 (-40 to 125C)
* <100uA/MHz
* ECC Dual-Bank Flash
* ECC SRAM
* Ethernet MAC

## Thermal

Thermal Jumpers: Vishay, THJP (170W/m-K, -65C to 150C) (preferred: 1608M/3216M, tin-plated nickel termination)
([Datasheet](https://www.vishay.com/docs/60157/thjp.pdf))

XY Thermal Pads: (testing) (1800 W/m-K, -40C to 120C)

Z Thermal Pads: (testing) (28 W/m-K, -55C to 400C)

## USB

USB-C 24-pin Connector: Wurth Electronik, 632723300011 (SMT/THT standard-mount, -40C to 105C, 6.2mm insertion length,  1.9mm pin length)

[USB-IF DOC LIBRARY](https://www.usb.org/documents)

[USB2 SPEC-DL WEBPAGE, 2021-07-01](https://usb.org/document-library/usb-20-specification)

[USB4 SPEC-DL WEBPAGE, 2021-06-09](https://www.usb.org/document-library/usb4tm-specification)

[USB POWER DELIVERY SPEC-DL WEBPAGE, 2021-07-06](https://www.usb.org/document-library/usb-power-delivery)

[USB Type-C REV2.1 SPEC-DL WEBPAGE, 2021-05-25](https://www.usb.org/document-library/usb-type-cr-cable-and-connector-specification-revision-21)

[USB Type-C LOCKING SPEC-DL WEBPAGE, 2016-03-09](https://www.usb.org/document-library/usb-type-cr-locking-connector-specification)

## Connector

General-Purpose Wire-to-Wire: Molex, CP-4.5 Series (600V/10A max, 16-20/22-26AWG, -40C to 120C, polarized/color-mating, locking, genderless terminals, halogen-free)

High-Current: Wurth Electronik, THT External-Thread, 74651173 (M3, 50A, -55C to 150C, tin-plated brass)

Low-Current Permanent Wire-to-Board: Molex, Board-In 2.5mm Series, Right-Angle Models (3A/125V max, -40 to 125C, 0.22 to 0.35mm2 wire, halogen-free)

## Fuse

48V-Power Time-Delay Fuse: Schurter, UMT-H Series (C-UL-US/TUV/CQC, AECQ, -55 to 125C, 125VAC/72VDC, 5.3x16mm, 500A breaking)
([Datasheet](https://www.schurter.com/en/datasheet/typ_UMT-H.pdf))

Class-J Time-Delay Fuse: Mersen, AJT Series (UL/CSA, 200kA-AC/100kA-DC interrupt, open fuse indication, dual-element) (aka 4TAR9 at Grainger Canada)
([Datasheet](https://ep-us.mersen.com/sites/mersen_us/files/DS-AJT-Class-J-Time-Delay-Mersen.pdf))

Fuse Reducer: Mersen J636 (UL/CSA, 600V, adapts 30A fuse to 60A fuseholders)

## Single Pair Ethernet (SPE)

(SPE: IEEE 802.3)

[SPE Summary, Microchip Webpage](https://www.microchip.com/en-us/solutions/ethernet-technology/single-pair-ethernet)

100BASE-T1, TI, SZZY009, 2018 ([PDF](https://www.ti.com/lit/wp/szzy009/szzy009.pdf))

[OPEN Alliance](https://www.opensig.org/)

* video-audio bridge
* time-sensitive networking (TSN)

## Wireless

(Wifi: IEEE 802.11)

[Wifi Alliance](https://www.wi-fi.org/)

Wifi Antenna: 2.4/5/6GHz, <1.5 VSWR, 80%+ efficiency, omnidirectional, -30 to 85C, SMA-M

* 2400 to 2485 MHz
* 5150 to 5850 MHz
* 5925 to 7125 MHz

RF Bulkhead: SMA-F to SMA-F, 18GHz max, <1.22 VSWR, <2mohm, -65 to 165C, 50 ohm impedance

* stainless steel body
* beryllium copper contact
* gold finish (body+contact)
* PTFE insulation
* silicone seal

RF Cable: SMA-M to SMA-M, 8GHz max, <1.5 VSWR, gold finish, 50 ohm impedance

## Instruction Set Architecture

ISA: Complex, Reduced (General), Reduced (Graphics)

AMD, Intel, Nvidia

[RISC-V International](https://riscv.org/)

[ARM](https://www.arm.com)

[SiFive](https://www.sifive.com/)

## NOTES

Thermal Asymptote: When current flows through a trace, its temperature approaches infinity; when a soldering tip touches a pad, its temperature approaches the tip temperature. 

Footprints are spaced to support part-holding with tweezers (0.8mm tip-thickness).

Same-net pads can be closer together. Different-net pads should be further apart.