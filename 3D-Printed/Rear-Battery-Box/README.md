# Rear Battery Box

## Material / part requirements:

* Carbon-Fiber PA6 Nylon (Polymaker Polymide CF-PA6)
* 0.4mm hardened nozzle at 300°C
* Magigoo PA on 45°C bed

## Part Orientation (top):

I found this orientation produces a strong part and doesn't need support material:

![Battery Box Top Orientation](/3D-Printed/Images/BatteryBoxTopOrientation.png "Battery Box Top Orientation")
![Battery Box Top Orientation](/3D-Printed/Images/BatteryBoxTopPreview.png "Battery Box Top Orientation")

## Part Orientation (bottom):

I found this orientation produces a strong part and allows for easy support material removal:

![Battery Box Bottom Orientation](/3D-Printed/Images/BatteryBoxBottomOrientation.png "Battery Box Bottom Orientation")
![Battery Box Bottom Orientation](/3D-Printed/Images/BatteryBoxBottomPreview.png "Battery Box Bottom Orientation")

**You will want to print these parts one a time to keep the layer time as short as possible. This makes layer adhesion as strong as possible.**

## Slicer settings:
Assuming your hot end is up to the task of printing abrasives at 300°C and you've got a filament dryer capable of drying Nylon, printing CF-PA6 Nylon isn't too tricky. Here's the general slicer settings I use:

* Nozzle - 300°C
* Bed - 45°C
* Part cooling fan off (100% for bridging **ONLY**)
* Minimum layer time - 0 seconds (PrusaSlicer calculates whacky layer times when generating support material)
* 1.4mm retraction (This works on my MK3S extruder with an E3D Volcano and Nozzle-X)
* Extrusion Width - 0.5mm for everything except support material which is 0.35mm
* Layer Height - 0.15mm-0.25mm ( I used 0.25mm)
  * Using a 0.5mm extrusion width allows up to 0.25mm layer height while maintaining good layer adhesion
  * I've not really noticed reduced layer adhesion within this layer height range.
* Extrusion Multiplier - 0.86 (or 86%)
  
  ![Battery Box Bottom Orientation](/3D-Printed/Images/ExtrusionMultiplier.jpg "Battery Box Bottom Orientation")

  * This can vary depending on how dry your filament is. This is the multiplier I ended up using when it is fresh out of the vacuum sealed packaging. In theory, if you can get this stuff completely dry, it'll be 1.00 
  * I print small 20x20x2 calibration parts at 100% infill to determine what multiplier to use. Make sure you use the same extrusion width, layer height, and infill/skin overlap settings you will be using to print your parts. You want a smooth top surface with no gaps and just a little bit of roughness that you can see and feel with your fingernail around the edges of the infill where it overlaps the perimeters.
  * Dimensional accuracy is less important for this part and layer adhesion is most important, so err on the side of over-extrusion.

* Perimeters - 4
* Top/Bottom layers - 2mm (4 layers @0.25mm layer height)
* Detect thin walls
* Detect bridging perimeters
* Don't support bridges
* 33% Gyroid infill
* Generate support material (only for bottom piece)
* Print speed - 40mm/s-80mm/s (infill an support fast, small/external perimeters slow)
* Bridge speed - 30mm/s
* Bridge flow ratio - 0.4 (40%)