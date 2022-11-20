[:arrow_left: Back to Table of Contents](/README.md)

# Switchwire z-stop mount - beta testing
![](/images/z-stop.jpg)

**:warning: This guide not complete, use at your own risk.**

**:warning: Testing for z-stop mount is not complete, use at your own risk.**

This allows a z-stop to be mounted on the Switchwire. This provides the ability to do nozzle probing, and take take advantage of [auto z calibration](https://github.com/protoloft/klipper_z_calibration). I use this in combination with [:arrow_right: nozzle-scrub](/nozzle-scrub/)

**:warning: Requires holes to be drilled in your Y Carriage**

## What else is needed
### Enderwire
- [Voron 2.4 nozzle_probe.stl](https://github.com/VoronDesign/Voron-2/tree/Voron2.4/STLs/Z_Endstop)
### Switchwire
- [KlickyProbe_Long_v2.stl](https://github.com/jlas1/Klicky-Probe/blob/main/Probes/KlickyProbe/STL/KlickyProbe_Long_v2.stl)
### GCR
- TODO

## BOM
- M3 bolts 16mmx2n 10mmx2
- M3 nuts
- M3 heatsets

## Instructions
- You will need to align the mount on the under side of the bed, as illustrated for your printer. There are registration features to align the mount properly.
- Mark and drill the holes once the mount is aligned.
- A zip-tie hole is included to assist with wire management.

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
TODO

## TODO
- add support for [GCR carriage](https://gulfcoast-robotics.com/products/modular-y-carriage-plate-upgrade-creality-ender-3-point-leveling)
