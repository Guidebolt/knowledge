# CNC Machining

Modern CNC machines are capable of micron-scale (0.001+ mm) material processing. Typical accuracy and repeatability are under 10um (linear) and under 0.01 degrees (angular).

## Setup

The ideal machine space is a climate-controlled room (temperature, humidity, airflow) with a flat, level, finished floor (ex. thick polished reinforced concrete).

We recommend a solid-state 3-phase converter (240VAC 1P to 240VAC 3P) that is rated for at least twice the rated power of the machine as marked on its nameplate (ex. 10kVA machine, 25kVA converter). This safety factor is important for burst power stability (ex. spindle ramp-up) and burst regeneration tolerance (ex. spindle braking). 

We recommend a step-down transformer (240VAC 3P to 220VAC 3P, delta-wye) that supports at least the rated power of the machine (ex. 10kVA machine, 10kVA transformer or better).

## Tooling

For tapping, we use NT Tool Synchrofit 2 (elastic tapholders) with dual-contact BT30 (NT Tool, AHO type).

Function | Toolholder (NT Tool) | Collet (NT Tool) | Tap Interface Standard
---|---|---|---
M2 | WBT-AHO30A-SMH8-75 | ER8-3.0A | DIN371
M2.5 | WBT-AHO30A-SMH8-75 | ER8-3.0A | DIN371
M3 | WBT-AHO30A-SMH8-75 | ER8-3.5A | DIN371
M4 | WBT-AHO30A-SMH16-90 | ER16GH-4.5-3.4 | DIN371
M5 | WBT-AHO30A-SMH16-90 | ER16GH-6-4.9 | DIN371
M6 | WBT-AHO30A-SMH16-90 | ER16GH-6-4.9 | DIN371
M8 | WBT-AHO30A-SMH16-90 | ER16GH-8-6.3 | DIN371
M10 | WBT-AHO30A-SMH16-90 | ER16GH-7-5.5 | DIN376
M12 | WBT-AHO30A-SMH16-90 | ER16GH-9-7.1 | DIN376

## Operation

The automatic tool change command (ex. M06 T88) selects a tool number (88) in the tool library, checks whether that tool is installed in the ATC carousel according to the ATC list (ex. tool 88 in ATC slot 10), then, if installed, performs an ATC cycle to that ATC slot (10).

Setting new tools on the ATC list can only be done in MDI mode, for accidental change prevention.

The manual-pulse-generator pendant axis-selection knob must be set to OFF in order to move the machine-head (else "Handle Mode" alarm). 

Workpiece clamping force deforms the part while held. Accurately machined dimensions may not survive when the part is released. Minimize clamping force while maintaining sufficient workpiece retention. Plan fabrication around clamp-release deflection.

## Overview

Dimensional Standard: Metric

Machine: [Brother Speedio M200X3](https://machinetool.global.brother/en-ap/mx3/index.aspx) (5-axis VMC with turning-capable rotary table)

Spec | Description
---|---
Main Spindle RPM | 16K
Turning Spindle RPM | 2K
Travel (XYZ position, A tilt, C turn) | 200x440x305, 120 ~ -30, 360+
Simultaneous Axes | 4 (XYZ + A/C)
Positioning Accuracy | 6~20um
Linear Repeatability | under 6um
Angular Repeatability | under 0.005 degrees
Nominal Power Input | 10kVA (200-230VAC 3P+GND)
Nominal Air Input | 0.5MPa 165L/min (SMC, KK130 connector)

Add-Ons (most are default on NA product package):

* 16k rpm spindle with dual-contact BT30 spindle-toolholder interface
* 22-slot automatic tool-changer (1.4s chip-chip) (0.8s tool-tool)
* top cover
* PLC
* A-axis clamp (turning axis) and C-axis clamp (4th axis)
* chip shower and 150L coolant tank with chute
* automatic grease lubricator
* Coolant-Thru-Spindle Interface (CTSI) (WARNING: requires 1.5MPa)
* hydraulic interface

[Autodesk POST](https://cam.autodesk.com/hsmposts)



---



## CAD-CAM Workflow

Step | Tool
---|---
General Design | Regular Documents
CAD | Autodesk Inventor
CAM | Autodesk Inventor CAM

## Toolholders

### Assorted

We generally prefer dual-contact hydraulic toolholders with short gage lengths (ex. 45mm) and direct tool mounting (no collets) for best rigidity and runout. 

* Standard hydro holders for light milling, drilling, and finishing.
* Slim hydro holders for tighter spaces. 
* Strong hydro holders for roughing.

Use | MFG | Product Family | Ordering ID | Description (mm)
---|---|---|---|---
6D | Big Daishowa | Slim Hydro | BBT30-HDC6S-60 | dual-contact, 60 gage
6D | Maritool | Standard Hydro | BT30-HC6-2.25D | dual-contact, 60 gage
6D | Big Daishowa | Standard Hydro | BBT30-HDC6-45 | dual-contact, 45 gage
8D | Big Daishowa | Standard Hydro | BBT30-HDC8-45 | dual-contact, 45 gage
10D | Big Daishowa | Standard Hydro | BBT30-HDC10-45 | dual-contact, 45 gage
12D | Big Daishowa | Standard Hydro | BBT30-HDC12-45 | dual-contact, 45 gage
12D Strong | YG1 | Power E Hydro | CBT30-HC12P-69 | strong hydro, torque withstand 110Nm
20D Strong | YG1 | Power E Hydro | CBT30-HC20P-90 | strong hydro, torque withstand 520Nm
External/Facing (20 square vertical) | NT Tool | Turning Tools for Brother Speedio | 2120 12020098 | BT30, Right-Hand, 98 Gage, 20x20x50 Toolslot
Facing (20 square horizontal) | NT Tool | Turning Tools for Brother Speedio | 2120 11020081 | BT30, Right-Hand, 81 Gage, 20x20x58 Toolslot
Boring Bar (10 round vertical) | NT Tool | Turning Tools for Brother Speedio | 2120 00010038 | BT30, 38 Gage, 10 DIA x 40 DP Toolslot

https://www.bigdaishowa.com/en/products/tool-holders/hydraulic-tool-holders

https://en.nttool.com/products/pid/158/

## Tools

### Endmill

YG1

Series | Spec (DIA/DOC/LG) | Use | Ordering ID
---|---|---|---
ALUPOWER | 12x24x83x0.5R | ALU | 4XNEM12005RET


WIDIA

Series | Spec (DIA/DOC/LG) | Use | Ordering ID
---|---|---|---
Varimill Extreme | 12x24x83x0.5R | PMKSH | 4XNEM12005RET
Varimill 1 | BALL 6x10x57 | PMKSH | 47N006002T

### Drill

WIDIA, Varidrill 3xD (PMKNS) (solid carbide, coated, grade WU25PD)

https://www.widia.com/ca/en/products/holemaking/solid-carbide-drills/varidrill.html

Drill DIA (mm) | Hole Purpose | Shank DIA (mm) | Ordering ID
---|---|---|---
1.984 | 2D PREP | 4h6 | VDS201A01984
2.1 | M2 SCREW | 4h6 | VDS201A02100
2.5 | M3 TAP DRILL | 4h6 | VDS201A02500
2.947 | 3D PREP | 4h6 | VDS201A02947

YG1, Dream Drill Alu 5xD (solid carbide with coolant-thru)

Drill DIA (mm) | Hole Purpose | Shank DIA (mm) | Ordering ID
---|---|---|---
3.1 | M3 SCREW | 6h6 | DGE433031
3.3 | M4 TAP DRILL | 6h6 | DGE433033
3.9 | 4D PREP | 6h6 | DGE433039
4.1 | M4 SCREW | 6h6 | DGE433041
5 | M6 TAP DRILL | 6h6 | DGE433050
5.9 | 6D PREP | 6h6 | DGE433059
6.1 | M6 SCREW | 8h6 | DGE433061

### Reamer

WIDIA High-Speed Reamers for Blind Holes (solid carbide)

https://www.widia.com/ca/en/products/holemaking/reaming-tools/hsr--high-speed-reamers--carbide.html

Grade K10F: uncoated fine-grain carbide (supports PMKNS, but best for non-ferrous reaming)

Hole DIA/TOL (mm) | Shank DIA (mm) | Ordering ID
---|---|---
2H7 | 3 | 2446025
3H7 | 3 | 2446029
4H7 | 4 | 2446031
5H7 | 6 | 2437472
6H7 | 6 | 2437523
8H7 | 8 | 2437525
10H7 | 10 | 2437526
12H7 | 12 | 2437527

### Taps

Video | Link
---|---
Tapping Basics | https://www.youtube.com/watch?v=bkrUzGooA9k
YG1 Prime Tap Intro | https://www.youtube.com/watch?v=p6AU1jIXxmw

YG1, PRIME TAP (COATED HSS, PMKN) (2022 CATALOG PG321)

TRE30 (SPIRAL FLUTE, COARSE THREAD, BLIND HOLE 2.5xD, CHAMFER DIN2197-C)

TRJ15 (SPIRAL POINT, COARSE THREAD, THRU HOLE 3xD, CHAMFER DIN2197-B)

Thread | Tap Standard | Ordering ID
---|---|---
M2 | DIN371 | TRE30136GS
M2 | DIN371 | TRJ15136GS
M2.5 | DIN371 | TRE30176GS
M3 | DIN371 | TRE30206GS
M3 | DIN371 | TRJ15206GS
M4 | DIN371 | TRE30246GS
M4 | DIN371 | TRJ15246GS
M5 | DIN371 | TRE30286GS
M6 | DIN371 | TRE30316GS
M6 | DIN371 | TRJ15316GS
M8 | DIN371 | TRE30366GS
M8 | DIN371 | TRJ15366GS
M10 | DIN371 | TRE30426GS
M10 | DIN371 | TRJ15426GS
M12 | DIN376 | TRE30506GS
M12 | DIN376 | TRJ15506GS

### Chamfering

Chamfering: Carmex,  (carbide grade MT8) (PMKNSH)

Carmex, Mini Chamfer

Carmex, Multi-Function Tools

8mm cutter DIA is ideal for small parts because holes are typically for M6 and under (for efficient Z plunge chamfering). 

Type | Use (hole DIA, material grade) | Description (Internal DEG x Cutter DIA x Max Radial Cut x Tool Length x Shank DIA) | Ordering ID
---|---|---|---
Multi-Function | CHAMFER PMKNSH | 90x8x4x73x10 | MF 1008 L16 A90 CR3
Multi-Function | SPOT PMKNSH |  | MF 0605 L10 A120 CR3
Multi-Function | ENGRAVE PMKNSH |  | MF 0605 L10 A60 CR3
Mini Chamfer | 2+ PMKNSH | 90x1.5x0.3x39x3 | MC 03015 C3 A90 MT8
Mini Chamfer | 2+ KNS | 90x1.5x0.3x39x3 | MC 03015 C3 A90 K20
Mini Chamfer | 3+ PMKNSH | 90x2.5x0.5x39x3 | MC 03025 C6 A90 MT8
Mini Chamfer | 3+ KNS | 90x2.5x0.5x39x3 | MC 03025 C6 A90 K20

### Turning



### Other

Facemill

Single Point Diamond Tools

## Workholding

We use Schunk KSC3 self-centering vises for their high clamping force (35kN) (workpiece pre-stamping is not required), fully encapsulated spindle, and 10um repeatability.

[KSC3 Info Sheet](https://web.archive.org/web/20230119081205if_/https://d16vz4puxlsxm1.cloudfront.net/asset/076200133045-Prod/document_0bieptt4oh63nfolgemvvlk24p/Flyer:%20KONTEC%20KSC3%20Centric%20Clamping%20Vises)

[KSC3 Webpage](https://schunk.com/ca/en/workpiece-clamping-technology/manual-clamping-systems/centric-clamping-vises/ksc3/c/PGR_6876)

Compared to the previous gen (KSC):

* better anti-corrosion (nickel-plated body)
* better mounting flexibility (Lang 96x96 M10 compatible)
* more compact form-factor (driving hex does not stick out)

Function | Description | Schunk Product ID
---|---|---
Vise with Reversible Jaws | KSC3 grip 125-160 | 1514238
Vise | KSC3 125-160 | 1514241
Mounting Pin | SPA-40RF (between vise and quick-plate) | 0432369
Indexing Pin | IXB-V1 (between vise and quick-plate) | 0432371
Quick Plate | NSE3-138-V1 | 1313723
Adapter Plate | (between quick-plate and machine-table) | custom
5-axis System Jaw | compact, not reversible, requires top jaws, 1-piece | 432472
Ground Top Jaw | simple flat, 1-piece | 1373278
Prismatic Top Jaw | for round workpieces, 1-piece | 1373344

These vises support a clamping range of 0 to 156mm/163mm (with the default reversible jaws) but they only have a ~40mm actuation range; the system jaws must be reversed and/or remounted (to either the inner or outer position). For max ranges of different system jaws, see the KSC3 info sheet, page 24 (default reversible jaw is 10). 

For best efficiency building prototype parts, use multiple vises because it's faster and more reliable to quick-swap the vise than the jaws.

Name | Function | Description
---|---|---
Vise1 | 0 - 40mm (up to 1.5") | reversible jaws, inner
Vise2 | 38 - 78mm (2" to 3") | reversible jaws, outer
Vise3 | 85 - 125mm (3" to 4") | reversible jaws, inner, reversed
Vise4 | 123 - 163mm (5" to 6") | reversible jaws, outer, reversed
Vise5 | 0 - 40mm (up to 1.5") | 5-axis jaws with ground top jaws, inner
Vise6 | 38 - 78mm (2" to 3") | 5-axis jaws with ground top jaws, outer

* driving interface: 12mm male hex (use socket)
* driving max torque: 100 Nm
* jaw screw head: M10 female hex
* jaw screw target torque: 60 Nm

## Supporting Tools

BT30 tool handling: Maritool, 30-Taper-Lock

https://www.maritool.com/Mill-Tool-Holders-Accessories/c23_51/p18752/BT30-Standard-or-Dual-Contact-Tightening-Fixture/product_info.html

Coolant: LubeCorp, GreenCut Cutting Fluid

[Product Page](https://www.lubecorp.com/greencut-cutting-fluid/)

## Power Supply

Utility (240VAC 1P) -> Main Breaker Panel -> Solid-State Phase Converter (240VAC 3P) -> Fusible Disconnect -> Delta-Wye Step-Down Transformer (220VAC 3P) -> 3-Phase Electrical Outlet

Dedicated Phase Converter: Phase Technologies, PTE010RQT-H3S1 (Phase Perfect Enterprise, 10HP, NEMA 3R, Quiet, On/Off Switch, Protec Surge Protection, 30kg) (input 1-phase 240VAC, output 3-phase 240VAC with max steady-state 36A and class 10 thermal-overload motor-starting)

Fusible Disconnect (pre-transformer): Schneider Electric, CH362AWK (60A/600V/3P, NEMA 3R/12, CSA) (with fuses, Mersen AJT30; fuse-reducers, Mersen J636)

Dedicated Step-Down Transformer: 3-phase 240VAC to 3-phase 220VAC, isolation, 10kVA

Receptacle/Plug (NEMA15-50, post-transformer): Hubbell, HBL8450A/HBL8451C (CSA/UL)

## Air Supply

Dedicated Air Compressors: Makita, MAC320Q (4 parallel units) (each rated 50% duty cycle per hour)
