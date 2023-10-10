# System Design

## Resources

### General

Description | Link
---|---
Human Engineering Design Standard (MIL-STD-1472H) (RCMD) | [WEB-PDF](http://everyspec.com/MIL-STD/MIL-STD-1400-1499/MIL-STD-1472H_57041/)

* Time Format: [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) (ex. 2022-12-31) (strongly recommended)
* Text Format: [Markdown](https://commonmark.org/) (strongly recommended)
* Project Management: [ISO 21502:2020](https://www.iso.org/standard/74947.html) 

### Assorted

Description | Links
---|---
1968 Golden Globe Race (sail around the world) | [WEB](https://www.worksinprogress.co/issue/the-maintenance-race/) / [HackerNews](https://news.ycombinator.com/item?id=32196345)
Next-Gen UI Examples | [WEBSITE](https://www.hudsandguis.com) / [HackerNews](https://news.ycombinator.com/item?id=31105513)
Aesthetic Intuition Practice | [WEBSITE](https://cantunsee.space/)
The Design of Everyday Things (Book, 2013, Don Norman) |
The Design of Future Things (Book, 2009, Donald A Norman) |
Handbook of Human Factors and Ergonomics (Book, 2021, 5th Edition, Gavriel Salvendy and Waldermar Karwowski) |

## Key Knowledge

Description | Notes
---|---

**Design is description and desire for how something can and should be.** Draw lines and curves (form). Fill with atoms (composition). Symbolize ideas (abstraction). Plan cause-effect possibilities (interactive potential). 

## Abstract Design

Keyword | Description
---|---
**Design Finality** | Make design decisions that survive (ideally forever, but at least up to the upcoming/next commercial release)

### Quality

**Absolute Quality Score (X / 5)**: The general measure of quality of a product or service. 

* 5/5 = one of the best possible designs based on leading-edge technologies with zero false-tradeoffs and zero relevant-errors
* 4/5 = excellent design with significant optimizations, no major errors or false-tradeoffs
* 3/5 = good design; no major errors affecting primary requirements, optimized
* 2/5 = sufficient design; no significant errors, mostly unoptimized, clear unrealized-potential
* 1/5 = barely functional; significant errors, generally unoptimized, clear unrealized-potential
* 0/5 = does not meet functional requirements

**Incremental Quality Score (X + I)**: An additive measure of each meaningful improvement on top of the base design as marked by +1 score (ex. +3 for a batch of 3 improvements). The base design is the existing design (for design revisions) OR the simplest possible design (for new designs).

Example: The design of scissors. Consider 2 thin steel blocks with sharpened inner edges and holes, held together by a locknut and bolt (absolute 0/5, incremental X). Add rounded edges and simple finger-slots on the holding-end (1/5, X+2). 

### Design Direction



**Unlimited Possibility Space**: The idea of a space where absolutely anything can happen. The greater your imagination, the greater fraction of this space is thinkable.

**Available Possibility Space**: What is possible in the world within a certain timeframe, from a collective or individual perspective.

**Design Goals**: The abstract and specific reasons for considering a design space in the first space.

**General Branching**: Grouping similar design possibilities under a single keyword/concept. Remove bad branches from the design space. Avoid tunnel visioning into a good branch where other good, perhaps better, branches also exist.

**False Tradeoffs**: Where normally an improvement in A causes a worsening in B, a new approach that allows a pure improvement in A. Ideally discover all false tradeoffs and accordingly apply all pure improvements possible.

**Prioritization**: Deciding the best design balance of strengths and weaknesses, supported by a deep understanding of the goals, and required by the existence of true tradeoffs.

**Specific Completion**: Finalizing all design details required to build a prototype or produce at scale with perfect clarity.

## Practical Design

**Basic 1**: Safety, Performance, Reliability, Durability, Longevity

Note: durability means it does not break easily, longevity means it generally works for a long time, reliability means it consistently works (during its specified lifetime, even if non-critical parts break easily). Something can be reliable and fragile/short-lived.

**Basic 2**: Size, Weight, Form, Noise, Power, Functional Efficiency (input-output)

**Lifecycle**: Design for... Manufacturing, Transportation, Storage, Assembly, Deployment, Configuration, Customization, Maintenance, Repair, Removal, Recycling

**Environment**: Design for... Temperature (ex. thermal expansion), Ingress/Submersion (ex. dust/dirt/sand/water), Condensation, Erosion (natural/artificial), Corrosion, Sunlight (ex. UV exposure), Precipitation (avoid standing water, assess drip dynamics for externalities), Pressure (atmospheric/special)

Design Goals:

Description | Notes
---|---
Single User Operation | 


### Safety

**Safety Methods**: Danger Removal, Danger Reduction, Shielding, Lockout, Signaling, Intuitive Interface (subconsciously guide safe user experience), Instructions

**Failure Planning**: Self-Test (Start-up, Dynamic), Pre-Failure Signals/Mechanisms, Graceful Failure, Human Error Tolerance, Blackbox Logging (identify root cause, improve next version)

Functional Safety:
[IEC 61508](https://webstore.iec.ch/publication/5515) (industrial), 
[ISO 26262](https://www.iso.org/standard/68383.html) (automotive),
[IEC 60730](https://webstore.iec.ch/publication/3117) (household)

### Common

**Common Events**: Impact Test (random shock), Compression Test (random weight), Drop Test (avoid damage/injury/shatter/chip)

**Dynamic Environment**: Rolling Stopper (Recovery from Fall on Angled Surface), Relatively-Distinct Color (Lost-and-Found Detection)

**Cleaning**: Smooth Surfaces, Hand-Fitting Internal Volumes, Compatible with Water Immersion and Spray, Minimal Contact with Floor, Easy-Clean Exterior (non-magnetic, non-adhesive, cleaning-chemical-compatible), Low-Splash Surface, Acceptable-Splash-Angle Surface

### Optimization

**Speed**: Motion, Data Transmission, Data Processing, Chemical Reaction Rate

### Usability

**Constrained Use**: One-Handed Use, Independent Use, Low-Tactile-Sense Use, Color-Blind Use, Impaired Vision Use, Impaired Hearing Use, Long-Distance Use, Awkward-Angle Use

**Ergonomic Methods**: Rounded Corners and Edges (Comfortable Handling), Handle (Intuitive Carrying), Grab Points (Non-Slip Lifting), Low Thermal Conductivity (Warm Handling), Tactile Feedback (Correct-Input Signal)

**Intuitive Sequence**: Left-to-Right, Top-to-Bottom

### Reliability

Temperature: operating range, derating, cycling before use, cycling during use, freeze-thaw resistance, flame retardance (UL94)

### Maintenance

Signals: Maintenance Reminder, Problem Warning, Maintenance Guiding

Special: Spare Parts Inside Product (Useful Unity), First-to-Fail is Easiest-to-Replace (Zero Maintenance Damage Mitigation), On-Part Info Sticker/Engraving (ex. Company Name, Part Number)

### Durability

Resistance: Scratch, Chip, Dent, Vibrate, Fatigue, Shock, Ingress (prevention, ) Chemical, Galvanic Corrosion

### Size, Weight, Form

Fit Through: Standard Door, Garage Door, Car Door, Spiral Corridor, 

Fits Inside: Car Trunk, Car Seat, Backpack, Pocket

Special: Stackable Storage, Stackable Operation, Stands Upright Independently, Table Function (Large Flat Top), Floor Weight (High-Traction, High-Weight), Step-Stool (Small Flat Top, High-Stability)

Mechanical Unity: consistent physical connectivity; ex. car gas-cap is tethered

## Notes

* disaster-tolerant design









