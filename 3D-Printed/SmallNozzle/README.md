# 0.25mm Nozzle Parts

## Material / part requirements:

* Carbon-Fiber PA6 Nylon (Polymaker Polymide CF-PA6)
* Filament dryer which can dry Nylon
* 0.25mm hardened nozzle at 300°C
* Magigoo PA on 45°C bed
* Print each part one at a time to keep the layer time as short as possible. This makes layer adhesion as strong as possible.

## Slicer settings:

Assuming your hot end is up to the task of printing abrasives at 300°C and you've got a filament dryer capable of drying Nylon, printing CF-PA6 Nylon isn't too tricky. Here's the general slicer settings I use:

* Nozzle - 300°C
* Bed - 45°C
* Part cooling fan off (100% for bridging **ONLY**)
* Minimum layer time - 0 seconds (PrusaSlicer calculates whacky layer times when generating support material)
* 1mm retraction (This works on my Printrbot extruder with an E3D V-6 and Nozzle-X)
* Extrusion Width - 0.3mm for everything except:
    * Support material - 0.22mm
    * Perimeters - 0.25mm
* Layer Height - 0.1mm-0.2mm ( I used 0.2mm)
* Perimeters - 5 (1.25mm)
* Top/Bottom layers - 2mm (5 layers @0.2mm layer height)
* Detect thin walls
* Detect bridging perimeters
* Don't support bridges
* 33% Gyroid infill
* Support Contact Z Distance - 0.05mm (smaller gap improves layer adhesion with these layers)
* Print speed - 40mm/s-80mm/s (infill and support fast, small/external perimeters slow)
* Bridge speed - 30mm/s
* Bridge flow ratio - 0.64 (Currently, lower values with this nozzle size cause PrusaSlicer mess up subsequent layers)
* Extrusion Multiplier - 0.86 (Whatever you arrived at with calibration prints)

## Idler Gear:

* No support Material
* XY Size Compensation - up to -0.09 (more than that removes too much material from small-side gear teeth) 
    * You'll need to test-fit this gear in the transmission to fine-tune this. It should be a tight mesh and feel like it needs to break-in a little
* No part cooling

![Idler Gear Orientation](/3D-Printed/Images/IdlerGearOrientation.png)
![Idler Gear Preview](/3D-Printed/Images/IdlerGearPreview.png)

## Spur Gear:

* No support Material
* XY Size Compensation - Same as you used for printing Idler Gear
* 100% bridging fan
* 100% fan on infill after bridging layer (This will keep bridge layer from warping)

    ![Add Custom G-Code](/3D-Printed/Images/AddCustomG-Code.png)
    * Move the top layer view slider (In PrusaSlicer) to the first layer after the bridging layer
    * Right-click the "+" and select "Add Custom G-Code"
    * Type M106 S255 and click OK (for single-extruder printers with Marlin firmware)
    * Move the top layer view slider (In PrusaSlicer) to the next layer
    * Right-click the "+" and select "Add Custom G-Code"
    * Type M106 S0 and click OK

![Spur Gear Orientation](/3D-Printed/Images/SpurGearOrientation.png)
![Spur Gear Preview](/3D-Printed/Images/SpurGearPreview.png)