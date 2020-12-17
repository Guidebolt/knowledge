# Design, Electrical

2020-11-07

Official Guidebolt Electrical-Design Standard

## Resources

[Ultimate Electronics Book](https://ultimateelectronicsbook.com) - Free online book with interactive schematics and simulations

## KEYWORDS

MUST means required. Exceptions must be peer-reviewed and approved.

SHOULD means recommended. Exceptions must be justified and documented.

GOOD means an idea or option for high-quality/ideal consideration.

## QUICK CHECKLIST

Metric-standard design. Non-metric parts and units are corrected converted.

Qualification of all parts and materials under company requirements for design safety and reliability.

Use of company-standardized parts and materials as applicable.

Clearance between board-edge and conductor-layers.

Clearance between board-edge and parts.

Clearance between parts.

Overvoltage protection of all external pins.

Overcurrent protection of all external power pins.

Safe power dissipation of all thermally challenged parts.

Safe power dissipation of all power and return paths.

Impedance matching of differential/parallel signals.

## PCB FABRICATION STANDARD

Fabrication Class: IPC-2 or IPC-3

PCB Plating: ENIG

Soldermask Color: Green

Silkscreen Color: White

Electrical Testing: Yes

Impedance Control: Yes () or No ()

## QUALITY

MUST: The design has at least 50K hours MTBF (5 YEARS).

GOOD: The design has at least 150K hours MTBF (15 YEARS). 

SHOULD: The design uses automotive-grade parts where possible (for high reliability).

MUST: The design is RoHS-compliant (RoHS3, EU Directive 2015/863) (RoHS exemptions are allowed)

GOOD: The design is RoHS-compliant without exemptions.

GOOD: The design is halogen-free (IEC 61249-2-21).

GOOD: The design is red-phosphorous-free and antimony-free.

GOOD: The design is REACH-compliant.

GOOD: The design is rated to UL94-V0 for flame-resistance.

GOOD: The design has glow-wire-qualified power-connectors.

SHOULD: The design has matte-tin-finish where tin-plating is used (for reduced tin whiskering).

SHOULD: The design has an operating-temperature range of -40C to 85C.

GOOD: The design has an operating-temperature range of -40C to 125C.

SHOULD: The design has a minimum part size of 1608 METRIC (for ease of assembly and repair).

## PCB

SHOULD: The PCB has rounded corners (for safe handling).

SHOULD: The PCB has rounded corner radius of 5mm MIN.

SHOULD: The PCB has all parts placed with at least 1mm clearance at 2 opposing faces (for ease of assembly).

SHOULD: The PCB has green soldermask (for visual comfort).

GOOD: The PCB is fabricated with impedance-control (for signal integrity).

GOOD: The PCB has conformal-coating or encapsulation (for extreme applications).

GOOD: The PCB has high thermal stability (ex. low-CTE, cycling tolerance).

GOOD: The PCB has high electromechanical stability (ex. CAF, electromigration).

GOOD: The PCB has high thermal conductivity (ex. 0.7W/mK is a good non-ceramic benchmark).

GOOD: The PCB has good impedance-properties (ex. low relative-permittivity, low dissipation-factor).

MUST: all PCB-mounting-holes support metric screws

SHOULD: All PCBs have at least 4 mounting holes.

SHOULD: All PCB mounting holes are patterned as a simple shape (ex. square, rectangle).

## PARTS

GOOD: The part is moisture-sensitivity-level 1 (for high shelf-life without special handling).

SHOULD: The design uses MLC capacitors with soft-terminated ends (for bend-crack resistance).

SHOULD: The design uses aluminum-polymer capacitors over aluminum-electrolytic capacitors (for higher lifetime).

## SILKSCREEN

MUST: Silkscreen text includes the following list (minimum):

* company name
* part-number with revision-code (ex. ABC-MK1R3)
* batch number
* part perimeter-outline (one per part)
* part reference-designator (one per part)
* functional-label (one per external-pin)

MUST: Silkscreen text must not overlap exceeding the line thickness.

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

## FOOTPRINTS

MUST: All THT holes have a minimum-diameter equal to maximum-lead-diameter + 0.25mm (IPC-2222 Level A).

MUST: All THT annular-rings have a minimum-diameter equal to minimum-hole-dia + 0.7mm (IPC-2221 Level A).

SHOULD: all pads, rounded corners

SHOULD: pad rounded-corners, minimum radius 0.25mm

## VIAS

SHOULD: standard sizes (hole-dia, annular-ring-dia).

* 0.4mm, 0.8mm (small)
* 0.5mm, 1mm (normal-compact)
* 0.5mm, 1.2mm (normal)

SHOULD: full-depth vias (normal plated-thru-hole, no blind or buried)

SHOULD: no vias in pad

SHOULD: via-hole-edge to pad-edge spacing, minimum 0.2mm

SHOULD: via-hole-edge to via-hole-edge spacing, minimum 0.5mm

## SPACING

SHOULD: board-edge to external-layer-conductor, minimum 0.25mm

SHOULD: board-edge to internal-layer-conductor, minimum 0.5mm

SHOULD: board-edge to any-layer-conductor, minimum 1mm

SHOULD: board-edge to hole-edge, minimum 1mm

SHOULD: board-edge to part-perimeter, minimum 1mm

SHOULD: board-edge to SMT-part-perimeter, minimum 3mm





