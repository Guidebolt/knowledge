# Tools - 3D Printing

Read [here](https://www.lulzbot.com/learn/tutorials/2019-3d-printer-buyers-guide-compare-technologies) about different types of 3D printers.

We use the following FFF-type 3D printers:

* Lulzbot Taz Pro
* Lulzbot Mini 2

We recommend using a 3D printer that supports a detachable data drive (like a USB drive or SD card). Portable drive support is essential for convenient printing because MCAD design work often occurs on a desktop computer far away from the 3D printer. Also, tethered prints depend on a persistent printer-computer data-link which is more prone to disruptions (ex. sleep mode, loose cables) and commits the computer (stay tethered nearby, send data without interruptions) for the print duration.

We recommend placing your 3D printer on a hard, flat table surface because it significantly improves the stability of your print bed (especially for larger work volumes). Uneven, soft tabletop surfaces can cause the print-bed to sag and wobble at its corners (especially during fast and long travel movements), causing poor inter-filament adhesion both horizontally (line-to-line) and vertically (layer-to-layer).

We recommend setting an aggressive Z-offset (low nozzle-to-bed distance) to ensure good first-layer-to-bed adhesion and good layer-to-layer/line-to-line adhesion. Excessive nozzle-to-bed distance can cause weak vertical adhesion that peels easily and horizontal gaps that sharply weaken the print.

We recommend setting a balanced nozzle-wipe temperature (high enough to soften the on-nozzle filament, low enough to avoid filament dripping) for consistently accurate pre-print calibration. A dirty nozzle can interfere with the automatic Z-probing sequence, either stopping the print process entirely or causing over-compensated bed leveling (which excessively reduces the nozzle Z clearance and ruins the first-layer).

We recommend setting a high printing temperature to ensure strong inter-filament adhesion. But keep the temperature low enough to avoid stringing, which is hazardous and can add significant post-processing work.

We recommend setting a high bed temperature to maintain good first-layer-to-bed adhesion throughout the entire print, especially for larger prints which warp more easily (usually after a few layers).


