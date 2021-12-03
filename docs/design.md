# Design

2021-11-10

Good design comes from good design thinking. In hardware development, you arrange physical atoms. In software development, you arrange abstract states. In both cases, you plan the interactive sequence of the system.

## Standard Design Model

Unlimited Possibility Space: An idea of a space where absolutely anything can happen. The greater your imagination, the greater fraction of this space is thinkable.

Available Possibility Space: What is possible in the world within a certain timeframe, from a collective or individual perspective of control.

Goals: The common-abstract and application-specific reasons for considering a design space in the first place.

General Branching: Grouping similar possibilities under a single keyword and concept (or a single key-phrase and its set of concepts). Remove a clearly-bad branch from the design space to simplify the consideration (deletion or single-branch-focusing is very risky). Important to remove only the bad branch and not let it overlap with a fraction of good branches!

Optimization: Think of different options that maximize particular strengths or minimize particular weaknesses. Look for and remove false tradeoffs to enable absolute improvements towards a more balanced design.

Prioritization: Decide the best balance of strengths and weaknesses, given the reality of fundamental tradeoffs that remain after optimization. 

Specific Completion: The comprehensive completion of all design details required to build a prototype or produce at scale.

## Standard Design Procedure

## Assorted Reading

Human Engineering: [MIL-STD-1472, archived on EVERYSPEC](http://everyspec.com/MIL-STD/MIL-STD-1400-1499/MIL-STD-1472H_57041/)

Electrical-Part Testing: [MIL-STD-202](http://everyspec.com/MIL-STD/MIL-STD-0100-0299/MIL-STD-202G_2397/)

## Design Goals

**Basic 1**: Safety, Performance, Reliability, Durability, Longevity

Note: durability means it does not break easily, longevity means it generally works for a long time, reliability means it consistently works (during its specified lifetime, even if non-critical parts break easily). Something can be reliable and fragile/short-lived.

**Basic 2**: Size, Weight, Form, Noise, Power, Functional Efficiency (input-output)

**Lifecycle**: Design for... Manufacturing, Transportation, Storage, Assembly, Deployment, Configuration, Customization, Maintenance, Repair, Removal, Recycling

**Environment**: Design for... Temperature (ex. thermal expansion), Ingress/Submersion (ex. dust/dirt/sand/water), Condensation, Erosion (natural/artificial), Corrosion, Sunlight (ex. UV exposure), Precipitation (avoid standing water, assess drip dynamics for externalities), Pressure (atmospheric/special)

## Safety

**Safety Methods**: Danger Removal, Danger Reduction, Shielding, Lockout, Signaling, Intuitive Interface (subconsciously guide safe user experience), Instructions

**Failure Planning**: Self-Test (Start-up, Dynamic), Pre-Failure Signals/Mechanisms, Graceful Failure, Human Error Tolerance, Blackbox Logging (identify root cause, improve next version)

Functional Safety:
[IEC 61508](https://webstore.iec.ch/publication/5515) (industrial), 
[ISO 26262](https://www.iso.org/standard/68383.html) (automotive),
[IEC 60730](https://webstore.iec.ch/publication/3117) (household)

## Common

**Common Events**: Impact Test (random shock), Compression Test (random weight), Drop Test (avoid damage/injury/shatter/chip)

**Dynamic Environment**: Rolling Stopper (Recovery from Fall on Angled Surface), Relatively-Distinct Color (Lost-and-Found Detection)

**Cleaning**: Smooth Surfaces, Hand-Fitting Internal Volumes, Compatible with Water Immersion and Spray, Minimal Contact with Floor, Easy-Clean Exterior (non-magnetic, non-adhesive, cleaning-chemical-compatible), Low-Splash Surface, Acceptable-Splash-Angle Surface

## Optimization

Efficiency

**Speed**: Motion, Data Transmission, Data Processing, Chemical Reaction Rate

## Usability

**Constrained Use**: One-Handed Use, Independent Use, Low-Tactile-Sense Use, Color-Blind Use, Impaired Vision Use, Impaired Hearing Use, Long-Distance Use, Awkward-Angle Use

**Ergonomic Methods**: Rounded Corners and Edges (Comfortable Handling), Handle (Intuitive Carrying), Grab Points (Non-Slip Lifting), Low Thermal Conductivity (Warm Handling), Tactile Feedback (Correct-Input Signal)

**Intuitive Sequence**: Left-to-Right, Top-to-Bottom

## Reliability

**Automotive Part Standards**: [AEC Qualification](http://www.aecouncil.com/AECDocuments.html)

Temperature: operating range, derating, cycling before use, cycling during use, freeze-thaw resistance, flame retardance (UL94)

## Maintenance

Signals: Maintenance Reminder, Problem Warning, Maintenance Guiding

Special: Spare Parts Inside Product (Useful Unity), First-to-Fail is Easiest-to-Replace (Zero Maintenance Damage Mitigation), On-Part Info Sticker/Engraving (ex. Company Name, Part Number)

## Durability

Resistance: Scratch, Chip, Dent, Vibrate, Fatigue, Shock, Ingress (assume it happens), Chemical, Galvanic Corrosion

## Size, Weight, Form

Fit Through: Standard Door, Garage Door, Car Door, Spiral Corridor, 

Fits Inside: Car Trunk, Car Seat, Backpack, Pocket

Special: Stackable Storage, Stackable Operation, Stands Upright Independently, Table Function (Large Flat Top), Floor Weight (High-Traction, High-Weight), Step-Stool (Small Flat Top, High-Stability)

Mechanical Unity: consistent physical connectivity; ex. car gas-cap is tethered

## Electrical

* Lightning Resistance
* ESD Resistance
* Overvoltage Protection (OVP)
* Overcurrent Protection (OCP)
* Reverse Polarity Protection (RPP)
* Electromagnetic Compatibility (EMC)

## Design Finality

**Design finality**: a measure of the similarity between the current design and the intended release design. Design finality can be measured at any fraction or scope of a given system. In practice, design finality is best measured for major decisions and modules. Design finality should not be confused with design perfection. Here, finality means that the design is good enough to be built into a real-world system generating value outside of the development environment, reflecting the quality threshold of the development team. A final design is built, released (ex. MK1), then improved on (as upgrade or replacement) by the next final design (ex. MK2). The benefit of design finality is important for reducing the non-transferable sunk-cost of non-final work between a prototype and the product that must be at least viable and at best excellent. For example, a major design change can cause all CAD work and fabrication work on the current prototype to be completely discarded. Ideally, all major design decisions should be quality-final for the future and development-practical in the present. The cost of design finality is the time required to verify its correctness and the opportunity cost of building a rough non-design-final full-system (instead of building a single design-final module).

* SIMPLE: The design is a functional placeholder and not intended to be final.
* STANDARD: The design is functional and logically consistent with at least the general elements of the final design.
* SEMIFINAL: The design is optimized and requires contextual accumulation and real world testing to reach finality.
* FINAL: The design is final at both idea and implementation and ready for direct inclusion in the next release.







