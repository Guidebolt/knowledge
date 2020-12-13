# General Design

In hardware development, you arrange physical atoms. In software development, you arrange abstract states. In both cases, you plan the interactive sequence of the system.

## Efficiency

* Power Efficiency
* Volume Efficiency
* Mass Efficiency

## Speed

* Motion
* Data Transmission
* Data Processing

## Sequence

* Danger Removal
* Danger Reduction
* Shielding
* Signaling

## Ergonomics

* Rounded Corners and Edges (Comfortable Handling)
* Handle (Intuitive Carrying)
* Grab Points (Non-Slip Lifting)
* Low Thermal Conductivity (Warm Handling)
* Tactile Response (Input-Detect Confirmation)

## Intuition

* Left-to-Right Sequence (Observe/Interact)
* Top-to-Bottom Sequence (Observe/Interact)

## Edge Cases

* Rolling Stopper (Recovery from Fall on Angled Surface)
* Distinct Color relative to Application Environments (Detection)

## Ease of Cleaning

* Smooth Surfaces
* Hand-Fitting Internal Volumes
* Compatible with Water Immersion and Spray
* Minimal Contact with Floor
* Non-Magnetic Exterior
* Non-Adhesive Exterior
* Cleaning-Chemical-Compatible Exterior

## Ease of Maintenance

* Problem Warning Signal
* Maintenance Reminder Signal
* Maintenance Guiding Signal
* Graceful Failure Process
* First-to-Fail Points are Easy-to-Replace
* On-Part Identifying Sticker/Engraving (Company Name, Part Number, Serial Number)
* Spare-Parts Inside the Product

## Integration

* Parallel Surfaces (Grip-Mounting)
* Hole (Screw or Cord)

## Impaired and Constrained Use

* One Handed Use
* Low-Tactile-Sense Use
* Color-Blind Use
* Blind Use
* Deaf Use
* Long-Distance Use
* Awkward-Angle Use

## Compact Operation

* Stackable Storage
* Stackable Operation
* Stands Upright Independently
* Fits Through Door
* Fits In Car

## Extra Functionality

* Table Function (Large Flat Top)
* Floor Weight (High-Traction, High-Weight)
* Step-Stool (Small Flat Top, High-Stability)

## Mechanical

* Fatigue Strength
* Shock Resistance
* Drop Resistance (Normal, High, Fall)
* Vibration Resistance
* Ingress Protection (IP)

## User

* Human-Error Prevention/Mitigation/Resistance

## Electrical

* Lightning Resistance
* ESD Resistance
* Overvoltage Protection (OVP)
* Overcurrent Protection (OCP)
* Reverse Polarity Protection (RPP)
* Electromagnetic Compatibility (EMC)

## Temperature

* Operating Temperature
* Thermal Derating
* Thermal Cycling Before Use
* Thermal Cycling During Use
* Freeze-Thaw Resistance
* Flame Retardance (UL94)

## Chemical

* Chemical Resistance
* UV Resistance
* Environmental Corrosion, Galvanic Corrosion

## Automotive Standards

* AEC-Q100 (Integrated Circuits)
* AEC-Q101 (Discrete Semiconductors)
* AEC-Q200 (Passive Parts)

## Military Standards

* MIL-STD-202 (Electrical-Part Testing)

## Mechanical Unity

Mechanical unity is the degree of physical connectivity between separate parts during operation.

Example: A modern car has a gas-cap that is tethered to the vehicle for a no-drop user-experience. This avoids the ergonomic hassle of having the gas cap fall underneath the car. This avoids the explosion risk of driving/parking with an unsealed gas-port after the cap is lost.

## Design Finality

### What is Design Finality

Design finality is a measure of the similarity between the current design and the release design.

Design finality can be measured at any fraction or scope of a given system. In practice, design finality is best measured for important decisions and modules.

Design finality should not be confused with design perfection. Here, finality means that the design is good enough to be built into a real-world system generating value outside of the development environment. A final design is built, used, then improved on (as upgrade or replacement) by the next final design.

Design finality should not be confused as only the fulfillment of minimum performance requirements. Here, finality means that the design has reached a standard of quality that reflects the intentions of the designers constrained by currently available technologies and time/resource budgeting. In other words, design finality is a special choice within the possibility space of differently prioritized designs. For example, when the designer thinks that a significantly better possibility exists with low development-cost, they may determine the current satisfactory solution to be non-final.

### Why Measure Design Finality

The evaluation of design finality is important for reducing the non-transferable sunk-cost of non-final work. For example, a major design change can cause all CAD work and fabrication work on the current prototype to be completely discarded. Ideally, one works only on final designs and implementations to be included in the next release.

### How to Measure Design Finality

Design finality is generally measured in qualitative basis with a minimum of 2 levels (final or non-final).

...

* Simple
* Standard
* Semifinal
* Final

SIMPLE: The design is a functional placeholder and not intended to be final.

STANDARD: The design is functional and logically consistent with at least the general elements of the final design.

SEMIFINAL: The design is optimized and requires contextual accumulation and real world testing to reach finality.

FINAL: The design is final at both idea and implementation and ready for direct inclusion in the next release.
