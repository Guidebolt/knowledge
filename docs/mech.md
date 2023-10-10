# Mechanical Design

## Material Science

### Composition

[Periodic Table of Elements (PubChem)](https://pubchem.ncbi.nlm.nih.gov/periodic-table/)

**Elemental Composition**: All physical materials are made of elements.

**Molecular Structure**: One or more elements chemically bond into molecules.

**Crystal Structure**: Molecules are scattered randomly (amorphous) or organized to some pattern (crystalline) based on intermolecular dynamics.

Example: steel

**Cutouts, Infill, Porosity**: Internal geometry can include various forms of material removal/absence such as slots (strength-weight optimizing) and voids (open-cell, closed-cell).

**Composite Structure**: Different materials can be combined at the geometric level.

Example: reinforced concrete

**Residual Stress**: Uneven changes in temperature/microstructure causing spring-like internal tension.

Example: hot-rolled steel

### Properties

**Yield Strength**: Permanent deformation limit. 

**Ultimate Tensile Strength**: stretch-break limit (MPa)

**Fracture Strength**: stress at break

**Thermal Expansion**

**Galvanic Corrosion**

**Resonant Frequency**

### Selection

**6061-T6 Aluminum**

**A4 (SAE 316) Stainless Steel**

**A2 (SAE 304) Stainless Steel**

---

3D Printing Filaments:

* Prototyping: Precision PLA (±20um DIA) based on [Natureworks 3D870](https://www.natureworksllc.com/~/media/Files/NatureWorks/Technical-Documents/Technical-Data-Sheets/TechnicalDataSheet_3D870_monofilament_pdf.pdf?la=en)

## Fasteners

### Standard

Our fastener standard is passivated stainless steel (A2/A4; 304/316) in metric sizes (generally hex-socket/hex-head coarse-threaded M2 thru M12). We often use M2x0.4, M3x0.5, M4x0.7, M6x1, M8x1.25, M10x1.5, M12x1.75; we rarely use M2.5x0.45 and M5x0.8.

* M2 and M3 for micromechanical/electronic (ex. car remote, phone)
* M4 for light structural (ex. VESA mounting standard)
* M6 and M8 for medium structural
* M10 and M12 for heavy structural

M6 is a particularly good general-purpose size with over 5kN proof load (500kg). It has good compatibility (dimensionally close to the 1/4-20 imperial size) and universality (standard thread for aluminum breadboards).

Screw Thread | Common Lengths (mm)
---|---
M2 | 
M2.5 | 6, 8, 10, 12, 16
M3 | 6, 8, 10, 12, 16, 20, 25, 30
M4 | 10, 14, 16, 20, 25, 30, 35, 40, 50
M5 | 
M6 | 12, 16, 20, 25, 30, 35, 40

[Tensile Load and Proof Load Charts (engineeringtoolbox)](https://www.engineeringtoolbox.com/metric-bolts-minimum-ultimate-tensile-proof-loads-d_2026.html)

For improved reliability, we like to use:

* stainless steel self-locking nuts (nylon-insert or metal-tension)
* stainless steel threaded-insert nuts for plastic designs

We use: IUTC-M2, IUTC-M3, IUTC-M4, IUTC-M6 (DISTR: Hi-Tech Fasteners, Bisco Industries)

### Special

Specialty fasteners help in plastic, sheet metal, laminate, ceramic, composite, and exotic applications.

[Specialty Fastener Catalog (Pemnet)](https://www.pemnet.com/catalog-downloads/)

## Geometry

### Common Issues

* all corners/edges are not deburred/radiused/chamfered





## Resources

Description | Link
---|---
History of the jerry can | https://web.archive.org/web/20070524182038if_/http://www.americanheritage.com/articles/magazine/it/1987/2/1987_2_62.shtml

Additive Manufacturing, CCAT Shop Tour, 2022: [Youtube Link](https://www.youtube.com/watch?v=oVEN8h3fr6s)

Forums:

[https://www.reddit.com/r/IndustrialDesign/](https://www.reddit.com/r/IndustrialDesign/)

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

## Acoustics

Basic Acoustic Theory:

* Sound waves propagate through a medium (ex. air)
* When sound waves contact a different medium (ex. air to wall), some waves are reflected by the new medium; some waves are absorbed in the new medium (as heat or kinetic resonance); some waves propagate through the new medium.

The industry-standard for acoustic insulation is mass-loaded vinyl (MLV). We don't like its PVC base because the plasticizer off-gas causes reduced longevity and health risks (ok but not ideal). It seems a more durable and safe alternative is mass-loaded EVA. 

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