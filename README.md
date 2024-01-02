# modkipz40

A pocket keyboard using mouse switches, now with 🤌 *ergonomics* 🤌

![an image of my modkipz40](https://github.com/ChrisChrisLoLo/modkipz40/blob/main/photos/PXL_20231210_225053966.NIGHT.jpg?raw=true)

# Status

v0.1 should now work without issue (tvs diode data lines have been corrected), though hasn't been produced and explicitly confirmed yet.

v0.0 has an error where the usb lines are swapped when connected to the tvs diode. I was able to get around this by cutting out the tvs diode and jumping the usb data line pads. After doing this, the board worked without issue.

# About

This is my second pocket keyboard using mouse switches, and the successor to the [bunchiez40](https://github.com/ChrisChrisLoLo/bunchiez40). The key difference is that it has a angle between the key halves.

This board is a PCBA, so only the switches need to be soldered on. The board makes use of a STM32F072 as it's MCU.

Blog post about my experience building the board can be found [here](https://chrischrislolo.github.io/orthoLabLogs/modkipz40-how-i-used-ergogen-for-the-first-time.html)

# Case

Case files can be found in the `case` directory. The case was largely created by extrusions from the dxf outlines generated from Ergogen. Ergogen file can be found in the `drafts` directory.

Case can be 3D printed. In theory the case can also be CNC'ed, though this hasn't been explicitly tested.

# PCB

PCB can be found in the `pcb` files. The `outputs.zip` file contains the files needed for the PCB, and `lemmingz40_modified.csv` and `lemmingz40_bottom-pos_modified.csv` contain the BOM and position files needed for PCBA.

Please confirm that the PCB has the `v0.1` silkscreen on it, as it fixes an error in `v0.0`. Note that `v0.1` should work as it emulates a manual fix, but `v0.1` has not yet been officially produced and verified.

# Directory Structure

`drafts` contains the ergogen file used to generate pcb outlines and case extrusions.

`pcb` contains the source code and output files required to produce a PCBA.

# BOM

You will need the following to make a modkipz40

- 8x 4.5mm M1.6 screws
    - ideally the screws are countersunk
- 8x 1-2mm bumpons
    - Sj5302 works for me, though generally anything works
- 40x kailh/huano 7.3mm mute switches
    - I used huano black mute switches for this build
- 1x PCBA
- 1x bottom case
    - I FDM 3D printed mine, though any manufacturing technique should work
- 1x top case
    - Same as the bottom case

# Assembly

The assembly process should generally be straightforward

- Flash the board with firmware
- Confirm that board works by shorting a key
- Solder the switches onto the board. The switches should be placed on the blank side of the PCBA, so that the switch pins are soldered on the same side as the MCU
- Screw bottom of case to PCBA
- Screw top of case to PCBA
- Add bumpons to the bottom of the case. The bumpons should be on every corner of the case bottom

# Firmware

Firmware source code can be found [here](https://github.com/ChrisChrisLoLo/vial-qmk/tree/sporewoh/keyboards/sporewoh/modkipz40)

# Sponsors
If you like what I make, please consider becoming a [sponsor](https://github.com/sponsors/ChrisChrisLoLo)! Your support allows me to continue creating experimental keyboard designs, as well as help me iterate and retest existing ones! 
