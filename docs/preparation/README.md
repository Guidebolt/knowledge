# README

In hardware development, you arrange physical atoms. In software development, you arrange abstract states. In both cases, you plan the interactive sequence of the system.

## Mechanical Design

## Electrical Design

Good electronics meet material safety standards such as RoHS, REACH, and JEDEC halogen-free (J-STD-609). Good parts are also flame-resistant (UL94-V0 is good) and EM-compatible (CISPR) as both low-interference and high-tolerance. Part moisture-sensitivity (MSL-1 is ideal) has minimal effect on operating performance (when assembled after correct handling) but better insensitivity provides flexibility (time, environment) for pre-assembly storage and processing.

For reliability, avoid pure-tin (ex. solder, plating) to eliminate the tin-whiskering failure-mechanism. Use PCB materials with low thermal expansion (CTE, cycling) and high electromechanical stability (CAF, electro-migration). For power electronics, prefer PCB materials with high thermal-solidity (Tg is glass-transition, Td is decomposition) and high thermal-conductivity (0.7W/mK is good non-ceramic benchmark). For signal electronics, prefer PCB materials with low dissipation-factor (Df), low relative-permittivity (Dk), and consistent impedance-control. Build PCBs with quality plating (ENIG is good) to a consistent fabrication class (IPC-2 is good, IPC-3 is better) and conduct pre-assembly electrical-testing (ex. flying probe).

For usability, prefer part packages that can be manually soldered and desoldered. 

For strategy, consider the immediate and long-term availability (current stock, factory lead-time, pending orders) of each part costed at prototype-quantity (1 to 100 typical) to production-quantity (1000 to 10K+ typical).

## Software Design
