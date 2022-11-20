[:arrow_left: Back to Table of Contents](/README.md)

# Switchwire nozzle-scrub - beta testing
![](/images/nozzle-scrub.jpg)

**:warning: This guide not complete, use at your own risk.**

**:warning: Testing for nozzle-scrub mount is not complete, use at your own risk.**

This allows a nozzle-scrub to be mounted on the Switchwire. This provides the ability to do nozzle probing, and take take advantage of [auto z calibration](https://github.com/protoloft/klipper_z_calibration). I use this in combination with [:arrow_right: z-stop](/z-stop/)

### Notes
- This is modeled after the [Decontaminator](https://github.com/VoronDesign/VoronUsers/tree/master/orphaned_mods/printer_mods/edwardyeeks/Decontaminator_Purge_Bucket_&_Nozzle_Scrubber) Props to the creator! (edwardyeeks I believe...)
- The brush mount here is a copy of 'Decontaminator', just trimmed down to fit the Switchwire
- Even the purge bucket is inspired by the 'Decontaminator'

**:warning: Only Enderwire conversions are supported at this time**

**:warning: Requires holes to be drilled in your Y Carriage**

## What else is needed
- TODO

## BOM
- M3 bolts 10mmx2, 6mmx2
- M3 nuts
- M3 heatsets
- 6x3 Magnets

## Instructions
- You will need to align the mount on the under side of the bed, as illustrated for your printer. There are registration features to align the mount properly.
- Mark and drill the holes once the mount is aligned.
- A zip-tie hole is included to assist with wire management.

## Config
These are my current settings, I highly recommend to check and possibly use your own.
```
## Switchwire
variable_brush_start:     17.8

# This value is defaulted from brush location in CAD (rear left). Change if your brush width is different.
variable_brush_width:     51

## These are only used if location_bucket_rear is False. You specify a custom location in y axis for your brush - see diagram above. ##
variable_brush_front:       0          
variable_brush_depth:       0
...
## Switchwire, not used but needs to be defined 
variable_bucket_left_width:    17.8

# These values are defaulted from bucket geometry in CAD (rear left location). Change only if you're using a custom bucket.
variable_bucket_right_width:   23            
variable_bucket_gap:           46	

# For V1.8, you may need to measure where your bucket start is and input into bucket_start. Otherwise, a value of 0 is for a default
# installation of purge bucket at rear left.
variable_bucket_start: 0
```
### Align and Drill
![](/nozzle-scrub/images/nozzle-scrub-ender-register-and-drill-example.PNG)

### Enderwire mount location
![](/nozzle-scrub/images/nozzle-scrub-ender-mount-location.PNG)

### Prusa MK3 Y Carrier location
TODO

### GCR carriage
TODO

## TODO
- add support for [Prusa MK3 Y Carrier](https://www.prusa3d.com/product/y-carriage-mk3-s/)
- add support for [GCR carriage](https://gulfcoast-robotics.com/products/modular-y-carriage-plate-upgrade-creality-ender-3-point-leveling)
