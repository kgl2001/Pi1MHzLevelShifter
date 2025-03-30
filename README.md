# Pi1MHz Level Shifter for use with BBC Micro and Master 128 computers.

This project allows a Raspberry Pi to be connected to the 1MHz port on the BBC Micro and Master 128 computers, and emulates a number of existing Beeb peripherals plus some new ones:

* ADFS Harddisc
* Music 5000 / 3000
* Expansion RAM (480Mbytes for a PiZero)

A PiZero, PiZeroW or PiZero2W and level shifter can sit under a Beeb or Master.

The Pi3A+ and Pi3B+ are also supported via a cable as it won't fit under the computer.

The latest Pi Firmware can be downloaded from the following sites:

https://github.com/dp111/Pi1MHz
https://www.stardot.org.uk/forums/viewtopic.php?t=19513

Some general notes:

* The source files are to be used with KiCAD v9.0.0 or later.
* The gerber files have been optimised for fabrication by JLCPCB. In particular, there is a 8mmx8mm silkscreen box on the rear of the PCB. This is to allow a 2D barcode, with unique serial number to be printed on the PCB.
* If you want the barcode to be added, then make sure to select this option in the 'Mark on PCB' field, and make sure to select 'Specify position' in the '2D Barcode Position' field, otherwise you will end up with a white 8mm x 8mm box printed on your PCB and a 8mm x 8mm barcode printed at a position of JLCPCBs choosing. Thrust me on this!
* If you don't want the barcode added, then remove the 8mm x 8mm box from the silkscreen layer and regenerate the gerbers. Otherwise you will end up with a white 8mm x 8mm box printed on your PCB.
* A combined CPL / BOM file is included in the gerber directory. Again, this is for use with JLCPCB, if you want to use their PCBA (PCB Assembly) to solder on all the SMD parts.
* You will need to source suitable 34 pin right angle and 40 pin straight through sockets, and solder these onto the PCB. The Raspberry Pi will connect to the 40 pin socket and the level shifter will plug into the 1Mhz port via the 34 pin socket.
* Be aware that it is possible to misalign the 34 pin socket both vertically and horizontally when plugging it into the 1MHz port so take care to ensure it is aligned correctly.
* The pins on the 1MHz bus connector may be tarnished if the header has not been used for many years. This can cause unreliable operation. This can usually be fixed with repeated removal and re-insertion of the level shifter into the header.
* Do not use a ribbon cable to connect the Raspberry Pi to the level shifter. Instead, the Raspberry Pi should be plugged directly into the level shifter.
* The level shifter can be plugged directly into the 1MHz bus connector in the well underneath the keyboard, or it can be attached to the 1MHz bus connector via a 34 way male / female ribbon cable.
* There is limited space in the well underneath the Master, so the the level shifter should initially be inserted at an angle and then straightened out as the level shifter is pushed home into the 1MHz bus connector.
* Due to the limited space underneath the Master, a compromise had to be made on the overall size of the level shifter board. Therefore, when fitting the level shifter into the Model B it may not be possible to push the level shifter fully into the 1MHz socket, otherwise the front face of the Pi will clash with part of the computer case. 
* No power is available from the 1MHz bus connector, so a 5v supply to power both the level shifter and Raspberry Pi must be found from elsewhere. A JST-XH (or similar) connector can be added to the level shifter board and both the level shifter board and the Pi can be powered via this connector.
* If attaching the level shifter directly to the 1MHz bus connector, it is possible to pick up a suitable 5v supply from either the tube connector or the user port. A separete supply is not required for the Raspberry Pi in this case. If both these ports are already in use, then an alternative location for powering the level shifter board and Raspberry Pi will need to be found.
* If picking up power from the tube connector or the user port, a small 2 core cable with a JST connector on one end and Dupont connector on the other end is recommended for connecting between the tube connector or the user port and the level shifter.
* If the level shifter is connected to the 1MHz bus connector via a ribbon cable then the simplest way to power the level shifter and Raspberry Pi is via a standard Raspberry Pi power supply connected to the Raspberry Pi. This will also power the level shifter. You should not attempt to use separate power supplies to power both the level shifter and the Raspberry Pi.

Please refer to the following discussion on Stardot for further details: https://www.stardot.org.uk/forums/viewtopic.php?t=18513

## Developer

The 1MHz level shifter board is developed and maintained by Ken Lowe.
    
## Hardware License (Creative Commons BY-SA 4.0)

Please see the following link for details: https://creativecommons.org/licenses/by-sa/4.0/

You are free to:

Share - copy and redistribute the material in any medium or format
Adapt - remix, transform, and build upon the material
for any purpose, even commercially.

This license is acceptable for Free Cultural Works.

The licensor cannot revoke these freedoms as long as you follow the license terms.

Under the following terms:

Attribution - You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.

ShareAlike - If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

No additional restrictions - You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.
