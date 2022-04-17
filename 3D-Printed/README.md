# 3D Printed parts guides

## Description

Different types of parts have their own guides:

* *[0.4mm nozzle](BigNozzle/README.md)*
* *[0.25mm nozzle](SmallNozzle/README.md)*

## Prerequisites

The sizing of these parts and this guide assume you'll be using PrusaSlicer. You are free to use whatever slicer you want, but be warned - You'll be on your own to figure out what settings work. I started out using Cura, but couldn't get support material to work well while being reasonably easy to remove.

* 3D printer(s) with the following capabilities (for printing carbon-fiber PA6 Nylon)
    * Hard 0.4mm and 0.25mm nozzle (hardened steel or equivalent)
    * 300°C capable hot-end (make sure you hot-tighten it at that temperature)
    * Heated bed
* Filament dryer
* High quality Carbon-Fiber filled PA6 filament (I used Polymaker Polymide CF-PA6)
* Magigoo or equivalent PA bed adhesive

# Before printing parts...

Save yourself from future headaches by drying your filament and doing some tuning. This material prints very different than PLA. It's also expensive, so these test prints are pretty minimal.

## Tune Extrusion Multiplier

Because CF-Nylon likes to absorb moisture, it's nearly impossible to keep it completely dry without storing it in a vacuum chamber. I've also found my E-steps are off compared to PLA likely due to how hard this stuff is. Rather than throw off E-steps for printing other types of filament, it's easier to tune extrusion multiplier for this material (you'll need to even if you do re-tune your E-steps).
![Extrusion Multiplier test prints](/3D-Printed/Images/ExtrusionMultiplier.jpg)

* Print small 20x20x2 calibration cubes at 100% infill to determine what multiplier to use. Make sure you use the same extrusion width, layer height, and infill/skin overlap settings you will be using to print your parts. (It shouldn't matter, but slicers be weird like that) You want a smooth top surface with no gaps and just a little bit of roughness that you can see and feel with your fingernail around the edges of the infill where it overlaps the perimeters.
* This can vary depending on how dry your filament is. 0.86 (or 86%) is the multiplier I ended up using after it's been out of the vacuum sealed packaging for a day or so (I don't have a vacuum chamber to store it in). In theory, if you can get this stuff completely dry and re-tune your E-steps, it'll be 1.00. I've never bene able to get higer than 0.87 with my filament dryer. I always store it in a sealed bag with desiccant in the box it came in and always print from the filament dryer (and leave it in there all day every time I do). I've found if I can't use at least 0.85 extrusion multiplier, that means it's too wet, will ooze like crazy and not have good layer adhesion.
* Dimensional accuracy is less important for most parts while layer adhesion is most important, so err on the side of over-extrusion.

## Tune Bridge Flow Ratio

CF-Nylon doesn't seem to exhibit die-swell and shrinking like PLA does, which makes bridging more difficult. Excellent bridging can still be accomplished with CF-Nylon, but it requires a much lower flow ratio than you're used to. It can also re-melt and warp/sag the bridging layer when printing the next layer - but there's a workaround for that which we should only need to use for printing the spur gear.
![Bridge Flow Ratio test prints (Top)](/3D-Printed/Images/BridgeFlow-Test-Top.jpg)
![Bridge Flow Ratio test prints (Bottom)](/3D-Printed/Images/BridgeFlow-Test-Bottom.jpg)
These were printed at 30mm/s bridge speed. First number is flow ratio percent and 2nd number is fan speed. The top piece is without bridge cooling for reference.

* Print 30x50x3 bridging test cubes with 0% infill and no support, 0 bottom layers, 2 top layers and 3 perimeters.
* Try different speeds and flow ratios with 100% bridge fan speed. Usually 20mm/s-30mm/s and 40%-70% flow ratio.
* I like to stop the test print a little more than half-way through the last layer so I can see both the bridging layer by itself and with the next layer on top of it.
* You want a flow ratio which produces the smoothest and flattest bridge and top layer as possible. In these pictures you can see that's probably somewhere around 55%-60%

## Authors

### Contributors - *Contributions are welcome!*

* Damon Palm

## Version History

* 0.1
    * Initial Release

## License

This project is licensed under the **GNU General Public License v3.0 License** \- see the [LICENSE File](/LICENSE) for details