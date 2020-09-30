# ELECTRICAL DESIGN STANDARD

2020-09-30

Official Guidebolt Electrical-Design Standard

## GENERAL TARGETS

We target:

* elemental composition, RoHS3 without exemptions, REACH, JEDEC (J-STD-609) halogen-free
* flame resistance, UL94-V0
* moisture-sensitivity-level, 1
* tin-whiskering avoidance, matte-finish
* high thermal stability, low-CTE, cycling tolerance
* high electromechanical stability, CAF, electro-migration
* thermal conductivity (0.7W/mK, good non-ceramic benchmark)
* impedance-control, low relative-permittivity, low dissipation-factor
* high-quality fabrication class (IPC-2, IPC-3)
* high-quality PCB plating (ENIG)
* ease of soldering assembly/disassembly

## GENERAL REQUIREMENTS

We require:

* elemental composition, RoHS3 with/without exemptions
* fabrication class: IPC-2 or better
* PCB plating: ENIG or better

## General

Required: all elements, RoHS-compliant (preferably RoHS3).

Preferred: all elements, REACH-compliant.

Preferred: all elements, halogen-free.

Preferred: all elements, flame-resistance UL94-V0.

Note that "X-Free" generally allows trace amounts below a standard threshold. For example, "halogen-free" and "zero halogen" are typically used interchangeably under the max 1500ppm of total halogens (IEC 61249-2-21).

Preferred: measurement standard, metric

Required: PCB build, fabrication-class IPC-2 (or better)

## Parts

Preferred: all parts, automotive-grade (qualified to AEC-Q).

Required: all parts, temperature-range for operation and storage. See list below.

* -40C to 85C (minimum)
* -40C to 105C (acceptable)
* -40C to 125C (good)
* -55C to 150C (excellent)

Preferred: All power-connectors are glow-wire-capable.

## PCB

Required: all PCBs, rounded corners.

Preferred: PCB rounded-corners, minimum radius 5mm.

Required: All PCBs have ENIG surface finish (or better).

Required: All parts are placed with at least 1mm spacing between parts.

Preferred: Fill to pad clearance, minimum 0.5mm

Preferred: PCB soldermask color, green.

Preferred: All signal PCBs are built with impedance control.

Required: All PCBs expected to endure high-moisture must have conformal-coating or encapsulation.

## PCB Silkscreen

Required: Every PCB has the following silkscreen text (minimum). Refer to list below.

* company name
* part-number (with revision number)
* batch number
* part perimeter-outline (one per part)
* part reference-designator (one per part)
* functional-label (one per external-pin)

Markings:

* flammability marker (ex. UL94V-0)
* WEEE directive marker

Compliance:

* RoHS
* REACH
* CE

Certifications:

* UL Recognized
* UL Listed

## PCB Material

Preferred: All power PCBs have thermal conductivity of 0.7 W/mK (or better).

## PCB Holes

Required: All THT holes have a minimum-diameter equal to maximum-lead-diameter + 0.25mm (IPC-2222 Level A).

Required: All THT annular-rings have a minimum-diameter equal to minimum-hole-dia + 0.7mm (IPC-2221 Level A).

## PCB Vias

Preferred: standard sizes (hole-dia, annular-ring-dia).

* 0.4mm, 0.8mm (small)
* 0.5mm, 1mm (normal-compact)
* 0.5mm, 1.2mm (normal)

Preferred: full-depth vias (normal plated-thru-hole, no blind or buried)

Preferred: no vias in pad

Preferred: via-hole-edge to pad-edge spacing, minimum 0.2mm

Preferred: via-hole-edge to via-hole-edge spacing, minimum 0.5mm

## PCB Pads

Required: all pads, rounded corners

Required: pad rounded-corners, minimum radius 0.25mm

## PCB Mounting

Required: all PCB-mounting-holes support metric screws

Preferred: All PCBs have at least 4 mounting holes.

Preferred: All PCB mounting holes are patterned as a simple shape (ex. square, rectangle).

## PCB Board Edge Clearance

Required: board-edge to external-layer-conductor, minimum 0.25mm

Required: board-edge to internal-layer-conductor, minimum 0.5mm

Preferred: board-edge to any-layer-conductor, minimum 1mm

Required: board-edge to hole-edge, minimum 1mm

Required: board-edge to part-perimeter, minimum 1mm

Preferred: board-edge to SMT-part-perimeter, minimum 3mm

## Protection

Required: All external pins have transient voltage protection.

## Lifetime

Required: All electronics have at least 50K hours MTBF.

Preferred: All electronics have at least 150K hours MTBF.

## Capacitors

Preferred: All MLCC capacitors have soft-terminated ends (bend-crack resistance).

Required: All high-value capacitors are aluminum-polymer type.



