# Electrical Design

## Introduction

Electrical engineering; design and development. Resistance, capacitance, inductance in the complex source-sink-impedance dynamics of signal-power transmission. Forward and return paths (ground shift), parasitics (leakage, distortion) and electromagnetics (EMI, EMC), form-tradeoffs (3D size, weight) and thermals (real-time distribution, ambient expansion, operating range, cycling, MTBF effects). Whiskering and corrosion (ECM, CAF), part-protection (SMT/THT shock-resist, IP rating, TVS, moisture-sensitivity, conformal-coat/encapsulation), user-safety (fuses, flammability, total-impact of material-lifecycle). Stack-up definition (layers, surface finish, impedance control), production stress (reflow conduction-paths, flux activation, soldermask-defined-pads), quality-assurance (optical inspection, QVL/PPAP), performance-limits and failure-modes (FIT, cascading-events). User experience (silkscreen, connector-mechanisms) and ease-of-maintenance (top vs bottom assembly, universal footprints/pinouts), modularity (universal interfaces, multiple firmware options).

## Reference

[Wire Gauge Chart (Powerstream)](https://www.powerstream.com/Wire_Size.htm)

## Great Resources

[Linear Circuit Design Handbook, 2008, by Analog Devices](https://www.analog.com/en/education/education-library/linear-circuit-design-handbook.html)

[Art of Electronics, 3rd Edition, by Paul Horowitz and Winfield Hill](https://archive.org/details/art-of-electronics-3e)

[Comparing Bus Solutions, rev C, by TI](https://www.ti.com/lit/an/slla067c/slla067c.pdf)

## Instruction Set Architecture

ISA: Complex, Reduced (General), Reduced (Graphics)

AMD, Intel, Nvidia

[RISC-V International](https://riscv.org/)

[ARM](https://www.arm.com)

[SiFive](https://www.sifive.com/)

## USB

[USB-IF DOC LIBRARY](https://www.usb.org/documents)

[USB2 SPEC-DL WEBPAGE, 2021-07-01](https://usb.org/document-library/usb-20-specification)

[USB4 SPEC-DL WEBPAGE, 2021-06-09](https://www.usb.org/document-library/usb4tm-specification)

[USB POWER DELIVERY SPEC-DL WEBPAGE, 2021-07-06](https://www.usb.org/document-library/usb-power-delivery)

[USB Type-C REV2.1 SPEC-DL WEBPAGE, 2021-05-25](https://www.usb.org/document-library/usb-type-cr-cable-and-connector-specification-revision-21)

[USB Type-C LOCKING SPEC-DL WEBPAGE, 2016-03-09](https://www.usb.org/document-library/usb-type-cr-locking-connector-specification)

## SPE

[SPE Summary, Microchip Webpage](https://www.microchip.com/en-us/solutions/ethernet-technology/single-pair-ethernet)

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

* vias-in-pad (0.2mm, 0.25mm)
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

## NOTES

Thermal Asymptote: When current flows through a trace, its temperature approaches infinity; when a soldering tip touches a pad, its temperature approaches the tip temperature. 

Footprints are spaced to support part-holding with tweezers (0.8mm tip-thickness).

Same-net pads can be closer together. Different-net pads should be further apart.