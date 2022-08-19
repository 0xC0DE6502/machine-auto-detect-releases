# Machine Auto Detect (MAD)
MAD is a tool for Acorn Electron developers. It is a small program that automatically detects which machine, real Electron or emulator, it runs on. MAD integrates easily with your program and allows you to write code, e.g. a timing critical part, that works well on any real Electron or emulator.

## Latest release
MAD v1.5 (20220819)

## Machines detected
MAD detects a real Electron and the following emulators: Electrem, Elkulator, Electroniq, CLK, MAME and ElkJS.

## How to use
0. Download the [MAD tape image](https://github.com/0xC0DE6502/machine-auto-detect-releases/raw/main/machine-auto-detect.uef) or the [MAD disk image](https://github.com/0xC0DE6502/machine-auto-detect-releases/raw/main/machine-auto-detect.ssd) 
1. Run and examine the BBC BASIC example program to learn how to load and execute MAD
2. Add MAD to your own program, e.g. `*LOAD MAD A00` (load address is flexible), `CALL &A00` and find the detected machine in the `X` register (see below)

## Features
* Location independent code, so load and execute anywhere (then discard)
* Zero page is preserved, but CPU registers and flags are not
* After calling MAD, the `A` register contains the MAD version (e.g. `&15` for MAD v1.5) and the `X` register contains the ID of the detected machine:
  - `-1` (`255`): Not an Electron (probably a BBC Micro or similar)
  - `0`: Real Electron
  - `1`: Electrem
  - `2`: Elkulator
  - `3`: Electroniq
  - `4`: CLK
  - `5`: MAME
  - `6`: ElkJS

## Contact
Please contact me on [Twitter](https://twitter.com/0xC0DE6502) if you have any issues or questions about MAD. I hope you find MAD useful and would like to be credited in your program if you use MAD. Cheers!

---

Machine Auto Detect (MAD) - Copyright (C) 2021-2022 [0xC0DE](https://twitter.com/0xC0DE6502)
