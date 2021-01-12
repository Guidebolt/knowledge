# Version Control

REV: 2021-01-11

## Version Naming

"MK" (mark) means major version. Number incremented.

Example: MK1

"R" (revision) means minor version. Number incremented.

Example: R2

A version name shall NOT be separated by any symbol.

Example, Bad: MK1-R2

Example, Good: MK1R2

"P" (prototype) means internal version. Number incremented.

Example: MK1R2P1

Products that have version names with "P" should NOT be released for public use, normally.

Internal versions are used to sequence and organize design-files through special cases when the design has not meaningfully changed.

Example: typo/excess-tolerance/low-export-quality/bitrot in MK1R2P1, fixed in MK1R2P2

## Version Control System

We use GIT. Good for small-size filesets. Strongly recommended.

[GIT Official Website](https://git-scm.com/)

