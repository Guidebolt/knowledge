# Version Control

REV: 2021-01-11

## Version Naming

"MK" (mark) means major version. The major version starts from 1 and increments as whole numbers (ex. 1, 2, 3). The major version increments when the design incurs a large change. A large change is when the quality of some factor (ex. speed, reliability) improves significantly and usually involves a fundamental improvement of the general design.

Example: MK1

"R" (revision) means minor version. The minor version starts from 1 and increments as whole numbers (ex. 1, 2, 3). The minor version increments when the design incurs a small change that is built or externally-communicated (ex. released-to-users or sent-to-suppliers).

Example: R2

Understanding the difference between names, major versions, and minor versions.

Example: Consider a car in development with name CAR-MK1R1. If the car's electronics become 20% more energy-efficient, the minor version should increment. If the project pivots to the design of a truck, the name of the product should change, ex. TRUCK-MK1R1. If the car adds self-driving technology, the major version should increment.

A version name shall reset its minor version to 1 whenever its major version increments.

Example, Bad: MK1R2 becomes MK2R2

Example, Good: MK1R2 becomes MK2R1

A version name shall NOT be separated by any symbol.

Example, Bad: MK1-R2

Example, Good: MK1R2

A version name shall ONLY be formed with uppercase symbols.

Example, Bad: mk1r2

Example, Good: MK1R2

A version name shall NOT use decimals in the incrementing-number.

Example, Bad: MK1R2.1

Example, Good: MK1R3

A version name shall not depend on another version name, regardless of any level of part-assembly branching.

Example, Bad: Part XYZ-MK1R10 in Assembly A-MK1R1 becomes Part XYZ-MK2R1 in Assembly B-MK2R1

Example, Good: Part XYZ-MK1R10 keeps its version name across any assembly, including A-MK1R1 and B-MK2R1. 

A version name can include an internal version number, symbolized by "T" (test) and incremented from 1 as a whole number.

Example: MK1R2T1

Internal versions are used to sequence and organize design-files through special cases when the design has not meaningfully changed.

Example: typo/excess-tolerance/low-export-quality/bitrot in MK1R2T1, fixed in MK1R2T2

Products with an internal version shall NOT be released for public use. Normally, once a product version is refined, the internal version is removed and the minor version is incremented, becoming ready for production release.

## Version Control System

We use GIT. Good for small-size filesets. Strongly recommended.

[GIT Official Website](https://git-scm.com/)

