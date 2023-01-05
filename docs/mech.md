# Mechanical Design

The design and development of good mechanical systems.

## Resources

Description | Link
---|---
History of the jerry can | https://web.archive.org/web/20070524182038if_/http://www.americanheritage.com/articles/magazine/it/1987/2/1987_2_62.shtml

## Videos

Additive Manufacturing, CCAT Shop Tour, 2022: [Youtube Link](https://www.youtube.com/watch?v=oVEN8h3fr6s)

## Aesthetic-Functional Design

(industrial design, product design)

Form and Function:

1. Form follows function: Durable, Comfortable, Compact (priorities)

2. Form adds function: Improvised Table, Handle, Mounting Point (examples)

3. Form has function: Aesthetic (ex. feelings), Intuition (ex. learning how to use something without instructions)

---

Principles: 

1. Consistent Design Language

2. Aesthetic-Conceptual Alignment

3. Easy-to-Use During Emergencies

---

Forums:

[https://www.reddit.com/r/IndustrialDesign/](https://www.reddit.com/r/IndustrialDesign/)

## Materials

Molecular Perspective: Elements, Compounds, Mixtures

[Table of Elements, PTABLE](https://ptable.com)

Preferred: 6061/7075 Aluminum, A4 Stainless Steel (A4SS)

3D Printing PLA: Natureworks 3D870 
([Datasheet](https://www.natureworksllc.com/~/media/Files/NatureWorks/Technical-Documents/Technical-Data-Sheets/TechnicalDataSheet_3D870_monofilament_pdf.pdf?la=en))

## Acoustics

Basic Acoustic Theory:

* Sound waves propagate through a medium (ex. air)
* When sound waves contact a different medium (ex. air to wall), some waves are reflected by the new medium; some waves are absorbed in the new medium (as heat or kinetic resonance); some waves propagate through the new medium.

The industry-standard for acoustic insulation is mass-loaded vinyl (MLV). We don't like its PVC base because the plasticizer off-gas causes reduced longevity and health risks (ok but not ideal). It seems a more durable and safe alternative is mass-loaded EVA. 

## Screws

Head Standards: Hex-Socket-Head (primary), Hex-Head 

(metric, A4 stainless steel, normal head size, M2 to M12)

M6x1 (12mm, 16mm, 20mm, 25mm, 30mm, 35mm, 40mm)

M4-0.7 (mm standards: 10, 14, 16, 20, 25, 30, 35, 40, 50)

M3-0.5 (mm standards: 6, 8, 10, 12, 16, 20, 25, 30)

M2.5-0.45 (6mm, 8mm, 10mm, 12mm, 16mm)

Notes: M6 is a strong standard for higher mechanical loads with over 5kN proof load. It is dimensionally close to the quarter-inch imperial-standard (good universal compatibility). It is the thread standard for mechanical jigs (ex. aluminum-breadboards).

## Threaded Insert, Press-Fit

Press-fit Threaded Inserts: Pemnet, NFPC (dist: Bisco)

* M3 (4.7mm DIA hole, 5.84mm LG insert)
* M4 (6.3mm DIA hole, 6.7mm LG insert)
* M6 (7.9mm DIA hole, 8mm LG insert)

## 

## Notes

THREAD SIZE.

We use M2 to M12 threading for all small to medium-scale applications.

Our standard increments:

* M2
* M2.5
* M3
* M4
* M5
* M6
* M8
* M12

M2 and M2.5 are the smallest sizes with common-stock and tooling-support. It is used in miniaturized devices such as car-remotes and phones.

M3 is our standard for small mechatronic devices. We usually prefer the marginal robustness over compactness (compared to smaller threads).

M4 is our strong standard for lower mechanical loads. It offers a proof load over 3000N (property class 5.8, middle-curve). It is used in the VESA international-mounting-standard.

M5, we don't use much because it's marginally different from M4 and M6. 

M8 and M12 are reserved for specific applications requiring high-strength or high-opening-diameter (ex. circular-connectors, cable glands).

HEAD DRIVE.

We use philips, hex-socket, and torx. 

We prefer hex-socket head-drive for most applications. It is a strong and practical balance of tool-accessibility (ex. hex keys are common), strength (ex. less stripping of driver-bit/device than philips/torx), and ease-of-assembly (ex. can be driven at an angle with ball-ends).

Philips optimizes for tool-accessibility. Saves time!

Torx optimizes for driving-strength. Improves mounting-torque (useful for getting the most out of small fasteners)!

MATERIAL.

* A2 stainless steel (SAE 304)
* A4 stainless steel (SAE 316)

## Ergonomics

A super common problem we see is a lack of rounded, chamfered, and deburred edges/corners! This affects not only ergonomics but also safety and reliability! Sharp corners can get dirty and cause infected cuts. Rough edges can abrade wire-jackets to various failure conditions.

## Pneumatics

[Basic Pneumatics (PDF, SMC, 2005)](https://www.smcpneumatics.com/pdfs/smc/basic_pneumatics.pdf)

[SMC, 2022 New AFF/AM/AMD Series](https://ca01.smcworld.com/catalog/New-products-en/mpv/es30-17-aff/index.html)

Compressed Air Purity Standard: ISO 8573

* Air Pre-Filters
* Air Compressors (ex. 4x pumps, paired 50% duty cycle)
* Inline Filters (ex. 15um)
* Check Valves
* Aftercooler
* Auto Drain
* Relief Valve (ex. 1 MPa)
* Water Separator 
* Main Line Filter (ex. 1um)
* Mist Separator (ex. 0.1um)
* Micro Mist Separator (ex. 0.01um)
* Purge Valve
* Tank (with ball-valve + auto-drain bottom)

The North American pipe thread standard is NPT. Our pipe/tube fitting standard is 1 inch NPT (thread size) and 316/A4 stainless steel (material), providing over 2500 LPM (90 CFM) flow capacity at 60 psi.

[Pipe Air Flow (PDF, Parker)](https://www.parker.com/parkerimages/pneumatic/serv/TEC-15.pdf)

## Cleaning

Preferred: easy-to-clean, see process list below.

* tool-free wipe
* tool-free scrub
* tool-required scrub
* cold-water rinse
* hot-water rinse

## Construction

[BuildingScience](https://www.buildingscience.com/)

[Belinda Carr](https://www.youtube.com/channel/UC_NzYRcT5IroUsMU2472ViQ)

## Thermal

Refrigerant

## Acoustic

Sound Dampening, Mass-Loaded EVA

https://ncma.org/resource/sound-transmission-class-ratings-for-concrete-masonry-walls/

## Finishing

How to spot galling | https://www.finishing.com/228/49.shtml