# Electrical Design

## Resources

### General

Description | Link
---|---
Art of Electronics, 3rd Edition, Paul Horowitz and Winfield Hill | https://archive.org/details/the-art-of-electronics-3rd-ed-2015_202008
Microcontrollers Intro (Jay Carlson) | https://jaycarlson.net/microcontrollers/
ROHM EE Knowledge Base | https://techweb.rohm.com/
Thermal Intuition (Texas Instruments, 2020) | https://www.ti.com/lit/an/slpa015/slpa015.pdf
Custom Silicon with Google | https://developers.google.com/silicon

### Circuit Design

Description | Link
---|---
Linear Circuit Design Handbook (Analog Devices, 2008) | https://www.analog.com/en/education/education-library/linear-circuit-design-handbook.html

### PCB Design

Description | Link
---|---
MFG Design Limits (Candor Industries) | https://www.candorind.com/design-limits/

### Architecture

Description | Link
---|---
Comparing Bus Solutions (Texas Instruments, 2017) | https://www.ti.com/lit/an/slla067c/slla067c.pdf

### Standards

Description | Link
---|---
Canada Electrical Code | https://www.csagroup.org/store/product/CSA%20C22.1:21/

### Reference

Description | Link
---|---
Wire Gauge Chart (Powerstream) | https://www.powerstream.com/Wire_Size.htm

## Key Knowledge

Topic | Keywords
--|--
basic | resistor, capacitor, inductor, impedance
x | ground shift, parasitics (leakage, distortion), reliability, whiskering, corrosion (ECM, CAF) 
reliability | corrosion, ionic contamination, dendritic growth, intermetallics, dielectric breakdown, charge trapping
thermal | expansion, cycling, real-time distribution, operating range, circuit-longevity (based on temp average/volatility), flammability
electromagnetics | (EMI, EMC)
mechanical | form trade-offs (weight, 3D size), part protection, SMT/THT shock-resist, ingress protection, transient voltage suppression, moisture sensitivity, conformal-coat/encapsulation
signal integrity | impedance matching/continuity, capacitive coupling, skin effect loss, trace length loss, dielectric loss, dissipation loss
power integrity | decoupling capacitor (against inductive delay), inductive bounce/ringing/kickback, snubber
PCB fabrication | layers, surface finish, impedance control, vias (landless, blind, buried, tented, filled, plated-over), soldermask-defined pads
PCB assembly | reflow conduction paths, flux activation, first-side mass limit of two-sided assembly
MCU workflow | IDE, IPE, debugger, production programmer
quality assurance | optical inspection, QVL/PPAP, MFG revision errata
extra | FIT, cascading-events, silkscreen, connector mechanisms, universal footprints/pinouts, standard interfaces, one-firmware multiple-configurations
debug | single-wire-debug (SWD), JTAG
regulatory compliance | RoHS, REACH, WEEE, CE (EU), UL Listed/Recognized, FCC, TUV, Flammability (ex. UL94V-0), EMC, RED (EU)

Qualified Vendor List (QVL), Qualified Parts List (QPL)

## Tools

### Main Design Program

[Kicad](https://www.kicad.org/) (STRONGLY RECOMMENDED)

Free, open-source, cross-platform, sponsored by CERN

#### Normal Workflow:

1. Prepare schematic symbols and layout footprints
2. Design schematic (abstract circuit design)
3. Import schematic into layout (each symbol should be mapped to a footprint)
4. Design layout (physical board design, all layers)

#### Export Workflow for PCB Fabrication 

1. Export layer files (outline/copper/soldermask/silkscreen, gerber format) and drill file (absolute, mm, excellon format).
2. Specify, as necessary, the layer stack-up (table) and any impedance control on which traces (table/graphic)
3. Specify extra info:

Specification | Notes
--|--
board material | 
finished copper thickness per layer | (ex. 2oz)
finish plating | (ex. ENIG)
finished board thickness | (ex. 1.6mm)
fabrication class | (ex. IPC2)
soldermask color | green (RCMD)
silkscreen color | white (RCMD)
depanelization | (ex. individually routed boards; one-up)
electrical testing | yes (RCMD)
board dimensional tolerance | (ex. +0mm, -0.2mm) (if important)
tented vias | (if any in design)
soldermask-defined pads | (if any in design)

#### Export Workflow for PCB Assembly:

Extras:

* Kicad Visual PCBA Plugin (for DIY PCB assembly): [InteractiveHtmlBom](https://github.com/openscopeproject/InteractiveHtmlBom)

### Assorted

Function | Name | Notes
--|--|--
Oscilloscope | Siglent SDS2104X Plus (2020) | 100-350MHz, 8-bit ADC, 2GSa/s, 4-channel
DC Power Supply | Siglent SPS5083X (2021) | 80V, 45A, 1080W, 1mV/1mA

## Design Targets

### System

Scope | Specification
--|--
measurement standard | metric
DC voltages | 48V, 24V, 12V, 5V, 3.3V

### Parts

Scope | Specification
--|--
nominal size | 1608 metric or bigger (smaller can be acceptable)
composition | RoHS (RoHS3, EU Directive 2015/863, without exemptions), halogen-free (IEC 61249-2-21), red-phosphorous-free, antimony-free, REACH (EU Regulation 1907/2006, without candidate substances)
operating temperature | -40C to 125C
reliability qualification | automotive (AEC-Q Grade 1)
quality assurance features | wettable flanks (for optical inspection; MOI/AOI)
moisture sensitivity (for assembly) | MSL 1 (low priority target)
lifetime | 10+ years
tin finish (if applicable) | matte-tin (reduced whiskering)

Special:

* glow-wire connectors (thermal ignition safety)
* soft-termination MLCC (anti-crack)
* aluminum-polymer bulk capacitors (long-life)

### PCB

Scope | Specification
--|--
impedance control | for high-frequency, precision-analog
material performance | high thermal stability (ex. low-CTE, cycling tolerance, high electromechanical stability, high thermal conductivity (ex. 0.7W/mK is a good non-ceramic benchmark), good impedance-properties (ex. low relative-permittivity, low dissipation-factor)
surface finish | ENIG
soldermask color | green (optical ergonomics)
silkscreen color | white
fabrication class | IPC2, IPC3
flame resistance | UL94-V0
mounting | M3 screws
corners | rounded (5mm+ radius)
Footprints | pad rounded-corner (0.05mm), BGA pads soldermask-defined, thermal reliefs for THT and high-maintenance SMT
PCB Assorted | Trace-to-Via Teardrop, 0.15mm thruhole dia tolerance
PCB Silkscreen | reference-designator for each part-footprint (ideal), remove designators when space is limited (use fab drawing for assembly), complete perimeter outline per footprint (incomplete outline for space; dotted/dashed outline for flux-scatter, ex. high-rel BGA assembly), functional label for every external pin
PCB Silkscreen Text Size | 1.2/0.6 mm height (normal/minimum), 0.2/0.15 mm line width (normal/minimum)
PCB Spacing (min) | 0.2mm board-edge to silkscreen-edge, 0.5mm board-edge to hole-edge
Via Size (drill dia, ring dia) | landless (0.2mm, 0.2mm), compact (0.25mm, 0.35mm), thermal (0.3mm, 0.5mm)
External Conductor Clearance (IPC-2221, min) | 0.1mm (30V class B3), 1.5mm (100V class B3), 3.2mm (170V class B3)
Internal Conductor Clearance (IPC-2221, min) | 0.05mm (30V), 0.1mm (100V), 0.2mm (300V)
quality assurance | electrical testing

PCB Silkscreen, Common Elements:

Meaning | Example | Required
--|--|--
Company Name | Guidebolt | Always If Possible
Part ID | BC2023R4 | Always If Possible
Component Designator | R1 | Always If Possible
Component Value | 1K | Optional
Batch Date/ID | 202305C1 | Optional
MFG Origin | Made in Canada with Imported Parts | Optional

### PCB Assembly

Scope | Specification
--|--
solder | lead-free solder (SAC305) containing low-activity no-halogen flux (category L0, no-clean, IPA-washable)
conformal coating | especially for condensing/high-altitude environments and compact high-voltage
underfill | for best shock and thermal cycling (especially for BGA, WLCSP)

### Protection

* Lightning Resistance
* ESD Resistance
* Overvoltage Protection (OVP)
* Overcurrent Protection (OCP)
* Reverse Polarity Protection (RPP)
* Electromagnetic Compatibility (EMC)

## PCB Parts and Circuits

### Basic

Resistor Standard: R1608M (SMT), AEC-Q200, 100V, Thin Film, Inorganic Passivation, -55C to 175C

MLC Capacitor Standard: AEC-Q200, 100V, Soft Termination, X7S/X8L

10A Diode: Diodes Inc, SBR10M100P5Q-13 (100V, 2uA leak-max 25C, 0.88V drop-max, 18ns switch, 245pF junction, -55 to 175C, 4x6.5/26mm2) (recommended)

### Controller Area Network (CAN)

Standards: CAN, CAN-FD, CAN-SiC (CiA 601-4), CAN-XL, CANOpen

CAN-FD Transceiver: (testing) (target spec: CAN-FD-SiC, AECQ-G1, 8Mbps, -58 to 58V bus fault tolerance, exposed pad, ESD tolerance, UVLO, standby, VIO, hot-swap, thermal shutdown, 3x3mm)

### RS485

RS485 Transceiver: Maxim Integrated, MAX14775EATA+ 
(-40 to 125C, 20Mbps, -65 to 65V fault tolerance, hot-swap, thermal shutdown, 3 to 5.5V input, SCP, reliable output state)
(3x3x0.75mm, TDFN8, exposed pad, side pads)
([Datasheet](https://datasheets.maximintegrated.com/en/ds/MAX14775E-MAX14776E.pdf))

We wanted 100Mbps (ex. Maxim Integrated, MAX22501E) but we highly value 60V+ fault protection (given our 48VDC power standard) and our current node MCU frequencies are too low anyway (future goal, 1GHz+ low-power compact MCUs).

### Single Pair Ethernet (SPE)

(SPE: IEEE 802.3)

[SPE Summary, Microchip Webpage](https://www.microchip.com/en-us/solutions/ethernet-technology/single-pair-ethernet)

100BASE-T1, TI, SZZY009, 2018 ([PDF](https://www.ti.com/lit/wp/szzy009/szzy009.pdf))

[OPEN Alliance](https://www.opensig.org/)

* video-audio bridge
* time-sensitive networking (TSN)

### APU

ISA: Complex, Reduced (General), Reduced (Graphics)

AMD, Intel, Nvidia

[RISC-V International](https://riscv.org/)

[ARM](https://www.arm.com)

[SiFive](https://www.sifive.com/)

* 8 Core, 16 Thread, 3+ GHz Base, iGPU
* Cache: L1-I 32KBx8, L1-D 32KBx8, L2 512KBx8, L3 16MBx1
* 64GB DDR5 RAM Support
* <30W TDP

### General Memory

Commercial SATA 2.5FF SSD: SAMSUNG, 870 EVO, 4TB (0 to 70C, 2400TBW) 
([Datasheet](https://semiconductor.samsung.com/resources/data-sheet/Samsung_SSD_870_EVO_Data_Sheet_Rev1.1.pdf))

Industrial M.2 NVMe SSD: (testing) (target spec: PCIe 3.0, NVMe 1.4, -40C to 85C, 2280FF, SLC, vibration/shock/altitude)

### MCU

* integrated development environment (IDE) (develop MCU firmware)
* integrated programming environment (IPE) (upload MCU firmware) (advanced mode, production mode)

* AECQ-G1 (-40 to 125C)
* <100uA/MHz
* ECC Dual-Bank Flash
* ECC SRAM
* Ethernet MAC

SWD over USB-C: 

* SWDIO (A2, B2) (digital signal, continuously unique, debug data)
* SWDCLK (A3, B3) (digital signal, single frequency clock, debug data rate)
* RST (A10, B10) (digital signal, simple momentary, debug start sequencing)
* VTG (A11, B11) (analog signal, constant, debug I/O voltage setting)

### Embedded Memory

https://www.fujitsu.com/jp/group/fsm/en/products/index.html

Ferroelectric RAM (non-volatile): 4Mbit (AEC-Q100), 50MHz max, 10+ trillion writes/reads (4mA max at 50MHz), 120ns write cycle

Resistive RAM (non-volatile): 12Mbit, 10MHz max, 1 million writes (1.5mA typical), unlimited reads (0.15mA typical at 5MHz)

NRAM (carbon nanotubes): 

### Thermal

Thermal Jumpers: Vishay, THJP (170W/m-K, -65C to 150C) (preferred: 1608M/3216M, tin-plated nickel termination)
([Datasheet](https://www.vishay.com/docs/60157/thjp.pdf))

XY Thermal Pads: (testing) (1800 W/m-K, -40C to 120C)

Z Thermal Pads: (testing) (28 W/m-K, -55C to 400C)

### USB

USB-C 24-pin Connector: Wurth Electronik, 632723300011 (SMT/THT standard-mount, -40C to 105C, 6.2mm insertion length,  1.9mm pin length)

[USB-IF DOC LIBRARY](https://www.usb.org/documents)

[USB2 SPEC-DL WEBPAGE, 2021-07-01](https://usb.org/document-library/usb-20-specification)

[USB4 SPEC-DL WEBPAGE, 2021-06-09](https://www.usb.org/document-library/usb4tm-specification)

[USB POWER DELIVERY SPEC-DL WEBPAGE, 2021-07-06](https://www.usb.org/document-library/usb-power-delivery)

[USB Type-C REV2.1 SPEC-DL WEBPAGE, 2021-05-25](https://www.usb.org/document-library/usb-type-cr-cable-and-connector-specification-revision-21)

[USB Type-C LOCKING SPEC-DL WEBPAGE, 2016-03-09](https://www.usb.org/document-library/usb-type-cr-locking-connector-specification)

### Connector

General-Purpose Wire-to-Wire: Molex, CP-4.5 Series (600V/10A max, 16-20/22-26AWG, -40C to 120C, polarized/color-mating, locking, genderless terminals, halogen-free)

High-Current Detachable: Wurth Electronik, THT External-Thread, 74651173 (M3, 50A, -55C to 150C, tin-plated brass)

Medium-Current Permanent Wire-to-Board: Molex, Solder-Right (1.95mm low-profile, 28AWG to 14AWG crimp, dual THT mounting, 1.6mm thick PCB compatible, -40C to 105C) (40N pullout-min for 16AWG)

Low-Current Permanent Wire-to-Board: Molex, Board-In 2.5mm Series, Right-Angle Models (3A/125V max, -40 to 125C, 0.22 to 0.35mm2 wire, halogen-free)

### Fuse

48V-Power Time-Delay Fuse: Schurter, UMT-H Series (C-UL-US/TUV/CQC, AECQ, -55 to 125C, 125VAC/72VDC, 5.3x16mm, 500A breaking)
([Datasheet](https://www.schurter.com/en/datasheet/typ_UMT-H.pdf))

Class-J Time-Delay Fuse: Mersen, AJT Series (UL/CSA, 200kA-AC/100kA-DC interrupt, open fuse indication, dual-element) (aka 4TAR9 at Grainger Canada)
([Datasheet](https://ep-us.mersen.com/sites/mersen_us/files/DS-AJT-Class-J-Time-Delay-Mersen.pdf))

Fuse Reducer: Mersen J636 (UL/CSA, 600V, adapts 30A fuse to 60A fuseholders)

### Wireless

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

https://www.digikey.com/en/articles/unlicensed-915-mhz-band-fits-many-applications-and-allows-higher-transmit-power

## Infrastructure Parts and Circuits

20A 125V Duplex Outlet: Schneider Electric, Square D, X Series, SQR42204WH (tamper-resistant, matte white, outdoor, heavy-duty)

---

NEMA 15-50 Straight Plug: Hubbell, HBL8451C

NEMA 15-50 Receptacle: Hubbell, HBL8450A (requires 63mm-hole 2-gang wallplate, deep 2-gang box)

63mm-hole 2-gang Wallplate: Hubbell, SS701 (stainless steel)

Deep 2-gang 3/4-Hub Box: Thomas and Betts, 2IHD5-2 (requires 3/4-hub closure x2, 3/4-hub fitting)

3/4-hub closure: Thomas and Betts, PLG-2-RD (zinc) (can also be sourced from 3/4-hub box included-accessories)

---

1/2-hub AC90 fitting: Thomas and Betts, CI71 (zinc alloy) 

3/4-hub AC90 fitting: Thomas and Betts, CI72 (zinc alloy)

---

Thomas and Betts, Iberville, Commercial Grade Fittings: [PDF](https://tnb.ca.abb.com/en/pdf-catalogues/fittings-and-conduit-systems/Commercial-Grade-Fittings/Iberville-Commercial-grade-fittings.pdf)

## PCB Assembly

### Underfill

[Capillary Underfill Dispensing Method (web article, GPD Global)](https://gpd-global.com/capillary-underfill-dispensing.php)

As summarized in [Test-to-Fail Methodology for Accurate Reliability and Lifetime Evaluation of eGaN Devices in Solar Applications (PDF article, EPC)](https://epc-co.com/epc/portals/0/epc/documents/articles/bp-052023.pdf), underfill significantly improves the failure rate to zero (88 devices, 1800 ramp-dwell cycles of -40C to 125C).

[Henkel Loctite Board-Level Underfill Solutions (PDF)](https://dm.henkel-dam.com/is/content/henkel/lt-8332-brochure-board-level-underfills-and-encapsulants)

## Notes

Thermal Asymptote: When current flows through a trace, its temperature approaches infinity; when a soldering tip touches a pad, its temperature approaches the tip temperature. 

Footprints are spaced to support part-holding with tweezers (0.8mm tip-thickness).

Same-net pads can be closer together. Different-net pads should be further apart.

## Other Resources

(less common use)

Description | Link
---|---
MIL-STD-202: Electrical Part Testing | [WEB-PDF](http://everyspec.com/MIL-STD/MIL-STD-0100-0299/MIL-STD-202H_CONSOLIDATED_18APR2015_52148/)
AEC Qualification | [WEB-PDF](http://www.aecouncil.com/AECDocuments.html)