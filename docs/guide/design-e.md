# Design E

Official Guidebolt Electrical Design Guide

Last Updated: 2021-03-22

## Introduction

Great electrical designers have a deep understanding of resistance, capacitance, inductance in the complex source-sink-impedance dynamics of signal-power transmission. Forward and return paths (ground shift), parasitics (leakage, distortion) and electromagnetics (EMI, EMC), form-tradeoffs (size/weight) and thermals (real-time distribution, ambient expansion, operating range, cycling, MTBF effects). Whiskering and corrosion (ECM, CAF), part-protection (SMT/THT shock-resist, IP rating, TVS, moisture-sensitivity, conformal-coat/encapsulation), user-safety (fuses, flammability, total-impact of material-lifecycle). Stack-up definition (layers, surface finish, impedance control), production stress (reflow conduction-paths, flux activation, soldermask-defined-pads), quality-assurance (optical inspection, QVL/PPAP), performance-limits and failure-modes (FIT, cascading-events). User experience (silkscreen, connector-mechanisms) and ease-of-maintenance (top vs bottom assembly, universal footprints/pinouts), modularity (universal interfaces, multiple firmware options).

## Great Resources

[Linear Circuit Design Handbook, 2008, by Analog Devices](https://www.analog.com/en/education/education-library/linear-circuit-design-handbook.html)

[Art of Electronics, 3rd Edition, by Paul Horowitz and Winfield Hill](https://archive.org/details/art-of-electronics-3e)

[Comparing Bus Solutions, rev C, by TI](https://www.ti.com/lit/an/slla067c/slla067c.pdf)

## Basics

Unit Standard: Metric. Dimensions are mostly mm and um.

Company-wide Lists: qualified vendor list (QVL), qualified parts list (QPL), shared symbol/footprint library.

Lifetime: 5 years MIN, 15 years TARGET MTBF

Safety: RoHS-compliant (RoHS3, EU Directive 2015/863, without exemptions), halogen-free (IEC 61249-2-21), red-phosphorous-free, antimony-free, REACH-compliant (U Regulation 1907/2006, without candidate substances).

Reliability: AEC-Q (target, grade 1), UL94-V0 flame resistance, glow-wire connectors, tin-finishes are matte-tin (reduced whiskering), operating temperature -40C to 85C MIN (-40C to 125C TARGET), MSL1 TARGET, MLCCs have soft-termination (bend-crack resistance), bulk capacitors are solid-material (ex. aluminum-polymer over aluminum-electrolytic for higher lifetime).

Usability: 1608 metric size TARGET (ease-of-assembly/repair), 4 mounting holes (square or rectangle pattern TARGET).

Ergonomics: rounded corners (major radius 5mm MIN).

Options: conformal-coating, encapsulation.

## PCB

Fabrication Class: must be IPC-2 or IPC-3 for traditional fab.

Surface Finish: must be ENIG.

Soldermask Color: Green

Silkscreen Color: White

Electrical Testing: Yes

Impedance Control: Yes for high-frequency or analog PCBs.

Material: high thermal stability (ex. low-CTE, cycling tolerance, high electromechanical stability, high thermal conductivity (ex. 0.7W/mK is a good non-ceramic benchmark), good impedance-properties (ex. low relative-permittivity, low dissipation-factor).

Assembly: Must use lead-free solder. Preferred alloy is SAC305. Must use low-activity no-halogen (category L0) flux. Preferred flux is no-clean IPA-washable (good performance without cleaning but can be cleaned).

## FOOTPRINTS

All pads must have rounded corners with radius 0.05mm MIN.

BGA footprint pads are generally recommended to be soldermask-defined.

SMT pads and reflow THT pads can be solid-connected to conductor-planes.

Easy-maintenance SMT pads and selective THT pads should have thermal-reliefs.

## VIAS

We prefer full-depth vias (normal plated-thru-hole, no blind or buried). 

Vias-in-pad are good for space and thermals. We use them with exposed-pad-ICs when we have space.

Via sizes:

```
Drill Dia, Annular Ring Dia

Small: 0.2mm, 0.25mm (vias-in-pad standard)

Compact: 0.25mm, 0.3mm (advanced-fab standard)

Normal: 0.4mmm, 0.8mm (traditional-fab standard)

0.4/0.8 is the default via size in Kicad (popular). It requires a large-enough drill bit that breaks/wears less than smaller sizes (cost-effective).

Easy: 0.5mm, 1.2mm (IPC-2221 Level-A)

```

## SPACING

board-edge to silkscreen, min 0.2mm

board-edge to external-layer-conductor, min 0.25mm

board-edge to internal-layer-conductor, min 0.5mm

board-edge to hole-edge, minimum 1mm

via-hole-edge to pad-edge spacing, minimum 0.2mm

via-hole-edge to via-hole-edge spacing, minimum 0.5mm

Footprints are spaced to support part-holding with tweezers (0.8mm tip-thickness).

Same-net pads can be closer together. Different-net pads should be further apart.

## SILKSCREEN

Attempt to have a reference-designator for each part-footprint.

Attempt to have a complete perimeter outline per part-footprint. In some cases a broken/dotted line is important for flux-scatter (ex.  high-reliability BGA assembly).

Must have a functional-label per external-pin.

MINIMUM:

* Company Name (ex. Guidebolt)
* Part ID (ex. SOMEPART-MK1R3)
* Batch ID (ex. 2021-01-20_XYZFAB)
* MFG Origin (ex. Made in Canada with imported parts)

SPECIAL:

* flammability marker (ex. UL94V-0)
* WEEE directive marker
* RoHS
* REACH
* CE
* UL Recognized
* UL Listed





