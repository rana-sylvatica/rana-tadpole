# rana-tadpole
## Pocket-sized digital controller
![IMG_0856_01](https://github.com/rana-sylvatica/rana-tadpole/assets/95242582/c3fc73cc-1a0c-49a2-8b72-7b2aa71d1f71)

### Overview:

#### NOTE: I am in the process of updating this repository with information and design files for the Rana Tadpole V2.  This process isn't quite done yet - wait a few days if you are looking to build your own Tadpole V2 (I'll remove this note once I'm done with the update)

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
   - These can be purchased from me (injection molded PBT) or 3D printed.  Link to purchase: https://ko-fi.com/s/469357a31c
   - Additional notes for 3D printing:
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
   - These can be purchased from me (die cut textured silicone rubber), or lasercut from EVA foam or similar.  Link to purcahse from me: https://ko-fi.com/s/3146277fc0
   - Example foam that works well: https://www.amazon.com/gp/product/B07V5PR459
 - ####  Ribbon cable
   - 12 pin, 0.5mm pitch, 50mm length FFC, Same side contacts (sometimes called "Forward Direction"
   - Example items: https://www.digikey.com/en/products/detail/assmann-wsw-components/AFFC-050-12-051-11/6570261, [https://www.aliexpress.us/item/3256803954097404.html](https://www.aliexpress.us/item/3256805295157150.html)
 - #### Grounding foam
   - Optional, but helps with ESD protection if using the PCB backplate.  Link: https://www.aliexpress.us/item/3256805239781097.html 
 - #### Hardware
   - Screws
     - 2x M3x6mm (for securing the USB C board).  Link: https://www.mcmaster.com/94500A221/
     - 6x M3x10mm (for securing the backplate/motherboard).  Link: [https://www.mcmaster.com/92095A181/](https://www.mcmaster.com/92095A182/) OR [https://www.aliexpress.us/item/2255800885711092.html](https://www.aliexpress.us/item/3256804883804669.html?)
   - Spacers
     - Can either use:
       - 6x X-profile o-rings, dash number 104.  Link: https://www.mcmaster.com/90025K513/
       - 3mm thick gaskets using the files in this repo - these can be 3D printed in soft TPU or die cut from silicone or similar

#### Extras: 
 - #### USB C-USB A cable (for PC/switch compatibility)
   - Any USB data cable will work
 - #### USB C-GCC cable (for gamecube/wii compatibility)
   - Several suppliers, but HHL or my store are good options: https://handheldlegend.com/products/retro-c-gamecube-cable-usb-c-to-gamecube-cable?variant=40183052337286, https://ko-fi.com/s/bc4af1084a
 - #### Belt clip
   - .STL file provided for 3D printing
 - #### Carry bag
   - Canvas zipper pouches that measure at least 8" x 6" work well


### Assembly guide:

See YouTube video: https://www.youtube.com/watch?v=oF4wL67agoM

NOTE: This is slightly out of date now, given the V2 version that adds the slide switch.  I may eventually make an updated build guide, but for now this is still mostly relevant.

### Dual Firmware Switch:

The Rana Tadpole V2 has a fun new feature - two different flash memory chips, with a switch on the side of the controller to select between them.  This is very useful if you want to use your Tadpole for both platform fighters and traditional fighters - you can load HayBox on one memory slot and GP2040-CE on the other.

#### IMPORTANT NOTE: Do not flip the firmware switch while the device is plugged in.  Unplug it, flip the switch to the other position, and plug it back in.

### Aux USB C Port:

Another new feature of the Tadpole V2 is the auxillary USB C port on the side of the controller.  The main purpose of this is for passthrough authentication when using GP2040-CE firmware, to get PS4/PS5 compatibility without additional input latency.  

This port is also capable of becoming a flexible expansion port in the future, with many possibilities including: an adapter to connect a GCC for mixed input (left hand GCC, right hand Tadpole) gameplay, pluggable analog joystick(s), etc.

#### MORE INFO TO COME HERE

### Firmwares:

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
   - For HayBox: hold Start (may be different if using a fork of HayBox.  For example, https://github.com/GRAMCTRL/HayBox-GRAM uses "A" as the button hold to get into BOOTSEL mode).
   - For pico-rectangle: hold C-Right
   - For GP2040-CE: hold Start + Select + Up (refer to the GP2040-CE layout graphic)
  
   Additional notes on HayBox:
   - The HayBox-GRAM fork brings a few features such as web remapping (see below) and a dedicated Rivals 2 mode, that aren't (yet) in a pre-compiled release of mainline HayBox.
     - In the firmware-binaries folder is a .UF2 file for the Tadpole configuration of this firmware.  Until there is a mainline HayBox release that includes these new features, this is a good choice.
     - To access the remapper, go to remapp.ing, hold Start when plugging in the Tadpole, and follow the instructions on the screen.
  
   Additional notes on GP2040-CE:
   - The Rana Tadpole version of GP2040-CE can be downloaded from: https://gp2040-ce.info/downloads (scroll down until you find the Tadpole download link)
   - Hold Start (refer to the GP2040-CE layout graphic) on plugin to put it in web-config mode to change button mappings, go to https://gp2040-ce.info/web-configurator/ to access the configurator
   - To enable passthrough authentication for PS4/PS5 compatibility (with an appropriate adapter such as a Brook Wingman, Honson F5, Mayflash Magicboots, or Haute42 Booter5), go to the peripheral mapping section of the GP2040-CE Web Configurator and enable USB Host  mode on pin 9 as shown in the image below:
     
     ![image](https://github.com/user-attachments/assets/72e85c38-159a-497a-b7da-5fe01bf1f00f)

