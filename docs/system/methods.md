# Methods





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
