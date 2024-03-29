[:arrow_left: Back to Table of Contents](/README.md)

# Switchwire z-stop mount - beta testing
![](/images/z-stop.jpg)

**:warning: This guide not complete, use at your own risk.**

**:warning: Testing for z-stop mount is not complete, use at your own risk.**

This allows a z-stop to be mounted on the Switchwire. This provides the ability to do nozzle probing, and take take advantage of [auto z calibration](https://github.com/protoloft/klipper_z_calibration). I use this in combination with [:arrow_right: nozzle-scrub](/nozzle-scrub/)

**:warning: Requires holes to be drilled in your Y Carriage**
**:warning: The ender stock bed leveling wheels do not fit, you can try hard mounting**

## See it in action
Credit to krapstar#0301
[![](https://img.youtube.com/vi/y8KPx6Bqce4/0.jpg)](https://www.youtube.com/watch?v=y8KPx6Bqce4)

## What else is needed
### Enderwire
- [Voron 2.4 nozzle_probe.stl](https://github.com/VoronDesign/Voron-2/tree/Voron2.4/STLs/Z_Endstop)
### Switchwire
- [KlickyProbe_Long_v2.stl](https://github.com/jlas1/Klicky-Probe/blob/main/Probes/KlickyProbe/STL/KlickyProbe_Long_v2.stl)
### GCR
- [Voron 2.4 nozzle_probe.stl](https://github.com/VoronDesign/Voron-2/tree/Voron2.4/STLs/Z_Endstop)

## BOM
- M3 bolts 16mmx2n 10mmx2
- M3 nuts
- M3 heatsets

## Instructions
- You will need to align the mount on the under side of the bed, as illustrated for your printer. There are registration features to align the mount properly.
- Mark and drill the holes once the mount is aligned.
- A zip-tie hole is included to assist with wire management.

## Configs
- TODO 🙂 meanwhile, [this (from LoganFraser)](https://github.com/LoganFraser/VoronMods/tree/main/KlickySetup) is a really good start
- Consider [adaptive bed mesh](https://github.com/kyleisah/Klipper-Adaptive-Meshing-Purging#user-content-fn-1-1a6a9635a25976ce62c2dfde4d2f1470), somewhat un-related but pretty cool.

### Enderwire
#### Align and Drill
![](/z-stop/images/z-stop-ender-register-and-drill-example.PNG)

#### Enderwire mount location
![](/z-stop/images/z-stop-ender-mount-location.PNG)

### Switchwire
#### Notes

Switchiwre has much less space to work with compared to ender wire. 
The z-stop needs to be on the front of the bed. You also need to change your klicky to the 'long' or 'longer'

**:warning: You need to use [KlickyProbe_Long_v2.stl](https://github.com/jlas1/Klicky-Probe/blob/main/Probes/KlickyProbe/STL/KlickyProbe_Long_v2.stl)**
![](/z-stop/images/z-stop-prusa-KlickyProbe_Long_v2.PNG)

Very tight tolerances, testing will prove if this fits or not (I only own Enderwire)
![](/z-stop/images/z-stop-prusa-tight-tolerances.PNG)

#### Align and Drill
![](/z-stop/images/z-stop-prusa-register-and-drill-example.PNG)
#### Prusa MK3 Y Carrier location
![](/z-stop/images/z-stop-prusa-mount-location.PNG)

#### GCR carriage
You need to rotate the GCR bed. The z-stop-gcr-mount.stl will bolt to the existing holes on the (now) back right, similar to Enderwire mentioned above.


## TODO
- add support for [GCR carriage](https://gulfcoast-robotics.com/products/modular-y-carriage-plate-upgrade-creality-ender-3-point-leveling)
