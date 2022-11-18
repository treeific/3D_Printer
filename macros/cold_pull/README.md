[:arrow_left: Back to Table of Contents](/README.md)

# Cold Pull macro - beta testing
![](/macros/cold_pull/images/cold_pull.jpg)

**:warning: This guide not complete, use at your own risk.**

**:warning: Testing for is not complete, use at your own risk.**

Setup the variables like hotend and cold_pull. hotend should be normal printing temp, cold pull should be the temp when you can manaully cold pull


## What else is needed
- your extruder gears need to be tightened correctly. The way I read to do this is basically... Tighten them so the motor will skip before the teeth grind into the filament.
- I run my cold pull 'press' long enough to skip the extruder 1 or 2 times, just to be sure... If you hear your's skipping more than you'd like, then read comment on 'press variable and choose a value for you'
- I run some case fans and case light to get my attention when it's done. I commented these out. You can run a beeper here if you have it.

## Macro
[gcode_macro _LOGGER]
gcode:
	{% set msg = params.MSG|string %}

	{ action_respond_info(msg) }

[gcode_macro COLD_PULL]
gcode:
    # Change these
    {% set hotend =  235 %} 		# my melting temp for ABS
    {% set cold_pull = 105 %}		# my cold pull for ABS
    {% set press = 11 %}			# how long to press/extrude filiment while cooling off
    								# @ 20mm... 20 about 60 seconds, 16 about 75 seconds, 14 about 85 seconds, 13 about 90 seconds, 10 about 120 seconds

    # Shouldn't need to change these
    {% set prime = 1 %}             # purge in mm
    {% set prime_delay = 20 %}      # wait in sec
    {% set cool_down = 1 %}         # wait in min
    {% set notify_wait = 5 %}       # wait in sec

    # start work
        _LOGGER MSG="Starting cold pull process."
        _LOGGER MSG="Warm up."
    M109 S{hotend}                          # warm up
        _LOGGER MSG="TURN_OFF_HEATERS"
    TURN_OFF_HEATERS                        # start cooling off
        _LOGGER MSG="Press the plastic while cooling"
    M83                                     # relative extrustion
    G1 E20 F{press}                         # @ 20mm... 20 about 60 seconds, 16 about 75 seconds, 14 about 85 seconds, 13 about 90 seconds, 10 about 120 seconds
        _LOGGER MSG="Cool way down"
    M109 S60                                # Cool down to cold and wait
        _LOGGER MSG="Waiting"
    G4 P{cool_down*60000}                   # Wait for the whole hotend to reach cold_pull temp
        _LOGGER MSG="Raise to almost cold_pull temp"
    M109 S{cold_pull-10}                       # Warm up to almost cold_pull temp
        _LOGGER MSG="Set cold_pull temp and start pulling"
    M104 S{cold_pull}                       # Warm up to cold_pull temp
    G4 P{5000}                              # Wait for temp to rise a little
        _LOGGER MSG="Automatic Cold Pull!"
    G1 E-20 F60                              # Try an automatic pull... 20mm@1mms
    #_case_fan_on                            # It's ready! Notify somehow...
    #_bed_fan_on                             # It's ready! Notify somehow...
    #_case_light_on                          # It's ready! Notify somehow...
    G4 P{notify_wait*1000}                  # Wait for attention
        _LOGGER MSG="Pull Manually!"
    #_case_fan_off                           # Give up the attention
    #_bed_fan_off                            # Give up the attention