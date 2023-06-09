![DandaCart](Images/dandacart_logo.png)
# Dandanator Cartridge System
Most of us ZX Spectrum fans are well aware of the ZX Dandanator! Mini, a game cartridge for the Spectrum computers. It is a fine piece of hardware, the only problem is that the ROM quickly gets filled with games, especially if you want to play Multiload titles, and then there are some hard choices about what to keep and what to delete. This project, based on the idea of my fellow retro enthusiast Artur Grütz, aims to rectify it.

The DandaCart simply moves the onboard memory chip to a cartridge. The device remains fully compatible with the original Dandanator (including Multiply and joystick support). Now you can burn as many cartridges as you want and simply swap them out as necessary! There is also something very satisfying about inserting a real, physical cartridge to play a game.

One of the stated goals of the Dandanator project is to be “a platform for developing and releasing cartridge games”. Now, with a system of replaceable cartridges, this could become a reality!

![DandaPhoto](Images/20230505_165824.jpg)

This repository contains the KiCad projects for three PCBs: the base board (_DandaCartBase_) and two versions of the cartridge board (_DandaCartDIP_ and _DandaCartPLCC_). You can choose the cartridge PCB version based on the type of the SST39SF040 memory you have available (DIP-32 or PLCC-32); be aware, however, that the PLCC version is more difficult to solder, there is no PLCC socket in the design, because the cartridge would become too bulky then. The _Gerbers_ directory contains ZIPs ready for manufacturing — the cartridge PCBs are already panelized (six cartridge PCBs on one board).

## See DandaCart in action
[Youtube Video](https://youtu.be/q8KvgayKHwo)

## Building the DandaCart
The Bill of Materials can be found in the _DandaCartBase/BOM_ directory and is almost the same as for the original Dandanator, only instead of the PLCC socket a 2x18pin edge card connector is used. As for the cartridge connector, when soldering it to the base board, two pins will have to be removed; I was originally planning for the cartridges to have a notch in the PCB and for the edge connector to have a keying tab, but I had run into difficulties with the notch on the panelized layout, so I finally decided for the cartridge housing itself to be keyed (to prevent incorrect insertion), but by then I had already routed quite a few traces through the gap, and with the cartridge slot running across the board it was really difficult to route all the traces to the rear expansion connector, so I decided to leave it like that.

![DandaPhoto2](Images/20230505_233213.jpg)

The _3DModels_ directory contains STL files for printing the base board enclosure and the cartridge enclosure. There is also the _Label_ directory with a label for the cartridges (to be printed on self-adhesive 10x15 cm photo paper).

All the software, such as .hex and .jed files for programming the onboard microcontroller and the GAL chip, manuals etc. are available at the Dandanator site:
http://www.dandare.es/Proyectos_Dandare/Proyectos.html

The Multiply expansion Github repository is available at:
https://github.com/mad3001/Multiply

## License
LICENSE: CC BY-SA 4.0
https://creativecommons.org/licenses/by-sa/4.0/

## Acknowledgements
Of course, full credits go to Dandare, the creator of the original Dandanator, as well as Mad3001 and OverCLK, the co-creators of the Multiply expansion. All I did was some PCB routing and some light CAD work. Special thanks to Artur Grütz for his idea of replaceable cartridges!
