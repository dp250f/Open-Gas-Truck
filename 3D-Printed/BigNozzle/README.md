# 0.4mm Nozzle Parts

## Material / part requirements:

* Carbon-Fiber PA6 Nylon (Polymaker Polymide CF-PA6)
* Filament dryer which can dry Nylon
* 0.4mm hardened nozzle at 300°C
* Magigoo PA on 45°C bed
* Print each part one at a time to keep the layer time as short as possible. This makes layer adhesion as strong as possible.

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
* Perimeters - 4 (2mm)
* Top/Bottom layers - 2mm (8 layers @0.25mm layer height)
* Detect thin walls
* Detect bridging perimeters
* Don't support bridges
* 33% Gyroid infill
* Support Contact Z Distance - 0.05mm (smaller gap improves layer adhesion with these layers)
* Print speed - 40mm/s-80mm/s (infill and support fast, small/external perimeters slow)
* Bridge speed - 30mm/s
* Bridge flow ratio - 0.55 (Whatever you arrived at with calibration prints)
* Extrusion Multiplier - 0.86 (Whatever you arrived at with calibration prints)

## Rear Battery Box Top (optional):

* No support Material
* 100% bridging fan
* Bridging angle - Set it to go across the shortest edge

![Battery Box Top Orientation](/3D-Printed/Images/BatteryBoxTopOrientation.png)
![Battery Box Top Preview](/3D-Printed/Images/BatteryBoxTopPreview.png)

## Rear Battery Box Bottom (optional):

* Support on build plate only (only on outside of part)
* 100% bridging fan
* Bridging angle - Set it to go across the shortest edge
* Remove support material as soon as possible

![Battery Box Bottom Orientation](/3D-Printed/Images/BatteryBoxBottomOrientation.png)
![Battery Box Bottom Preview](/3D-Printed/Images/BatteryBoxBottomPreview.png)

## Transmission Case Top:

* Inside dimensions are critical on this part, so that side must face up
* Support on build plate only
* No part cooling
* Remove support material as soon as possible

![Transmission Case Top Orientation](/3D-Printed/Images/TransmissionCaseTopOrientation.png)
![Transmission Case Top Preview](/3D-Printed/Images/TransmissionCaseTopPreview.png)

## Transmission Case Bottom:

* Inside dimensions are critical on this part, so that side must face up
* Support on build plate only
* No part cooling
* Remove support material as soon as possible

![Transmission Case Bottom Orientation](/3D-Printed/Images/TransmissionCaseBottomOrientation.png)
![Transmission Case Bottom Preview](/3D-Printed/Images/TransmissionCaseBottomPreview.png)

## Electronics Tray:

* Support enabled everywhere
* 100% bridging fan
* Bridging angle - Set it to go across the shortest edge
* Remove support material as soon as possible

![Electronics Tray Orientation](/3D-Printed/Images/ElectronicsTrayOrientation.png)
![Electronics Tray Preview](/3D-Printed/Images/ElectronicsTrayPreview.png)

## Receiver Cover:

* No support Material
* No part cooling

![Receiver Cover Orientation](/3D-Printed/Images/ReceiverCoverOrientation.png)
![Receiver Cover Preview](/3D-Printed/Images/ReceiverCoverPreview.png)

## Front Chassis Braces:

* Support on build plate only
* No part cooling
* Print one at a time

![Front Chassis Brace Orientation](/3D-Printed/Images/FrontLeftChassisBraceOrientation.png)
![Front Chassis Brace Preview](/3D-Printed/Images/FrontLeftChassisBracePreview.png)

## Fuel Tank Mounts:

* Support on build plate only
* No part cooling
* Print one at a time if layer time is over 60 seconds

![Rear Fuel Tank Mount Orientation](/3D-Printed/Images/RearFuelTankMountOrientation.png)
![Rear Fuel Tank Mount Preview](/3D-Printed/Images/RearFuelTankMountPreview.png)

## Small Parts:

* Includes the following parts -
    * Brake lever
    * Brake Mount
    * Chassis shim (x4)
    * Fuel line clip
    * Servo slider
    * Tank mount chassis shim
    * Transmission brace
* No support Material
* No part cooling
* Print fewer parts at a time if layer time is over 60 seconds

![Small Parts Orientation](/3D-Printed/Images/SmallPartsOrientation.png)
![Small Parts Preview](/3D-Printed/Images/SmallPartsPreview.png)