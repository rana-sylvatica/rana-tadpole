# rana-tadpole
## Pocket-sized digital controller
![IMG_0856_01](https://github.com/rana-sylvatica/rana-tadpole/assets/95242582/c3fc73cc-1a0c-49a2-8b72-7b2aa71d1f71)

### Overview:

The Rana Tadpole is a pocket-sized 20-button digital controller, designed for platform fighters but usable for other fighting games, platformers, etc.

Unlike most other similar controller designs that use either keyboard switches or arcade buttons, the Tadpole uses mouse switches (Kailh GM 4.0 if using the provided BOM files - there are other compatible switches that can be subsituted as well at the builders discretion).

With the mouseclick switches, the Tadpole has best-in-class button travel distance, a mere 0.8mm until bottom-out, for fast reactions and precise inputs.  The mouseclick switches also enable the entire board to be easily factory assembled, cutting down on cost and build time.

This repository contains design files for all required components to build your own Rana Tadpole.  Scroll down for open source license information, parts list, link to build guide, and user guide.

### Attributions:

Many thanks to [Quark](https://github.com/Armastardo) for the PCB design for both the motherboard and daughterboard!

### Licensing:

This project is licensed under CERN Open Hardware Licence Version 2 - Strongly Reciprocal

In short, this means:
 - License applies to publicly available hardware designs
 - Allows use, reproduction, modification, distribution, and sale of the design
 - License requires distribution under same terms, attribution to original designer(s)
 - Does not grant trademark rights, includes disclaimer of liability
 - License may be terminated for non-compliance

Anyone may use these design files to make their own Rana Tadpole(s) for personal use or to sell, or modify the design however they wish.
However, if a modified design is distributed (either digitally or physically beyond personal use), the modified design must be publicly posted under the same terms.

Note: if selling Rana Tadpoles, YOU MUST link to this repo (or your fork of this repo, if you modify the design) on your store page.  If selling in-person, MAKE SURE to communicate that this is an open-source project, and provide (via QR code or similar) a way for the customer to access this repo (or the applicable fork).

All these files are posted as-is. This source is distributed WITHOUT ANY EXPRESS OR IMPLIED WARRANTY, INCLUDING OF MERCHANTABILITY, SATISFACTORY QUALITY AND FITNESS FOR A PARTICULAR PURPOSE. 

If you are interested in supporting this project, donations are accepted at [paypal.me/RanaLabs](https://www.paypal.me/RanaLabs).

### Parts list:

The Rana Tadpole build requires the following list of components:
 - #### Case
   - 3D printed or CNC machined, see CAD files
   - Additional notes:
     - JLCPCB or PCBway are affordable CNC machining vendors.  If you want the screw holes threaded at the factory (rather than doing it by hand), you will need to create a drawing specifying the thread type, hole position, and thread depth.
     - If 3D printing the case, the provided file is designed to have the screws thread directly into the plastic.  Getting a good fit on your printer may require some adjustment.  The files can also be modified to accept heat set inserts, or other screws (such as specialized thread-cutting screws) can be subsituted for the machine screws as well.  Just do your research on hole diameters, etc.
     - I plan to post a case model in the future that is designed for ordering inexpensively from a 3D printing service such as JLCPCB, but that design is not quite ready yet.
 - #### Button caps
   - 3D printed, see CAD files
   - Additional notes:
     - For best quality, order the Tadpole_Button_x8 file from JLCPCB or other 3D printing service in SLS or MJF nylon
     - Resin printing also works well
     - These buttons are difficult to print with a FDM printer, but please let me know if you find a modification to the design that allows them to print well!
 - #### Motherboard
   - Embedded rp2040 PCB with factory-soldered mouseclick switches, see KiCAD and Gerber files
   - The Gerber and assembly files are generated for ordering through JLCPCB.  Other PCB fabs can also be used, but you may need to generate the production files differently.  (applicable to all three PCB components here)
 - #### USB Breakout board
   - USB C board with case grounding and ESD protection, see KiCAD and Gerber files
 - #### Backplate
   - Silkscreen PCB (or lasercut/3D printed). KiCAD/Gerber, DXF, and .STEP files available
 - #### Foam pads
   - Lasercut EVA foam, DXF files available
   - Example foam that works well: https://www.amazon.com/gp/product/B07V5PR459
 - ####  Ribbon cable
   - 12 pin, 0.5mm pitch, 50mm length FFC
   - Example items: https://www.digikey.com/en/products/detail/assmann-wsw-components/AFFC-050-12-051-11/6570261, https://www.aliexpress.us/item/3256803954097404.html
 - #### Grounding foam
   - Optional, but helps with ESD protection if using the PCB backplate.  Link: https://www.aliexpress.us/item/3256805239781097.html 
 - #### Hardware
   - Screws
     - 2x M3x6mm (for securing the USB C board).  Link: https://www.mcmaster.com/94500A221/
     - 6x M3x8mm (for securing the backplate/motherboard).  Link: https://www.mcmaster.com/92095A181/ OR https://www.aliexpress.us/item/2255800885711092.html
   - Spacers
     - 6x X-profile o-rings, dash number 104.  Link: https://www.mcmaster.com/90025K513/

#### Extras: 
 - #### USB C-USB A cable (for PC/switch compatibility)
   - Any USB data cable will work
 - #### USB C-GCC cable (for gamecube/wii compatibility)
   - Several suppliers such as B0XX, Frame1, JunkFoodArcades, HandHeldLegend.  HHL is currrently the best option for price/quality: https://handheldlegend.com/products/retro-c-gamecube-cable-usb-c-to-gamecube-cable?variant=40183052337286
 - #### Belt clip
   - .STL file provided for 3D printing
 - #### Carry bag
   - Canvas zipper pouches that measure at least 8" x 6" work well


### Assembly guide:

See YouTube video: https://www.youtube.com/watch?v=oF4wL67agoM

### User guide:

There are three different open-source firmwares that the Rana Tadpole is compatible with: 
 - [HayBox](https://github.com/JonnyHaystack/HayBox)
   - Compatible with:
     - PC (as XInput or DInput device)
     - GameCube
     - Wii
     - Switch
     - N64
     - Other consoles (via Brook Wingman adapter)
 - [pico-rectangle](https://github.com/JulienBernard3383279/pico-rectangle)
   - Compatible with:
     - PC (as emulated GC adapter or XInput device)
     - GameCube
     - Wii
     - Switch
     - Other consoles (via Brook Wingman adapter)
 - [GP2040-CE](https://gp2040-ce.info/#/README)
   - Generally used for traditional fighting games, compatible with:
     - PC
     - PS3
     - PS4
     - Switch
     - Other consoles (via Brook Wingman adapter)
    
    Please refer to the documentation for each firmware for more information.

   #### Default layouts:

   HayBox and pico-rectangle:
   ![smash_layout_transparent](https://github.com/rana-sylvatica/rana-tadpole/assets/95242582/be8bfa13-1f5c-4dd3-b879-04f589a3813d)

   GP2040-CE:
   ![gp2040ce_layout_transparent](https://github.com/rana-sylvatica/rana-tadpole/assets/95242582/6a730d0e-c2af-4caa-a8e8-48382a2b9a84)

   #### Switching and flashing firmwares:

   To flash a firmware, the rp2040 chip inside the Tadpole motherboard must be put in BOOTSEL mode, at which point the controller will show up as a mass storage device when plugged into a computer and the fimrware file can be copied to it.

   There are two ways of putting the Tadpole in BOOTSEL mode.  First, there is a small button on the motherboard that can be held down as the board is plugged into the PC.  However, this can be inconvenient as it requires disassembling the controller to access this button.

   The alternative method is to use hold a button (or button combination) specific to the particular firmware, when plugging into the PC.
   - For HayBox: hold Start
   - For pico-rectangle: hold C-Right
   - For GP2040-CE: hold Start + Select + Up (refer to the GP2040-CE layout graphic)
  
   Additional notes on GP2040-CE:
   - Eventually, the Rana Tadpole configuration may be added to the GP2040-CE website.  For now, just use the .UF2 file in this repository.
   - Hold Start on plugin to put it in web-config mode to change button mappings
