# CNC Machining

Modern CNC machines are capable of micron-scale (0.001+ mm) material processing. Typical accuracy and repeatability are under 10um (linear) and under 0.01 degrees (angular).

## Setup

The ideal machine space is a climate-controlled room (temperature, humidity, airflow) with a flat, level, finished floor (ex. thick polished reinforced concrete) 


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



## Workflow

Step | Tool
---|---
General Design | 
CAD | Autodesk Inventor
CAM | Autodesk Inventor CAM

## Toolholders

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

* Adapter Plate: custom-made (2 air inlets: unlock, turbo) (adapts M200X3 table)
* Quick Plate: Schunk, VERO-S series, NSE3-138-V1 (supports 2-pos anti-spin, 4.4kg) (OID:1313723)
* Vise: Schunk, KSC grip 125-160 (natural VERO-S interface, 8.7kg) (OID:0432463)
* Clamping Pin: Schunk, SPA-40RF (between vise and quick-plate) (OID:0432369)
* Anti-Spin Pin: Schunk, IXB-V1 (between vise and quick-plate) (OID:0471980)

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
